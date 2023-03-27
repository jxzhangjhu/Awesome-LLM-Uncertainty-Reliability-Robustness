# Awesome-LLM-Reliability-Robustness-Safety
<!-- Awesome-LLM-Robustness: a curated list of Robustness, Reliability and Safety in Large Language Models -->

\
[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/hee9joon/Awesome-Diffusion-Models) 
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Made With Love](https://img.shields.io/badge/Made%20With-Love-red.svg)](https://github.com/chetanraj/awesome-github-badges)

This repository contains a collection of resources and papers on **Reliability**, **Robustness**  and **Safety** in **Large Language Models (LLMs)**.

"*Large language models have limited reliability, limited understanding, limited range, and hence need human supervision*. " - Michael Osborne, Professor of Machine Learning in the Dept. of Engineering Science, University of Oxford, January 25, 2023 

<!-- ## Contents
- [Resources](#resources)
  - [Introductory Posts](#introductory-posts)
  - [Introductory Papers](#introductory-papers)
  - [Introductory Videos](#introductory-videos)
  - [Introductory Lectures](#introductory-lectures)
  - [Tutorial and Jupyter Notebook](#tutorial-and-jupyter-notebook)

- [Papers](#papers)
  - [Survey](#survey)
  - [Reliability](#reliability)
    - [Generation](#generation)
    - [Segmentation](#segmentation)
  - [Robustness](#robustness)
    - [Generation](#generation-1)
    - [Conversion](#conversion)

 -->

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



# Papers

## Evaluation & Survey

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




## Reliability

### Uncertainty

**Teaching Models to Express Their Uncertainty in Words** \
*Stephanie Lin, Jacob Hilton, Owain Evans* \
TMLR 2022. [[Paper](https://arxiv.org/abs/2205.14334)] [[Github](https://github.com/sylinrl/CalibratedMath)] [[TMLR](https://openreview.net/forum?id=8s8K2UZGTZ)] [[Slide](https://owainevans.github.io/pdfs/chai_calibration_owain.pdf)]\
28 May 2022

**Semantic Uncertainty: Linguistic Invariances for Uncertainty Estimation in Natural Language Generation** \
*Lorenz Kuhn, Yarin Gal, Sebastian Farquhar* \
ICLR 2023. [[Paper](https://arxiv.org/abs/2302.09664)] \
19 Feb 2022

**Active Prompting with Chain-of-Thought for Large Language Models** \
*Shizhe Diao, Pengcheng Wang, Yong Lin, Tong Zhang* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2302.12246)][[Github](https://github.com/shizhediao/active-prompt)] \
23 Feb 2023 


### Calibration

**Calibrating Sequence likelihood Improves Conditional Language Generation** \
*Yao Zhao, Misha Khalman, Rishabh Joshi, Shashi Narayan, Mohammad Saleh, Peter J. Liu* \
ICLR 2023. [[Paper](https://arxiv.org/abs/2210.00045)]\
30 Sep 2022



### Ambiguity 

**CLAM: Selective Clarification for Ambiguous Questions with Generative Language Models** \
*Lorenz Kuhn, Yarin Gal, Sebastian Farquhar* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2303.09508)] \
15 Dec 2022


### Hallucination

**Survey of Hallucination in Natural Language Generation** \
*Ziwei Ji, Nayeon Lee, Rita Frieske, Tiezheng Yu, Dan Su, Yan Xu, Etsuko Ishii, Yejin Bang, Wenliang Dai, Andrea Madotto, Pascale Fung* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2202.03629)] \
8 Feb 2022


### Truthful 

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

**Reliable Natural Language Understanding with Large Language Models and Answer Set Programming** \
*Abhiramon Rajasekharan, Yankai Zeng, Parth Padalkar, Gopal Gupta* \
arXiv 2023. [[Paper](https://arxiv.org/abs/2302.03780)] \
7 Feb 2023 


## Robustness
### Invariance


### Distribution Shift

### Out-of-Distribution 

**Out-of-Distribution Detection and Selective Generation for Conditional Language Models** \
*Jie Ren, Jiaming Luo, Yao Zhao, Kundan Krishna, Mohammad Saleh, Balaji Lakshminarayanan, Peter J. Liu* \
ICLR 2023. [[Paper](https://arxiv.org/abs/2209.15558)] \
30 Sep 2022 


### Generalization

### Adversarial 

**Reliability Testing for Natural Language Processing Systems** \
*Samson Tan, Shafiq Joty, Kathy Baxter, Araz Taeihagh, Gregory A. Bennett, Min-Yen Kan* \
ACL-IJCNLP 2021. [[Paper](https://arxiv.org/abs/2105.02590)] \
06 May 2021

<!-- > new metric to evaluate the prompt  -->



## Safety

### Bias

### Fairness

### Privacy




<!-- # Research Team & Reseachers 

- [Owain Evans](https://owainevans.github.io/): Research Associate in Artificial Intelligence, University of Oxford
 -->

