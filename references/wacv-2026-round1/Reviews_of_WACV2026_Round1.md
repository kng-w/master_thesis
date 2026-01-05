# Reviews of WACV 2026 Round1

Tag: Research Log (https://www.notion.so/Research-Log-64b6c6130e5341db8d1b5ac4f5ac0836?pvs=21)
Created Date: September 6, 2025

## **Meta Review of Submission967 by Area Chair DKtc**

- Meta Reviewby Area Chair DKtc 30 Aug 2025, 13:45 (modified: 06 Sept 2025, 02:14)Area Chairs, Authors, Reviewers Submitted, Program Chairs[Revisions](https://openreview.net/revisions?id=Q1EDtqbycY)
- **Metareview:**
  This paper introduces Manga109Script, a dataset with paired scripts and manga layouts for approximately 20,000 pages. The authors define a new task, Script2Layout, which involves generating manga layouts from a given script. They leverage VLLMs to create the script data and subsequently develop models specifically for this task. A comparative analysis demonstrates that these Script2Layout models surpass current layout generation methods, showing notable improvements in key metrics like mean Intersection over Union (mIoU).
  Two reviewers give the negative feedbacks to this work while one reviewer give the positive feedback. The AC checks the main paper and comments of the reviewers, finds the meaningful contribution of dataset. Thus, AC suggests to re-submit to the next round. The authors need to solve all the issues in the next draft.
- **Final Recommendation:**
  Recommend resubmission in round 2 with updated paper and rebuttal

## **Official Review by Reviewer rBct**

- Official Reviewby Reviewer rBct 22 Aug 2025, 17:05 (modified: 06 Sept 2025, 02:07)Program Chairs, Area Chairs, Reviewers Submitted, Reviewer rBct, Authors[Revisions](https://openreview.net/revisions?id=HMiPUWEn7C)
- **Paper Summary:**
  This paper introduces script data for roughly 20,000 pages from the Manga109 dataset and creates the Manga109Script dataset, which links scripts to manga layouts. This is a valuable dataset that can support applications aimed at translating narratives into visual media, as exemplified by manga.
- **Paper Strengths:**
  1. This paper introduces an annotation-assisted method to generate script data from manga images using VLLMs, validated by human evaluators.
  2. This paper publishes the first professional script-format manga storytelling dataset and related benchmark.
- **Major Weaknesses:**
  The experiments in this paper are exclusively focused on black-and-white manga. It is unclear how the proposed method would perform on color comics. Have the authors considered this, and could they comment on the potential impact on performance?
  In Table 2, T5 achieves the best mIoU, whereas DeepSeek excels in the Panel-Inserted metric. The authors should provide a more in-depth analysis of this discrepancy. Specifically, what are the architectural reasons (decoder-only vs. encoder-decoder) that lead to one model performing better on one metric and not the other?
  Figure 1 appears to be a rasterized image, which makes the text within it non-selectable and blurry upon magnification. For better readability and accessibility, I strongly recommend regenerating this figure as a vector graphic (e.g., PDF, SVG, or EPS).
- **Minor Weaknesses:**
  Minor Writing and Formatting Issues: The manuscript requires some minor polishing. For instance:
  1. Punctuation in Equations: Equations should be treated as part of the sentence and be followed by appropriate punctuation (e.g., a comma or a period).
  2. Incorrect Quotation Marks: The use of backticks for quotes (e.g., Table 1) is non-standard. Please use proper quotation marks (e.g., "Table 1" or 'Table 1', or often, no quotes are needed at all for references, e.g., Table 1). Please ensure consistent and correct formatting for all quotes and references throughout the paper.
- **Round 1 Recommendation:** 4: Borderline Accept
- **Round 1 Justification:**
  This paper proposes the first professional script-format manga storytelling dataset and related benchmark. This is a valuable dataset that can support applications aimed at translating narratives into visual media, as exemplified by manga. I have decided to be positive in this round. Moveover, the paper would be significantly strengthened by including experiments on layout-to-image generation[1]. Building upon the proposed layout analysis to generate actual images would provide a more complete and compelling demonstration of the method's capabilities.

[1]Ranni: Taming text-to-image diffusion for accurate instruction following

- **Resubmission:** Yes, the paper is of reasonable quality but requires some revisions before it can be accepted.
- **Revisions For Resubmission:**
  N/A
- **Confidence Level:** 3 - Moderate Confidence: The reviewer is reasonably knowledgeable about the topic. They understand the paper's methodology and results.

## **Official Review by Reviewer uizG16**

- Official Reviewby Reviewer uizG 16 Aug 2025, 16:05 (modified: 06 Sept 2025, 02:07)Program Chairs, Area Chairs, Reviewers Submitted, Reviewer uizG, Authors[Revisions](https://openreview.net/revisions?id=ff2YnNNQkd)
- **Paper Summary:**
  This paper presents a dataset for script-to-layout generation in comics. It constructs 20k script data samples from Manga109, collects layout-to-script data using a VLM, and trains an LLM to achieve script-to-layout generation.
- **Paper Strengths:**
  1. A new dataset was constructed for script-to-layout generation, which can promote the automation of manga design to some extent.
  2. A considerable number of experiments were conducted to validate the performance of the proposed method.
  3. 3.The method is described relatively clearly.
- **Major Weaknesses:**
  1. The paper claims that the way the dataset is constructed is a contribution, using a visual prompting method (drawing circles) and designing a rule-based algorithm for panel reading order. However, I tested several Manga examples with GPT-4.1 using the prompt “Translate the text in the comic into English and identify the speaking order.” GPT-4.1 is fully capable of recognizing the speaking order and providing correct translations. In my opinion, this is not a significant issue at present. Additionally, I think it is unnecessary to identify the characters in the Manga, as this does not have much impact on layout generation.
  2. The paper does not propose any innovative methods. The performance advantages over other layout generation models mainly come from fine-tuning with Manga109script.
  3. Existing methods also require layout elements as input, and there does not seem to be much difference from the proposed Script2Layout method.
  4. Regarding evaluation metrics, theoretically there is no ground truth for this kind of layout generation, so it is unreasonable to calculate the overlap with the so-called ground truth. The layout does not have a unique answer; many predictions can be reasonable. Consider using human evaluation or scoring by a multimodal large model.
  5. As for generalization, both the test and training datasets are from Manga109, the similarity is too high, it would be better to test on other datasets.
  6. Furthermore, the fine-tuned method does not seem to show significant performance advantages.
- **Minor Weaknesses:**
  1. The figures are very blurry and of poor quality. It is recommended to use vector graphics.
- **Round 1 Recommendation:** 2: Weak Reject
- **Round 1 Justification:**
  Overall, the contribution of this work appears limited. Its application scope is rather narrow, being restricted to manga. The level of novelty is also not sufficiently clear, and the problem formulation seems somewhat artificial. As noted in my comments, the proposed complex design may not be necessary, since models such as GPT-4.1 can already generate scripts effectively. Furthermore, fine-tuning LLMs on the proposed dataset yields only marginal improvements, and the performance does not show a clear advantage over existing methods without fine-tuning. This suggests that current approaches already exhibit strong generalization ability for layout generation. Finally, I find the evaluation methodology less convincing. Based on these observations, I am inclined to recommend rejection.
- **Resubmission:** No, the required revisions are too extensive for a resubmission in the time that is available.
- **Revisions For Resubmission:**
  In my view, the contribution of this work to the field and the community appears rather limited. The level of novelty is not sufficiently clear, as the complex construction pipeline described in the paper may not represent a genuine core innovation, especially since the problem could potentially be addressed in a simpler manner. Moreover, the dataset provides only marginal benefits, and fine-tuning the LLM does not demonstrate a significant advantage over existing methods without fine-tuning.
- **Confidence Level:** 4 - High Confidence: The reviewer has strong expertise in the area. They are highly familiar with the relevant literature and can critically evaluate the paper.

## **Official review by wrik**

Official Reviewby Reviewer wrik 11 Aug 2025, 03:26 (modified: 06 Sept 2025, 02:07)Program Chairs, Area Chairs, Reviewers Submitted, Reviewer wrik, Authors[Revisions](https://openreview.net/revisions?id=cT0529eqfG)

- **Paper Summary:**
  This paper introduces Manga109Script, a dataset with paired scripts and manga layouts for approximately 20,000 pages. The authors define a new task, Script2Layout, which involves generating manga layouts from a given script. They leverage VLLMs to create the script data and subsequently develop models specifically for this task. A comparative analysis demonstrates that these Script2Layout models surpass current layout generation methods, showing notable improvements in key metrics like mean Intersection over Union (mIoU).
- **Paper Strengths:**
  1. This paper defines a new Script2Layout task and provides detailed description of the dataset's creation. The comprehensive description of experiments and results offers a robust understanding of the research.
  2. The paper addresses a practical challenge in manga creation and holds potential in bridging the gap between narrative scripts and visual layouts. The evaluation with both quantitative metrics (FID, mIoU) and qualitative analysis, validates the effectiveness of the proposed method.
- **Major Weaknesses:**
  1. A notable limitation is the reliance on existing VLLMs and rule-based algorithms for script generation. While the process aims to handle narrative flow, it lacks technical innovation in ensuring coherence and continuity, especially across multiple pages.
  2. The paper's scope is somewhat narrow, focusing predominantly on layout generation. A more holistic discussion of the dataset's broader utility, potential biases, or applications beyond the defined task would enhance its contribution to the field.
- **Minor Weaknesses:**
  the manga109 dataset is somehow out of date in both style and size. A dataset with more recent style and color comics, together with larget amont of data would make this work more significant and practical
- **Round 1 Recommendation:** 3: Borderline Reject
- **Round 1 Justification:**
  The Scirpt2Layout is pretty abstract, is there some method to prove the imporvement or contribution of this dataset/this task in the final generation of Manga?
- **Resubmission:** Yes, the paper is of reasonable quality but requires some revisions before it can be accepted.
- **Revisions For Resubmission:**
  It's better to proved addition results with dataset of larger diversity and higher quality.
- **Confidence Level:** 4 - High Confidence: The reviewer has strong expertise in the area. They are highly familiar with the relevant literature and can critically evaluate the paper.
