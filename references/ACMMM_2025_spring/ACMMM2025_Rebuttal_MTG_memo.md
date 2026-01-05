# ACMMM2025 リバタル Rebuttal 準備

Tag: Research Log (https://www.notion.so/Research-Log-64b6c6130e5341db8d1b5ac4f5ac0836?pvs=21)
Created Date: June 11, 2025 → June 19, 2025
RECORD: PosterLlama (https://www.notion.so/PosterLlama-2136833ec28b807da88af839ab3a8263?pvs=21)

# OpenReview

---

[](https://openreview.net/forum?id=igrR5GZdB3#discussion)

# Review まとめ

---

## Reviewer 1 (ryDR)

- Review 本文
    
    **Review of Submission 4528**
    
    Official Reviewby Reviewer ryDR25 May 2025, 19:37 (modified: 09 Jun 2025, 23:38)Program Chairs, Senior Area Chairs, Area Chairs, Reviewer ryDR, Authors[Revisions](https://openreview.net/revisions?id=v2ILv2Stsj)
    
    **Review:**
    
    Summary:
    
    The paper presents Manga109Script, a newly constructed dataset comprising script data for approximately 20,000 manga pages from the Manga109 dataset. The primary objective is to facilitate the Script2Layout task, where narrative scripts are used to generate coherent and expressive manga layouts. Utilizing Vision Large Language Models (VLLMs) such as GPT-4, the authors generate scripts that include scene headings, action descriptions, and dialogues. They then develop and evaluate several Script2Layout models, demonstrating that incorporating script information significantly enhances layout generation quality compared to existing methods. The dataset and associated code are to be made available upon publication, providing a valuable resource for future research in manga layout generation and visual storytelling.
    
    Strengths
    
    1. The introduction of Manga109Script addresses a significant gap in the domain of manga layout generation by providing a large-scale, script-aligned dataset. This enables the exploration of script-based layout generation, which has been under-researched due to data scarcity.
    2. The authors employ a robust method for script generation using VLLMs with visual prompting and speaker-aware dialogue sequencing. The multi-step interaction with GPT-4 ensures that the scripts are contextually coherent and aligned with the original manga narratives.
    3. Human evaluation metrics such as Scene Heading Recall, Scene Heading Precision, Action Description Precision, Out-of-Context Action Description Detection Accuracy, and Dialogue Recall add credibility to the dataset's quality, demonstrating its reliability for downstream tasks.
    4. The paper is well-structured, with clear explanations of the problem formulation, data construction process, and experimental setup. Figures and tables are effectively used to illustrate key points and results.
    
    Weaknesses
    
    1. The script generation process relies on GPT-4. This dependence may raise concerns regarding reproducibility and reliability.
    2. While the paper provides quantitative and qualitative evaluations, it lacks a detailed error analysis. Understanding the common failure modes of the Script2Layout models could provide deeper insights and guide future improvements.
    3. The evaluation primarily focuses on comparisons with existing layout generation methods. Exploring alternative script generation techniques or incorporating multiple VLLMs could strengthen the experiment part.
    
    **Rating:** 6: Marginally above acceptance threshold
    
    **Confidence:** 4: The reviewer is confident but not absolutely certain that the evaluation is correct
    
    **Fit:** Very clearly a multimedia paper, of interest to a large part of the community
    
    **Fit Justification:**
    
    Script2Layout is a multimedia task.
    
    **Technical Quality:** 5
    
    **Presentation Quality:** 6
    
    **Rebuttal Questions:**
    
    Please refer to the weakness part.
    
    **Additional Comments:**
    
- 日本語要約
    
    **レビュー概要：**
    
    本論文は、Manga109データセットから約20,000ページのマンガに対応するスクリプトデータを構築した「Manga109Script」を提案しています。主な目的は、物語のスクリプトを使用して一貫性のある表現力豊かなマンガのレイアウトを生成する「Script2Layout」タスクを実現することです。GPT-4などのVision Large Language Models（VLLMs）を活用して、シーン見出し、アクション説明、対話を含むスクリプトを生成しています。著者らは複数のScript2Layoutモデルを開発・評価し、スクリプト情報を組み込むことで、既存手法と比較してレイアウト生成の品質が大幅に向上することを実証しています。データセットと関連コードは論文公開時に利用可能となり、マンガレイアウト生成とビジュアルストーリーテリング研究の貴重なリソースとなります。
    
    **長所：**
    
    1. Manga109Scriptは、大規模なスクリプト連携データセットを提供することで、マンガレイアウト生成分野における重要なギャップを埋めています。これにより、データ不足により研究が進んでいなかったスクリプトベースのレイアウト生成の探求が可能になりました。
    2. 著者らは、ビジュアルプロンプティングと発話者を意識した対話シーケンスを用いて、VLLMsによるスクリプト生成の堅牢な手法を採用しています。GPT-4との多段階的な相互作用により、スクリプトが文脈的に一貫し、元のマンガの物語と整合することを保証しています。
    3. シーン見出しのリコール率、シーン見出しの精度、アクション説明の精度、文脈外アクション説明の検出精度、対話のリコール率などの人的評価指標により、データセットの品質の信頼性が示され、下流タスクへの信頼性が実証されています。
    4. 論文は問題定式化、データ構築プロセス、実験セットアップについて明確な説明がなされており、図表が重要なポイントと結果を効果的に説明するために使用されています。
    
    **短所：**
    
    1. スクリプト生成プロセスがGPT-4に依存しています。この依存性は再現性と信頼性に関する懸念を引き起こす可能性があります。
    2. 論文は定量的・定性的評価を提供していますが、詳細なエラー分析が欠けています。Script2Layoutモデルの一般的な失敗モードを理解することで、より深い洞察が得られ、将来の改善の指針となる可能性があります。
    3. 評価は主に既存のレイアウト生成手法との比較に焦点を当てています。代替的なスクリプト生成技術の探求や複数のVLLMsの統合により、実験部分をより強化できる可能性があります。
    
    **評価：** 6：受理閾値をわずかに上回る
    
    **確信度：** 4：評価が正しいことについて確信はあるが、絶対的な確信ではない
    
    **適合性：** 明確にマルチメディア論文であり、コミュニティの大部分にとって興味深い内容
    
    **適合性の根拠：** Script2Layoutはマルチメディアタスクである。
    
    **技術的品質：** 5
    
    **プレゼンテーション品質：** 6
    
    **リバタルへの質問：** 短所の部分を参照してください。
    
    **追加コメント：**
    
- 先生のコメント
    1. GPT-4 に頼りすぎていて、Script の生成における再現性と信頼性が保証されてないのでは？← 同様な手法を扱っている論文をそろえる
    2. 失敗例に関する評価が足りていない ← Appendix に書いてあることを伝えつつ、さらに補足的な分析があれば述べる。そしてこのことは、camera rady には載せるということを主張する
    3. 他の脚本生成での分析や VLLM を組み込みこむことでの評価は ? ← このような分析がなくても通っている論文を示す
- 反論の方針
    
    

## Reviewer 2 (wi4V)

- Review 本文
    
    **This paper presents an practical approach to manga layout generation by incorporating script information. The research is well-structured, addressing a clear problem in the field of creative AI and manga production. The authors provide comprehensive experiments and evaluations, comparing their approach with existing methods. While the work shows promise in improving layout generation, there are some concerns regarding the technical innovation in script construction and the depth of dataset application evaluation.**
    
    Official Reviewby Reviewer wi4V19 May 2025, 17:08 (modified: 09 Jun 2025, 23:38)Program Chairs, Senior Area Chairs, Area Chairs, Reviewer wi4V, Authors[Revisions](https://openreview.net/revisions?id=trwyYeYsLZ)
    
    **Review:**
    
    The paper introduces Manga109Script, a novel dataset linking scripts to manga layouts for approximately 20,000 pages from the Manga109 dataset. The authors propose a task called Script2Layout to generate manga layouts directly from scripts. They use Vision Large Language Models (VLLMs) to create script data and develop manga layout generation models that take scripts as input. The research compares these Script2Layout models with existing layout generation methods under various constraints, demonstrating improved performance, especially in mean Intersection over Union (mIoU) metrics.
    
    Pros: 1. The paper clearly defines the Script2Layout task and provides a thorough explanation of the Manga109Script dataset creation process. The methodology, experiments, and results are described in detail, giving readers a comprehensive understanding of the research. 2. The research addresses a practical problem in manga production, potentially bridging the gap between narrative scripts and visual layouts. The extensive evaluation using both quantitative metrics (FID, mIoU) and qualitative analysis demonstrates the effectiveness of the proposed approach.
    
    Cons: 1. While the paper presents a new dataset and task, the script/data generation process relies heavily on existing VLLMs and rule-based algorithms. While the process attempts to address narrative continuity across pages, it primarily focuses on structuring interactions with GPT-4o. There is limited innovation in how narrative continuity is maintained or enhanced, especially given the constraint of limited token length. This could impact the coherence and fluidity of the generated scripts across multiple pages. The technical innovation in script construction appears limited, as it primarily combines existing technologies rather than introducing novel algorithms or methods. 2. Although the paper provides extensive evaluations of the Script2Layout models, the assessment of the dataset's broader applications and potential impact on the field could be more comprehensive. The research focuses primarily on layout generation, but it could benefit from exploring other potential uses of the Manga109Script dataset or discussing its limitations and potential biases.
    
    Minor Issues: 1. Line 120: Typo Section 2.1: “unaerexplored” should be “underexplored”; 2. Line 150: “oppotunities” should be “opportunities”;
    
    **Rating:** 5: Marginally below acceptance threshold
    
    **Confidence:** 4: The reviewer is confident but not absolutely certain that the evaluation is correct
    
    **Fit:** Relevant to a part of the community
    
    **Fit Justification:**
    
    The paper fits well with the ACM Multimedia community as it bridges computer vision and natural language processing in multimedia content creation. It introduces a novel dataset and task that enhance visual storytelling, aligning with the community's focus on multimedia analysis and generation
    
    **Technical Quality:** 4
    
    **Presentation Quality:** 7
    
    **Rebuttal Questions:**
    
    Here are some questions for the authors to address during the rebuttal:
    
    1. Technical Innovation: Can you elaborate on the specific technical innovations introduced in the process of constructing manga scripts using VLLMs? How does this approach differ from existing methods?
    2. Dataset Applications: Could you provide more details on the potential applications of the Manga109Script dataset beyond layout generation? How might this dataset be utilized in other areas of multimedia research or industry?
    3. Limitations and Future Work: What are the current limitations of your approach, and what future work do you envision to address these challenges? How might you improve the integration of script information into layout generation?
    
    **Additional Comments:**
    
    No
    
- 日本語訳
    
    本論文は、スクリプト情報を組み込むことでマンガのレイアウト生成に対する実用的なアプローチを提示しています。この研究は、クリエイティブAIとマンガ制作分野における明確な課題に取り組んでおり、構造が整っています。著者らは包括的な実験と評価を提供し、既存手法との比較を行っています。レイアウト生成の改善において有望な結果を示していますが、スクリプト構築における技術的革新性とデータセット応用評価の深さについていくつかの懸念があります。
    
    **レビュー内容：**
    
    本論文はManga109Scriptを紹介しています。これはManga109データセットから約20,000ページのマンガのレイアウトとスクリプトをリンクさせた新しいデータセットです。著者らはScript2Layoutと呼ばれるタスクを提案し、スクリプトから直接マンガのレイアウトを生成します。Vision Large Language Models (VLLMs)を使用してスクリプトデータを作成し、スクリプトを入力として受け取るマンガレイアウト生成モデルを開発しています。この研究では、様々な制約下でこれらのScript2Layoutモデルを既存のレイアウト生成手法と比較し、特に平均Intersection over Union (mIoU)指標において改善された性能を示しています。
    
    **長所：**
    
    1. 論文はScript2Layoutタスクを明確に定義し、Manga109Scriptデータセット作成プロセスについて詳細な説明を提供しています。方法論、実験、結果が詳細に記述されており、読者に研究の包括的な理解を与えています。
    2. この研究はマンガ制作における実践的な問題に取り組み、物語のスクリプトとビジュアルレイアウトの間のギャップを埋める可能性を持っています。定量的指標（FID、mIoU）と定性的分析の両方を用いた広範な評価により、提案手法の有効性が実証されています。
    
    **短所：**
    
    1. 論文は新しいデータセットとタスクを提示していますが、スクリプト/データ生成プロセスは既存のVLLMsとルールベースのアルゴリズムに大きく依存しています。ページ間の物語の連続性に対処しようとしていますが、主にGPT-4oとの相互作用の構造化に焦点を当てています。特にトークン長の制限を考慮すると、物語の連続性がどのように維持・強化されるかについての革新性は限定的です。これは複数ページにわたるスクリプトの一貫性と流動性に影響を与える可能性があります。スクリプト構築における技術的革新性は、新しいアルゴリズムや手法を導入するというよりも、既存の技術を組み合わせているに過ぎないように見えます。
    2. 論文はScript2Layoutモデルの広範な評価を提供していますが、データセットのより広い応用可能性とその分野への潜在的な影響の評価をより包括的にする余地があります。研究は主にレイアウト生成に焦点を当てていますが、Manga109Scriptデータセットの他の潜在的な用途を探求したり、その制限やバイアスについて議論したりすることで、さらに充実した内容になる可能性があります。
    
    **細かな問題点：**
    
    1. 120行目：セクション2.1の"unaerexplored"は"underexplored"の誤字
    2. 150行目："oppotunities"は"opportunities"の誤字
    
    **評価：** 5：受理閾値をわずかに下回る
    
    **確信度：** 4：評価が正しいことについて確信はあるが、絶対的な確信ではない
    
    **適合性：** コミュニティの一部に関連性がある
    
    **適合性の根拠：**
    本論文は、マルチメディアコンテンツ作成におけるコンピュータビジョンと自然言語処理の橋渡しをするものであり、ACMマルチメディアコミュニティに適合しています。視覚的ストーリーテリングを強化する新しいデータセットとタスクを導入しており、マルチメディア分析と生成に焦点を当てるコミュニティの方向性に合致しています。
    
    **技術的品質：** 4
    
    **プレゼンテーション品質：** 7
    
    **リバタルへの質問：**
    以下の質問について、リバタルで著者からの回答を求めます：
    
    1. 技術的革新性：VLLMsを使用したマンガスクリプト構築プロセスにおける具体的な技術的革新について詳しく説明できますか？この手法は既存の手法とどのように異なりますか？
    2. データセットの応用：レイアウト生成以外のManga109Scriptデータセットの潜在的な応用について、より詳細な情報を提供できますか？このデータセットはマルチメディア研究や産業の他の分野でどのように活用できる可能性がありますか？
    3. 制限事項と今後の展望：現在のアプローチの制限は何で、これらの課題に対処するためにどのような今後の研究を想定していますか？スクリプト情報のレイアウト生成への統合をどのように改善できますか？
    
    **追加コメント：**
    なし
    
- 先生からのコメント
    
    2と3はこの人独自の質問だが、回答できそう？そもそも、漫画が思っているより広い市場と応用を持っているって思ってもらう方が無難かな。文化圏の差とかがありそうなら、それも認識してもらう。フランス人とか、漫画は子どものもので大人が触れるものではないって意識の人は自分以上の世代だととても多いから。
    
    → 自分の回答: 2 の質問について、漫画市場が拡大しておいることと、脚本からレイアウトを生成する研究は、映画やアニメにおける絵コンテの生成など、他の映像分野の研究に応用可能性を持っていることが回答になると考えます。 
    
    先生: これに加えて、漫画自体も情報伝達のフォーマットとして広告や教材など、単なる娯楽以上の広がりがあることをいっておくのは良さそうですね。
    
- 反論の方針
    1. 過去の同様な取り組み、一連の画像から物語を抽出する方法を取り上げつつ、我々の研究にどのような新規性があるのかを主張する。
    2. 次の２つの論点を主張する。一つは、この研究は、物語性のある視覚表現の制作全般に活用される可能性を持つと考えること。例えば、映画やアニメなどでも、テキストベースの脚本から中間表現として絵コンテが制作される。あらゆる視覚表現の中間表現の制作プロセスを支える技術として応用される可能性を持つと考える。もう一つは、そもそも漫画の市場は現在大きく拡大していることをFactとともに伝え、その拡大は教育やビジネス書における表現形式としても有益な表現として認められつつあり、本研究の社会的意義は大きいことをいう。
    3. 現状、Script データは一連の物語の中にある1ページを描写する表現になっているものの、レイアウトの生成はページ単位で独立に行う取り組みになっている。漫画など物語性をもつ視覚表現は、ひとつまえのページのレイアウト状況が対象のページのレイアウトに大きな影響を与えることは容易に想像でき、この点を考慮できていないことが本研究の limitation である。この課題に対して、今後の研究として、そのページに至るまでのレイアウト情報およびScript 情報を取り込み、レイアウトを生成する取り組みを行っていきたい。

## Reviewer 3 (zWvj)

- Review 本文
    
    **Work of dataset developed on exsiting images with LLM generated annotations and corresponding evaluation experiments**
    
    Official Reviewby Reviewer zWvJ16 May 2025, 00:39 (modified: 09 Jun 2025, 23:38)Program Chairs, Senior Area Chairs, Area Chairs, Reviewer zWvJ, Authors[Revisions](https://openreview.net/revisions?id=H0NNw0ysu5)
    
    **Review:**
    
    This paper presents Manga109Script dataset that consist of manga layout data generated from given script from Manga109 dataset. The authors used Vision Large Language Models (VLLMs) to generate scripts from the Manga109 dataset based on the unique narrative structure of manga, and employed visual prompting and speaker-aware dialogue sequencing to create high-quality script data. The authors also developed and evaluated manga layout generation models based on the proposed dataset and several LLMs, which prove that the script information improves layout generation quality compared to existing methods.
    
    Pros:
    
    1. The idea of generating manga layout from scripts by VLM and vice verse sounds novel and interesting
    2. The experiments seem adequate to validate the performance of the manga layout generation models developed on the dataset
    
    Cons:
    
    1. The dataset is based on existing manga image dataset and VLM generated prompts, and the manga layout generation models are based on existing LLM models, making the contribution limited
    2. The diversity of the images in the dataset seems to be limited. For example, there are only Japanese manga of many years ago, and all images seem to be black and white, which may limit the potential application
    3. The scripts are generated by VLM, and the Script2Layout models trained on the dataset are based on existing LLMs. The performance gap may be because of the distribution bias between the VLM and the LLM
    
    **Rating:** 4: Ok but not good enough - rejection
    
    **Confidence:** 3: The reviewer is fairly confident that the evaluation is correct
    
    **Fit:** Relevant to a part of the community
    
    **Fit Justification:**
    
    This paper presents a manga dataset with scripts, which do involve multimedia, but personally I believe computer vision or computer graphic conferences/journals are better fit
    
    **Technical Quality:** 4
    
    **Presentation Quality:** 5
    
    **Rebuttal Questions:**
    
    1. Will the dataset be publicly available?
    2. Is the dataset preparation pipeline effective to color images or comics of other languages?
    3. How to eliminate the influence of VLM used to annotate the images and the LLMs used in Script2Layout models?
    
    **Additional Comments:**
    
    This work is potentially beneficial to both ML society and comic industry. However, I think the the currently quality is slightly below the bar of ACMMM. It would make the contribution more solid if there are larger amount of more recent and more diverse data, like color images, comics with different languages, comics of different styles. Also, it would be more convincing if there are feedbacks from artists/readers.
    
    - 日本語訳
        
        この論文は、Manga109データセットから与えられたスクリプトから生成されたマンガレイアウトデータで構成されるManga109Scriptデータセットを提案しています。著者らは、マンガ特有の物語構造に基づいてManga109データセットからスクリプトを生成するために Vision Large Language Models (VLLMs) を使用し、視覚的プロンプトとスピーカーを意識したダイアログシーケンスを採用して高品質なスクリプトデータを作成しました。また、提案されたデータセットと複数のLLMsに基づいてマンガレイアウト生成モデルを開発・評価し、スクリプト情報が既存手法と比較してレイアウト生成の品質を向上させることを証明しています。
        
        **長所：**
        
        1. VLMによるスクリプトからのマンガレイアウト生成（およびその逆）というアイデアは斬新で興味深い
        2. データセットで開発されたマンガレイアウト生成モデルの性能を検証する実験は適切に行われている
        
        **短所：**
        
        1. データセットは既存のマンガ画像データセットとVLMで生成されたプロンプトに基づいており、マンガレイアウト生成モデルは既存のLLMモデルに基づいているため、貢献度が限定的
        2. データセット内の画像の多様性が限られている。例えば、何年も前の日本のマンガのみで、すべての画像が白黒であり、潜在的な応用を制限する可能性がある
        3. スクリプトはVLMによって生成され、データセットで訓練されたScript2Layoutモデルは既存のLLMsに基づいている。性能の差はVLMとLLM間の分布バイアスによる可能性がある
        
        **評価：** 4：まあまあだが十分ではない - 不採択
        
        **確信度：** 3：評価が正しいことについてかなりの確信がある
        
        **適合性：** コミュニティの一部に関連性がある
        
        **適合性の根拠：**
        この論文はスクリプト付きのマンガデータセットを提示しており、マルチメディアは関係していますが、個人的にはコンピュータビジョンやコンピュータグラフィックスの会議/ジャーナルの方が適していると考えます。
        
        **技術的品質：** 4
        
        **プレゼンテーション品質：** 5
        
        **リバタルへの質問：**
        
        1. データセットは公開される予定ですか？
        2. データセット作成パイプラインはカラー画像や他言語のコミックに対しても効果的ですか？
        3. 画像のアノテーションに使用されたVLMとScript2Layoutモデルで使用されたLLMsの影響をどのように排除しますか？
        
        **追加コメント：**
        この研究はML社会とコミック産業の両方に潜在的に有益です。しかし、現在の品質はACMMMの基準をわずかに下回っていると考えます。カラー画像、異なる言語のコミック、異なるスタイルのコミックなど、より最近の、より多様なデータが大量にあれば、貢献度がより確実なものになるでしょう。また、アーティスト/読者からのフィードバックがあれば、より説得力のあるものになるでしょう。
        
- 日本語訳
    
    既存画像とLLM生成アノテーション、および対応する評価実験に基づくデータセットの成果
    
    公式レビュー (レビュアー zWvJ)
    
    2025年5月16日 00:39 (修正: 2025年6月9日 23:38)
    
    プログラム委員長、シニアエリアチェア、エリアチェア、レビュアー zWvJ、著者
    
    **レビュー:**
    
    本論文は、Manga109データセットから与えられたスクリプトに基づいて生成された漫画レイアウトデータから構成されるManga109Scriptデータセットを提示しています。著者らは、漫画独自の物語構造に基づき、Vision Large Language Models (VLLMs) を用いてManga109データセットからスクリプトを生成し、ビジュアルプロンプティングと話者認識対話シーケンスを採用して高品質なスクリプトデータを作成しました。著者らはまた、提案されたデータセットといくつかのLLMに基づいて漫画レイアウト生成モデルを開発し、評価しました。これにより、既存の手法と比較して、スクリプト情報がレイアウト生成品質を向上させることが証明されました。
    
    **長所:**
    
    - VLMと、その逆でスクリプトから漫画レイアウトを生成するというアイデアは斬新で興味深い。
    - データセット上で開発された漫画レイアウト生成モデルの性能を検証する上で、実験は適切に見える。
    
    **短所:**
    
    - データセットは既存の漫画画像データセットとVLMが生成したプロンプトに基づいており、漫画レイアウト生成モデルは既存のLLMモデルに基づいているため、貢献が限定的である。
    - データセット内の画像の多様性が限られているように見える。例えば、かなり昔の日本の漫画しかなく、すべての画像が白黒であるため、潜在的な応用が制限される可能性がある。
    - スクリプトはVLMによって生成されており、データセットで訓練されたScript2Layoutモデルは既存のLLMに基づいている。性能差は、VLMとLLM間の分布バイアスに起因する可能性がある。
    
    **評価:** 4: 悪くはないが十分ではない - 不採択
    
    **確信度:** 3: レビュアーは評価が正しいとかなり確信している。
    
    **適合性:** コミュニティの一部に関連性がある。
    
    適合性の根拠:
    
    本論文は、スクリプト付きの漫画データセットを提示しており、マルチメディアを含みますが、個人的には、コンピュータビジョンまたはコンピュータグラフィックスの会議/ジャーナルがより適していると考えます。
    
    技術的品質: 4
    
    発表品質: 5
    
    **反論に関する質問:**
    
    - データセットは公開される予定ですか？
    - データセット準備パイプラインは、カラー画像や他の言語のコミックにも効果的ですか？
    - 画像の注釈付けに使用されたVLMと、Script2Layoutモデルで使用されたLLMの影響をどのように排除しますか？
    
    **追加コメント:**
    
    本研究は、MLコミュニティとコミック業界の両方に潜在的に有益です。しかし、現在の品質はACMMMの基準をわずかに下回っていると思います。より最近の、より多様なデータ（カラー画像、異なる言語のコミック、異なるスタイルのコミックなど）が大量にあれば、貢献はより確固たるものになるでしょう。また、アーティストや読者からのフィードバックがあれば、より説得力が増すでしょう。
    
- 先生からのコメント
    
    > Will the dataset be publicly available?
    > 
    
    には、yesで
    
    > Is the dataset preparation pipeline effective to color images or comics of other languages?
    > 
    
    → Yesを多少の根拠とともに示せばOK。例えばvisual promptingは元々color imageに対して行われているし、むしろinformationが増えるからやりやすいはず、とか、言語に特有の何かは使っていないので、他の言語で動かないと考える合理的な理由がない、もっとspecificに指摘を貰えると今後の参考になり、嬉しい、といって査読者に適当であることを許さないようにする、とか。
    
    > How to eliminate the influence of VLM used to annotate the images and the LLMs used in Script2Layout models?
    > 
    
    → これも、Performance gapの項目のことだと思うが、ちょっとよくわからない…
    
    自分の感想: おそらくこの reviewer は、VLLMを使って、その script を作ったのだから、その VLLM と近しい分布を持っている LLM があれば、そこからが画像を再構成するときに、その分布の利点を使って、より精度の高い、レイアウトを生成してしまえるのでは？と言っていると思われる。→ 画像情報としての特徴量と生成されるレイアウトの数値情報は、その形態の違いから特徴量空間において十分に乖離したものになっていると考えられるので、このような影響は無視できるほど小さいと考える。
    
- 反論の方針
    1. yes
    2. カラーや他の言語でも原理的にうまく適応されるはず。そもそも Visual Prompting はカラー画像で提案されている手法である。カラー画像は、白黒が画像に比べ情報量が多く理解が用意になることが知られている。また、言語においても日本語以外でうまくいかない合理的な理由がない。これらを Fact とともに伝える。
    3. あなたの言う VLM と LLM の影響というのは、VLM と LLM の分布の近さがパフォーマンスに及ぼす影響についてのことでしょうか。と一度きちんと確認しつつ、私は、それらの影響は限りになく小さいと考える。と主張する。なぜなら、Script2LayoutモデルとしてLLMが生成するレイアウト表現は、VLMに与える漫画画像の表現と大きく乖離した表現をとっており、生成に影響を与えた分布の近さをたどって、レイアウト生成の精度が向上するようなことはないと考える。と主張する。
    

## Reviewer4 (ZqvN)

- Review 本文
    
    **Review of Submission #4528**
    
    Official Reviewby Reviewer ZqvN05 May 2025, 09:52 (modified: 09 Jun 2025, 23:38)Program Chairs, Senior Area Chairs, Area Chairs, Reviewer ZqvN, Authors[Revisions](https://openreview.net/revisions?id=k5ZYPfvtZV)
    
    **Review:**
    
    This paper constructs the Manga109Script dataset that creates script data for approximately 20,000 pages from the existing Manga109 dataset. An annotation-assisted method is introduced to generate script data from manga images using existing VLLMs. Several baselines are used for the script-based layout generation task. However, the contribution of the whole data creation process is not very clear. The key idea of this paper is to create a new dataset that could support script-based manga layout generation. However, the proposed dataset comes from the existing Manga109script dataset. The script data is generated by existing VLMs. The only contribution is the human evaluation process for quality verification. I cannot see new insights for the proposed benchmark.
    
    **Rating:** 4: Ok but not good enough - rejection
    
    **Confidence:** 4: The reviewer is confident but not absolutely certain that the evaluation is correct
    
    **Fit:** Very clearly a multimedia paper, of interest to a large part of the community
    
    **Fit Justification:**
    
    This paper focuses on the manga image understanding task, which includes multiple subtasks that align with the ACM Multimedia Topics of Interest.
    
    **Technical Quality:** 5
    
    **Presentation Quality:** 5
    
    **Rebuttal Questions:**
    
    1. The difference between the proposed Scirpt2Layout and the existing layout generation model is also not clear. As shown in Fig.2, it is not difficult to extract elements from the script (using rule-based or LLM-based processing) for existing layout generation models.
    2. The current evaluation metrics and compared methods are not thorough. Additional geometric and content-aware evaluation metrics are necessary to evaluate the layout quality. In addition, existing content-aware layout generation methods, including PosterLlama and LVMs, should be compared and discussed in the experiments.
    
    **Additional Comments:**
    
    As this paper focuses on the script2layout task, it would be better to show the script data in the qualitative comparisons.
    
    - 日本語訳
        
        この論文は、既存のManga109データセットから約20,000ページ分のスクリプトデータを作成するManga109Scriptデータセットを構築しています。既存のVLLMsを使用してマンガ画像からスクリプトデータを生成する注釈支援手法が導入されています。スクリプトベースのレイアウト生成タスクに対していくつかのベースラインが使用されています。しかし、データ作成プロセス全体の貢献度が明確ではありません。この論文の主要なアイデアは、スクリプトベースのマンガレイアウト生成をサポートできる新しいデータセットを作成することですが、提案されたデータセットは既存のManga109Scriptデータセットから得られたものです。スクリプトデータは既存のVLMsによって生成されており、唯一の貢献は品質検証のための人間による評価プロセスです。提案されたベンチマークに新しい洞察を見出すことができません。
        
        **評価：** 4：まあまあだが十分ではない - 不採択
        
        **確信度：** 4：評価が正しいことについてかなりの確信があるが、完全に確信しているわけではない
        
        **適合性：** 明確にマルチメディア論文であり、コミュニティの大部分にとって関心のあるもの
        
        **適合性の根拠：**
        この論文はマンガ画像理解タスクに焦点を当てており、ACMマルチメディアの関心トピックに合致する複数のサブタスクを含んでいます。
        
        **技術的品質：** 5
        
        **プレゼンテーション品質：** 5
        
        **リバタルへの質問：**
        
        1. 提案されたScript2Layoutと既存のレイアウト生成モデルとの違いが明確ではありません。図2に示されているように、既存のレイアウト生成モデルに対して（ルールベースまたはLLMベースの処理を使用して）スクリプトから要素を抽出することは難しくありません。
        2. 現在の評価指標と比較手法が十分ではありません。レイアウトの品質を評価するために、追加の幾何学的およびコンテンツを考慮した評価指標が必要です。さらに、PosterLlamaやLVMsを含む既存のコンテンツを考慮したレイアウト生成手法を実験で比較・議論する必要があります。
        
        **追加コメント：**
        この論文はscript2layoutタスクに焦点を当てているため、定性的比較でスクリプトデータを示す方が良いでしょう。
        
- 日本語訳
    
    提出物 #4528 のレビュー
    
    公式レビュー (レビュアー ZqvN)
    
    2025年5月5日 09:52 (修正: 2025年6月9日 23:38)
    
    プログラム委員長、シニアエリアチェア、エリアチェア、レビュアー ZqvN、著者
    
    **レビュー:**
    
    本論文は、既存のManga109データセットから約20,000ページ分のスクリプトデータを作成するManga109Scriptデータセットを構築しています。既存のVLLMを用いて漫画画像からスクリプトデータを生成するアノテーション補助手法が導入されています。スクリプトベースのレイアウト生成タスクにはいくつかのベースラインが使用されています。しかし、データ作成プロセス全体の貢献はあまり明確ではありません。本論文の主なアイデアは、スクリプトベースの漫画レイアウト生成をサポートできる新しいデータセットを作成することです。しかし、提案されたデータセットは既存のManga109データセットから派生しており、スクリプトデータは既存のVLMによって生成されています。唯一の貢献は、品質検証のための人間による評価プロセスです。提案されたベンチマークに新しい洞察は見られません。
    
    **評価:** 4: 悪くはないが十分ではない - 不採択
    
    **確信度:** 4: レビュアーは評価が正しいと確信しているが、絶対的な確実性はない。
    
    **適合性:** 非常に明確なマルチメディア論文であり、コミュニティの大部分にとって興味深い。
    
    適合性の根拠:
    
    本論文は、漫画画像理解タスクに焦点を当てており、ACMマルチメディアの関心分野に合致する複数のサブタスクを含んでいます。
    
    技術的品質: 5
    
    発表品質: 5
    
    **反論に関する質問:**
    
    - 提案されたScript2Layoutと既存のレイアウト生成モデルとの違いも明確ではありません。図2に示されているように、既存のレイアウト生成モデルにとって、スクリプトから要素を抽出すること（ルールベースまたはLLMベースの処理を使用）は難しくありません。
    - 現在の評価指標と比較手法は徹底されていません。レイアウト品質を評価するには、追加の幾何学的およびコンテンツ認識型の評価指標が必要です。さらに、PosterLlamaやLVMを含む既存のコンテンツ認識型レイアウト生成手法も、実験で比較・議論されるべきです。
    
    **追加コメント:**
    
    本論文はscript2layoutタスクに焦点を当てているため、定性的な比較でスクリプトデータを示すと良いでしょう。
    
- 先生からのコメント
    
    
- 反論の方針
    1. 既存のレイアウト生成モデルのために、Script から要素を抽出することが難しくないということは、我々も全く同じ考えであり、本研究は、むしろそのプロセスにおいて課題を見出したものである。Script には、キャラクター同士の関係や動作、状況の説明が含まれる。それはレイアウトに大きな影響を与えるものであると考えるが、既存のレイアウト生成モデルでは、それらの多くの情報を捨てざるを得ない。本研究は、Script に書かれた情報を直接に活用することで、レイアウトの生成精度を向上することが確認された。
    2. まず、前提において、背景画像がすでに既知とするポスターなどのレイアウト生成とは異なり、漫画画像の下書きすらない制作過程において、下書きの制作に有益な技術として Script2Layout モデルを提案している。したがって、Occulusion や Readability score などの評価指標は本問題設定の上で活用が困難な評価指標であると考えている。漫画という表現形式の上で、適切な評価指標を考案することは、今後取り組むべき課題としたい。また、比較するメソッドとしてとり挙げた既存手法はいずれもレイアウト生成手法として高い精度を誇り、特に LayoutPrompter は、content-aware な手法である。

---

# GoodNote

---

[Reviewの分析およびPosterLlamaについての確認.pdf](ACMMM2025%20%E3%83%AA%E3%83%8F%E3%82%99%E3%82%BF%E3%83%AB%20Rebuttal%20%E6%BA%96%E5%82%99%2020f6833ec28b804394c2f2cddc2c220a/Review%E3%81%AE%E5%88%86%E6%9E%90%E3%81%8A%E3%82%88%E3%81%B2%E3%82%99PosterLlama%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6%E3%81%AE%E7%A2%BA%E8%AA%8D.pdf)

[Reviewの分析およびPosterLlamaについての確認_2.pdf](ACMMM2025%20%E3%83%AA%E3%83%8F%E3%82%99%E3%82%BF%E3%83%AB%20Rebuttal%20%E6%BA%96%E5%82%99%2020f6833ec28b804394c2f2cddc2c220a/Review%E3%81%AE%E5%88%86%E6%9E%90%E3%81%8A%E3%82%88%E3%81%B2%E3%82%99PosterLlama%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6%E3%81%AE%E7%A2%BA%E8%AA%8D_2.pdf)

# e-mail announce from [tpc@acmmm2025.org](mailto:tpc@acmmm2025.org), tpc(technical Program Comittee)

### 1

- 本文
    
    Dear Kengo Watanabe,
    
    According to the timeline, the reviews have been released on Monday June 9, 2025. We have secured at least three reviews for each submission, while most submissions have received four or five reviews.
    
    As announced on the conference website and the OpenReview submission form, papers co-authored by authors that did not contribute to the review process by completing their assignments - despite numerous reminders and deadline extensions - will not receive reviews at this stage. In contrast to other conferences of this size, we will not desk-reject the affected papers, but instead the authors of the affected papers will not be able to see the reviews during the rebuttal period and, therefore, won’t be able to participate in the rebuttal.
    
    Unfortunately, OpenReview is currently experiencing technical difficulties with the rebuttal comment process, presumably due to recent updates to the platform, which is affecting multiple venues including ACM Multimedia. We are in contact with OpenReview to find a solution as quickly as possible. We are as frustrated by this delay as you are and will keep you updated as soon as the OpenReview team has resolved the issue. Due to this delay, the rebuttal deadline will also be extended, with more information to follow soon.
    
    When there is something clearly wrong with the reviews, consult the Author's Advocate guidelines to assess whether you should make a request for mediation:
    
    [https://acmmm2025.org/authors-advocate/](https://acmmm2025.org/authors-advocate/)
    
    To all the hundreds of you who emailed us, we hear you, we are not ignoring you, and we will get back to you as soon as we can. We are all in this together and appreciate your patience with this. As soon as OpenReview has the rebuttal process back, we will continue with the regularly scheduled programming.
    
    Sincerely yours,
    
    Jenny, Luca, Phoebe, Stevan, Tien, and Wen-Huang
    
    Technical Program Chairs
    
    Please note that responding to this email will direct your reply to [tpc@acmmm2025.org](mailto:tpc@acmmm2025.org).
    
- 要点
    
    このメールの重要ポイント：
    
    - レビュー公開について：
        - 2025年6月9日（月）にレビューが公開
        - 各論文に対して最低3件、多くは4-5件のレビューを確保
    - レビュー担当者としての義務について：
        - レビュー担当を完了しなかった著者の論文は、この段階でレビューを閲覧できない
        - デスクリジェクトはされないが、リバタル期間中にレビューを見ることができず、リバタルにも参加できない
    - システムの技術的問題：
        - OpenReviewでリバタルコメントプロセスに技術的な問題が発生
        - 解決に向けて対応中
        - リバタルの締切は延長予定
    - レビューに問題がある場合：
        - Author's Advocate（著者擁護者）のガイドラインを参照
        - 調停要請が必要かどうかを判断することを推奨
    - 問い合わせについて：
        - 多数のメールを受け取っており、順次対応予定
        - OpenReviewのリバタルプロセスが復旧次第、通常のスケジュールを再開

### 2

- 本文
    
    Dear Kengo Watanabe,
    
    The rebuttal option is now available on OpenReview. To compensate for the delay caused by the technical issues, we extended the deadline for rebuttals to 19 June 2025 (AoE). We again apologise for any inconvenience this may have caused.
    
    To respond to the reviews, please follow the instructions below.
    
    1. Log into OpenReview and select ACMMM 2025 Conference Authors in Your Active Consoles.
    2. Go to the paper for which you would like to post a rebuttal and carefully read reviewer comments.
    3. Click on the button Rebuttal to add one rebuttal per review.
    4. Address reviewer comments in a concise manner, indicating which review you are responding to. The rebuttals should be self-contained and should not contain links to the external materials such as code and videos.
    5. Note that the rebuttal must maintain anonymity.
    
    The instructions can also be found on the following page: [https://acmmm2025.org/information-for-authors/](https://acmmm2025.org/information-for-authors/)
    
    Sincerely yours,
    
    Jenny, Luca, Phoebe, Stevan, Tien, and Wen-Huang
    
    Technical Program Chairs
    
    Please note that responding to this email will direct your reply to [tpc@acmmm2025.org](mailto:tpc@acmmm2025.org).
    
- 要点
    
    このメールの重要ポイント：
    
    - リバタルの提出期限：2025年6月19日 AoE まで延長
    - 提出手順：
        - OpenReviewにログインし、「ACMMM 2025 Conference Authors」を選択
        - 対象論文のレビューを確認
        - 各レビューに対して個別にリバタルを提出（「Rebuttal」ボタンを使用）
        - レビューへの返答は簡潔に、どのレビューに対する返答かを明確に
        - 外部リンク（コードやビデオ）は含めない
    - 重要な注意事項：
        - 匿名性を維持すること
        - 各リバタルは自己完結的であること

### 3

- 本文
    
    Dear Kengo Watanabe,
    
    We have received multiple requests for clarification about the rebuttal formatting. As communicated in our previous email, you should follow these steps to submit your rebuttals:
    
    - Log into OpenReview and select ACMMM 2025 Conference Authors in Your Active Consoles
    - Go to the paper for which you would like to post a rebuttal and carefully read reviewer comments
    - Click on the button Rebuttal to add one rebuttal per review.
    - Address reviewer comments in a concise manner, indicating which review you are responding to. The rebuttals should be self-contained and should not contain links to the external materials such as code and videos.
    - Note that the rebuttal must maintain anonymity.
    
    Rebuttal instructions are also available on the following page: [https://acmmm2025.org/information-for-authors/](https://acmmm2025.org/information-for-authors/)
    
    Below are the answers to some frequently asked questions:
    
    - What does "Click on the button Rebuttal to add one rebuttal per review." mean? This means that if you have received N reviews (e.g. N=3) you should repeat the procedure N times to add N rebuttals (i.e. one per review). If you received 3 reviews, you should add 3 rebuttals. If you received 4 reviews, you should add 4 rebuttals etc.
    - Is it possible to edit or delete the rebuttal? Yes, you can edit or delete rebuttal during the rebuttal period, which ends on 19.06.2025 23:59 AoE.
    - Can I add an image to my Rebuttal? As per OpenReview documentation, the platform does not support images.
    - How can I format text of the rebuttal? As noted in OpenReview Rebuttal form, which opens once you click on the button Rebuttal: "Rebuttals can include Markdown formatting and LaTeX forumulas, for more information see [https://openreview.net/faq](https://openreview.net/faq)"
    
    Have a nice weekend!
    
    Sincerely yours,
    
    Jenny, Luca, Phoebe, Stevan, Tien, and Wen-Huang
    
    Technical Program Chairs
    
    Please note that responding to this email will direct your reply to [tpc@acmmm2025.org](mailto:tpc@acmmm2025.org).x
    
- 要点
    
    このメールのポイント：
    
    - リバタルの提出方法について：
        - OpenReviewにログインし、ACMMM 2025 Conference Authorsを選択
        - 対象論文のレビューを確認
        - 各レビューに対して1つずつリバタルを提出（例：3つのレビューに対して3つのリバタル）
        - 外部リンクや画像は含めないこと
        - 匿名性を保持すること
    - リバタルの編集・削除：
        - 期限（2025年6月19日23:59 AoE）まで可能
    - フォーマットについて：
        - 画像は使用不可
        - MarkdownとLaTeXの数式が使用可能
    - 締切：2025年6月19日23:59 AoE

# Rebuttal の検討

## Reviewer 1

## Response to Reviewer ryDR25

We sincerely thank Reviewer ryDR25 for their thoughtful evaluation and constructive feedback. We address your concerns in the order raised.

**1. On GPT-4 Dependence, Reproducibility, and Reliability**

Our methodology builds upon established techniques with proven reliability. We strategically combine Chain-of-Thought prompting, Visual Prompting, and multi-step interaction methods that have been individually validated in prior work. Our novel integration addresses manga-specific challenges including character re-identification across panels and narrative continuity maintenance. This technical foundation, combined with comprehensive human evaluation across multiple metrics (Scene Heading Precision: 0.838, Action Description Precision: 0.664), ensures methodological robustness.

Importantly, recent top-tier publications demonstrate community acceptance of single-LLM methodologies when they enable significant contributions. G-Eval (EMNLP 2023) relies entirely on GPT-4 for evaluation frameworks and achieved superior performance. LLaVA (NeurIPS 2023 Oral) uses GPT-4 for generating all 158K multimodal instruction samples, earning oral designation. VisDiff (CVPR 2024 Oral) employs GPT-4 as both generator and evaluator. These works achieved highest recognition, indicating that the research community values practical innovation when robust validation accompanies the methodology.

**2. On Detailed Error Analysis**

We acknowledge this important point. Our supplementary material (Sec. B) includes failure case analysis such as "excessive speech balloon enlargement." We recognize this area for deeper exploration in future work, which will inform improved script generation methodologies and provide valuable insights for the research community.

**3. On Experimental Scope and Alternative Methods**

Our focus on establishing Script2Layout effectiveness reflects accepted practice for novel task introduction. Recent breakthrough papers like Genie (ICML 2024 Best Paper) established entirely new capabilities without exhaustive baseline comparison. Similarly, SyncDreamer (ICLR 2024 Spotlight) and StableRep (NeurIPS 2023) achieved top recognition by demonstrating core feasibility rather than comprehensive method exploration.

Our results consistently demonstrate that script information fundamentally improves layout generation across multiple models and metrics (e.g., Swallow-13B FID: 35.845→18.415 with script input). This establishes the foundational effectiveness necessary for future exploration of alternative script generation methods.

Thank you for your valuable feedback, which strengthens our contribution.

## Reviewer 2

### **Response to Reviewer wi4V**

We sincerely thank the reviewer for the thoughtful feedback. Below we address the three points raised:

1.  **Technical Innovations in Script Construction**

While our pipeline relies on VLLMs, it introduces key innovations specific to the manga domain:

**(a)** We adapt visual prompting to black-and-white manga, marking each character’s face with a colored circle and listing corresponding names. This facilitates speaker-aware script generation and, to our knowledge, is the first such application in manga.

**(b)** To enable long-range story understanding over 100–200 pages, we introduce a synopsis generation step. A summary of all preceding pages is generated and provided to the model alongside the current page input. This maintains narrative continuity while meeting token constraints. Unlike VIST or StoryGen, which use short image sequences, our setting handles an order of magnitude longer contexts.

**(c)** The system outputs scripts in a professional Japanese screenplay format, including scene headings, action descriptions, and dialogue. This structured output is distinct from prior work on free-form visual storytelling.

1.  **Dataset Applications (Beyond Layout Generation)**

Manga109Script supports broader applications in media production:

**(a)** The alignment of page images with professional script triples enables data-driven automation of intermediate formats like name boards or storyboards, widely used in manga, anime, and film pre-production.

**(b)** The manga market is expanding rapidly and diversifying into educational and business contexts. Our dataset and models can help lower creative barriers, offering accessible tools for drafting and structuring visual narratives.

These directions demonstrate impact beyond layout generation, supporting both academic and industrial use cases.

1.  **Limitations and Future Work**

Currently, each page is processed independently, limiting cross-page coherence. We plan to summarize the layouts and scripts of the previous *k* pages into a context vector and concatenate it with the current page script. Early results on four-page inputs show smoother layout transitions.

## Reviewer 3

### Reviewer zWvj – Rebuttal

**Q1. Will the dataset be publicly available?**

Yes. The Manga109Script dataset will be made publicly available upon acceptance of the paper, in accordance with the licensing conditions of the original Manga109 dataset.

**Q2. Is the dataset preparation pipeline effective for color images or comics in other languages?**

We believe the proposed pipeline can be effectively extended to both color images and comics written in languages other than Japanese. Visual prompting was originally developed for color images and benefits from the rich semantics that colors provide. For instance, color facilitates the extraction of contextual cues such as character identity and scene boundaries, which enhances visual understanding in long-form narratives. As the information density in color images is typically higher than in monochrome images, adapting our method to color content is not only feasible but potentially even easier. Regarding multilingual applicability, our prompting structure is language-agnostic and requires only that speaker names be appropriately annotated. Therefore, we see no fundamental obstacle to using this pipeline in non-Japanese contexts.

In addition, the Manga109 dataset contains a wide variety of genres and art styles that reflect modern manga production and remains a valuable resource for academic research. This is evidenced by top-tier publications such as [1], which use only Manga109 data to demonstrate strong results in manga analysis and understanding.

**Q3. How to eliminate the influence of VLMs and LLMs?**

We appreciate the concern regarding potential overlap in the distributions learned by the vision-language models used for script generation and the large language models used in Script2Layout. However, we believe that any such influence is negligible. The input modalities and tasks for the two stages are fundamentally different. In the first stage, script generation is guided by visual inputs and constrained to output production-quality Japanese screenplays with explicit structure. In the second stage, Script2Layout models receive only the textual script and output spatial layouts. As the representations are distinct and the tasks require different forms of reasoning, it is unlikely that performance is meaningfully affected by shared latent knowledge between the models.

[1] Xie, M. et al. “Advancing Manga Analysis: Comprehensive Segmentation Annotations for the Manga109 Dataset.” *CVPR 2025*.

## Reviewer 4

### **Rebuttal to Reviewer ZqvN**

We sincerely thank Reviewer ZqvN for the valuable feedback.

**Q1. On the difference between Script2Layout and existing layout models**

We appreciate the reviewer’s comment and completely agree that extracting elements such as characters and speech balloons from a script using rule-based or LLM-based methods is technically feasible. Our research starts from the same understanding. However, we observe a limitation in this approach: while scripts include rich narrative information—such as character relationships, actions, and situational descriptions—that strongly influence layout, existing layout generation methods must reduce this to a small set of discrete tokens, inevitably discarding much of that information. Our method addresses this limitation by directly conditioning layout generation on the full script, allowing the model to utilize descriptions of characters, actions, and settings in a unified manner. This leads to improved layout fidelity, especially in conveying story flow and spatial consistency.

**2. On evaluation metrics and comparisons**

We acknowledge that our evaluation metrics can be expanded in future work. However, our problem setting is fundamentally different from that of poster layout generation, where background images are pre-given. In our case, the task is to generate an initial draft of a manga layout from only the script, without any background images. As such, occlusion-based and readability-based metrics designed for background-aware settings are not directly applicable. Regarding the methods we compared against, we chose strong baselines known for their layout accuracy, including LayoutPrompter, which is a content-aware method. We also plan to expand our comparisons to include more content-aware models that use training-based approaches, to further validate our framework.

# MTG

Summary

このミーティングでは、学術論文のレビューに対するリバッタル（反論）戦略について議論されました。参加者は論文が予想より厳しい評価を受けたことを受け、効果的な反論方法を検討しています。

### 論文の概要と評価状況

- 漫画のスクリプトからレイアウト生成に関する研究
- 予想より厳しい評価スコアを受けた
- GPT-4のみを使用している点が批判されている
- テクニカルイノベーションが足りないという指摘

### リバッタル戦略のポイント

- 反論は事実に基づくべき、単なる意見表明は避ける
- 簡潔に書く（2500字制限あり、長すぎると読まれない）
- 査読者が事実を誤解している点や不公平な判断基準を指摘する
- アルゴリズム的新規性ではなく、データセットとしての貢献を強調する
- 同様のアプローチ（GPTのみ使用）で採択された論文を引用する

### 具体的な反論内容

- GPT-4のみを使用していても再現性はある（APIとバージョン指定で再現可能）
- 技術的革新より、コミュニティへの貢献が重要であることを主張
- 本研究はアルゴリズム研究ではなくデータセット研究であることを明確にする
- 既存手法（ポスターラマなど）と本研究の違いを明確に説明する
    - セリフだけでなく演出情報も含めたスクリプト全体を活用している点

### 課題と改善点

- エラー分析が不足している点は認め、アペンディックスで対応すると約束する
- ACMマルチメディアで採択された類似手法の論文を少なくとも3つ引用する
- ノースクリプトとスクリプトの比較結果をもっと強調する

### アクション項目

- [ ]  ACMマルチメディアで採択された類似手法の論文を探す
- [ ]  リバッタル草案を修正し、より簡潔で事実に基づいた内容にする
- [ ]  発端に相談して、リバッタルを進めるかICCVを優先するか決定する
- [ ]  締切（7月19日AOE）までに提出できるよう準備を進める

### 次のステップ

- 発端に相談して最終方針を決定する
- 7月19日の締切までにリバッタルを提出するか判断する
- ICCVの提出も検討中（優先度の判断が必要）

Notes

Transcript

コメントに置いちゃいましたがありがとうございますえっとまず結構厳しいスコアでそうですね 思ったより厳しかった悲しいちょっとなんか茶読者に恵まれてないなっていう感じはあるけどそれも含めて茶読なんで おだしょー リンク貼ったやつが なぜかほぼ同じ評価で でもオーラルで去年通ってる ですけど あれは一人すごい肯定的な 探索者がいて レバッタルに加えてなんかあそこに見えてない範囲ですごいこの論文通さなきゃダメだよって言ったら なんか始まろうっていうレビューアーがいたからと思うんですけどなるほどそういうエンジェルみたいなレビューアーがたまに現れることはあるんだけどまぁちょっと期待し

かなり運がいい場合だけなので、どうしようかなっていう感じですね。 おだしょー なんやっけ サイバー エージェントのワークショップが サドクじゃないんですよね あれ ね三沢 そうなんですねおだしょー あれ なんか なんや っけ オーガナイザーが 選ぶって書いてあるそれはそれでさどっかりって言えないなそれで通すのなんかイマイチかなっていう気もするんですよね レビューって書いてあるね

でもレビューって書いてあるのか

ん?何に通したの?あ、茶読付きのあ、そうですね、茶読ありに通したとは言えるかな

すみません、そうか、あれ何、僕こう 間違いしたのは何だノンプラシーディングトラックかの方はオーガナイザーが ジュリーするって書いてあるのか プロセーディングストラックに 出せば一応ピアレビューになるシングルブラインドだから名前 ありの状態で送ってシングル ですね

7月3日7月3日がデッドラインのやつですよねそうですね7月3日 一週間で結果が出るよ これピアレビューすごいな早すぎない?すごいですね 自分の知識は当然 少ないんですけど、ACMMと比べると全然早いんですね。 何本ぐらい投稿される想定なんかわかんないけど相当少ない想定で1話のオーガナイザーだけでバッてやるんじゃないかな3日ぐらい

しばらくお待ちください。

なんで僕としてはICCBもどうせ行かなきゃいけないから地球一周しなきゃいけなくなるんで レシーブも10秒で通ったらまあ嬉しいわ 無理とは言わないけどどうしましょうね まあいいや、とりあえずレバッタリの草案から見ていきましょうありがとうございます、今正直その、割と日本語ベースでずっと考えて書いてて英語に言えば まず日本語のやつを共有してくれてもよかったんですけどすいません、確かに、そうですよね、それもしかもなんか

ちょっと今…質問…そうですねほう…今…ちょっと今すぐには出せないんですけどじゃあ順番に見ていくと割と英語があんま想定と違っている感じになってたのが 今になって色気づいた LLM丸出しな感じに もうちょっとちゃんといろいろやればよかったです すみませんそうですね まずこういうやつはちゃんとナンバリングして書かないと 見つかるって分からないんで 文字数使っちゃうけど、もう少しファーストオーサーの名前と論文のフルタイトルと すぐググれるぐらいにしないと不親切ですね本文の中にそれを記述する感じですそれとも

論文みたくそれでやって後ろに参照つけてっていう僕はなんかよくABCって書くんですけど茶道の時も書いてます 査読のときなんか本、元の論文の1、2、3とややこしいんでなるほど変えてるんですけどまああんまりそういう細やかな聞くぶりをする人いないんでそれははい、ぜひ 教えていただいたんで 踏襲します三つあるよっていう形で反論して あんまり長々書かないほうがいいですはっきり言って こうやらないと これ読んでる間にもう嫌になると思うレビューは 2500文字、メールで改めてそのなんかいろいろ 質問が来たからその質問に改めて答えますみたいなメールが追加できてましてそれも共有させて頂ければと思ったんですけどあれですよね1レビューに対して1レバってるやったりとかそうですそうですそれでなんかラディとかなんかで結構その

でもボタンは1個しかないよねみたいなそれどうすんねんみたいなけんけんガクガクなったんですけどそれに対して毎回上のボタンを その3回レビュアがいたら3人分 押してっていう風になっててそう しかももうレビュアに押した 瞬間見えるそうなんですねそうそうだった 昨日、2500文字っていう制限があるのは分かってたんですけど、それって何回やっても2500文字ずつ追加されるのかなっていうのを確認したくて押しちゃったんですけど。 おだしょー そう なんか見えて いるんでしばやん なんか僕がレビューしている ほかのやつでレビュア1の回答とか書いてあってレビュア1って 誰やねんって番号が123じゃないから

標準順も何か場合によって変わ ったりするかもしれないんでそこは気を付けてくださいはいまず基本的にレバッタルって何か っていうと事実に関する 理解をされていることに対する反論とかあとアンフェアなジャッジに対して 授業基準はこうあるべきじゃないの?っていうファクトの提示なので それ以外の意見共鳴は、基本。

特にエリアチェアにとって立ってみるときにこの人何が言いたいのっていうのはすごいわかんなくなるので本当になんていうのかな 削った方がいいです 余計なことは GPT-4でだけしかやってないことを理由にアンリライアブル 言うけど 過去にちゃんとACMマルチ メディアでそういう条件で通っている論文が3個以上あるんで この 論文だけそれを理由にそれを リジェクトの理由にするとかメジャーコンサートにするのはちょっと アンフェアだよねっていう書き方をしたほうがいいな

その

おだしょー なるほど三沢 ACMマルチメディアじゃなくても いいけど 1個ぐらいはACMマルチメディアのほうがいいおだしょー そうしました

おだしょー 要するに 査読基準は ここにあるべきじゃないんですかっていうのをファクトベースで言う とか 本当に論文書いてあることと全然違うことを言ってるこいつ っていうのをファクチュアルエラーですって 結構 ファクチュアルエラー ですっていうの 喧嘩腰になるけどね どうしても でも 最後のレビュア とか そうだよねりなたむ そういうときはエリア チェアにこいつ読んでねえっていうのは伝わるように するっていうのが大事はいあとはなんか僕これ難しいんだけどインギンブレイにはならない程度に丁寧に書かなきゃいけないいろいろ書き方見てまして

デビュアーは神様だったり、そういう記事とかもあって、そういう感じで書くべきか、みたいな。でも、そこら辺は環状労働はGPTがやってくれるんで。 最後チェックGPTにして 攻撃力じゃないですよねっていうのをチェックするのがいいですPromptかなんかで なんでここはまずGPTしか使ってないよっていうことを言っているのにここGPTしか使ってないっていうトピックと全然関係ないことがひたすら書いてあるように で、もう丸といらないとなるほどうーんそうなんだ

えっとそれなんでそれを書いてしまったかというとあーでもそうか これは何かそれでも工夫している みたいなこと言ってるんですよねそうです工夫とあと何か手法について 何かその手法のリプロダクティブ おだしょー Dのところで三宅 Dスピリッド 再現性ですねおだしょー その手法に再現性はあるのかって その手法とその再現性三宅 いや これは多分 GPT-4を使ったら 再現性なくなるんじゃないのって指摘なのおだしょー なるほど そこをちゃんと。なるほど。

なので これはGPT-4を使っても ビプロディシビリティとリタイアビリティはそんなにめっちゃ損なわれる わけじゃないですっていうのを 反証しなきゃいけなくて まずGPTの バージョンちゃんと指定してAPIでやってるから 再現できるはず っていうのを先に書かなきゃいけない気がする まずGPT使えばみんな一緒だし、他のモデルにも使える手法であるべきっていう、そういうことではなかったんです。そういうことでもあるけど、まずとにかく再現としてはそれで、同じモデル付け合いはまずみんなできるように。 を言って さらにそのモデルだけ 使ってるやつがそもそも他の研究でちゃんと採択されてるしだからリアイアビリティーでもう これを理由にしてリアイアビリティーがないっていうのはちょっと

フェアじゃないよねっていう、そこまで言わなくていいけど、この人は仲間なんで、どっちかっていう感じで進めていくのがいいです。

ちょっといろいろずれてますよねそうそうそう だから あとはファイルとペーパー

エラーランニシスなかったのは僕の投稿直前にないって気づいてごめんって言ってた部分ですよねいやすいません でも自分も そうですねこれは なので 反証できないです たぶん せめてものをアペンディクスに つけたんですよね確かつけましたなのでそこには最低限つけて あるよっていうのを言いつつ やっぱり言う通りコモンフェイラーモードが分かるのはすごい大事なので言えるんだったらちゃんとそれを つけた状態で出すアペンディック 推測をもっと強化するっていうそれがポモフェーラーモードが 分かるように強化して修正しますって約束ベースで書いて

書くのでいいような気がする 約束別で書くこと自体はレバッタリ的にはあまり意味がないんだけど誘導者の心象を良くするっていう意味で 何も書かないよりは文字書けるんだったらそれを書いておくべき3番目は 廣瀬 データセットジェネレーション のときに他のモデルとか使わなくていいのみたいな話だっけ廣瀬 と思いましたね 自分はそう 解釈してやってました でもこれも だからそれしてない 論文を3つあげればいいと思っていて今の書き方だと これらがデータセットを 生成する論文なのかどうかすらよく分かんない ちょっといい?

こうやってよくわかんないね 回答だってデータセット生成するときに いくつかのやつで おだしょー そうですねりなたむ データセットを作成する とかおだしょー よし

それが聞かれてるんでね

レイアウトジェネレーションメソッド スクリプトジェネレーションのところも複数の VLLM でやってみたらよかったんじゃないのって言ってるでしょ と思っていたので、なんかスクリプトをいろんなパターンのスクリプトでやってみたらっていうことなのかなって思っても、結局スクリプトの種類いろいろ いやとかって思ったんですけど違いますかねこれはだから複数のVLLMでスクリプト ジェネレーションしたらって言ってるんでしょ

これはでも一個でいいはずだよね

ここに書いてあることが まず そもそもこの英語が伝わんないんだけどブレイクスルーペーパーだから どうとかそうですよね あんまりそれ この3つが一体どういう関係でここに並んでいるのかは分かんないから、これは全然効果的じゃない。 構築する絵でGPTだけに頼っている論文で見つけたはずですねそれを書かなきゃいけないまずだからこの名前をあげるのは本文のこういうところでいいんで 大事なのは、なんでこれを上げているのかっていうのがちゃんと明記されていることが大事なのに、それが書いてないんで、書くべきことがずれてるんですよね。 先説とVLNが

エイリアン まだバルーン

本日はご覧いただきありがとうございます。

ええっと

ベストペーパーかどうかはさ、別になんか正直、あんまり主張しても、だってそれじゃ全部ベストペーパーになるわけじゃないから いやほんとにそう思います、あのーそうですね、それ、あのー、そうですね、いやすみません、自分がちゃんと確認してないんですけど、そのー、ま、生成、生成してもらっ… て言ったんですがそれが入ってたっていうそうですねあーなるほどすいませんちょっとあのもうちょっとうまくLMとお付き合いしながら 制作すればよかったです。こんな形になってたかっていう。時間があんまりないんで、とりあえず先にどんどんいきましょう。お願いします。

3つ上げるときに少なくとも1個はACM マルチメディアがいいですベケアは3つともだけど

レビューアーにはテクニカルリゾンベーションがないって言ってるやつは はい、テクニカルイノベーションがなんか、さどく要件、さどく基準としてテクニカルコントリビューションがない からダメメントは書いてないっていうのをまず押さなきゃいけないなるほど

レビューやガイドラインとかで 書いてないことを基準にされると困るので

基本的にレビュアーガイドラインに限らず、コミュニティへの貢献っていうのが一番大事だよねっていう立場で書くとACがうんって言う。 なるほど 確かにちょっと今そこを一番迷ってて正直まあ既存手法の色々組み合わせたっていうことでしかないかなと思ってて でもこの論文はデータセットペーパー なのでデータセントリックなコントリビューションが大事なんですよそこを押すことが重要だったんですよ なんか無理にいろいろ 工夫を書こうとしちゃってましたそうですね そういう意味ではなんか

今レギュラーミーティングだと見せられないけど 2人しかいないから見せてしまうと去年のACMマルチメディアの

うん

何だっけ

どこに貼ったんだろう

ドッ 今後のとこにあったんだっけなしかしたらえっとdm のところかもしれません

一番最初に自分が挙げさせていただいた稲葉先生 あとは岡田くん北川さんもいらっしゃったのでちょっと挙げちゃったんですけど ここのリプライの途中にあるよ。

どうもありがとうございました。

これかなありがとうございますでこの人はレバッタに対して なんかこんな感じで書いてるんだけど

なんか、これ僕は割と、オーサーじゃなくて、他の読者と同じタイトな立場で書いてるんで、このまま書くとちょっと なんか偉そうにしすぎてるオーサーって感じがしちゃうんで書き方はちょっとこのままではいけないんだけどポイントは

ええ。

あ、これか。

【コメント】雰囲気の効果がいけるかな

まさに同じことを書いてるねNo Algorithmic Contribution

だけど、これはアルゴリズムペーパーじゃなくてデータセットペーパーなので、アルゴリズムセントリックビューじゃなくて いえいえ

なんかまあ今時普通だよねみたいな 書き方が欲しい あとなんだこれファクトエラーをだから僕もこのレビュー放送のためのファクトファクチュアルエラーを言いまくってるんだけど

うーん まあここかな一番大事やん

あとこれか, weighing more on the contribution to the community

うん、なるほど。

ここら辺が大事かなという気がします

でもやっぱりこの論文を見ると 他の読者が明らかに分かってないよねっていうのを

素敵シーンだよな、いろいろ。

しっかりID載せてって言ってほうが いいですね

あとは再現率が低いのを問題にしてるけど F1スコアでは一番いいしむしろ最近のレンズボキャブラリーキャッシュ デンスビデオキャプショニングでは実は従来手法も再現率ばっかり高くて プレシジョンが低いことが問題になっているのです むしろ再現率じゃない方を高くして F1スコアを上げるのはトレンドに乗ってる

ですよね なんで まあ でも こういうことを主張する していくしかないですね さっきのやつなるほど

戻すと

ちょっと無理に、今の書き方とだいぶ違くて、無理に、なんか、あのー

新しいっぽいことをいっぱい書いてしまいましたね。いろいろしながら、これは他ではやってないだろうっていうこともあるんじゃないかな。それはズレてる。 ですよね やっぱりレビューアー とのコミュニケーションが取れないとレバットルが失敗しますねなるほど ありがとうございますこれやっぱりテクニカルに イノベーションがないっていうデータセットでコミュニティに 貢献する部分で そのテクニカルなアルゴリズム的な新しさっていうのはその再録条件ではないはずだってちゃんと書くっていうのは大事です

データセットコントリビューションで アルゴリズミックなコントリビューションなくて通っている論文を参考上げるというパターンですね そうするとだってテクニカルイグレーションがないから落とすってこの人それ以上主張できなくなりますよね確かにそういうふうにもうそれ以上この人が言ってることを何回 平行線たどらずこっちが完全にこうなんか反論できなくさせるのがいいレバッタリでただ単に俺はこう思ういや私はこう思うって言い合うのはもう全くレバッタリの意味がない いやまさにそうですよね、確かにもうあるないというか、こっちはある、本当になんかいい工夫をしてると思ってる、いやそれはいい工夫じゃないっていうこのやりとりは

不毛ですもんね、確かに。それは不毛だし、そもそもレバッタルとしてそれをやってはいけないって書いてないですか、どっかに。あ、ほんとですか。ちょっとあんまり書いてない。レバッタルの場っていうのは、なんか意見表明の場ではないよって。 完全に間違ってるななので、反論できないことに関しては ベストエフォートで心象を良くする以外のことしかできないし反論すべきところはもうファクトベースでバシッと反論してもうそれ以上同じことを繰り返したら黙れみたいな状態に できないといけない。なので、3つACMアルティメットのノブが上げてって言ってるのも、それ3本通ってるのにこのノブだけ落とすのはおかしいでしょってちゃんと言うっていう。

はい。

だから他の何か会議じゃない方がいいですはいわかりました ちょっと じゃあちゃんとSCMアルチメディアでサーフェイスしますSCMの1個はさっきあげたやつがあるんで あと2つ挙げてくださいはい ありがとうございますデータセットアプリケーションはこれは挙げれるって言えばいいし そもそも漫画 自体もなんか広いよっていうのを言った方がいいです 漫画単体でも十分広い、なんかその史上規模が大きいんですっていう話はなんか大事だと思うんですよね

あとはフューチャーワークのリミテーション1個だけ今2番のところでいいですかデータセットの 応用先っていうところと、スクリプトトゥーレイアウトっていう手法に対する応用先っていうことで、これはデータセッターに関する応用ってことだから、あまりスクリプトトゥーレイアウト というものの応用先を主張してもあんまりダメなのかなとか色々悩んでしまったんですがそこっていかがですかね今回のスクリプト自体が どう使えるかってそこにフォーカスした方がいいんですかね漫画市場がまずあのでかいってことを主張した上でなんですけどまずその

スクリプト自体単体で価値があるんだったらそれは主張したらいいしそれに加えてそこから漫画のレイアウトの対になっているデータもあるよっていうところで

言えるので 今の話は僕の目的には どっちかを選ぶんじゃなくて両方を書けるはずだった

主砲はだってデータセットがある から初めてできるようになってるんで当然何か含まれてるけど 主砲だけじゃないはず

3、2番のLimitation for Future Work

一応ここについてはあれを書きましたね現状はレイアウト単体 はい、漫画のページ1ページごとの生成になっているんだけれども、まあ、本来的に言えば、いや、これはね。 そういう細かい話をしてもしょうがないんですよね

ごめんね

スクリプト情報のインテグレーションをレイアウトジェネレーションに変更する方法はありますか?

質問の意味が

ここで聞きたい

スクリプトをインテグレートする って言ってるんだけど そもそもスクリプトしかないはずなんだよね レイアウトジェネレーションの入力として

これも応用の話に近いんじゃないかな だからその漫画だけなのっていうところ

ですよね だからスクリプトって こっちのほうがむしろその データセット単体じゃなくて スクリプトから漫画生成もあるしスクリプトから絵コンテとか 映画のほうの生成もあるし こうそういう広がりっていうのはあるはずだよねみたいなそれもなんかそのレイアウトですよねみたいな書き方の方がいいんじゃないかな

このリミテーションの部分の何か解釈ってどうしたらいいんですかカレントリミテーションオブユアアプローチってことで難しいですね これでもそんなに重要なのかな ちょっとこれってもう何か書いたりそのままなの?あ、そうです。これと匹敵させていただきました。他の部分でもヒントはない。 あ、そうですね、この人のやつにはそうですね、上の部分のヒントはなかったと

ありがとうございました

ご視聴ありがとうございました

これがコンスのネガティブなところですね。

とにかくテクニカルインニューベーション に気を取られている

他のポテンシャルユースについてを いろいろエクスプローアするともっとベニフィットがあるよって言ってる

ので3番はそれに対応してるんじゃない やっぱり

いやこれ結構読み取るの大変なんですよ大体まあ茶読書はレビューコメントそんななんかわかりやすく書いてくれないんで ありがとうございます。全然勘違いした。うん。

なんでこういう

ここの部分を変えた方がいいですね。 3番行くと、これはイエスで良くて

この長く書かなくていいですよここで切ったら

修理歴を残しながらやるのはどうするんだっけ、これか。

Is the data preparation pipeline effective for color images or other images? イエスだよね。

YES ってつけたらいいねはっきり最初にタッチを明らかにするとWE BELIEVE の言葉いらんかもしれん これかなり明らかだよねと思ってますねはいなのでその本当だったらカラー画像とその白黒画像だと白黒画像カラー画像の方が 画像理解が絶やすいっていう論文を探すべきかなと思ったんですけどちょっと探すべき?探すべきです。ファクトベースなんで ファクト要素から引っ張ってくる しかないので探すべきそれは探しつつということですかねそうですね

ビジュアルプロンクティングはからイメージ図からそうですね

うん

まあいいか、いらないか。長いんだな、でも。なんかとにかく長い、回答が。なんか2500文字全部使わんといかんかなっていう、そのなんか、強迫感。 使わない 使うにしても使い方が 革新にいくまでに距離を作ってるから良くないなるほど 端的に言って 必要な分で長くなる分にはいいけどってことですね あと長くなればなるほど読んでもらえないよ確かにレビュー屋さんはいっぱい読むわけですもんね もうエリアチェアもね エリアチェア 20分ぐらい見てるのよやば なるほど それは嫌になりますね嫌になるの確かに嫌になってるの

しかも同期2つとかやってるときあるからね最悪

なんで、そういう人の気持ちになると短い方がいいです。わかりました。ちゃんと視聴をきちんともっとわかりやすくさせていただきます。はい。

で、えーっと、これはなんだ?ここなんですけど、ここがちょっとハテナってなっていたところだったと思うんですけど 元の部分、それこそ上のところのヒントから考えるとこの人が良かった点として 画像からスクリプトを作ったり、スクリプトからレイアウトを作ったり、行ったり来たりしてるアイディアが面白いねみたいな、そういうことが書いてあったんです。 それを読み解くに、こう行ったり来たりの関係性で、なんか分布が近かったら その言語から元に戻すときに、その分布の影響をうまく使って、 言語情報の中にもレイア…なんて言うんでしょうねその分布におけるそのレイアウト情報みたいなのも含んじゃってるから有利になっちゃってんじゃないのっていう主張をしてるん…

じゃなかろうかって推測したんですよねだってちょっと複雑なんですけど今これあ、そうですそうですで

どこに書いたらそれ一回きてるの一番目がとまずプロスそうです一番目で

ヴァイスバーサーって言うんだよな男ってヴァイスバーサーではないよねっていうことを言っているんで、そういう解釈をされているのかなっていう イメージがあって、なのでそのスクリプトを生成したVLMとレイアウトを生成するLLMに分布的な近寄りがあれば 有利になっちゃうんじゃないのっていう 指摘なのかなって思ったんですよあーなるほど って解釈したんですよね

おだしょー パフォーマンスギャップ っていうのはベースラインメソッドだったしばやん そうですねおだしょー VLMって何使ったんだ っけしばやん いや スクリプトを生成 するためだけに使ってますね VLLでもその時ってGPTそうですGPTを使ってます有利になったのも強かったのもGPTなんですねGPTは結局ACMマルチメディアで では載せていないですね、GPTの実験結果は。GPTのやつは、昨日、新にエクスクラシブルにできなかった。 しなかったので、一回オジャンになって使っているLMはスワロー、サラシナとか、VLMとは同じモデルは使ってないです。

なるほど

これはまずなんか、なるほど面白いですねっていう。

ことを言った上で

これもでも全ての何かに言える よねこういうの調べた論文ないですか ね そこまで調べていなかったです。

このいってこいで、いってこいの時に近しいモデルを使っちゃうとダメとか、離れすぎてるとダメとかって

ちょまど そういうりなたむ これ じゃあ 何かその スラッシュなどか使ったやつのベースになってる プレッド まあ でも それも全部GPTじゃないよな オープンスマイク

これパッと回答方針が思いつかないですね

その表現形式が結構異なるよっていうところで 自分はちょっと主張しちゃったんですけど もうちょっとファクトをちゃんと 意見表明じゃないっていうところで言うとやっぱりファクトを集めないとダメっていうところですよねそうですね

それかもう論理的に完全に正しいっていうことを論理的に完全に正しく言えるかどっちかですね難しくて無理ですね

何が痛いかわからないな

まあ、どっちか、まあそうだね、せいせい

これ VLAMじゃなくていいと思うん ですけどね LLAMでもいいので

では、はい。

それが、というか、何だっけなまあ、それが理科

バイアスあるよって論文しか見つからなそうだな

あるいは

おだしょー いや どうなんだろうね もう これって

VLMってこれ日本語対応のやつ 使ったんだっけVLMはGPT-4なのでそうですね 日本語に対応してます

LLMとかでデータセットを作って

ベースラインが

作成に用いたベースラインよりいい 回答結果を出すってことは普通にあるよね

普通にやるよね。

🐕🐕🐕

これ 悪魔の証明みたいになってる 気がするな 関連は出るよね だってGPT

3とかで作ったデータ設定に対して 4.0のほうがいいとか 普通にあるよね

なんで こういうときはですね ちょっと苦肉の策ではあるんですけど面白い してきえすねといついつええええっとえーばい そういうバイアスの影響がゼロである。

みなさん、ご視聴ありがとうございました。 GPTOが含まれていない

うん

このようなバイアス

ご視聴ありがとうございました

データセッションを生成するモデルと、SMLデータセッションを生成します。 おつかれさまです。それでは、また会いましょう。

このアンティンテイを調べるわへん。

危機という知識があるのであれば、みなさんも教えてください。 要するに監査学者は結構無責任なんですよね

こういうことがあるんじゃないの?って言ってるけどあるかもしれないけどそれあるんだったら論文で教えてくれないと困るよっていう ことを書いてあげると、見つけられたらごめんだけど、相手が見つけられなかったら、なんか結構イタモンだなって こういう書き方をしたほうがいい ですね

たしかになんか悪魔の証明って言うと、なんか往々にしてそういう状況になる気がしますよね。相手が。 相手が提出すべきものを提出せずに次行くおうあーなるほど

で 最後ですが この人が一番読んでないんですねそうですね ただ一方でポスター ラマーを改めてちゃんと読むので 問題設定とかは大きく違うんですが、言わんとしていることはちょっとだけ論点が分かったっていうのと、自分がそこが聞き入れてなかった不備あったなっていうのはちょっと思うんですよね。 次のICCVとかにそこ改善できればと思うんですけど多分この人が言ってるのはそのコンテンツアウェアなレイアウト生成っていう研究 あるよねっていうことを言っていてそれと何が違うのってところでもそこが十分にその研究も他にあるんだからそこもちゃんと調べて比較してよっていうのが

多分この人に言ってることだと思うんですよ。で、コンテンツアウェアとコンテンツアウェアじゃないやつの生成は、えっと、コンテンツアウェアじゃない方はレイアウトDMとかのようにその要素をこう 数値化して、ID化して生成するっていうところで、コンテンツアウェアのやつとしては、その中身、テキストの文面とかをちゃんと 利用して生成しているという研究があったんですね。それがポスターラーマとかが実際そうだったので、そこともちゃんと比べなきゃいけないでしょっていうのを 言われているんですよ 一方でその一番のポイントはその例えばその今回の漫画生成で言うとセリフの中身のセリフの えっと

まあそのセリフの中身ですね 中身自体をそのまま直接利用してるってこと以上にその前のスクリプトの内容をちゃんと直接利用してるってことが 本研究の一番の目的であり 手法のちょっと分かんなかった もう一回言ってレイアウト生成の分野において コンテンツアウェアな生成とコンテンツアウェアじゃない生成の対立じゃないですけど、そこの部分の最後のあたりに2つの違いがよくない すいません、2つの違いは、最後のはセリフを直接使うっていうこと以上に、つまり並べる要素としてセリフがあって、このセリフ どこですかっていう問いを立てることが今回できるようになったっていうことを言ってるんじゃなくて今回の論文では

そのセリフがどういう文脈・物語情景の中で使われているかという情報も使えるようにしていることが、本研究の 一番の主張ですよってことが伝われば一応反論になるのかなって思って この現状の草案を書いているっていうところですちょっとわかんないですセリフを直接使うって言ってるのはセリフがコンテンツだって言ってる?そうですセリフの中身です要はセリフっていうセリフ1がどこかじゃなくて 例えばまた会いましょうってセリフがあったらまた会いましょうって文面を直接使うことでレイアウト生成に影響があるでも物語情景って言ってるのもコンテンツじゃない?コンテンツはその 例えば

誰々が誰々ん 誰々が誰々に向かって真剣な面持ちで喋るとかその真剣な面持ちでみたいな形容詞とか あとはどう振り向いて言うとか、その振り向いてとかっていう、そういった文面は既存のコンテンツアウェアな生成には使えない。 使われてない っていうところが ポイントかなと思っているっていうことですこれもコンテンツですよね

われわれの手法もコンテンツ アウェアの一部ではあります

中で従来はセリフしか使ってなかった って何に対応してるのか全然わかんないそうですね 従来はフォスターラマ とか ポスターラマは何をしてる?ポスターラマは、ポスターラマの前提は、ポスターの背景があって、その上に例えば50%オフとか あとはタイトル その商品名とかっていうのを配置するっていうそういうタスクをしてるんですけどその商品名とかを タイトルとかっていう風に抽象化せずに、商品編名のままとか、50%オフとかっていう、そういう言葉のまま使っているっていうのがポスターラマーだったんですよね。 そうなんだけど、それってでもなんか、最初の

なんか一章で書いた内容でそういうのとは違うよねっていうのを言えない?演出なんですよねそうです演出が違うっていうのが 必要だと思った

うーん

それをここに書いてやるの?と思ってますね最初に書いてやる?最初に書いてやるのがそれのつもりで書いてます脚本 まずその言われているのが脚本って別に既存手法でも 脚本から既存手法で使うための要素を取り出すことは簡単だよね だったら既存手法と何が違うのって言われているのであなたのおっしゃる通り脚本からそのレア度要素を取り出すことは簡単だと思います だけどそのプロセスが 課題なんじゃないかというふうに主張しています つまりそのプロセスにおいて脚本に書かれたレイアウト要素以外のそれこそ 演出表現だったりが どっさり抜けちゃいますよね 我々はその演出表現とかがレイアウトに及ぼす影響をあの えっときちんと影響強く感じており

それを使えるようにしたのが本論文ですっていうような主張をしたつもりです

なんかこうセリフだけ入れて 生成させてっていうのはしたんだっけそれまさにノースクリプトがその あの正直その研究その生成になっているはずなんです セリフの中身だけを使ってあとはキャラクターの名前だけを使って 実際スクリプトを使った方が 良い結果になっているってことを論文の中で主張しているはずですそれはここに書いてある たしかに描いてないですねその、そうです描いてないですそれ描かなきゃいけないたしかに今むちゃくちゃ思いませんたしかにそれですね

三宅 これでいいじゃんおだしょー これですね 確かに

これでいいじゃんいやそれでしたそれでしたねあとポスターラマとかで言うとラマを同じくそれこそ ローラでほぼ同じような手法なんですけどローラで学習させてってっていう中であの中へ フォーマット html ベースにして 入出力を考えているとかそういうことがあったりするんですけどその既存、そうですねポスターラマとかと比較せよって言われている中においてそのそういうフォーマットとかがそろっ フォーマットとかは準拠してないなって思ったんですけどつまりそのノースクリプトとスクリプトの比較で ノースクリプトだと全然で、 スクリプトあったらいい感じになっているっていう主張において、フォーマットの影響をどう考えるかっていうのをちょっと悩んだ。

ですがこれって聞かれてんのこれ聞かれてはないです ただポスター ラバー聞かれてないなら答えなくていいん じゃないかなちょっとすみませんあと5分しかないんですみませんまず何を言おうとしたかという とまずこれはそうなんだけど 以上で終わりたいと思います。

本日はご視聴ありがとうございました。 もっとコンピューターウェアが違いを述べているのを メインの質問メインの一つかなちょっと待ってもう一回質問

このディファレンスですよねディファレンスちゃんとこう

ディファレンスノビティブをちゃんと明記する その上でポスターを日章に入れるよと

エレメントフォーマンスのスクリプト

難しくない難しくないからやってるんだよねそれを言っそうですねあのそうです それがさっき言った脚本情報からレイアウト要素を抜き出して、その抜き出したものだけで生成することは簡単だよねって言って 言われちゃってるんですけど抜き出すことが問題なんじゃないのっていうことを言いたい抜き出すって何?脚本があった時に脚本からそのレイアウトを作りたいってなった時に このレビアは既存の手法はその中身だけ、要素だけ、演出を除いて要素だけを使えるモデルでも 要素を抜き出すことは簡単で、その要素を使った生成手法はもうすでにあるんだから、別にいいでしょっていうその…

脚本があって、脚本からそのセリフ情報とかキャラクター情報だけを取り出すことが簡単で、それを入力としたモデルはもうポスターラマとかであるんだから えっとそれでいいじゃない 何をしたのあなたは何をしたのって言っているんだと思うんですよで 自分の主張はや その要素を取り出して使っていますけどその脚本の中にはその演出情報っていうのが含まれててその影響が強く出るはずなんだからあ、違う違う、たぶんね、それはね、まずこう この研究はアルゴリズムの研究ではないなるほどで、アルゴリズムが同じでも データに単なるセリフとか配置するテキスト以上の情報が

含まれているというのと、その処刑情報とかもろもろ によるレイアウトの変化を調べられるようにしたのが て言わないと、相手の土俵に乗っちゃうと負けパターンが出せる分かりましたそうでしょ、だって我々アルゴリズムの新しさで戦ってないんでそこでアルゴリズム 一緒でしょって言われても いや アルゴリズム一緒じゃないんかって悪いんじゃって言わなきゃいけないそうか ありがとうございます 確かに なるほど ありがとうございます はい。その上で、だからセリフのみと、そのセリフ以上のデータが入る勉強を調べた。 この字で売りのこの部分が公権だよというわけです。

NOT SOLO

これは具体的なの上げてくれって 言わなきゃ駄目ですね

評価をってことですかうん 具体的な評価指標を上げてくれれば次 追加しますよって書いたら終わりですねなるほど自分も一応調べてOcclusionとかReadabilityのことかなって思ったんですけどそれは背景画像があってその上にレイアウトを載せるっていうそういう手法の時によく使われる手法なんで 背景をそもそも前提としてない本研究では ちょっとそぐわないっていう主張したんですけどそこまでそれでなんか自分で問題点を挙げて 自分で解決してるからなんか答えひとりごとになってますよね確かに その相手がそれを送る順とかリーダビリティを

知っているとは限らないですもんね、確かに。ありがとうございます。じゃあ、ちょっとやめます。その相手が背景画像を前提としている手法にはそうじゃないよって、その… 勘違いみたいなものが何か指摘じゃないですけど何か言うことってしなくてもいいんでしょうかそれを書くんだら上の方でポスターラムを上げていいのって上の方だっけ えっと下であげてます下であげてる じゃあ下であげてるんだったらポスターラーマーは 背景で画像が多く入力されているので、問題設定が違っています。 同じメトリックは使えないよって 書いてあるじゃないですかありがとうございます

こういう方針で書かなきゃいけない ですので それはそれとして結局これをレバッタリするのかどうか とか レバッタリした場合ってこれ結果出るのだいぶ先ですよねそうですね なので ICCVを優先すると 結局取り下げることになると思いますそこはなんか ここ2人で話してもしょうがないんで次のミーティングの時に話しますかはい お願いします これ間に合うんだっけ 金曜日で金曜日に提出できればと思ってます 締め切りは20日の あそうかじゃないかっていいのか大丈夫かないつかTD20日の真ん中ぐらいですか19日はAOEなので

じゃあ じゃあ 発端に相談しましょうはい よろしくお願いしますじゃあ 発端にしましょうはい すいません お時間取っていただいて 本当にありがとうございますはい 失礼します失礼します
		

### 意見表明ではない

Reviewer 1

- GPT-4o だけを使っていることを理由に、リジェクトされえない
    - なぜなら、ACMMM でも通っている。
- 補足資料につけていることの主張
- データセットの制作を

Reviewer 2

- Technical Contribution を基準にするなということを主張する
- データセットのコントリビューションがこの論文にはあるということをきちんと伝えないといけない

Reviewer 3

1. 面白い指摘だと思います
    1. bias を改善する必要あり、

Reviewer 4