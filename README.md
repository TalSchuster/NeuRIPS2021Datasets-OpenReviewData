# Crawl and Visualize NeurIPS 2021 Datasets and Benchmarks Track OpenReview Data

based on [evanzd/ICLR2021-OpenReviewData](https://github.com/evanzd/ICLR2021-OpenReviewData)

## Descriptions

This Jupyter Notebook contains the data crawled from NeurIPS 2021 Datasets and Benchmarks Track OpenReview webpages and their visualizations. The list of submissions (sorted by the average ratings) can be found here.


## Prerequisites
* python 3.7
* selenium
* pandas
* seaborn
* imageio
* wordcloud
* tqdm
* [`edgewebdriver`](https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/)
  * NOTE: You can also use `chromedriver` by setting `driver = webdriver.Chrome('chromedriver.exe')`.


## Crawl Data
1. Run `crawl_paperlist.py` to crawl the list of papers (~0.5h).
2. Run `crawl_reviews.py` to crawl the reviews (~1.5h).
   * NOTE: currently only review ratings are crawled.


## Visualization

**Keywords Frequency**

The top 50 common keywords (uncased) and their frequency:

<p align="center">
    <img src="asset/keywords.png" width="720"/>
</p>

**Keywords Cloud**

The word clouds formed by keywords of submissions show the hot topics including *deep learning*, *reinforcement learning*, *representation learning*, *graph neural network*, etc.

<p align="center">
    <img src="asset/wordcloud.png" width="720"/>
</p>

**Ratings Distribution**

The distribution of reviewer ratings centers around 5 (mean: 5.367).

<p align="center">
    <img src="asset/ratings_dist.png" width="720"/>
</p>

**Keywords vs Ratings**

The average reviewer ratings and the frequency of keywords indicate that to maximize your chance to get higher ratings would be using the keywords such as *deep generative models*, or *normalizing flows*.

<p align="center">
    <img src="asset/keyword_ratings.png" width="720"/>
</p>

**All NeurIPS 2021 Datasets and Benchmarks Track Submissions**

(Collected at 07/08/2020).

|   Rank |   AvgRating |   STDRating | Title                                                                                                                                                                          | Ratings       | Decision   |
|-------:|------------:|------------:|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------|:-----------|
|      1 |        8.5  |        1    | [RadGraph: Extracting Clinical Entities and Relations from Radiology Reports](https://openreview.net/forum?id=pMWtc5NKd7V)                                                     | 9, 9, 9, 7    | Unknown    |
|      2 |        8.33 |        1.15 | [ATOM3D: Tasks on Molecules in Three Dimensions](https://openreview.net/forum?id=FkDZLpK1Ml2)                                                                                  | 9, 9, 7       | Unknown    |
|      3 |        8.33 |        1.53 | [Pervasive Label Errors in Test Sets Destabilize Machine Learning Benchmarks](https://openreview.net/forum?id=XccDXrDNLek)                                                     | 7, 10, 8      | Unknown    |
|      4 |        8    |        0    | [Programming Puzzles](https://openreview.net/forum?id=fe_hCc4RBrg)                                                                                                             | 8, 8, 8       | Unknown    |
|      5 |        8    |        1    | [A Large-Scale Database for Graph Representation Learning](https://openreview.net/forum?id=1xDTDk3XPW)                                                                         | 7, 8, 9       | Unknown    |
|      6 |        8    |        1    | [CCNLab: A Benchmarking Framework for Computational Cognitive Neuroscience](https://openreview.net/forum?id=1vC5GFOXuhM)                                                       | 8, 9, 7       | Unknown    |
|      7 |        8    |        1.73 | [CommonsenseQA 2.0: Exposing the Limits of AI through Gamification](https://openreview.net/forum?id=qF7FlUT5dxa)                                                               | 7, 7, 10      | Unknown    |
|      8 |        7.67 |        0.58 | [Q-Pain: A Question Answering Dataset to Measure Social Bias in Pain Management](https://openreview.net/forum?id=Ud1K-l71AI2)                                                  | 8, 7, 8       | Unknown    |
|      9 |        7.67 |        0.58 | [Which priors matter? Benchmarking models for learning latent dynamics](https://openreview.net/forum?id=qBl8hnwR0px)                                                           | 8, 8, 7       | Unknown    |
|     10 |        7.67 |        0.58 | [NaturalProofs: Mathematical Theorem Proving in Natural Language](https://openreview.net/forum?id=Jvxa8adr3iY)                                                                 | 8, 7, 8       | Unknown    |
|     11 |        7.67 |        1.53 | [It's COMPASlicated: The Messy Relationship between RAI Datasets and Algorithmic Fairness Benchmarks](https://openreview.net/forum?id=qeM58whnpXM)                             | 8, 9, 6       | Unknown    |
|     12 |        7.67 |        2.08 | [EEGEyeNet: a Simultaneous Electroencephalography and Eye-tracking Dataset and Benchmark for Eye Movement Prediction](https://openreview.net/forum?id=Nc2uduhU9qa)             | 6, 10, 7      | Unknown    |
|     13 |        7.33 |        0.58 | [LiRo: Benchmark and leaderboard for Romanian language tasks](https://openreview.net/forum?id=JH61CD7afTv)                                                                     | 7, 7, 8       | Unknown    |
|     14 |        7.33 |        0.58 | [TenSet: A Large-scale Program Performance Dataset for Learned Tensor Compilers](https://openreview.net/forum?id=aIfp8kLuvc9)                                                  | 7, 7, 8       | Unknown    |
|     15 |        7.33 |        0.58 | [A Unified Few-Shot Classification Benchmark to Compare Transfer and Meta Learning Approaches](https://openreview.net/forum?id=Q0hm0_G1mpH)                                    | 8, 7, 7       | Unknown    |
|     16 |        7.33 |        1.15 | [Variance-Aware Machine Translation Test Sets](https://openreview.net/forum?id=hhKA5k0oVy5)                                                                                    | 6, 8, 8       | Unknown    |
|     17 |        7.33 |        1.53 | [Teach Me to Explain: A Review of Datasets for Explainable Natural Language Processing](https://openreview.net/forum?id=ogNcxJn32BZ)                                           | 6, 7, 9       | Unknown    |
|     18 |        7.33 |        1.53 | [Automatic Construction of Evaluation Suites for Natural Language Generation Datasets](https://openreview.net/forum?id=CSi1eu_2q96)                                            | 7, 6, 9       | Unknown    |
|     19 |        7    |        0    | [EventNarrative: A large-scale Event-centric Dataset for Knowledge Graph-to-Text Generation](https://openreview.net/forum?id=3ZQqjt_Q6b)                                       | 7, 7, 7       | Unknown    |
|     20 |        7    |        0    | [A Spoken Language Dataset of Descriptions for Speech-Based Grounded Language Learning](https://openreview.net/forum?id=Yx9jT3fkBaD)                                           | 7, 7, 7       | Unknown    |
|     21 |        7    |        1    | [FEVEROUS: Fact Extraction and VERification Over Unstructured and Structured information](https://openreview.net/forum?id=h-flVCIlstW)                                         | 6, 8, 7       | Unknown    |
|     22 |        7    |        1    | [CSAW-M: An Ordinal Classification Dataset for Benchmarking Mammographic Masking of Cancer](https://openreview.net/forum?id=nlJ1rV6G_Iq)                                       | 7, 6, 8       | Unknown    |
|     23 |        7    |        1    | [B-Pref: Benchmarking Preference-Based Reinforcement Learning](https://openreview.net/forum?id=ps95-mkHF_)                                                                     | 6, 7, 8       | Unknown    |
|     24 |        7    |        1    | [The Multi-Agent Behavior Dataset: Mouse Dyadic Social Interactions](https://openreview.net/forum?id=NevK78-K4bZ)                                                              | 6, 7, 8       | Unknown    |
|     25 |        7    |        1    | [CARLA: A Python Library to Benchmark Algorithmic Recourse and Counterfactual Explanation Algorithms](https://openreview.net/forum?id=vDilkBNNbx6)                             | 6, 8, 7       | Unknown    |
|     26 |        7    |        1    | [A Procedural World Generation Framework for Systematic Evaluation of Continual Learning](https://openreview.net/forum?id=LlCQWh8-pwK)                                         | 6, 8, 7       | Unknown    |
|     27 |        7    |        1.73 | [ThreeDWorld: A Platform for Interactive Multi-Modal Physical Simulation](https://openreview.net/forum?id=db1InWAwW2T)                                                         | 6, 9, 6       | Unknown    |
|     28 |        7    |        1.73 | [Personalized Benchmarking with the Ludwig Benchmarking Toolkit](https://openreview.net/forum?id=hwjnu6qW7E4)                                                                  | 8, 5, 8       | Unknown    |
|     29 |        7    |        2.65 | [PASS: An ImageNet replacement for self-supervised pretraining without humans](https://openreview.net/forum?id=BwzYI-KaHdr)                                                    | 5, 6, 10      | Unknown    |
|     30 |        7    |        2.65 | [Therapeutics Data Commons: Machine Learning Datasets and Tasks for Drug Discovery and Development](https://openreview.net/forum?id=8nvgnORnoWr)                               | 9, 8, 4       | Unknown    |
|     31 |        6.75 |        0.96 | [CUAD: An Expert-Annotated NLP Dataset for Legal Contract Review](https://openreview.net/forum?id=7l1Ygs3Bamw)                                                                 | 8, 7, 6, 6    | Unknown    |
|     32 |        6.75 |        1.5  | [ReaSCAN: Compositional Reasoning in Language Grounding](https://openreview.net/forum?id=Rtquf4Jk0jN)                                                                          | 8, 8, 5, 6    | Unknown    |
|     33 |        6.67 |        0.58 | [The PAIR-R24M Dataset for Multi-animal 3D Pose Estimation](https://openreview.net/forum?id=-wVVl_UPr8)                                                                        | 7, 7, 6       | Unknown    |
|     34 |        6.67 |        0.58 | [Generating Datasets of 3D Garments with Sewing Patterns](https://openreview.net/forum?id=Pq8FBz0gZHY)                                                                         | 7, 6, 7       | Unknown    |
|     35 |        6.67 |        1.15 | [HiRID-ICU-Benchmark --- A Comprehensive Machine Learning Benchmark on High-resolution ICU Data.](https://openreview.net/forum?id=SnC9rUeqiqd)                                 | 6, 8, 6       | Unknown    |
|     36 |        6.67 |        1.15 | [Contemporary Symbolic Regression Methods and their Relative Performance](https://openreview.net/forum?id=xVQMrDLyGst)                                                         | 6, 6, 8       | Unknown    |
|     37 |        6.67 |        1.53 | [The People’s Speech: A Large-Scale Diverse English Speech Recognition Dataset for Commercial Usage](https://openreview.net/forum?id=R8CwidgJ0yT)                              | 8, 5, 7       | Unknown    |
|     38 |        6.4  |        1.14 | [Benchmarking Multi-Agent Deep Reinforcement Learning Algorithms in Cooperative Tasks](https://openreview.net/forum?id=cIrPX-Sn5n)                                             | 7, 8, 6, 6, 5 | Unknown    |
|     39 |        6.33 |        0.58 | [Multimodal AutoML on Tables with Text Fields](https://openreview.net/forum?id=9_eyi9ymJcZ)                                                                                    | 6, 7, 6       | Unknown    |
|     40 |        6.33 |        0.58 | [MultiBench: Multiscale Benchmarks for Multimodal Representation Learning](https://openreview.net/forum?id=izzQAL8BciY)                                                        | 7, 6, 6       | Unknown    |
|     41 |        6.33 |        0.58 | [Benchmarking Bias Mitigation Algorithms in Representation Learning through Fairness Metrics](https://openreview.net/forum?id=OTnqQUEwPKu)                                     | 6, 6, 7       | Unknown    |
|     42 |        6.33 |        0.58 | [FedScale: Benchmarking Model and System Performance of Federated Learning](https://openreview.net/forum?id=LZ5cx2yismf)                                                       | 6, 6, 7       | Unknown    |
|     43 |        6.33 |        0.58 | [OmniPrint: A Configurable Printed Character Synthesizer](https://openreview.net/forum?id=R07XwJPmgpl)                                                                         | 7, 6, 6       | Unknown    |
|     44 |        6.33 |        0.58 | [The Neural MMO Platform for Massively Multiagent Research](https://openreview.net/forum?id=J0d-I8yFtP)                                                                        | 6, 7, 6       | Unknown    |
|     45 |        6.33 |        0.58 | [Modeling Worlds in Text](https://openreview.net/forum?id=7FHnnENUG0)                                                                                                          | 6, 7, 6       | Unknown    |
|     46 |        6.33 |        1.15 | [An Extensible Benchmark Suite for Learning to Simulate Physical Systems](https://openreview.net/forum?id=pY9MHwmrymR)                                                         | 7, 7, 5       | Unknown    |
|     47 |        6.33 |        1.53 | [Open Bandit Dataset and Pipeline: Towards Realistic and Reproducible Off-Policy Evaluation](https://openreview.net/forum?id=GfWRFRuO51B)                                      | 6, 5, 8       | Unknown    |
|     48 |        6.33 |        1.53 | [VALUE: A Multi-Task Benchmark for Video-and-Language Understanding Evaluation](https://openreview.net/forum?id=9E3dTIMxL8S)                                                   | 8, 5, 6       | Unknown    |
|     49 |        6.33 |        1.53 | [Protein-Ligand Docking Surrogate Models: A SARS-CoV-2 Benchmark for Deep Learning Accelerated Virtual Screening](https://openreview.net/forum?id=ip0FhVivoX0)                 | 6, 8, 5       | Unknown    |
|     50 |        6.33 |        2.08 | [RedCaps: Web-curated image-text data created by the people, for the people](https://openreview.net/forum?id=VjJxBi1p9zh)                                                      | 8, 7, 4       | Unknown    |
|     51 |        6.33 |        2.52 | [Physion: Evaluating Physical Prediction from Vision in Humans and Machines](https://openreview.net/forum?id=CXyZrKPz4CU)                                                      | 9, 4, 6       | Unknown    |
|     52 |        6.25 |        1.26 | [AIT-QA: Question Answering Dataset over Complex Tables in the Airline Industry](https://openreview.net/forum?id=cB3OdLInAr9)                                                  | 6, 5, 6, 8    | Unknown    |
|     53 |        6.25 |        1.71 | [Reinforcement Learning Benchmarks for Traffic Signal Control](https://openreview.net/forum?id=LqRSh6V0vR)                                                                     | 4, 6, 7, 8    | Unknown    |
|     54 |        6    |        0    | [Pl@ntNet-300K: a new plant image dataset for the evaluation of set-valued classifiers](https://openreview.net/forum?id=aH0NedstEei)                                           | 6, 6, 6       | Unknown    |
|     55 |        6    |        0    | [Benchmark for Compositional Text-to-Image Synthesis](https://openreview.net/forum?id=bKBhQhPeKaF)                                                                             | 6, 6, 6       | Unknown    |
|     56 |        6    |        0    | [A Benchmark of Medical Out of Distribution Detection](https://openreview.net/forum?id=oUg5rC_95OM)                                                                            | 6, 6, 6       | Unknown    |
|     57 |        6    |        0.82 | [DABS: a Domain-Agnostic Benchmark for Self-Supervised Learning](https://openreview.net/forum?id=Uk2mymgn_LZ)                                                                  | 6, 7, 6, 5    | Unknown    |
|     58 |        6    |        1    | [MiniHack the Planet: A Sandbox for Open-Ended Reinforcement Learning Research](https://openreview.net/forum?id=skFwlyefkWJ)                                                   | 6, 5, 7       | Unknown    |
|     59 |        6    |        1    | [One Million Scenes for Autonomous Driving: ONCE Dataset](https://openreview.net/forum?id=KBbxt3JGn0Y)                                                                         | 6, 5, 7       | Unknown    |
|     60 |        6    |        1    | [Towards a robust experimental framework and benchmark for lifelong language learning](https://openreview.net/forum?id=yJyIjWyPJgs)                                            | 7, 6, 5       | Unknown    |
|     61 |        6    |        1    | [The Caltech Off-Policy Policy Evaluation Benchmarking Suite](https://openreview.net/forum?id=IsK8iKbL-I)                                                                      | 7, 5, 6       | Unknown    |
|     62 |        6    |        1    | [Revisiting Time Series Outlier Detection: Definitions and Benchmarks](https://openreview.net/forum?id=r8IvOsnHchr)                                                            | 5, 6, 7       | Unknown    |
|     63 |        6    |        1    | [Systematic Evaluation of Causal Discovery in Visual Model Based Reinforcement Learning](https://openreview.net/forum?id=xfeO8f9gLT0)                                          | 7, 5, 6       | Unknown    |
|     64 |        6    |        1    | [MLPerf Tiny Benchmark](https://openreview.net/forum?id=8RxxwAut1BI)                                                                                                           | 7, 6, 5       | Unknown    |
|     65 |        6    |        1.73 | [Measuring the State of Document Understanding](https://openreview.net/forum?id=tNMPcy9PovC)                                                                                   | 5, 5, 8       | Unknown    |
|     66 |        6    |        1.73 | [Vox Populi, Vox DIY: Benchmark Dataset for Crowdsourced Audio Transcription](https://openreview.net/forum?id=3_hgF1NAXU7)                                                     | 4, 7, 7       | Unknown    |
|     67 |        6    |        1.73 | [The Medkit-Learn(ing) Environment: Medical Decision Modelling through Simulation](https://openreview.net/forum?id=xiFJn0fbFX9)                                                | 7, 7, 4       | Unknown    |
|     68 |        6    |        1.73 | [CRAFT: A Benchmark for Causal Reasoning About Forces and inTeractions](https://openreview.net/forum?id=GVe2IvtZtVY)                                                           | 5, 8, 5       | Unknown    |
|     69 |        6    |        1.73 | [LoveDA: A Remote Sensing Land-Cover Dataset for Domain Adaptation Semantic Segmentation](https://openreview.net/forum?id=_-O9SefMb99)                                         | 7, 4, 7       | Unknown    |
|     70 |        6    |        1.73 | [CodeXGLUE: A Machine Learning Benchmark Dataset for Code Understanding and Generation](https://openreview.net/forum?id=6lE4dQXaUcb)                                           | 4, 7, 7       | Unknown    |
|     71 |        6    |        2    | [QAConv: Question Answering on Informative Conversations](https://openreview.net/forum?id=QkOBP-aD1qA)                                                                         | 8, 6, 4       | Unknown    |
|     72 |        6    |        2    | [MDP Playground: A Design and Debug Testbed for Reinforcement Learning](https://openreview.net/forum?id=VtqyY2dvE6h)                                                           | 4, 6, 8       | Unknown    |
|     73 |        6    |        2    | [RobustBench: a standardized adversarial robustness benchmark](https://openreview.net/forum?id=X-sH548WreZ)                                                                    | 6, 8, 4       | Unknown    |
|     74 |        6    |        2.16 | [HumBugDB: a large-scale acoustic mosquito dataset](https://openreview.net/forum?id=FNUijta5T-1)                                                                               | 4, 6, 5, 9    | Unknown    |
|     75 |        6    |        2.16 | [The Single Hyperparameter Benchmark for Reinforcement Learning](https://openreview.net/forum?id=R_CuaMJKvDs)                                                                  | 6, 7, 3, 8    | Unknown    |
|     76 |        5.75 |        0.5  | [TWEET-FD: A Dataset for Multiple Foodborne Illness Incident Detection Tasks](https://openreview.net/forum?id=saUHJ1iZhiO)                                                     | 6, 6, 5, 6    | Unknown    |
|     77 |        5.75 |        0.96 | [The Benchmark Lottery](https://openreview.net/forum?id=5Str2l1vmr-)                                                                                                           | 6, 7, 5, 5    | Unknown    |
|     78 |        5.75 |        0.96 | [Challenging America: Digitized Newspapers as a Source of Machine Learning Challenges](https://openreview.net/forum?id=gx7TEqAogg8)                                            | 7, 5, 5, 6    | Unknown    |
|     79 |        5.75 |        1.26 | [Timers and Such: A Practical Benchmark for Spoken Language Understanding with Numbers](https://openreview.net/forum?id=HrhaC-bLC5U)                                           | 6, 7, 6, 4    | Unknown    |
|     80 |        5.67 |        0.58 | [An Empirical Study of Graph Contrastive Learning](https://openreview.net/forum?id=fYxEnpY-__G)                                                                                | 6, 6, 5       | Unknown    |
|     81 |        5.67 |        0.58 | [CBLUE: A Chinese Biomedical Language Understanding Evaluation Benchmark](https://openreview.net/forum?id=4Y3vzl_NEyG)                                                         | 6, 6, 5       | Unknown    |
|     82 |        5.67 |        0.58 | [FHIST: A Benchmark for Few-shot Classification of Histological Images](https://openreview.net/forum?id=aAMgwCmP930)                                                           | 6, 6, 5       | Unknown    |
|     83 |        5.67 |        0.58 | [HPO-B: a Large-Scale Reproducible Benchmark for Black-Box HPO based on OpenML](https://openreview.net/forum?id=99P5Hbti02)                                                    | 6, 6, 5       | Unknown    |
|     84 |        5.67 |        0.58 | [All-In-One Drive: A Comprehensive Perception Dataset with High-Density Long-Range Point Clouds](https://openreview.net/forum?id=yl9aThYT9W)                                   | 6, 5, 6       | Unknown    |
|     85 |        5.67 |        0.58 | [Hangul Fonts Dataset: a Hierarchical and Compositional Dataset for Investigating Learned Representations](https://openreview.net/forum?id=EHfBhk6IkYF)                        | 5, 6, 6       | Unknown    |
|     86 |        5.67 |        0.58 | [JECC: Commonsense Reasoning Tasks Derived fromInteractive Fictions](https://openreview.net/forum?id=erOBVUgvryF)                                                              | 5, 6, 6       | Unknown    |
|     87 |        5.67 |        0.58 | [RealCause: Realistic Causal Inference Benchmarking](https://openreview.net/forum?id=m28E5RN64hi)                                                                              | 5, 6, 6       | Unknown    |
|     88 |        5.67 |        0.58 | [CityNet: A Multi-city Multi-modal Dataset for Smart City Applications](https://openreview.net/forum?id=sZHXepQkCGF)                                                           | 5, 6, 6       | Unknown    |
|     89 |        5.67 |        0.58 | [BiToD: A Bilingual Multi-Domain Dataset For Task-Oriented Dialogue Modeling](https://openreview.net/forum?id=dA2Q8CfmGpp)                                                     | 5, 6, 6       | Unknown    |
|     90 |        5.67 |        1.15 | [GrowSpace: Learning How to Shape Plants](https://openreview.net/forum?id=vyyHxhnZJSB)                                                                                         | 5, 7, 5       | Unknown    |
|     91 |        5.67 |        1.15 | [WaveFake: A Data Set to Facilitate Audio DeepFake Detection](https://openreview.net/forum?id=IO7jcf63iDI)                                                                     | 5, 7, 5       | Unknown    |
|     92 |        5.67 |        1.15 | [StudentSADD: Mobile Depression and Suicidal Ideation Screening of College Students during the Coronavirus Pandemic](https://openreview.net/forum?id=eOOiCyZ_h9f)              | 5, 7, 5       | Unknown    |
|     93 |        5.67 |        1.53 | [GitTables: A Large-Scale Corpus of Relational Tables](https://openreview.net/forum?id=yYQuqGcxFvb)                                                                            | 4, 6, 7       | Unknown    |
|     94 |        5.67 |        1.53 | [A ground-truth dataset of real security patches](https://openreview.net/forum?id=Q0SbORK5zoN)                                                                                 | 7, 6, 4       | Unknown    |
|     95 |        5.67 |        1.53 | [ImageNet-21K Pretraining for the Masses](https://openreview.net/forum?id=Zkj_VcZ6ol)                                                                                          | 4, 7, 6       | Unknown    |
|     96 |        5.67 |        2.08 | [Cluster3D: A Dataset and Benchmark for Clustering Non-Categorical 3D CAD Models](https://openreview.net/forum?id=dA2Iov0Ecxt)                                                 | 8, 5, 4       | Unknown    |
|     97 |        5.5  |        1.73 | [A Realistic Simulation Framework for Learning with Label Noise](https://openreview.net/forum?id=e9P6bypUFd)                                                                   | 7, 4, 4, 7    | Unknown    |
|     98 |        5.33 |        0.58 | [Benchmarking the Robustness of CNN-based Spatial-Temporal Models](https://openreview.net/forum?id=lg3iGvFQ5V)                                                                 | 6, 5, 5       | Unknown    |
|     99 |        5.33 |        0.58 | [Rethinking the Role of Hyperparameter Tuning in Optimizer Benchmarking](https://openreview.net/forum?id=s6M0gjo0rL0)                                                          | 5, 5, 6       | Unknown    |
|    100 |        5.33 |        0.58 | [Natural Adversarial Objects](https://openreview.net/forum?id=fE_gwAAKM7O)                                                                                                     | 5, 5, 6       | Unknown    |
|    101 |        5.33 |        0.58 | [ExpMRC: Explainability Evaluation for Machine Reading Comprehension](https://openreview.net/forum?id=pl6xnx3jZMh)                                                             | 5, 6, 5       | Unknown    |
|    102 |        5.33 |        0.58 | [ZeroWaste Dataset: Towards Automated Waste Recycling](https://openreview.net/forum?id=DAkP1TT_Ubm)                                                                            | 5, 5, 6       | Unknown    |
|    103 |        5.33 |        1.15 | [Brax - A Differentiable Physics Engine for Large Scale Rigid Body Simulation](https://openreview.net/forum?id=VdvDlnnjzIN)                                                    | 6, 6, 4       | Unknown    |
|    104 |        5.33 |        1.15 | [The Argoverse Trajectory Retrieval Benchmark](https://openreview.net/forum?id=ooWbKrRIk9G)                                                                                    | 6, 6, 4       | Unknown    |
|    105 |        5.33 |        1.15 | [Addressing "Documentation Debt" in Machine Learning: A Retrospective Datasheet for BookCorpus](https://openreview.net/forum?id=Qd_eU1wvJeu)                                   | 4, 6, 6       | Unknown    |
|    106 |        5.33 |        1.53 | [Towards a universal dataset and metrics for training and evaluating table extraction models](https://openreview.net/forum?id=6lYwZ6yknRw)                                     | 5, 4, 7       | Unknown    |
|    107 |        5.33 |        1.53 | [MMVText: A Large-Scale, Multidimensional Multilingual Dataset for Video Text Spotting](https://openreview.net/forum?id=nvPp2SomA98)                                           | 7, 4, 5       | Unknown    |
|    108 |        5.33 |        1.53 | [PROCAT: Product Catalogue Dataset for Implicit Clustering, Permutation Learning and Structure Prediction](https://openreview.net/forum?id=HQ-6VDYUxGn)                        | 4, 7, 5       | Unknown    |
|    109 |        5.33 |        1.53 | [Monash Time Series Forecasting Archive](https://openreview.net/forum?id=I01l7rc0jcb)                                                                                          | 7, 4, 5       | Unknown    |
|    110 |        5.33 |        2.08 | [SODA10M: Towards Large-Scale Object Detection Benchmark for Autonomous Driving](https://openreview.net/forum?id=kUkp7WdUny9)                                                  | 7, 3, 6       | Unknown    |
|    111 |        5.33 |        2.31 | [Chest ImaGenome Dataset for Clinical Reasoning](https://openreview.net/forum?id=qMxVrCug4rI)                                                                                  | 4, 8, 4       | Unknown    |
|    112 |        5.33 |        2.31 | [Synthetic Benchmarks for Scientific Research in Explainable Machine Learning](https://openreview.net/forum?id=oRHIGl9PMxj)                                                    | 8, 4, 4       | Unknown    |
|    113 |        5.25 |        0.96 | [Irregular Shape Instance Segmentation](https://openreview.net/forum?id=48CBzhshpcS)                                                                                           | 6, 4, 5, 6    | Unknown    |
|    114 |        5    |        0    | [On Predicting and Generating a Good Break Shot in Billiards Sports](https://openreview.net/forum?id=aEMLMjbvftN)                                                              | 5, 5, 5       | Unknown    |
|    115 |        5    |        0    | [Robustness Disparities in Commercial Face Detection](https://openreview.net/forum?id=1Y9fPheTgpp)                                                                             | 5, 5, 5       | Unknown    |
|    116 |        5    |        0.82 | [NATURE: Natural Auxiliary Text Utterances forRealistic Spoken Language Evaluation](https://openreview.net/forum?id=LL_LfK7dfpR)                                               | 4, 5, 6, 5    | Unknown    |
|    117 |        5    |        1    | [VISIOCITY: A New Benchmarking Dataset and Evaluation Framework Towards Realistic Video Summarization](https://openreview.net/forum?id=iBLHqLgbRn)                             | 5, 6, 4       | Unknown    |
|    118 |        5    |        1    | [A Dataset of Discovering Drug-Target Interaction from Biomedical Literature](https://openreview.net/forum?id=Mop0QMT5yei)                                                     | 4, 5, 6       | Unknown    |
|    119 |        5    |        1    | [MQBench: Towards Reproducible and Deployable Model Quantization Benchmark](https://openreview.net/forum?id=TUplOmF8DsM)                                                       | 4, 6, 5       | Unknown    |
|    120 |        5    |        1    | [Particulate Matter Dataset Collected with Vehicle Mounted IoT Devices in Delhi-NCR](https://openreview.net/forum?id=q7XJj9_egih)                                              | 6, 4, 5       | Unknown    |
|    121 |        5    |        1    | [Bongard-HOI: Benchmarking Few-Shot Visual Reasoning for Human-Object Interactions](https://openreview.net/forum?id=mHrF3-r8-8t)                                               | 4, 6, 5       | Unknown    |
|    122 |        5    |        1    | [VoxelScape: Large Scale Simulated 3D Point Cloud Dataset of Urban Traffic Environments](https://openreview.net/forum?id=JNvy4qBcxHW)                                          | 4, 6, 5       | Unknown    |
|    123 |        5    |        1    | [SeasonDepth: Cross-Season Monocular Depth Prediction Dataset and Benchmark under Multiple Environments](https://openreview.net/forum?id=kOxP7Fbeduy)                          | 6, 5, 4, 4, 6 | Unknown    |
|    124 |        5    |        1.15 | [ARKitScenes - A Diverse Real-World Dataset for 3D Indoor Scene Understanding Using Mobile RGB-D Data](https://openreview.net/forum?id=tjZjv_qh_CE)                            | 4, 6, 4, 6    | Unknown    |
|    125 |        5    |        1.73 | [ComSum: Commit Messages Summarization and Meaning Preservation](https://openreview.net/forum?id=4lvu1B4Y0E)                                                                   | 6, 6, 3       | Unknown    |
|    126 |        5    |        1.73 | [RealCity3D: A Large-scale Georeferenced 3D Shape Dataset of Real-world Cities](https://openreview.net/forum?id=VjFn0L5T7NU)                                                   | 7, 4, 4       | Unknown    |
|    127 |        5    |        2    | [Graph Robustness Benchmark: Rethinking and Benchmarking Adversarial Robustness of Graph Neural Networks](https://openreview.net/forum?id=pBwQ82pYha)                          | 7, 5, 3       | Unknown    |
|    128 |        5    |        2    | [Turath-150K: Image Database of Arab Heritage](https://openreview.net/forum?id=Wb4vR9NPE6_)                                                                                    | 3, 7, 5       | Unknown    |
|    129 |        5    |        2.45 | [Scenic4RL: Programmatic Modeling and Generation of Reinforcement Learning Environments](https://openreview.net/forum?id=dtjnxfS9OE4)                                          | 5, 5, 8, 2    | Unknown    |
|    130 |        4.75 |        0.96 | [Hi-Phy: A Benchmark for Hierarchical Physical Reasoning](https://openreview.net/forum?id=AcL1ORzw0Nf)                                                                         | 5, 4, 6, 4    | Unknown    |
|    131 |        4.75 |        1.71 | [SMART-Rain: A Degradation Evaluation Dataset for Autonomous Driving in Rain](https://openreview.net/forum?id=NqErRNg_8Fb)                                                     | 3, 4, 7, 5    | Unknown    |
|    132 |        4.67 |        0.58 | [A2X: An Agent and Environment Interaction Benchmark for Multimodal Human Trajectory Prediction](https://openreview.net/forum?id=f5zF1mgCLR0)                                  | 5, 4, 5       | Unknown    |
|    133 |        4.67 |        1.15 | [The Tarteel Dataset: Crowd-Sourced and Labeled Quranic Recitation](https://openreview.net/forum?id=TAdzPkgnnV8)                                                               | 4, 4, 6       | Unknown    |
|    134 |        4.67 |        1.15 | [Arena: A Scalable and Configurable Benchmark for Policy Learning](https://openreview.net/forum?id=7hQLXPnfrqk)                                                                | 4, 6, 4       | Unknown    |
|    135 |        4.67 |        2.08 | [DIPS-Plus: The Enhanced Database of Interacting Protein Structures for Interface Prediction](https://openreview.net/forum?id=lwlkxYsGDi)                                      | 7, 4, 3       | Unknown    |
|    136 |        4.67 |        2.52 | [Age dataset: age of death and other basic information for over 1.31 million historical figures (data, methods and applications)](https://openreview.net/forum?id=ls__H1FcLwv) | 2, 7, 5       | Unknown    |
|    137 |        4.33 |        0.58 | [NeoRL: A Near Real-World Benchmark for Offline Reinforcement Learning](https://openreview.net/forum?id=DSo2Zteb9l8)                                                           | 4, 4, 5       | Unknown    |
|    138 |        4.33 |        0.58 | [Geon3D: Benchmarking 3D Shape Bias towards Building Robust Machine Vision](https://openreview.net/forum?id=8HkbjXqbAnz)                                                       | 5, 4, 4       | Unknown    |
|    139 |        4.33 |        0.58 | [A Framework for Cluster and Classifier Evaluation in the Absence of Reference Labels](https://openreview.net/forum?id=eYg8ssXm3BT)                                            | 4, 5, 4       | Unknown    |
|    140 |        4.33 |        0.58 | [Karenina: Modeling the Complexity of Negative Emotions to Better Serve Industry Goals](https://openreview.net/forum?id=rX_fl1Gd0k4)                                           | 5, 4, 4       | Unknown    |
|    141 |        4.33 |        0.58 | [DermX: a Dermatological Diagnosis Explainability Dataset](https://openreview.net/forum?id=wBOBL5b-aa9)                                                                        | 5, 4, 4       | Unknown    |
|    142 |        4.33 |        0.58 | [CatLC: Catalonia Multiresolution Land Cover Dataset](https://openreview.net/forum?id=fl5PtMeGJ8z)                                                                             | 5, 4, 4       | Unknown    |
|    143 |        4.33 |        0.58 | [Modeling and Optimizing Laser-Induced Graphene](https://openreview.net/forum?id=IsYUDnbIqay)                                                                                  | 4, 5, 4       | Unknown    |
|    144 |        4.33 |        1.15 | [Design-Bench: Benchmarks for Data-Driven Offline Model-Based Optimization](https://openreview.net/forum?id=0OyT3oVv_Rk)                                                       | 3, 5, 5       | Unknown    |
|    145 |        4.33 |        1.53 | [MAIN: A Multi-agent Indoor Navigation Benchmark for Cooperative Learning](https://openreview.net/forum?id=B-d4pw2JdT)                                                         | 6, 4, 3       | Unknown    |
|    146 |        4.33 |        1.53 | [High-Dimensional Gene Expression and Morphology Profiles of Cells across 28,000 Genetic and Chemical Perturbations](https://openreview.net/forum?id=Blmvlo-yRR9)              | 6, 4, 3       | Unknown    |
|    147 |        4    |        0    | [Three million images and morphological profiles of cells treated with matched chemical and genetic perturbations](https://openreview.net/forum?id=rCRyg1-Yovi)                | 4, 4, 4       | Unknown    |
|    148 |        4    |        1    | [Reconstruction benchmark for obfuscated representations](https://openreview.net/forum?id=ldUthK0EVx8)                                                                         | 4, 3, 5       | Unknown    |
|    149 |        4    |        1    | [Multi-Domain Conditional Image Translation: Translating Driving Datasets from Clear-Weather to Adverse Conditions](https://openreview.net/forum?id=CYhs2XrEFNA)               | 5, 3, 4       | Unknown    |
|    150 |        4    |        1    | [A Dataset for Label Aggregation from Crowdsourced Triplet Similarity Comparisons](https://openreview.net/forum?id=xZWBVuL_ip9)                                                | 4, 3, 5       | Unknown    |
|    151 |        4    |        1    | [NAS-Bench-360: Benchmarking Diverse Tasks for Neural Architecture Search](https://openreview.net/forum?id=cbFfF4g9fIy)                                                        | 3, 4, 5       | Unknown    |
|    152 |        4    |        2    | [HypeML: A Health AI Promotional Language Dataset](https://openreview.net/forum?id=ASeMiqai-k1)                                                                                | 6, 4, 2       | Unknown    |
|    153 |        3.67 |        0.58 | [Deep Credal Neural Network: Characterization of Imprecision Between Categories](https://openreview.net/forum?id=-I6La-GJS5b)                                                  | 3, 4, 4       | Unknown    |
|    154 |        3.67 |        1.15 | [Using Dynamic Neural Networks to Model the Speed-Accuracy Trade-Off in People](https://openreview.net/forum?id=pOf_IV_-XG)                                                    | 5, 3, 3       | Unknown    |
|    155 |        3.33 |        0.58 | [Rail-5k: a Real-World Dataset for Rail Surface Defects Detection](https://openreview.net/forum?id=YJHXfcTDaqw)                                                                | 4, 3, 3       | Unknown    |
|    156 |        3.33 |        0.58 | [New Zealand Open Environmental Science Data sets](https://openreview.net/forum?id=70XgWMiBeH7)                                                                                | 3, 4, 3       | Unknown    |
|    157 |        3.33 |        0.58 | [Multi-Dataset Benchmarks for Masked Identification using Contrastive Representation Learning](https://openreview.net/forum?id=ktkr1GgZrK4)                                    | 4, 3, 3       | Unknown    |
|    158 |        3    |        1    | [“There will be consequences!” Datasets and Benchmarks towards Causal Relation Extraction and Societal Event Forecasting](https://openreview.net/forum?id=PQldd-oUHa8)         | 3, 2, 4       | Unknown    |
|    159 |        2.67 |        0.58 | [EEG Thinking1 Datasets: Think-Count-Recall (TCR) and Read-Write-Type (RWT)](https://openreview.net/forum?id=dTxWk9K5KC)                                                       | 3, 3, 2       | Unknown    |
|    160 |        2.67 |        1.53 | [Indian-CT, Dataset and Analysis of Chest CT Scans of COVID-19 Patients Using Light-weight CNN](https://openreview.net/forum?id=t1kTABPcp9s)                                   | 4, 3, 1       | Unknown    |
|    161 |        2    |        0    | [SkillBERT: "Skilling" the BERT to classify skills using Electronic Recruitment Records](https://openreview.net/forum?id=JjuthZiKQ8H)                                          | 2, 2, 2       | Unknown    |
