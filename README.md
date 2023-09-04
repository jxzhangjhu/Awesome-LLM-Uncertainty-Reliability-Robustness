# Awesome-LLM-Uncertainty-Reliability-Robustness

\
[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/hee9joon/Awesome-Diffusion-Models) 
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Made With Love](https://img.shields.io/badge/Made%20With-Love-red.svg)](https://github.com/chetanraj/awesome-github-badges)

This repository, called **UR2-LLMs** contains a collection of resources and papers on **Uncertainty**, **Reliability** and **Robustness** in **Large Language Models**. 

"*Large language models have limited reliability, limited understanding, limited range, and hence need human supervision*. " - Michael Osborne, Professor of Machine Learning in the Dept. of Engineering Science, University of Oxford, January 25, 2023 

*Welcome to share your papers, thoughts and ideas in this area!* 

## Contents

- [Resources](#resources)
  - [Introductory Posts](#introductory-posts)
  - [Technical Reports](#technical-reports)
  - [Tutorial](#tutorial)
- [Papers](#papers)
  - [Evaluation and Survey](#evaluation-and-survey)
  - [Uncertainty](#uncertainty)
    - [Uncertainty Estimation](#uncertainty-estimation)
    - [Calibration](#calibration)
    - [Ambiguity](#ambiguity)
    - [Confidence](#confidence)
    - [Active Learning](#active-learning)
  - [Reliability](#reliability)
    - [Hallucination](#hallucination)
    - [Truthfulness](#truthfulness)
    - [Reasoning](#reasoning)
    - [Prompt tuning, optimization and design](#prompt-tuning-optimization-and-design)
    - [Instruction and RLHF](#instruction-and-rlhf)
    - [Tools and external APIs](#tools-and-external-apis)
  - [Robustness](#robustness)
    - [Invariance](#invariance)
    - [Distribution Shift](#distribution-shift)
    - [Out-of-Distribution](#out-of-distribution)
    - [Adaptation and Generalization](#adaptation-and-generalization)
    - [Adversarial](#adversarial)
    - [Attribution](#attribution)
    - [Causality](#causality)
<!--   - [Safety](#safety)
    - [Bias and Fairness](#bias-and-fairness)
    - [Privacy](#privacy) -->



# Resources
## Introductory Posts


**GPT Is an Unreliable Information Store** \
*Noble Ackerson* \
[[Link](https://towardsdatascience.com/chatgpt-insists-i-am-dead-and-the-problem-with-language-models-db5a36c22f11)] \
20 Feb 2023 

<!-- > Comments \
- Large Language models are unreliable information stores. What can we do about this?
By design, these systems do not know what they do or don’t know.

- GPT is trained on massive amounts of text data without any inherent ability to verify the accuracy or truthfulness of the information presented in that data.

- So should we build on top of factually unreliable GPTs?
Yes. Though when we do, we must ensure we add the appropriate trust and safety checks and the practical constraints through techniques I’ll share below. When building atop these foundational models, we can minimize inaccuracy using proper guardrails with techniques like prompt engineering and context injection.

Or, if we have our own larger datasets, more advanced approaches such as Transfer learning, fine-tuning, and reinforcement learning are areas to consider.

nice blog -->

**“Misusing” Large Language Models and the Future of MT** \
*Arle Lommel* \
[[Link](https://csa-research.com/Blogs-Events/Blog/Misusing-Large-Language-Models-and-the-Future-of-MT)] \
20 Dec 2022 

<!-- 1. Large language models make the “trust problem” worse. Despite the expectation that large language models would lead to the next wave of dramatic improvement in MT, they introduce some serious risks. One of the biggest challenges for MT now is that it is not reliable. Although the development of responsive and responsible MT should improve this, large language models that can produce convincing-sounding output that is nonsense are likely to increase the risk of dangerous or harmful translation errors. My experiments showed that users should not trust what Galactica says at face value, but instead need to examine it carefully to verify everything. Note that this problem will be worse in languages with relatively little training data in these models.

6. Quality estimation will become key. As the output of MT becomes more fluent, detecting problems will become increasingly difficult, which can: a) raise the risk that content can pose; and b) increase the cognitive load for MT editors and thereby decrease their efficiency. This means that quality estimation will become more important, requiring breakthroughs in this area. When the technology can reliably identify problems and risk, it will address the trust problem. -->


**Large language models: The basics and their applications** \
*Margo Poda* \
[[Link](https://www.moveworks.com/insights/large-language-models-strengths-and-weaknesses)] \
9 Feb 2023 

<!-- > Reliability needs human supervison which is the key! -->

**Prompt Engineering: Improving Responses & Reliability** \
*Peter Foy*\
[[Link](https://www.mlq.ai/prompt-engineering-techniques-improve-reliability/)]\
19 Mar 2023 

<!-- nice blog  -->

**OpenAI's Cookbook on Techniques to Improve Reliability** \
*OpenAI* \
[[Github](https://github.com/openai/openai-cookbook)] \
18 Mar 2023

**GPT/calibration tag** \
*Gwern Branwen* \
[[Link](https://gwern.net/doc/ai/nn/transformer/gpt/calibration/index#link-bibliography)]

**Prompt Engineering** \
*Lilian Weng*\
[[Link](https://lilianweng.github.io/posts/2023-03-15-prompt-engineering/)]


**LLM Powered Autonomous Agents** \
*Lilian Weng*\
[[Link](https://lilianweng.github.io/posts/2023-06-23-agent/)]


**Reliability in Learning Prompting**\
[[Link](https://learnprompting.org/docs/category/%EF%B8%8F-reliability)] 


**Building LLM applications for production** \
*Chip Huyen* \
[[Link](https://huyenchip.com/2023/04/11/llm-engineering.html)] \
11 Apr 2023 



## Technical Reports 

**GPT-4 Technical Report** \
*OpenAI* \
arXiv 2023. [[Paper](https://cdn.openai.com/papers/gpt-4.pdf)][[Cookbook](https://github.com/openai/evals)] \
16 Mar 2023 

**GPT-4 System Card** \
*OpenAI* \
arXiv 2023. [[Paper](https://cdn.openai.com/papers/gpt-4-system-card.pdf)] [[Github](https://github.com/openai/evals)]\
15 Mar 2023 

 
## Tutorial 

**Uncertainty Estimation for Natural Language Processing** \
*Adam Fisch, Robin Jia, Tal Schuster* \
COLLING 2022. [[Website](https://sites.google.com/view/uncertainty-nlp)]

<!-- ## Prompt Engineering & Papers

**PromptPapers** - [[Link](https://github.com/thunlp/PromptPapers)] 

**Awesome-Prompt-Engineering** - [[Link](https://github.com/promptslab/Awesome-Prompt-Engineering)]
 -->




# Papers

## Evaluation & Survey

**A Survey on Evaluation of Large Language Models** \
*Yupeng Chang, Xu Wang, Jindong Wang, Yuan Wu, Kaijie Zhu, Hao Chen, Linyi Yang, Xiaoyuan Yi, Cunxiang Wang, Yidong Wang, Wei Ye, Yue Zhang, Yi Chang, Philip S. Yu, Qiang Yang, Xing Xie* \
Arxiv 2023. [[Paper](https://arxiv.org/abs/2307.03109)][[Github](https://github.com/mlgroupjlu/llm-eval-survey)] \
6 Jul 2023 



**DecodingTrust: A Comprehensive Assessment of Trustworthiness in GPT Models** \
*Boxin Wang, Weixin Chen, Hengzhi Pei, Chulin Xie, Mintong Kang, Chenhui Zhang, Chejian Xu, Zidi Xiong, Ritik Dutta, Rylan Schaeffer, Sang T. Truong, Simran Arora, Mantas Mazeika, Dan Hendrycks, Zinan Lin, Yu Cheng, Sanmi Koyejo, Dawn Song, Bo Li* \
Arxiv, 2023. [[Paper](https://arxiv.org/abs/2306.11698)] [[Github](https://github.com/AI-secure/DecodingTrust/)] [[Website](https://decodingtrust.github.io/)] \
20 Jun 2023 

**Harnessing the Power of LLMs in Practice: A Survey on ChatGPT and Beyond** \
*Jingfeng Yang, Hongye Jin, Ruixiang Tang, Xiaotian Han, Qizhang Feng, Haoming Jiang, Bing Yin, Xia Hu* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2304.13712)][[Github](https://github.com/mooler0410/llmspracticalguide)] \
27 Apr 2023 

**How Robust is GPT-3.5 to Predecessors? A Comprehensive Study on Language Understanding Tasks** \
*Xuanting Chen, Junjie Ye, Can Zu, Nuo Xu, Rui Zheng, Minlong Peng, Jie Zhou, Tao Gui, Qi Zhang, Xuanjing Huang* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2303.00293)][[Github](https://github.com/textflint/textflint)] \
1 Mar 2023

**Holistic Evaluation of Language Models** \
*Percy Liang, Rishi Bommasani, Tony Lee, Dimitris Tsipras, Dilara Soylu, Michihiro Yasunaga, Yian Zhang, Deepak Narayanan, Yuhuai Wu, Ananya Kumar, Benjamin Newman, Binhang Yuan, Bobby Yan, Ce Zhang, Christian Cosgrove, Christopher D. Manning, Christopher Ré, Diana Acosta-Navas, Drew A. Hudson, Eric Zelikman, Esin Durmus, Faisal Ladhak, Frieda Rong, Hongyu Ren, Huaxiu Yao, Jue Wang, Keshav Santhanam, Laurel Orr, Lucia Zheng, Mert Yuksekgonul, Mirac Suzgun, Nathan Kim, Neel Guha, Niladri Chatterji, Omar Khattab, Peter Henderson, Qian Huang, Ryan Chi, Sang Michael Xie, Shibani Santurkar, Surya Ganguli, Tatsunori Hashimoto, Thomas Icard, Tianyi Zhang, Vishrav Chaudhary, William Wang, Xuechen Li, Yifan Mai, Yuhui Zhang, Yuta Koreeda* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2211.09110)] [[Website](https://crfm.stanford.edu/helm/latest/)] [[Github](https://github.com/stanford-crfm/helm)] [[Blog](https://crfm.stanford.edu/2022/11/17/helm.html)] \
16 Nov 2022

**Prompting GPT-3 To Be Reliable** \
*Chenglei Si, Zhe Gan, Zhengyuan Yang, Shuohang Wang, Jianfeng Wang, Jordan Boyd-Graber, Lijuan Wang* \
ICLR 2023. [[Paper](https://arxiv.org/abs/2210.09150)] [[Github](https://github.com/NoviScl/GPT3-Reliability)] \
17 Oct 2022

**Plex: Towards Reliability using Pretrained Large Model Extensions** \
*Dustin Tran, Jeremiah Liu, Michael W. Dusenberry, Du Phan, Mark Collier, Jie Ren, Kehang Han, Zi Wang, Zelda Mariet, Huiyi Hu, Neil Band, Tim G. J. Rudner, Karan Singhal, Zachary Nado, Joost van Amersfoort, Andreas Kirsch, Rodolphe Jenatton, Nithum Thain, Honglin Yuan, Kelly Buchanan, Kevin Murphy, D. Sculley, Yarin Gal, Zoubin Ghahramani, Jasper Snoek, Balaji Lakshminarayanan* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2207.07411)] \
15 Jul 2022

**Language Models (Mostly) Know What They Know** \
*Saurav Kadavath, Tom Conerly, Amanda Askell, Tom Henighan, Dawn Drain, Ethan Perez, Nicholas Schiefer, Zac Hatfield-Dodds, Nova DasSarma, Eli Tran-Johnson, Scott Johnston, Sheer El-Showk, Andy Jones, Nelson Elhage, Tristan Hume, Anna Chen, Yuntao Bai, Sam Bowman, Stanislav Fort, Deep Ganguli, Danny Hernandez, Josh Jacobson, Jackson Kernion, Shauna Kravec, Liane Lovitt, Kamal Ndousse, Catherine Olsson, Sam Ringer, Dario Amodei, Tom Brown, Jack Clark, Nicholas Joseph, Ben Mann, Sam McCandlish, Chris Olah, Jared Kaplan* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2207.05221)] \
11 Jul 2022 

**Augmented Language Models: a Survey** \
*Grégoire Mialon, Roberto Dessì, Maria Lomeli, Christoforos Nalmpantis, Ram Pasunuru, Roberta Raileanu, Baptiste Rozière, Timo Schick, Jane Dwivedi-Yu, Asli Celikyilmaz, Edouard Grave, Yann LeCun, Thomas Scialom* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2302.07842)] \
15 Feb 2023 

**A Survey of Evaluation Metrics Used for NLG Systems** \
*Ananya B. Sai, Akash Kumar Mohankumar, Mitesh M. Khapra* \
ACM Computing Survey, 2022. [[Paper](https://dl.acm.org/doi/abs/10.1145/3485766)] \
18 Jan 2022

**NL-Augmenter: A Framework for Task-Sensitive Natural Language Augmentation** \
*Kaustubh D. Dhole, et al.* \
ACL 2021. [[Paper](https://arxiv.org/abs/2112.02721)][[Github](https://github.com/GEM-benchmark/NL-Augmenter)] \
6 Dec 2021 

**TextFlint: Unified Multilingual Robustness Evaluation Toolkit for Natural Language Processing** \
*Tao Gui et al.* \
arXiv 2021. [[Paper](https://arxiv.org/abs/2103.11441)][[Github](https://github.com/textflint/textflint)] \
21 Mar 2021 

**Robustness Gym: Unifying the NLP Evaluation Landscape** \
*Karan Goel, Nazneen Rajani, Jesse Vig, Samson Tan, Jason Wu, Stephan Zheng, Caiming Xiong, Mohit Bansal, Christopher Ré* \
ACL 2021. [[Paper](https://arxiv.org/abs/2101.04840)] [[Github](https://github.com/robustness-gym/robustness-gym)] \
13 Jan 2021

**Beyond Accuracy: Behavioral Testing of NLP models with CheckList** \
*Marco Tulio Ribeiro, Tongshuang Wu, Carlos Guestrin, Sameer Singh* \
ACL 2020. [[Paper](https://arxiv.org/abs/2005.04118)][[Github](https://github.com/marcotcr/checklist)] \
8 May 2020


## Uncertainty

### Uncertainty Estimation

**Generating with Confidence: Uncertainty Quantification for Black-box Large Language Models** \
*Zhen Lin, Shubhendu Trivedi, Jimeng Sun* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2305.19187)] [[Github](https://github.com/zlin7/UQ-NLG)] \
30 May 2023. 

**Human Uncertainty in Concept-Based AI Systems** \
*Katherine M. Collins, Matthew Barker, Mateo Espinosa Zarlenga, Naveen Raman, Umang Bhatt, Mateja Jamnik, Ilia Sucholutsky, Adrian Weller, Krishnamurthy Dvijotham* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2303.12872)] \
22 Mar 2023 

**Navigating the Grey Area: Expressions of Overconfidence and Uncertainty in Language Models** \
*Kaitlyn Zhou, Dan Jurafsky, Tatsunori Hashimoto* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2302.13439)] \
25 Feb 2023 

**DEUP: Direct Epistemic Uncertainty Prediction** \
*Salem Lahlou, Moksh Jain, Hadi Nekoei, Victor Ion Butoi, Paul Bertin, Jarrid Rector-Brooks, Maksym Korablyov, Yoshua Bengio* \
TMLR 2023. [[Paper](https://arxiv.org/abs/2102.08501)] \
3 Feb 2023 


**On Compositional Uncertainty Quantification for Seq2seq Graph Parsing** \
*Zi Lin, Du Phan, Panupong Pasupat, Jeremiah Zhe Liu, Jingbo Shang* \
ICLR 2023. [[Paper](https://openreview.net/forum?id=rJcLocAJpA6)] \
1 Feb 2023 


**Neural-Symbolic Inference for Robust Autoregressive Graph Parsing via Compositional Uncertainty Quantification** \
*Zi Lin, Jeremiah Liu, Jingbo Shang* \
EMNLP 2022. [[Paper](https://arxiv.org/abs/2301.11459)] \
16 Jan 2023


**Teaching Models to Express Their Uncertainty in Words** \
*Stephanie Lin, Jacob Hilton, Owain Evans* \
TMLR 2022. [[Paper](https://arxiv.org/abs/2205.14334)] [[Github](https://github.com/sylinrl/CalibratedMath)] [[TMLR](https://openreview.net/forum?id=8s8K2UZGTZ)] [[Slide](https://owainevans.github.io/pdfs/chai_calibration_owain.pdf)]\
28 May 2022

**Semantic Uncertainty: Linguistic Invariances for Uncertainty Estimation in Natural Language Generation** \
*Lorenz Kuhn, Yarin Gal, Sebastian Farquhar* \
ICLR 2023. [[Paper](https://arxiv.org/abs/2302.09664)] \
19 Feb 2022


**Cold-Start Data Selection for Few-shot Language Model Fine-tuning: A Prompt-Based Uncertainty Propagation Approach** \
*Yue Yu, Rongzhi Zhang, Ran Xu, Jieyu Zhang, Jiaming Shen, Chao Zhang* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2209.06995)][[Github](https://github.com/yueyu1030/Patron)] \
15 Sep 2022


**Fine-Tuning Language Models via Epistemic Neural Networks** \
*Ian Osband, Seyed Mohammad Asghari, Benjamin Van Roy, Nat McAleese, John Aslanides, Geoffrey Irving* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2211.01568)][[Github](https://github.com/deepmind/neural_testbed)] \
3 Nov 2022 



**Uncertainty Quantification with Pre-trained Language Models: A Large-Scale Empirical Analysis** \
*Yuxin Xiao, Paul Pu Liang, Umang Bhatt, Willie Neiswanger, Ruslan Salakhutdinov, Louis-Philippe Morency* \
EMNLP 2022 (Findings). [[Paper](https://arxiv.org/abs/2210.04714)][[Github](https://github.com/xiaoyuxin1002/uq-plm)] \
10 Oct 2022 

**Uncertainty Estimation for Language Reward Models** \
*Adam Gleave, Geoffrey Irving* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2203.07472)] \
14 Mar 2022 

**Uncertainty Estimation and Reduction of Pre-trained Models for Text Regression** \
*Yuxia Wang, Daniel Beck, Timothy Baldwin, Karin Verspoor* \
TACL 2022. [[Paper](https://aclanthology.org/2022.tacl-1.39/)] \
Jun 2022 


**Uncertainty Estimation in Autoregressive Structured Prediction** \
*Andrey Malinin, Mark Gales* \
ICLR 2021. [[Paper](https://arxiv.org/abs/2002.07650)] \
18 Feb 2020 


**Unsupervised Quality Estimation for Neural Machine Translation** \
*Marina Fomicheva, Shuo Sun, Lisa Yankovskaya, Frédéric Blain, Francisco Guzmán, Mark Fishel, Nikolaos Aletras, Vishrav Chaudhary, Lucia Specia* \
TACL 2020. [[Paper](https://arxiv.org/abs/2005.10608)][[Dataset](https://github.com/facebookresearch/mlqe)] \
21 May 2020 


**Analyzing Uncertainty in Neural Machine Translation** \
*Myle Ott, Michael Auli, David Grangier, Marc’Aurelio Ranzato* \
ICML 2018.  [[Paper](https://proceedings.mlr.press/v80/ott18a.html)] \
2018 


### Calibration


**Do Large Language Models Know What They Don't Know?** \
*Zhangyue Yin, Qiushi Sun, Qipeng Guo, Jiawen Wu, Xipeng Qiu, Xuanjing Huang* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2305.18153)] 
29 May 2023 

**Just Ask for Calibration: Strategies for Eliciting Calibrated Confidence Scores from Language Models Fine-Tuned with Human Feedback** \
*Katherine Tian, Eric Mitchell, Allan Zhou, Archit Sharma, Rafael Rafailov, Huaxiu Yao, Chelsea Finn, Christopher D. Manning* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2305.14975)] \
24 May 2023 


**Towards Reliable Misinformation Mitigation: Generalization, Uncertainty, and GPT-4** \
*Kellin Pelrine, Meilina Reksoprodjo, Caleb Gupta, Joel Christoph, Reihaneh Rabbany* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2305.14928)] \
24 May 2023 



**Calibrated Interpretation: Confidence Estimation in Semantic Parsing** \
*Elias Stengel-Eskin, Benjamin Van Durme* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2211.07443)] [[Github](https://github.com/esteng/calibration_miso)] \
14 Nov 2022. 


**Calibrating Sequence likelihood Improves Conditional Language Generation** \
*Yao Zhao, Misha Khalman, Rishabh Joshi, Shashi Narayan, Mohammad Saleh, Peter J. Liu* \
ICLR 2023. [[Paper](https://arxiv.org/abs/2210.00045)]\
30 Sep 2022

**Calibrated Selective Classification** \
*Adam Fisch, Tommi Jaakkola, Regina Barzilay* \
TMLR 2022. [[Paper](https://arxiv.org/abs/2208.12084)] \
25 Aug 2022 


**Reducing conversational agents' overconfidence through linguistic calibration** \
*Sabrina J. Mielke, Arthur Szlam, Emily Dinan, Y-Lan Boureau* \
NAACL 2022. [[Paper](https://arxiv.org/abs/2012.14983)] \
22 Jun 2022 

**Re-Examining Calibration: The Case of Question Answering** \
*Chenglei Si, Chen Zhao, Sewon Min, Jordan Boyd-Graber* \
EMNLP 2022 Findings. [[Paper](https://arxiv.org/abs/2205.12507)] \
25 May 2022 

**Towards Collaborative Neural-Symbolic Graph Semantic Parsing via Uncertainty** \
*Zi Lin, Jeremiah Liu, Jingbo Shang* \
ACL Fingings 2022. [[Paper](https://aclanthology.org/2022.findings-acl.328.pdf)] \
22 May 2022


**Uncertainty-aware machine translation evaluation** \
*Taisiya Glushkova, Chrysoula Zerva, Ricardo Rei, André F. T. Martins* \
EMNLP 2021. [[Paper](https://arxiv.org/abs/2109.06352)] \
13 Sep 2021


**Calibrate Before Use: Improving Few-Shot Performance of Language Models** \
*Tony Z. Zhao, Eric Wallace, Shi Feng, Dan Klein, Sameer Singh* \
ICML 2021. [[Paper](https://arxiv.org/abs/2102.09690)][[Github](https://github.com/tonyzhaozh/few-shot-learning) \
19 Feb 2021

**How Can We Know When Language Models Know? On the Calibration of Language Models for Question Answering** \
*Zhengbao Jiang, Jun Araki, Haibo Ding, Graham Neubig* \
TACL 2021. [[Paper](https://arxiv.org/abs/2012.00955)][[Github](https://github.com/jzbjyb/lm-calibration)] \
2 Dec 2020

**Calibration of Pre-trained Transformers** \
*Shrey Desai, Greg Durrett* \
EMNLP 2020. [[Paper](https://arxiv.org/abs/2003.07892)][[Github](https://github.com/shreydesai/calibration)] \
17 May 2020


### Ambiguity 

**Selectively Answering Ambiguous Questions** \
*Jeremy R. Cole, Michael J.Q. Zhang, Daniel Gillick, Julian Martin Eisenschlos, Bhuwan Dhingra, Jacob Eisenstein* \ 
arXiv 2023. [[Paper](https://arxiv.org/abs/2305.14613)] \
24 May 2023 
 

**We're Afraid Language Models Aren't Modeling Ambiguity** \ 
*Alisa Liu, Zhaofeng Wu, Julian Michael, Alane Suhr, Peter West, Alexander Koller, Swabha Swayamdipta, Noah A. Smith, Yejin Choi* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2304.14399v1)][[Github](https://github.com/alisawuffles/ambient)] \
24 Apr 2023 

**Task Ambiguity in Humans and Language Models** \
*Alex Tamkin, Kunal Handa, Avash Shrestha, Noah Goodman* \
ICLR 2023. [[Paper](https://arxiv.org/abs/2212.10711)][[Github](https://github.com/alextamkin/active-learning-pretrained-models)] \
20 Dec 2022 


**CLAM: Selective Clarification for Ambiguous Questions with Generative Language Models** \
*Lorenz Kuhn, Yarin Gal, Sebastian Farquhar* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2212.07769)] \
15 Dec 2022

**How to Approach Ambiguous Queries in Conversational Search: A Survey of Techniques, Approaches, Tools, and Challenges** \
*Kimiya Keyvan, Jimmy Xiangji Huang* \
ACM Computing Survey, 2022. [[Paper](https://dl.acm.org/doi/abs/10.1145/3534965)] \
7 Dec 2022 

**Assistance with large language models** \
*Dmitrii Krasheninnikov, Egor Krasheninnikov, David Krueger* \
NeurIPS MLSW Workshop 2022. [[Paper](https://openreview.net/forum?id=OE9V81spp6B)] \
5 Dec 2022 

**Why Did the Chicken Cross the Road? Rephrasing and Analyzing Ambiguous Questions in VQA** \
*Elias Stengel-Eskin, Jimena Guallar-Blasco, Yi Zhou, Benjamin Van Durme* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2211.07516)][[Github](https://github.com/esteng/ambiguous_vqa)] \
14 Nov 2022 


**Abg-CoQA: Clarifying Ambiguity in Conversational Question Answering** \
*Meiqi Guo, Mingda Zhang, Siva Reddy, Malihe Alikhani* \
AKBC 2021. [[Paper](https://openreview.net/forum?id=SlDZ1o8FsJU)] \
22 Jun 2021 


### Confidence 

**What Are the Different Approaches for Detecting Content Generated by LLMs Such As ChatGPT? And How Do They Work and Differ?** \
*Sebastian Raschka* \
[[Link](https://sebastianraschka.com/blog/2023/detect-ai.html)] [[GPTZero](https://gptzero.me/)] \
1 Feb 2023 

**DetectGPT: Zero-Shot Machine-Generated Text Detection using Probability Curvature** \
*Eric Mitchell, Yoonho Lee, Alexander Khazatsky, Christopher D. Manning, Chelsea Finn* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2301.11305v1)][[Website](https://ericmitchell.ai/detectgpt/)] \
26 Jan 2023 

**Confident Adaptive Language Modeling** \
*Tal Schuster, Adam Fisch, Jai Gupta, Mostafa Dehghani, Dara Bahri, Vinh Q. Tran, Yi Tay, Donald Metzler* \
NeurIPS 2022. [[Paper](https://arxiv.org/abs/2207.07061)]
25 Oct 2022 


**Conformal risk control** \
*Anastasios N Angelopoulos, Stephen Bates, Adam Fisch, Lihua Lei, Tal Schuster* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2208.02814)][[Github](https://github.com/aangelopoulos/conformal-risk)] \
4 Aug 2022 


### Active Learning 
<!-- > https://github.com/baifanxxx/awesome-active-learning/blob/main/README.md -->


**A Survey of Active Learning for Natural Language Processing** \
*Zhisong Zhang, Emma Strubell, Eduard Hovy* \
EMNLP 2022. [[Paper](https://arxiv.org/abs/2210.10109)][[Github](https://github.com/zzsfornlp/zmsp)] \
18 Oct 2022 


**Active Prompting with Chain-of-Thought for Large Language Models** \
*Shizhe Diao, Pengcheng Wang, Yong Lin, Tong Zhang* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2302.12246)][[Github](https://github.com/shizhediao/active-prompt)] \
23 Feb 2023 


**Low-resource Interactive Active Labeling for Fine-tuning Language Models** \
*Seiji Maekawa, Dan Zhang, Hannah Kim, Sajjadur Rahman, Estevam Hruschka* \
EMNLP Findings 2022. [[Paper](https://aclanthology.org/2022.findings-emnlp.235/)] \
7 Dec 2022 

**Can You Label Less by Using Out-of-Domain Data? Active & Transfer Learning with Few-shot Instructions** \
*Rafal Kocielnik, Sara Kangaslahti, Shrimai Prabhumoye, Meena Hari, R. Michael Alvarez, Anima Anandkumar* \
NeurIPS Workshop 2022. [[Paper](https://arxiv.org/abs/2211.11798)] \
21 Nov 2022 


**AfroLM: A Self-Active Learning-based Multilingual Pretrained Language Model for 23 African Languages** \
*Bonaventure F. P. Dossou, Atnafu Lambebo Tonja, Oreen Yousuf, Salomey Osei, Abigail Oppong, Iyanuoluwa Shode, Oluwabusayo Olufunke Awoyomi, Chris Chinenye Emezue* \
EMNLP 2022. [[Paper](https://arxiv.org/abs/2211.03263)][[Github](https://github.com/bonaventuredossou/mlm_al)] \
7 Nov 2022 

**Active Learning Helps Pretrained Models Learn the Intended Task** \
*Alex Tamkin, Dat Pham Nguyen, Salil Deshpande, Jesse Mu, Noah Goodman* \
NeurIPS 2022. [[Paper](https://openreview.net/forum?id=0Ww7UVEoNue)][[Github](https://github.com/alextamkin/active-learning-pretrained-models)] \
31 Oct 2022 

**Selective Annotation Makes Language Models Better Few-Shot Learners** \
*Hongjin Su, Jungo Kasai, Chen Henry Wu, Weijia Shi, Tianlu Wang, Jiayi Xin, Rui Zhang, Mari Ostendorf, Luke Zettlemoyer, Noah A. Smith, Tao Yu* \
ICLR 2023. [[Paper](https://arxiv.org/abs/2209.01975)][[Github](https://github.com/hkunlp/icl-selective-annotation)] \
5 Sep 2022 


**Multi-task Active Learning for Pre-trained Transformer-based Models** \
*Guy Rotman, Roi Reichart* \
TACL 2022. [[Paper](https://arxiv.org/abs/2208.05379)] [[Github](https://github.com/rotmanguy/mtal)]\
10 Aug 2022
 
**AcTune: Uncertainty-Based Active Self-Training for Active Fine-Tuning of Pretrained Language Models** \
*Yue Yu, Lingkai Kong, Jieyu Zhang, Rongzhi Zhang, Chao Zhang* \
NAACL-HLT2022. [[Paper](https://aclanthology.org/2022.naacl-main.102/)] [[Github](https://github.com/yueyu1030/actune)]\
10 Jul 2022 

**Towards Computationally Feasible Deep Active Learning** \
*Akim Tsvigun, Artem Shelmanov, Gleb Kuzmin, Leonid Sanochkin, Daniil Larionov, Gleb Gusev, Manvel Avetisian, Leonid Zhukov* \
NAACL 2022. [[Paper](https://arxiv.org/abs/2205.03598)] [[Github](https://github.com/airi-institute/al_nlp_feasible)] \
7 May 2022 

**FAMIE: A Fast Active Learning Framework for Multilingual Information Extraction** \
*Minh Van Nguyen, Nghia Trung Ngo, Bonan Min, Thien Huu Nguyen* \
NAACL 2022. [[Paper](https://arxiv.org/abs/2202.08316)] [[Github](https://github.com/nlp-uoregon/famie)] \
16 Feb 2022 


**On the Importance of Effectively Adapting Pretrained Language Models for Active Learning** \
*Katerina Margatina, Loïc Barrault, Nikolaos Aletras* \
ACL 2022. [[Paper](https://arxiv.org/abs/2104.08320v2)] \
2 Mar 2022 

**Limitations of Active Learning With Deep Transformer Language Models** \
*Mike D'Arcy, Doug Downey* \
Arxiv 2022. [[Paper](https://openreview.net/forum?id=Q8OjAGkxwP5)] \
28 Jan 2022 

**Active Learning by Acquiring Contrastive Examples** \
*Katerina Margatina, Giorgos Vernikos, Loïc Barrault, Nikolaos Aletras* \
EMNLP 2021. [[Paper](https://arxiv.org/abs/2109.03764)][[Github](https://github.com/mourga/contrastive-active-learning)] \
8 Sep 2021


**Revisiting Uncertainty-based Query Strategies for Active Learning with Transformers** \
*Christopher Schröder, Andreas Niekler, Martin Potthast* \
ACL 2022 Findings. [[Paper](https://arxiv.org/abs/2107.05687)][[Github](https://github.com/webis-de/acl22-revisiting-uncertainty-based-query-strategies-for-active-learning-with-transformers)]  \
12 Jul 2021 

**Active Learning for Sequence Tagging with Deep Pre-trained Models and Bayesian Uncertainty Estimates** \
*Artem Shelmanov, Dmitri Puzyrev, Lyubov Kupriyanova, Denis Belyakov, Daniil Larionov, Nikita Khromov, Olga Kozlova, Ekaterina Artemova, Dmitry V. Dylov, Alexander Panchenko* \
EACL 2021. [[Paper](https://arxiv.org/abs/2101.08133)] \
18 Feb 2021 

**Fine-tuning BERT for Low-Resource Natural Language Understanding via Active Learning** \
*Daniel Grießhaber, Johannes Maucher, Ngoc Thang Vu* \
COLING 2020. [[Paper](https://arxiv.org/abs/2012.02462)] \
4 Dec 2020


## Reliability


### Hallucination

**Do Language Models Know When They're Hallucinating References?** \
*Ayush Agrawal, Lester Mackey, Adam Tauman Kalai* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2305.18248)] \
29 May 2023. 

**Self-contradictory Hallucinations of Large Language Models: Evaluation, Detection and Mitigation** \
*Niels Mündler, Jingxuan He, Slobodan Jenko, Martin Vechev* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2305.15852)] \
25 May 2023 

**Why Does ChatGPT Fall Short in Providing Truthful Answers?** \
*Shen Zheng, Jie Huang, Kevin Chen-Chuan Chang* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2304.10513)] \
24 May 2023 
 

**How Language Model Hallucinations Can Snowball** \
*Muru Zhang, Ofir Press, William Merrill, Alisa Liu, Noah A. Smith* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2305.13534)] \
22 May 2023 

**LM vs LM: Detecting Factual Errors via Cross Examination** \
*Roi Cohen, May Hamri, Mor Geva, Amir Globerson* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2305.13281)] \
22 May 2023


**HaluEval: A Large-Scale Hallucination Evaluation Benchmark for Large Language Models** \
*Junyi Li, Xiaoxue Cheng, Wayne Xin Zhao, Jian-Yun Nie, Ji-Rong Wen* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2305.11747)] 
19 May 2023 

**SelfCheckGPT: Zero-Resource Black-Box Hallucination Detection for Generative Large Language Models** \
*Potsawee Manakul, Adian Liusie, Mark J. F. Gales* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2303.08896)] [[Github](https://github.com/potsawee/selfcheckgpt)] \
8 Mar 2023 

**Check Your Facts and Try Again: Improving Large Language Models with External Knowledge and Automated Feedback** \
*Baolin Peng, Michel Galley, Pengcheng He, Hao Cheng, Yujia Xie, Yu Hu, Qiuyuan Huang, Lars Liden, Zhou Yu, Weizhu Chen, Jianfeng Gao* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2302.12813)] \
23 Feb 2023 
 

**RHO (ρ): Reducing Hallucination in Open-domain Dialogues with Knowledge Grounding** \
*Ziwei Ji, Zihan Liu, Nayeon Lee, Tiezheng Yu, Bryan Wilie, Min Zeng, Pascale Fung* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2212.01588)] \
3 Dec 2022 


**FaithDial: A Faithful Benchmark for Information-Seeking Dialogue** \
*Nouha Dziri, Ehsan Kamalloo, Sivan Milton, Osmar Zaiane, Mo Yu, Edoardo M. Ponti, Siva Reddy* \
TACL 2022. [[Paper](https://arxiv.org/abs/2204.10757)] \
22 Apr 2022 


**Survey of Hallucination in Natural Language Generation** \
*Ziwei Ji, Nayeon Lee, Rita Frieske, Tiezheng Yu, Dan Su, Yan Xu, Etsuko Ishii, Yejin Bang, Wenliang Dai, Andrea Madotto, Pascale Fung* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2202.03629)] \
8 Feb 2022


### Truthfulness 

**Inference-Time Intervention: Eliciting Truthful Answers from a Language Model** \ 
*Kenneth Li, Oam Patel, Fernanda Viégas, Hanspeter Pfister, Martin Wattenberg* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2306.03341)] [[Github](https://github.com/likenneth/honest_llama)] \
6 June 2023 



**The Internal State of an LLM Knows When its Lying** \
*Amos Azaria, Tom Mitchell* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2304.13734)] \
26 Apr 2023 


**TruthfulQA: Measuring How Models Mimic Human Falsehoods** \
*Stephanie Lin, Jacob Hilton, Owain Evans* \
ACL 2022. [[Paper](https://arxiv.org/abs/2109.07958)] [[Github](https://github.com/sylinrl/TruthfulQA)] [[Blog](https://www.lesswrong.com/posts/PF58wEdztZFX2dSue/how-truthful-is-gpt-3-a-benchmark-for-language-models)] \
8 Sep 2021

**Truthful AI: Developing and governing AI that does not lie** \
*Owain Evans, Owen Cotton-Barratt, Lukas Finnveden, Adam Bales, Avital Balwit, Peter Wills, Luca Righetti, William Saunders* \
arXiv 2021. [[Paper](https://arxiv.org/abs/2110.06674)] [[Blog](https://www.lesswrong.com/posts/aBixCPqSnTsPsTJBQ/truthful-ai-developing-and-governing-ai-that-does-not-lie)]\
13 Oct 2021


**Measuring Reliability of Large Language Models through Semantic Consistency** \
*Harsh Raj, Domenic Rosati, Subhabrata Majumdar* \
NeurIPS 2022 ML Safety Workshop. [[Paper](https://arxiv.org/abs/2211.05853)] \
10 Nov 2022 

### Reasoning 

**REFINER: Reasoning Feedback on Intermediate Representations** \
*Debjit Paul, Mete Ismayilzada, Maxime Peyrard, Beatriz Borges, Antoine Bosselut, Robert West, Boi Faltings* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2304.01904)] \
4 Apr 2023 

**OpenICL: An Open-Source Framework for In-context Learning** \
*Zhenyu Wu, YaoXiang Wang, Jiacheng Ye, Jiangtao Feng, Jingjing Xu, Yu Qiao, Zhiyong Wu* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2303.02913)] [[Github](https://github.com/shark-nlp/openicl)] \
6 Mar 2023 

**Reliable Natural Language Understanding with Large Language Models and Answer Set Programming** \
*Abhiramon Rajasekharan, Yankai Zeng, Parth Padalkar, Gopal Gupta* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2302.03780)] \
7 Feb 2023 

**Self-Consistency Improves Chain of Thought Reasoning in Language Models** \
*Xuezhi Wang, Jason Wei, Dale Schuurmans, Quoc Le, Ed Chi, Sharan Narang, Aakanksha Chowdhery, Denny Zhou* \
ICLR 2023. [[Paper](https://arxiv.org/abs/2203.11171)] \
21 Mar 2022 

**Chain of Thought Prompting Elicits Reasoning in Large Language Models.** \
*Jason Wei, Xuezhi Wang, Dale Schuurmans, Maarten Bosma, Ed Chi, Quoc Le, Denny Zhou*\
arXiv 2022. [[Paper](https://arxiv.org/abs/2201.11903)] \
28 Jan 2022 

**STaR: Self-Taught Reasoner Bootstrapping Reasoning With Reasoning.** \
*Eric Zelikman, Yuhuai Wu, Noah D. Goodman* \
NeurIPS 2022. [[Paper](https://arxiv.org/abs/2203.14465)][[Github](https://github.com/ezelikman/STaR)] \
28 Mar 2022 


**The Unreliability of Explanations in Few-shot Prompting for Textual Reasoning** \
*Xi Ye, Greg Durrett* \
NeurIPS 2022. [[Paper](https://arxiv.org/abs/2205.03401)] [[Github](https://github.com/xiye17/TextualExplInContext)]\
6 May 2022


**Rationale-Augmented Ensembles in Language Models** \
*Xuezhi Wang, Jason Wei, Dale Schuurmans, Quoc Le, Ed Chi, Denny Zhou*\
arXiv 2022. [[Paper](https://arxiv.org/abs/2207.00747)] \
2 Jul 2022

**ReAct: Synergizing Reasoning and Acting in Language Models** \
*Shunyu Yao, Jeffrey Zhao, Dian Yu, Nan Du, Izhak Shafran, Karthik Narasimhan, Yuan Cao* \
ICLR 2023. [[Paper](https://arxiv.org/abs/2210.03629)][[Github](https://github.com/ysymyth/ReAct)] [[Project](https://react-lm.github.io/)] \
6 Oct 2022 

**On Second Thought, Let's Not Think Step by Step! Bias and Toxicity in Zero-Shot Reasoning** \
*Omar Shaikh, Hongxin Zhang, William Held, Michael Bernstein, Diyi Yang* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2212.08061)] \
15 Dec 2022 

**On the Advance of Making Language Models Better Reasoners** \
*Yifei Li, Zeqi Lin, Shizhuo Zhang, Qiang Fu, Bei Chen, Jian-Guang Lou, Weizhu Chen* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2206.02336)][[Github](https://github.com/microsoft/CodeT)] \
6 Jun 2022 

**Ask Me Anything: A simple strategy for prompting language models** \
*Simran Arora, Avanika Narayan, Mayee F. Chen, Laurel Orr, Neel Guha, Kush Bhatia, Ines Chami, Frederic Sala, Christopher Ré*\
arXiv 2022. [[Paper](https://arxiv.org/abs/2210.02441)][[Github](https://github.com/HazyResearch/ama_prompting)] \
5 Oct 2022 

**MathPrompter: Mathematical Reasoning using Large Language Models** \
*Shima Imani, Liang Du, Harsh Shrivastava* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2303.05398)] \
4 Mar 2023

**Complexity-Based Prompting for Multi-Step Reasoning** \
*Yao Fu, Hao Peng, Ashish Sabharwal, Peter Clark, Tushar Khot* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2210.00720)][[Github](https://github.com/FranxYao/Complexity-Based-Prompting)]\
3 Oct 2022 

**Measuring and Narrowing the Compositionality Gap in Language Models**\
*Ofir Press, Muru Zhang, Sewon Min, Ludwig Schmidt, Noah A. Smith, Mike Lewis*\
arXiv 2022. [[Paper](https://arxiv.org/abs/2210.03350)][[Github](https://github.com/ofirpress/self-ask)] 
7 Oct 2022 

**Interleaving Retrieval with Chain-of-Thought Reasoning for Knowledge-Intensive Multi-Step Questions** \
*Harsh Trivedi, Niranjan Balasubramanian, Tushar Khot, Ashish Sabharwal* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2212.10509)][[Github](https://github.com/StonyBrookNLP/ircot)] \
20 Dec 2022 


### Prompt tuning, optimization and design

<!-- **Your Prompt is My Command** -->

**Promptboosting: Black-box text classification with ten forward passes** \
*Bairu Hou, Joe O’Connor, Jacob Andreas, Shiyu Chang, Yang Zhang* \
ICML 2023. [[Paper](https://proceedings.mlr.press/v202/hou23b.html)][[Github](https://github.com/UCSB-NLP-Chang/PromptBoosting)] \
23 Jan 2023 

**GrIPS: Gradient-free, Edit-based Instruction Search for Prompting Large Language Models** \
*Archiki Prasad, Peter Hase, Xiang Zhou, Mohit Bansal* \
EACL 2023. [[Paper](https://arxiv.org/abs/2203.07281)][[Github](https://github.com/archiki/grips)] \
Mar 14 2022 

**RLPrompt: Optimizing Discrete Text Prompts with Reinforcement Learning** \
*Mingkai Deng, Jianyu Wang, Cheng-Ping Hsieh, Yihan Wang, Han Guo, Tianmin Shu, Meng Song, Eric P. Xing, Zhiting Hu* \
EMNLP 2022. [[Paper](https://arxiv.org/abs/2205.12548)][[Github](https://github.com/mingkaid/rl-prompt)] \
25 May 2022 

**Black-box Prompt Learning for Pre-trained Language Models** \
*Shizhe Diao, Zhichao Huang, Ruijia Xu, Xuechun Li, Yong Lin, Xiao Zhou, Tong Zhang* \
TMLR 2023. [[Paper](https://arxiv.org/abs/2201.08531)][[Github](https://github.com/shizhediao/Black-Box-Prompt-Learning)] \
22 Jan 2022 

**Black-Box Tuning for Language-Model-as-a-Service** \
*Tianxiang Sun, Yunfan Shao, Hong Qian, Xuanjing Huang, Xipeng Qiu* \
ICML 2022. [[Paper](https://arxiv.org/abs/2201.03514)][[Github](https://github.com/txsun1997/Black-Box-Tuning)]\
10 Jan 2022 

**BBTv2: towards a gradient-free future with large language models** \
*Tianxiang Sun, Zhengfu He, Hong Qian, Yunhua Zhou, Xuanjing Huang, Xipeng Qiu* \ 
EMNLP 2022. [[Paper](https://aclanthology.org/2022.emnlp-main.259/)] [[Github](https://github.com/txsun1997/Black-Box-Tuning)] \
7 Dec 2022 


**Automatic Chain of Thought Prompting in Large Language Models** \
*Zhuosheng Zhang, Aston Zhang, Mu Li, Alex Smola*\
ICLR 2023. [[Paper](https://arxiv.org/abs/2210.03493)][[Github](https://github.com/amazon-science/auto-cot)]\
7 Oct 2022

**Automatic Prompt Augmentation and Selection with Chain-of-Thought from Labeled Data** \
*KaShun Shum, Shizhe Diao, Tong Zhang*\
arXiv 2023. [[Paper](https://arxiv.org/abs/2302.12822)][[Github](https://github.com/shizhediao/automate-cot)]\
24 Feb 2023 

**Large Language Models Are Human-Level Prompt Engineers** \
*Yongchao Zhou, Andrei Ioan Muresanu, Ziwen Han, Keiran Paster, Silviu Pitis, Harris Chan, Jimmy Ba* \
ICLR 2023. [[Paper](https://arxiv.org/abs/2211.01910)] [[Github](https://github.com/keirp/automatic_prompt_engineer)] \
3 Nov 2022 

**Fantastically Ordered Prompts and Where to Find Them: Overcoming Few-Shot Prompt Order Sensitivity** \
*Yao Lu, Max Bartolo, Alastair Moore, Sebastian Riedel, Pontus Stenetorp* \
ACL 2022. [[Paper](https://arxiv.org/abs/2104.08786)] 

**Active Example Selection for In-Context Learning** \
*Yiming Zhang, Shi Feng, Chenhao Tan* \
EMNLP 2022. [[Paper](https://arxiv.org/abs/2211.04486)][[Github](https://github.com/ChicagoHAI/active-example-selection)] \
8 Nov 2022 

**Selective Annotation Makes Language Models Better Few-Shot Learners** \
*Hongjin Su, Jungo Kasai, Chen Henry Wu, Weijia Shi, Tianlu Wang, Jiayi Xin, Rui Zhang, Mari Ostendorf, Luke Zettlemoyer, Noah A. Smith, Tao Yu* \
ICLR 2023. [[Paper](https://arxiv.org/abs/2209.01975)][[Github](https://github.com/HKUNLP/icl-selective-annotation)]\
5 Sep 2022 

**Learning To Retrieve Prompts for In-Context Learning** \
*Ohad Rubin, Jonathan Herzig, Jonathan Berant* \
NAACL-HLT 2022. [[Paper](https://arxiv.org/abs/2112.08633)][[Github](https://github.com/OhadRubin/EPR)] \
16 Dec 2021


### Instruction and RLHF 

**LaMini-LM: A Diverse Herd of Distilled Models from Large-Scale Instructions** \
*Minghao Wu, Abdul Waheed, Chiyu Zhang, Muhammad Abdul-Mageed, Alham Fikri Aji* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2304.14402)][[Github](https://github.com/mbzuai-nlp/lamini-lm)] \
27 Apr 2023 

**Self-Refine: Iterative Refinement with Self-Feedback** \
*Aman Madaan, Niket Tandon, Prakhar Gupta, Skyler Hallinan, Luyu Gao, Sarah Wiegreffe, Uri Alon, Nouha Dziri, Shrimai Prabhumoye, Yiming Yang, Sean Welleck, Bodhisattwa Prasad Majumder, Shashank Gupta, Amir Yazdanbakhsh, Peter Clark* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2303.17651)][[Github](https://github.com/madaan/self-refine)] [[Website](https://selfrefine.info/)] \
30 Mar 2023 


**Is Prompt All You Need? No. A Comprehensive and Broader View of Instruction Learning** \
*Renze Lou, Kai Zhang, Wenpeng Yin* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2303.10475)][[Github](https://github.com/RenzeLou/awesome-instruction-learning)] \
18 Mar 2023  

**Self-Instruct: Aligning Language Model with Self Generated Instructions** \
*Yizhong Wang, Yeganeh Kordi, Swaroop Mishra, Alisa Liu, Noah A. Smith, Daniel Khashabi, Hannaneh Hajishirzi* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2212.10560)] [[Github](https://github.com/yizhongw/self-instruct)] \
20 Dec 2022 


**Constitutional AI: Harmlessness from AI Feedback** \
*Yuntao Bai, et al (Anthropic)* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2212.08073)] \
15 Dec 2022 

**Discovering Language Model Behaviors with Model-Written Evaluations** \
*Ethan Perez et al.* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2212.09251)] \
19 Dec 2022 

**In-Context Instruction Learning** \
*Seonghyeon Ye, Hyeonbin Hwang, Sohee Yang, Hyeongu Yun, Yireun Kim, Minjoon Seo* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2302.14691)][[Github](https://github.com/seonghyeonye/ICIL)]\
28 Feb 2023 


### Tools and external APIs

**Internet-augmented language models through few-shot prompting for open-domain question answering**  \
*Angeliki Lazaridou, Elena Gribovskaya, Wojciech Stokowiec, Nikolai Grigorev* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2203.05115)] \
10 Mar 2023 

**Program of Thoughts Prompting: Disentangling Computation from Reasoning for Numerical Reasoning Tasks** \
*Wenhu Chen, Xueguang Ma, Xinyi Wang, William W. Cohen* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2211.12588)][[Github](https://github.com/wenhuchen/Program-of-Thoughts)]\
22 Nov 2022 

**PAL: Program-aided Language Models** \
*Luyu Gao, Aman Madaan, Shuyan Zhou, Uri Alon, Pengfei Liu, Yiming Yang, Jamie Callan, Graham Neubig* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2211.10435)] [[Github](https://github.com/reasoning-machines/pal)] [[Project](https://reasonwithpal.com/)] \
18 Nov 2022 

**TALM: Tool Augmented Language Models** \
*Aaron Parisi, Yao Zhao, Noah Fiedel* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2205.12255)] \
24 May 2022 

**Toolformer: Language Models Can Teach Themselves to Use Tool** \
*Timo Schick, Jane Dwivedi-Yu, Roberto Dessì, Roberta Raileanu, Maria Lomeli, Luke Zettlemoyer, Nicola Cancedda, Thomas Scialom* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2302.04761)] \
9 Feb 2023 


### Fine-tuning 

**Distilling Step-by-Step! Outperforming Larger Language Models with Less Training Data and Smaller Model Sizes** \
*Cheng-Yu Hsieh, Chun-Liang Li, Chih-Kuan Yeh, Hootan Nakhost, Yasuhisa Fujii, Alexander Ratner, Ranjay Krishna, Chen-Yu Lee, Tomas Pfister* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2305.02301)] \
3 May 2023 

<!-- https://github.com/shm007g/LLaMA-Cult-and-More -->
**FreeLM: Fine-Tuning-Free Language Model** \
*Xiang Li1, Xin Jiang, Xuying Meng, Aixin Sun, Yequan Wang* \
arXiv 2023. [[Paper](https://arxiv.org/pdf/2305.01616v1.pdf)] \
2 May 2023 


## Robustness
### Invariance 

**Invariant Language Modeling** \ 
*Maxime Peyrard, Sarvjeet Singh Ghotra, Martin Josifoski, Vidhan Agarwal, Barun Patra, Dean Carignan, Emre Kiciman, Robert West* \
EMNLP 2022. [[Paper](https://arxiv.org/abs/2110.08413)][[Github](https://github.com/epfl-dlab/invariant-language-models)] \
16 Oct 2021 


### Distribution Shift

**Exploring Distributional Shifts in Large Language Models for Code Analysis** \
*Shushan Arakelyan, Rocktim Jyoti Das, Yi Mao, Xiang Ren* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2303.09128)] \
16 Mar 2023 


### Out-of-Distribution 

**Out-of-Distribution Detection and Selective Generation for Conditional Language Models** \
*Jie Ren, Jiaming Luo, Yao Zhao, Kundan Krishna, Mohammad Saleh, Balaji Lakshminarayanan, Peter J. Liu* \
ICLR 2023. [[Paper](https://arxiv.org/abs/2209.15558)] \
30 Sep 2022 


### Adaptation and Generalization

**On the Domain Adaptation and Generalization of Pretrained Language Models: A Survey** \
*Xu Guo, Han Yu* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2211.03154)] \
6 Nov 2022 

### Adversarial 

**On the Robustness of ChatGPT: An Adversarial and Out-of-distribution Perspective** \
*Jindong Wang, Xixu Hu, Wenxin Hou, Hao Chen, Runkai Zheng, Yidong Wang, Linyi Yang, Haojun Huang, Wei Ye, Xiubo Geng, Binxin Jiao, Yue Zhang, Xing Xie* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2302.12095)] [[Github](https://github.com/microsoft/robustlearn)] \
22 Feb 2023 

**Reliability Testing for Natural Language Processing Systems** \
*Samson Tan, Shafiq Joty, Kathy Baxter, Araz Taeihagh, Gregory A. Bennett, Min-Yen Kan* \
ACL-IJCNLP 2021. [[Paper](https://arxiv.org/abs/2105.02590)] \
06 May 2021


### Attribution 

**Attributed Question Answering: Evaluation and Modeling for Attributed Large Language Models** \
*Bernd Bohnet, Vinh Q. Tran, Pat Verga, Roee Aharoni, Daniel Andor, Livio Baldini Soares, Massimiliano Ciaramita, Jacob Eisenstein, Kuzman Ganchev, Jonathan Herzig, Kai Hui, Tom Kwiatkowski, Ji Ma, Jianmo Ni, Lierni Sestorain Saralegui, Tal Schuster, William W. Cohen, Michael Collins, Dipanjan Das, Donald Metzler, Slav Petrov, Kellie Webster* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2212.08037)] \
15 Dec 2022 

### Causality 

**Can Large Language Models Infer Causation from Correlation?** \
*Zhijing Jin, Jiarui Liu, Zhiheng Lyu, Spencer Poff, Mrinmaya Sachan, Rada Mihalcea, Mona Diab, Bernhard Schölkopf* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2306.05836)] [[Github](https://github.com/causalnlp/corr2cause)] \
9 Jun 2023 


**Selection-Inference: Exploiting Large Language Models for Interpretable Logical Reasoning** \
*Antonia Creswell, Murray Shanahan, Irina Higgins* \
ICLR 2023. [[Paper](https://arxiv.org/abs/2205.09712)] \
19 May 2022

**Investigating causal understanding in LLMs** \
*Marius Hobbhahn, Tom Lieberum, David Seiler* \
NeurIPS 2022 Workshop. [[Paper](https://openreview.net/forum?id=st6jtGdW8Ke)][[Blog](https://www.lesswrong.com/posts/yZb5eFvDoaqB337X5/investigating-causal-understanding-in-llms)] \
3 Oct 2022 


<!-- blog https://zhuanlan.zhihu.com/p/608856445  -->

<!-- > new metric to evaluate the prompt  -->



<!-- ## Safety

### Bias and Fairness
> more papers can be found via https://github.com/uclanlp/awesome-fairness-papers 

**Logic Against Bias: Textual Entailment Mitigates Stereotypical Sentence Reasoning** \
*Hongyin Luo, James Glass* \ 
EACL 2023. [[Paper](https://arxiv.org/abs/2303.05670)] [[News][https://news.mit.edu/2023/large-language-models-are-biased-can-logic-help-save-them-0303]] \
10 Mar 2023 

**Measuring Fairness with Biased Rulers: A Survey on Quantifying Biases in Pretrained Language Models** \
*Pieter Delobelle, Ewoenam Kwaku Tokpo, Toon Calders, Bettina Berendt* \
arXiv 2021. [[Paper](https://arxiv.org/abs/2112.07447)] \
14 Dec 2021 

**Towards Understanding and Mitigating Social Biases in Language Models** \ 
*Paul Pu Liang, Chiyu Wu, Louis-Philippe Morency, Ruslan Salakhutdinov* \
ICML 2021. [[Paper](https://arxiv.org/abs/2106.13219)] [[Github](https://github.com/pliang279/LM_bias)] \
24 Jun 2021 

**Fairness-guided Few-shot Prompting for Large Language Models** \
*Huan Ma, Changqing Zhang, Yatao Bian, Lemao Liu, Zhirui Zhang, Peilin Zhao, Shu Zhang, Huazhu Fu, Qinghua Hu, Bingzhe Wu* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2303.13217)] [[Github](https://github.com/MaHuanAAA/g_fair_prompting)]\
23 Mar 2023

<!-- improve in-context learning  -->






<!-- # Research Team & Reseachers 

- [Owain Evans](https://owainevans.github.io/): Research Associate in Artificial Intelligence, University of Oxford
- [Tong Zhang]
 -->
 <!-- - [Sebastian Farquhar](https://sebastianfarquhar.com/): Deepmind, Oxford  -->
 <!-- [Elias Stengel-Eskin](https://esteng.github.io/) -->

