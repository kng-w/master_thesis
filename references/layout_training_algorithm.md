# Layout Training Algorithms

This document details the technical specifications of the models and training algorithms used in the Layout Training system.

## 1. Layouter Model (`PatternAGNN`)

The Layouter is a **Heterogeneous Graph Neural Network (GNN)** designed to predict the spatial layout of a manga spread.

### 1.1 Architecture
*   **Type**: Graph Transformer / HeteroGNN.
*   **Nodes**: `Spread`, `Panel`, `Character`, `CharacterInstance`, `Speech`.
*   **Edges**:
    *   Structural: `contains`, `in_panel`, `spoken_by`, `anchored_to`.
    *   Sequential: `next`, `prev` (for panels and speeches).
    *   Semantic: `interacts_with`, `cooccurs_in_panel`.
*   **Input Features**:
    *   **Text**: BERT/RoBERTa embeddings of narrative text (summary, script, dialogue).
    *   **Enums**: Learnable embeddings for cinematic attributes (`distance`, `angle`, `pose`, `emotion`).
    *   **Positional**: Learnable embeddings for `order`, `page_index`.

### 1.2 Output Heads
The model supports multiple output heads for bounding box prediction:
1.  **MDN (Mixture Density Network)**:
    *   Predicts parameters $(\mu, \Sigma, \pi)$ for a Mixture of Gaussians.
    *   Allows modeling multimodal distributions (multiple valid layouts).
    *   Loss: Negative Log Likelihood (NLL).
2.  **Quantized (Discrete)**:
    *   Predicts discrete tokens for quantized coordinates $(x, y, w, h)$.
    *   Vocabulary size: 1000 (default).
    *   Loss: Cross Entropy.

### 1.3 Pattern-Specific Variations
*   **Pattern A**: Standard Supervised Learning using Ground Truth Enums.
*   **Pattern C (Hint-Robust)**:
    *   **Cinematic Bottleneck**: Explicitly separates text and visual features.
    *   **Gradient Reversal**: Adversarial loss to prevent text encoder from learning visual information, ensuring reliance on the bottleneck.
*   **Pattern J (Concept Bottleneck)**:
    *   Masks all text features, forcing the model to rely *only* on cinematic enums.

---

## 2. Director Model (`DirectorLLM`)

The Director is a **Large Language Model (LLM)** that translates narrative text into cinematic instructions.

### 2.1 Architecture
*   **Base Model**: `gpt-oss-20b` (or similar).
*   **Adaptation**: LoRA (Low-Rank Adaptation) via `unsloth`.
*   **Input**: Narrative Text (Prompt).
*   **Output**: Structured JSON containing cinematic attributes.

### 2.2 Training Strategies
*   **Pattern B (SFT)**:
    *   Supervised Fine-Tuning on `(Narrative, GT Cinematic)` pairs.
    *   **Random Masking**: Randomly moves GT attributes from output to input (constraints) to teach the model to follow instructions.
*   **Pattern E (DPO)**:
    *   Direct Preference Optimization.
    *   Optimizes the model to generate cinematic instructions that lead to "better" layouts (as scored by Verifier/Cycle).

---

## 3. Verifier Model (`VerifierGNN`)

The Verifier evaluates the quality of a generated layout.

### 3.1 Architecture
*   **Type**: Heterogeneous GNN (similar to Layouter encoder).
*   **Input**:
    *   Narrative + Cinematic (Condition).
    *   Layout BBoxes (Candidate).
*   **Output**: Scalar Quality Score (0-1).

### 3.2 Training (Pattern I)
*   **Contrastive Learning**:
    *   **Positive**: Ground Truth Layouts.
    *   **Negative**: Perturbed Layouts (Jitter, Swap, Resize).
*   **Loss**: Binary Cross Entropy or Ranking Loss.

---

## 4. Cycle Consistency (`PatternD`)

Enforces semantic consistency between Layout and Cinematic.

### 4.1 Inverse Model
*   **Task**: Predict Cinematic Attributes *from* Layout BBoxes.
*   **Architecture**: GNN (Layout $\to$ Cinematic).

### 4.2 Cycle Loss
*   $L_{cycle} = \text{CrossEntropy}(Inverse(Layouter(C)), C)$
*   Ensures that the generated layout implies the original cinematic instruction $C$.
*   Used as a regularizer in Pattern D or a reward in Pattern K.
