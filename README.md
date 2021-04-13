# Paper List for Open-eNded Language Generation (ONLG)

![](https://img.shields.io/github/last-commit/thu-coai/PaperForONLG?color=blue) ![](https://img.shields.io/badge/PaperNumber-130-brightgreen) ![](https://img.shields.io/badge/PRs-Welcome-red) 

Contributed by [Jian Guan](https://jianguanthu.github.io/), [Zhexin Zhang](https://github.com/nonstopfor), [Zhuoer Feng](https://github.com/ZhuoerFeng)

### Introduction

**O**pen-e**N**ded **L**anguage **G**eneration (ONLG) refers to those generation tasks where only very limited information is given in the input and there are many plausible output for the same input (also known as one-to-many). ONLG roughly includes chit-chat dialog/story/review/essay generation, etc.





### Some active authors in the list

[Minlie Huang](http://coai.cs.tsinghua.edu.cn/hml/), [Stephen Roller](https://stephenroller.com/), [Nanyun Peng](https://violetpeng.github.io//), [Jianfeng Gao](https://www.microsoft.com/en-us/research/people/jfgao/?from=http%3A%2F%2Fresearch.microsoft.com%2Fen-us%2Fum%2Fpeople%2Fjfgao%2F), [Joelle Pineau](https://scholar.google.com/citations?user=CEt6_mMAAAAJ&hl=zh-CN), [Angela Fan](https://ai.facebook.com/people/angela-fan/), [Jason Weston](http://www.thespermwhale.com/jaseweston/), [Ryan Lowe](https://scholar.google.ca/citations?user=iRgYMuEAAAAJ&hl=en), [Noah A. Smith](https://homes.cs.washington.edu/~nasmith/)...



### Contents

* [0. Resource](#0-resource)
* [1. Survey](#1-survey)
* [2. Generative Model](#2-generative-model)
  * [2.1 Story](#21-story)
  * [2.2 Dialog](#22-dialog) 
  * [2.3 Others](#23-others)
* [3. Evaluation](#3-evaluation)
  * [3.1 Metric](#31-metric)
  * [3.2 Protocol](#32-protocol-for-human-evaluation)
* [4. Others](#4-others)



## 0. Resource

1. BLiMP: The Benchmark of Linguistic Minimal Pairs for English. Alex Warstadt, Alicia Parrish, Haokun Liu, Anhad Mohananey, Wei Peng, Sheng-FuWang, Samuel R. Bowman. `TACL 2020` [[pdf]](https://arxiv.org/abs/1912.00582) ![](https://img.shields.io/badge/evaluation-darkred)
2. **CLiMP: A Benchmark for Chinese Language Model Evaluation.** *Beilei Xiang, Changbing Yang, Yu Li, Alex Warstadt, Katharina Kann.* `arxiv 2021` [[pdf]](https://arxiv.org/abs/2101.11131) ![](https://img.shields.io/badge/evaluation-darkred)
3. **MultiTalk: A Highly-Branching Dialog Testbed for Diverse Conversations.** *Yao Dou, Maxwell Forbes, Ari Holtzman, Yejin Choi.* `AAAI 2021` [[pdf]](https://arxiv.org/abs/2102.01263) ![](https://img.shields.io/badge/dialog-gold)
4. **Measuring and Improving Consistency in Pretrained Language Models.** *Yanai Elazar, Nora Kassner, Shauli Ravfogel, Abhilasha Ravichander, Eduard Hovy, Hinrich Schütze, Yoav Goldberg.* `arxiv 2021` [[pdf]](https://arxiv.org/abs/2102.01017) ![](https://img.shields.io/badge/evaluation-darkred)
5. **The GEM Benchmark: Natural Language Generation, its Evaluation and Metrics.** *Sebastian Gehrmann et al.* `ACL 2021 workshop` [[pdf]](https://arxiv.org/abs/2102.01672) ![](https://img.shields.io/badge/evaluation-darkred)
6. **BOLD: Dataset and Metrics for Measuring Biases in Open-Ended Language Generation.** *Jwala Dhamala, Tony Sun, Varun Kumar, Satyapriya Krishna, Yada Pruksachatkun, Kai-Wei Chang, Rahul Gupta.* `FAccT 2021` [[pdf]](https://arxiv.org/abs/2101.11718) ![](https://img.shields.io/badge/story-navy)
7. **GLGE: A New General Language Generation Evaluation Benchmark.** *Dayiheng Liu et al.* `arxiv 2021` [[pdf]](https://arxiv.org/abs/2011.11928) ![](https://img.shields.io/badge/evaluation-darkred) 
8. **STORIUM: A Dataset and Evaluation Platform for Machine-in-the-Loop Story Generation.** *Nader Akoury, Shufan Wang, Josh Whiting, Stephen Hood, Nanyun Peng, Mohit Iyyer.* `EMNLP 2020` [[pdf]](https://arxiv.org/abs/2010.01717) ![](https://img.shields.io/badge/story-navy)
9. **GLUCOSE: GeneraLized and COntextualized Story Explanations.** *Nasrin Mostafazadeh, Aditya Kalyanpur, Lori Moon, David Buchanan, Lauren Berkowitz, Or Biran, Jennifer Chu-Carroll.* `EMNLP 2020` [[pdf]](https://arxiv.org/abs/2009.07758) ![](https://img.shields.io/badge/story-navy)
10. **CommonGen: A Constrained Text Generation Challenge for Generative Commonsense Reasoning.** *Bill Yuchen Lin, Wangchunshu Zhou, Ming Shen, Pei Zhou, Chandra Bhagavatula, Yejin Choi, Xiang Ren.* `Findings of EMNLP 2020` [[pdf]](https://arxiv.org/abs/1911.03705) ![](https://img.shields.io/badge/story-navy)
11. **A Large-Scale Chinese Short-Text Conversation Dataset.** *Yida Wang, Pei Ke, Yinhe Zheng, Kaili Huang, Yong Jiang, Xiaoyan Zhu, Minlie Huang.* `NLPCC 2020` [[pdf]](https://arxiv.org/abs/2008.03946) ![](https://img.shields.io/badge/dialog-gold)
12. **Storytelling with Dialogue: A Critical Role Dungeons and Dragons Dataset.** *Revanth Rameshkumar, Peter Bailey.* `ACL 2020` [[pdf]](https://www.aclweb.org/anthology/2020.acl-main.459/) ![](https://img.shields.io/badge/story-navy)
13. **MuTual: A Dataset for Multi-Turn Dialogue Reasoning.** *Leyang Cui, Yu Wu, Shujie Liu, Yue Zhang, Ming Zhou.* `ACL 2020` [[pdf]](https://arxiv.org/abs/2004.04494) ![](https://img.shields.io/badge/dialog-gold)
14. **Designing Precise and Robust Dialogue Response Evaluators.** *Tianyu Zhao, Divesh Lala, Tatsuya Kawahara.* `ACL 2020 short paper` [[pdf]](https://arxiv.org/abs/2004.04908) ![](https://img.shields.io/badge/dialog-gold)
15. **Recollection versus Imagination: Exploring Human Memory and Cognition via Neural Language Models.** *Maarten Sap, Eric Horvitz, Yejin Choi, Noah A. Smith, James Pennebaker.* `ACL 2020` [[pdf]](https://www.aclweb.org/anthology/2020.acl-main.178/) ![](https://img.shields.io/badge/story-navy)
16. **Exploring the Effect of Author and Reader Identity in Online Story Writing: the STORIESINTHEWILD Corpus.** *Tal August, Maarten Sap, Elizabeth Clark, Katharina Reinecke, Noah A. Smith.* `ACL 2020` [[pdf]](https://www.aclweb.org/anthology/2020.nuse-1.6/) ![](https://img.shields.io/badge/story-navy)
17. **Counterfactual Story Reasoning and Generation.** *Lianhui Qin, Antoine Bosselut, Ari Holtzman, Chandra Bhagavatula, Elizabeth Clark, Yejin Choi.* `EMNLP 2019` [[pdf]](https://arxiv.org/abs/1909.04076) ![](https://img.shields.io/badge/story-navy)
18. **Hierarchical neural story generation.** *Angela Fan, Mike Lewis, and Yann Dauphin.* `ACL 2018` [[pdf]](https://www.aclweb.org/anthology/P18-1082.pdf) ![](https://img.shields.io/badge/story-navy)
19. **Modeling Naive Psychology of Characters in Simple Commonsense Stories.** *Hannah Rashkin, Antoine Bosselut, Maarten Sap, Kevin Knight, Yejin Choi.* `ACL 2018` ![](https://img.shields.io/badge/story-navy)
20. **LSDSCC: a Large Scale Domain-Specific Conversational Corpus for Response Generation with Diversity Oriented Evaluation Metrics.** *Zhen Xu, Nan Jiang, Bingquan Liu, Wenge Rong, Bowen Wu, Baoxun Wang, Zhuoran Wang, Xiaolong Wang.* `NAACL 2018` [[pdf]](https://www.aclweb.org/anthology/N18-1188/) ![](https://img.shields.io/badge/dialog-gold)
21. **Visual storytelling.** *Ting-Hao Kenneth Huang, Francis Ferraro, Nasrin Mostafazadeh, Ishan Misra, Aishwarya Agrawal, Jacob Devlin, Ross Girshick, Xiaodong He, Pushmeet Kohli, Dhruv Batra, C. Lawrence Zitnick, Devi Parikh, Lucy Vanderwende, Michel Galley, Margaret Mitchell.* `NAACL 2016` [[pdf]](https://www.aclweb.org/anthology/N16-1147/) ![](https://img.shields.io/badge/story-navy)
22. **A Corpus and Cloze Evaluation for Deeper Understanding of Commonsense Stories.** *Nasrin Mostafazadeh, Nathanael Chambers, Xiaodong He, Devi Parikh, Dhruv Batra, Lucy Vanderwende, Pushmeet Kohli, James Allen.* `NAACL 2016` [[pdf]](https://www.aclweb.org/anthology/N16-1098/) ![](https://img.shields.io/badge/story-navy)
23. **WikiPlots.** *Mark Ridel.* `Github 2017` [[link]](https://github.com/markriedl/WikiPlots) ![](https://img.shields.io/badge/story-navy)



## 1. Survey

1. **Automatic Story Generation: Challenges and Attempts.** *Amal Alabdulkarim, Siyan Li, Xiangyu Peng.* `arxiv 2021` [[pdf]](https://arxiv.org/abs/2102.12634) ![](https://img.shields.io/badge/story-navy)
2. **Combining pre-trained language models and structured knowledge.** *Pedro Colon-Hernandez, Catherine Havasi, Jason Alonso, Matthew Huggins, Cynthia Breazeal.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2101.12294) ![](https://img.shields.io/badge/knowledge-red)
3. **A Survey of Knowledge-Enhanced Text Generation.** *Wenhao Yu, Chenguang Zhu, Zaitang Li, Zhiting Hu, Qingyun Wang, Heng Ji, Meng Jiang.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2010.04389) ![](https://img.shields.io/badge/dialog-gold) ![](https://img.shields.io/badge/story-navy) ![](https://img.shields.io/badge/knowledge-red)
4. **Automatic Story Generation: State of the Art and Recent Trends.**  *Brian Daniel Herrera-González, Alexander Gelbukh, and Hiram Calvo.* `MICA 2020` [[pdf]](https://link.springer.com/chapter/10.1007%2F978-3-030-60887-3_8) ![](https://img.shields.io/badge/story-navy)
5. **Towards Unified Dialogue System Evaluation: A Comprehensive Analysis of Current Evaluation Protocols.** *Sarah E. Finch, Jinho D. Choi.* `SIGDIAL 2020` [[pdf]](https://arxiv.org/abs/2006.06110) ![](https://img.shields.io/badge/dialog-gold)
6. **Challenges in Building Intelligent Open-domain Dialog Systems.** *Minlie Huang, Xiaoyan Zhu, Jianfeng Gao.* `TOIS 2020` [[pdf]](https://dl.acm.org/doi/abs/10.1145/3383123) ![](https://img.shields.io/badge/dialog-gold)
7. **Open-Domain Conversational Agents: Current Progress, Open Problems, and Future Directions.** *Stephen Roller, Y-Lan Boureau, Jason Weston, Antoine Bordes, Emily Dinan, Angela Fan, David Gunning, Da Ju, Margaret Li, Spencer Poff, Pratik Ringshia, Kurt Shuster, Eric Michael Smith, Arthur Szlam, Jack Urbanek, Mary Williamson.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2006.12442) ![](https://img.shields.io/badge/dialog-gold)
8. **A Survey of Evaluation Metrics Used for NLG Systems.** *Ananya B. Sai, Akash Kumar Mohankumar, Mitesh M. Khapra.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2008.12009) ![](https://img.shields.io/badge/evaluation-darkred)
9. **Evaluation of Text Generation: A Survey.** *Asli Celikyilmaz, Elizabeth Clark, Jianfeng Gao.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2006.14799) ![](https://img.shields.io/badge/evaluation-darkred)
10. **Survey on evaluation methods for dialogue systems.** *Jan Deriu, Alvaro Rodrigo, Arantxa Otegi, Guillermo Echegoyen, Sophie Rosset, Eneko Agirre & Mark Cieliebak.* `Artificial Intelligence Review 2020` [[pdf]](https://link.springer.com/article/10.1007/s10462-020-09866-x) ![](https://img.shields.io/badge/dialog-gold) ![](https://img.shields.io/badge/evaluation-darkred)  
11. **Judge the Judges: A Large-Scale Evaluation Study of Neural Language Models for Online Review Generation.** *Cristina Garbacea, Samuel Carton, Shiyan Yan, Qiaozhu Mei.* `arxiv 2019` [[pdf]](https://arxiv.org/abs/1901.00398) ![](https://img.shields.io/badge/evaluation-darkred)
12. **How NOT To Evaluate Your Dialogue System: An Empirical Study of Unsupervised Evaluation Metrics for Dialogue Response Generation.** *Chia-Wei Liu, Ryan Lowe, Iulian Serban, Mike Noseworthy, Laurent Charlin, Joelle Pineau.* `EMNLP 2016` [[pdf]](https://www.aclweb.org/anthology/D16-1230/) ![](https://img.shields.io/badge/dialog-gold) ![](https://img.shields.io/badge/evaluation-darkred)
13. **对话系统评价方法综述** *张伟男, 张杨子, 刘挺.* `中国科学 : 信息科学` [[pdf]](http://scis.scichina.com/cn/2017/N112017-00125.pdf) ![](https://img.shields.io/badge/dialog-gold) ![](https://img.shields.io/badge/evaluation-darkred)
14. **A Survey of Available Corpora for Building Data-Driven Dialogue Systems.** *Iulian Vlad Serban, Ryan Lowe, Peter Henderson, Laurent Charlin, Joelle Pineau.* `arxiv 2015` [[pdf]](https://arxiv.org/abs/1512.05742) ![](https://img.shields.io/badge/dialog-gold)



## 2. Generative Model

![](https://img.shields.io/badge/planning-planning-brightgreen) ![](https://img.shields.io/badge/knowledge-knowledge-red) ![](https://img.shields.io/badge/PreTrainingModel-ptm-blue)

### 2.1 Story

1. **Changing the Mind of Transformers for Topically-Controllable Language Generation.** *Haw-Shiuan Chang, Jiaming Yuan, Mohit Iyyer, Andrew McCallum.* [[pdf]](https://arxiv.org/abs/2103.15335) `EACL 2021` 
2. **Automated Storytelling via Causal, Commonsense Plot Ordering.** *Prithviraj Ammanabrolu, Wesley Cheung, William Broniec, Mark O. Riedl.* [[pdf]](https://arxiv.org/abs/2009.00829) `AAAI 2021` ![](https://img.shields.io/badge/knowledge-red)
3. **GraphPlan: Story Generation by Planning with Event Graph.** *Hong Chen, Raphael Shu, Hiroya Takamura, Hideki Nakayama.* [[pdf]](https://arxiv.org/abs/2102.02977) `arxiv 2021` ![](https://img.shields.io/badge/planning-brightgreen)
4. **Facts2Story: Controlling Text Generation by Key Facts.** *Eyal Orbach, Yoav Goldberg.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2012.04332) ![](https://img.shields.io/badge/planning-brightgreen)
5. **Story Generation with Rich Details.** *Fangzhou Zhai, Vera Demberg, Alexander Koller.* `COLING 2020`  [[pdf]](https://www.aclweb.org/anthology/2020.coling-main.212/)  ![](https://img.shields.io/badge/planning-brightgreen)
6. **Consistency and Coherency Enhanced Story Generation.** *Wei Wang, Piji Li, Hai-Tao Zheng.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2010.08822) ![](https://img.shields.io/badge/planning-brightgreen)
7. **Narrative Interpolation for Generating and Understanding Stories.** *Su Wang, Greg Durrett, Katrin Erk.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2008.07466) ![](https://img.shields.io/badge/planning-brightgreen)
8. **Plan-CVAE: A Planning-based Conditional Variational Autoencoder for Story Generation.** *Lin Wang, Juntao Li , Dongyan Zhao, Rui Yan.* `CCL 2020` [[pdf]](http://www.cips-cl.org/static/anthology/CCL-2020/CCL-20-083.pdf) ![](https://img.shields.io/badge/planning-brightgreen)
9. **Controllable Multi-Character Psychology-Oriented Story Generation.** *Feifei Xu, Xinpeng Wang, Yunpu Ma, Volker Tresp, Yuyi Wang, Shanlin Zhou, Haizhou Du.* `CIKM 2020` [[pdf]](https://dl.acm.org/doi/pdf/10.1145/3340531.3411937) ![](https://img.shields.io/badge/planning-brightgreen) ![](https://img.shields.io/badge/emotion-cyan)
10. **Creative Storytelling with Language Models and Knowledge Graphs.** *Xinran Yang, Ilaria Tiddi.* `CIKM 2020 workshop` [[pdf]](http://ceur-ws.org/Vol-2699/paper07.pdf) ![](https://img.shields.io/badge/knowledge-red)
11. **Modeling Protagonist Emotions for Emotion-Aware Storytelling.** *Faeze Brahman, Snigdha Chaturvedi.* `EMNLP 2020` [[pdf]](https://arxiv.org/abs/2010.06822) ![](https://img.shields.io/badge/planning-brightgreen) ![](https://img.shields.io/badge/emotion-cyan)
12. **PlotMachines: Outline-Conditioned Generation with Dynamic Plot State Tracking.** *Hannah Rashkin, Asli Celikyilmaz, Yejin Choi, Jianfeng Gao.* `EMNLP 2020` [[pdf]](https://www.aclweb.org/anthology/2020.emnlp-main.349/) ![](https://img.shields.io/badge/planning-brightgreen)
13. **Cue Me In: Content-Inducing Approaches to Interactive Story Generation.** *Faeze Brahman, Alexandru Petrusca, Snigdha Chaturvedi.* `AACL 2020` [[pdf]](https://arxiv.org/abs/2010.09935) ![](https://img.shields.io/badge/planning-brightgreen)
14. **Content Planning for Neural Story Generation with Aristotelian Rescoring.** *Seraphina Goldfarb-Tarrant, Tuhin Chakrabarty, Ralph Weischedel, Nanyun Peng.* `EMNLP 2020` [[pdf]](https://arxiv.org/abs/2009.09870) ![](https://img.shields.io/badge/planning-brightgreen)
15. **MEGATRON-CNTRL: Controllable Story Generation with External Knowledge Using Large-Scale Language Models.** *Peng Xu, Mostofa Patwary, Mohammad Shoeybi, Raul Puri, Pascale Fung, Anima Anandkumar, Bryan Catanzaro.* `EMNLP 2020` [[pdf]](https://arxiv.org/abs/2010.00840) ![](https://img.shields.io/badge/knowledge-red)
16. **A Knowledge-Enhanced Pretraining Model for Commonsense Story Generation.** *Jian Guan, Fei Huang, Zhihao Zhao, Xiaoyan Zhu, Minlie Huang*. `TACL 2020` [[pdf]](https://www.mitpressjournals.org/doi/pdf/10.1162/tacl_a_00302) ![](https://img.shields.io/badge/knowledge-red)
17. **Improving Neural Story Generation by Targeted Common Sense Grounding.** *Huanru Henry Mao, Bodhisattwa Prasad Majumder, Julian McAuley, Garrison Cottrell.* `EMNLP 2020` [[pdf]](https://www.aclweb.org/anthology/D19-1615/) ![](https://img.shields.io/badge/knowledge-red)
18. **A Character-Centric Neural Model for Automated Story Generation.** *Rui Yan et al.* `AAAI 2020` [[pdf]](https://ojs.aaai.org/index.php/AAAI/article/view/5536) ![](https://img.shields.io/badge/planning-brightgreen)
19. **Narrative Interpolation for Generating and Understanding Stories.** *Su Wang, Greg Durrett, Katrin Erk.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2008.07466)
20. **Strategies for structuring story generation.** *Angela Fan, Mike Lewis, and Yann Dauphin.* `ACL 2019` [[pdf]](https://www.aclweb.org/anthology/P19-1254) ![](https://img.shields.io/badge/planning-brightgreen)
21. **Plan-and-write: Towards better automatic storytelling.** *Lili Yao, Nanyun Peng, Ralph Weischedel, Kevin Knight, Dongyan Zhao, and Rui Yan.* `AAAI 2019` [[pdf]](https://www.aaai.org/ojs/index.php/AAAI/article/view/4726) ![](https://img.shields.io/badge/planning-brightgreen)
22. **Story ending generation with incremental encoding and commonsense knowledge.** *Jian Guan, Yansen Wang, and Minlie Huang.* `AAAI 2019` [[pdf]](https://www.aaai.org/ojs/index.php/AAAI/article/view/4612) ![](https://img.shields.io/badge/knowledge-red)
23. **Learning to Write Stories with Thematic Consistency and Wording Novelty**. *Juntao Li, Lidong Bing, Lisong Qiu, Dongmin Chen, Dongyan Zhao, and Rui Yan.* `AAAI 2019` [[pdf]](https://www.aaai.org/ojs/index.php/AAAI/article/view/3993/3871) 
24. **T-CVAE: Transformer-Based Conditioned Variational Autoencoder for Story Completion.** *Tianming Wang and Xiaojun Wan.* `IJCAI 2019` [[pdf]](http://184pc128.csie.ntnu.edu.tw/presentation/20-04-27/T-CVAE-%20Transformer-Based%20Conditioned%20Variational%20Autoencoder%20for%20Story%20Completion.pdf) ![](https://img.shields.io/badge/planning-brightgreen)
25. **Learning to Predict Explainable Plots for Neural Story Generation**. *Gang Chen, Yang Liu, Huanbo Luan, Meng Zhang, Qun Liu, and Maosong Sun.* `arxiv 2019` [[pdf]](https://arxiv.org/abs/1912.02395) ![](https://img.shields.io/badge/planning-brightgreen)
26. **Hierarchical neural story generation.** *Angela Fan, Mike Lewis, and Yann Dauphin.* `ACL 2018` [[pdf]](https://www.aclweb.org/anthology/P18-1082.pdf)
27. **Discourse-Aware Neural Rewards for Coherent Text Generation.** *Antoine Bosselut, Asli Celikyilmaz, Xiaodong He, Jianfeng Gao, Po-Sen Huang, Yejin Choi.* `ACL 2018` [[pdf]](https://www.aclweb.org/anthology/N18-1016/)
28. **A skeleton-based model for promoting coherence among sentences in narrative story generation.** *Jingjing Xu, Xuancheng Ren, Yi Zhang, Qi Zeng, Xiaoyan Cai, and Xu Sun.* `EMNLP 2018` [[pdf]](https://www.aclweb.org/anthology/D18-1462/) ![](https://img.shields.io/badge/planning-brightgreen)
29. **Event representations for automated story generation with deep neural nets.** *Lara Martin, Prithviraj Ammanabrolu, Xinyu Wang, William Hancock, Shruti Singh, Brent Harrison, and Mark Riedl.* `AAAI 2018` [[pdf]](https://arxiv.org/abs/1706.01331)
30. **Discourse-Driven Narrative Generation with Bipartite Planning.** *David R. Winer and R. Michael Young.* `ACL 2016` [[pdf]](https://www.aclweb.org/anthology/W16-6602/) ![](https://img.shields.io/badge/planning-brightgreen)

### 2.2 Dialog

1. **CARE: Commonsense-Aware Emotional Response Generation with Latent Concepts,** *Peixiang Zhong, Di Wang, Pengfei Li, Chen Zhang, Hao Wang, Chunyan Miao.* `AAAI 2021` [[pdf]](https://arxiv.org/abs/2012.08377v1) ![](https://img.shields.io/badge/knowledge-red) ![](https://img.shields.io/badge/emotion-cyan)
2. **DiSCoL: Toward Engaging Dialogue Systems through Conversational Line Guided Response Generation.** *Sarik Ghazarian, Zixi Liu, Tuhin Chakrabarty, Xuezhe Ma, Aram Galstyan, Nanyun Peng.* `arxiv 2021` [[pdf]](https://arxiv.org/abs/2102.02191) ![](https://img.shields.io/badge/planning-brightgreen)
3. **Keyword-Guided Neural Conversational Model.** *Peixiang Zhong, Yong Liu, Hao Wang, Chunyan Miao.* `AAAI 2021` [[pdf]](https://arxiv.org/abs/2012.08383) ![](https://img.shields.io/badge/planning-brightgreen)
4. **Learning to Plan and Realize Separately for Open-Ended Dialogue Systems.** *Sashank Santhanam, Zhuo Cheng, Brodie Mather, Bonnie Dorr, Archna Bhatia, Bryanna Hebenstreit, Alan Zemel, Adam Dalton, Tomek Strzalkowski, Samira Shaikh.* `Findings of EMNLP 2020` [[pdf]](https://arxiv.org/abs/2009.12506) ![](https://img.shields.io/badge/planning-brightgreen)
5. **A Large-Scale Chinese Short-Text Conversation Dataset.** *Yida Wang, Pei Ke, Yinhe Zheng, Kaili Huang, Yong Jiang, Xiaoyan Zhu, Minlie Huang.* `NLPCC 2020` [[pdf]](https://arxiv.org/abs/2008.03946) ![](https://img.shields.io/badge/ptm-blue)
6. **DIALOGPT : Large-Scale Generative Pre-training for Conversational Response Generation.** *Yizhe Zhang, Siqi Sun, Michel Galley, Yen-Chun Chen, Chris Brockett, Xiang Gao, Jianfeng Gao, Jingjing Liu, Bill Dolan.* `ACL 2020` [[pdf]](https://www.aclweb.org/anthology/2020.acl-demos.30/) ![](https://img.shields.io/badge/ptm-blue)
7. **Target-Guided Open-Domain Conversation.** *Jianheng Tang, Tiancheng Zhao, Chenyan Xiong, Xiaodan Liang, Eric Xing, Zhiting Hu.* [[pdf]](https://www.aclweb.org/anthology/P19-1565/) 
8. **Recipes for building an open-domain chatbot.** *Stephen Roller, Emily Dinan, Naman Goyal, Da Ju, Mary Williamson, Yinhan Liu, Jing Xu, Myle Ott, Kurt Shuster, Eric M. Smith, Y-Lan Boureau, Jason Weston.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2004.13637) ![](https://img.shields.io/badge/ptm-blue)
9. **Towards a Human-like Open-Domain Chatbot.** *Daniel Adiwardana, Minh-Thang Luong, David R. So, Jamie Hall, Noah Fiedel, Romal Thoppilan, Zi Yang, Apoorv Kulshreshtha, Gaurav Nemade, Yifeng Lu, Quoc V. Le.*  `arxiv 2020` [[pdf]](https://arxiv.org/abs/2001.09977) ![](https://img.shields.io/badge/ptm-blue)
10. **Adversarial Learning for Neural Dialogue Generation.** *Jiwei Li, Will Monroe, Tianlin Shi, Sébastien Jean, Alan Ritter, Dan Jurafsky.* `EMNLP 2017` [[pdf]](https://www.aclweb.org/anthology/D17-1230/)



### 2.3 Others

1. **All NLP Tasks Are Generation Tasks: A General Pretraining Framework.** *Zhengxiao Du, Yujie Qian, Xiao Liu, Ming Ding, Jiezhong Qiu, Zhilin Yang, Jie Tang.* `arxiv 2021` [[pdf]](https://arxiv.org/abs/2103.10360) ![](https://img.shields.io/badge/ptm-blue)
2. **Controllable Generation from Pre-trained Language Models via Inverse Prompting.** *Xu Zhou, Da Yin, Qingyang Zhong, Hongxia Yang, Zhilin Yang, Jie Tang.* `arxiv 2021` [[pdf]](https://arxiv.org/abs/2103.10685) ![](https://img.shields.io/badge/ptm-blue)
3. **Attribute Alignment: Controlling Text Generation from Pre-trained Language Models.** *Dian Yu, Kenji Sagae, Zhou Yu.* [[pdf]](https://arxiv.org/abs/2103.11070)  ![](https://img.shields.io/badge/ptm-blue)
4. **GeDi: Generative Discriminator Guided Sequence Generation.** *Ben Krause, Akhilesh Deepak Gotmare, Bryan McCann, Nitish Shirish Keskar, Shafiq Joty, Richard Socher, Nazneen Fatema Rajani.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2009.06367)  ![](https://img.shields.io/badge/ptm-blue)
5. **PAIR: Planning and Iterative Reﬁnement in Pre-trained Transformers for Long Text Generation.** *Xinyu Hua, Lu Wang.* `EMNLP 2020` [[pdf]](https://arxiv.org/abs/2010.02301) ![](https://img.shields.io/badge/planning-brightgreen)
6. **PLUG AND PLAY LANGUAGE MODELS : A SIMPLE APPROACH TO CONTROLLED TEXT GENERATION.** *Sumanth Dathathri, Andrea Madotto, Janice Lan, Jane Hung, Eric Frank, Piero Molino, Jason Yosinski, Rosanne Liu.* `ICLR 2020` [[pdf]](https://arxiv.org/abs/1912.02164)  ![](https://img.shields.io/badge/ptm-blue)
7. **Language Models are Few-Shot Learners.** *Tom B. Brown, Benjamin Mann, Nick Ryder, Melanie Subbiah, Jared Kaplan, Prafulla Dhariwal, Arvind Neelakantan, Pranav Shyam, Girish Sastry, Amanda Askell, Sandhini Agarwal, Ariel Herbert-Voss, Gretchen Krueger, Tom Henighan, Rewon Child, Aditya Ramesh, Daniel M. Ziegler, Jeffrey Wu, Clemens Winter, Christopher Hesse, Mark Chen, Eric Sigler, Mateusz Litwin, Scott Gray, Benjamin Chess, Jack Clark, Christopher Berner, Sam McCandlish, Alec Radford, Ilya Sutskever, Dario Amodei.* `OpenAI blog 2020` [[pdf]](https://arxiv.org/abs/2005.14165) ![](https://img.shields.io/badge/ptm-blue)
8. **Progressive Generation of Long Text.** *Bowen Tan, Zichao Yang, Maruan AI-Shedivat, Eric P. Xing, Zhiting Hu.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2006.15720)![](https://img.shields.io/badge/planning-brightgreen)
9. **BART: Denoising Sequence-to-Sequence Pre-training for Natural Language Generation, Translation, and Comprehension.** *Mike Lewis, Yinhan Liu, Naman Goyal, Marjan Ghazvininejad, Abdelrahman Mohamed, Omer Levy, Veselin Stoyanov, Luke Zettlemoyer.* `ACL 2020` [[pdf]](https://www.aclweb.org/anthology/2020.acl-main.703/) ![](https://img.shields.io/badge/ptm-blue)
10. **Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer.** *Colin Raffel, Noam Shazeer, Adam Roberts, Katherine Lee, Sharan Narang, Michael Matena, Yanqi Zhou, Wei Li, Peter J. Liu.* `JMLR 2020` [[pdf]](https://arxiv.org/abs/1910.10683) ![](https://img.shields.io/badge/ptm-blue)
11. **Long and Diverse Text Generation with Planning-based Hierarchical Variational Model.** *Zhihong Shao, Minlie Huang, Jiangtao Wen, Wenfei Xu, Xiaoyan Zhu.* `EMNLP 2019` [[pdf]](https://arxiv.org/abs/1908.06605) ![](https://img.shields.io/badge/planning-brightgreen)
12. **Language Models are Unsupervised Multitask Learners.** *Alec Radford, Jeffrey Wu, Rewon Child, David Luan, Dario Amodei, Ilya Sutskever.* `OpenAI blog 2019` [[pdf]](https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf) ![](https://img.shields.io/badge/ptm-blue)
13. **Improving Language Understanding by Generative Pre-Training.** *Alec Radford, Karthik Narasimhan, Tim Salimans, Ilya Sutskever.* `OpenAI blog 2018` [[pdf]](https://cdn.openai.com/research-covers/language-unsupervised/language_understanding_paper.pdf) ![](https://img.shields.io/badge/ptm-blue)
14. **Chinese poetry generation with planning based neural network.** *Zhe Wang, Wei He, Hua Wu, Haiyang Wu, Wei Li, Haifeng Wang, Enhong Chen.* `COLING 2016` [[pdf]](https://arxiv.org/abs/1610.09889) ![](https://img.shields.io/badge/planning-brightgreen)
15. **Sentence-Level Content Planning and Style Specification for Neural Text Generation**. *Xinyu Hua, Lu Wang*.  `EMNLP 2019` [pdf](https://arxiv.org/abs/1909.00734) ![](https://img.shields.io/badge/planning-brightgreen)
16. **Summarize, Outline, and Elaborate : Long-Text Generation via Hierarchical Supervision from Extractive Summaries**. *Xiaofei Sun, Chun Fan, Zijun Sun, Yuxian Meng, Fei Wu, JiWei Li*. `arxiv 2020` [pdf](https://arxiv.org/abs/2010.07074) ![](https://img.shields.io/badge/planning-brightgreen)



## 3. Evaluation

![](https://img.shields.io/badge/ReferencedMetric-ref-orange) ![](https://img.shields.io/badge/UnreferencedMetric-unref-yellow) ![](https://img.shields.io/badge/WithHumanRatingAsSupervision-sl-pink) ![](https://img.shields.io/badge/EvaluationFromMultipleDimension-multidim-darkgreen)

### 3.1 Metric

1. **Perception Score, A Learned Metric for Open-ended Text Generation Evaluation.** *Jing Gu, Qingyang Wu, Zhou Yu.* `AAAI 2021` [[pdf]](https://arxiv.org/abs/2008.03082) ![](https://img.shields.io/badge/ref-orange)
2. **UNION: An Unreferenced Metric for Evaluating Open-ended Story Generation.** *Jian Guan, Minlie Huang.* `EMNLP 2020` [[pdf]](https://arxiv.org/pdf/2009.07602.pdf) ![](https://img.shields.io/badge/unref-yellow)
3. **GRADE: Automatic Graph-Enhanced Coherence Metric for Evaluating Open-Domain Dialogue Systems.** *Lishan Huang, Zheng Ye, Jinghui Qin, Liang Lin, Xiaodan Liang.* `EMNLP 2020` [[pdf]](https://arxiv.org/abs/2010.03994) ![](https://img.shields.io/badge/unref-yellow)
4. **GRUEN for Evaluating Linguistic Quality of Generated Text.** *Wanzheng Zhu and Suma Bhat.* `Findings of EMNLP 2020` [[pdf]](https://arxiv.org/abs/2010.02498) ![](https://img.shields.io/badge/multidim-darkgreen)
5. **How To Evaluate Your Dialogue System: Probe Tasks as an Alternative for Token-level Evaluation Metrics.** *Prasanna Parthasarathi, Joelle Pineau, Sarath Chandar.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2008.10427)
6. **BLEURT: Learning robust metrics for text generation.** *Thibault Sellam, Dipanjan Das, and Ankur Parikh.* `ACL 2020` [[pdf]](https://doi.org/10.18653/v1/2020.acl-main.704) ![](https://img.shields.io/badge/ref-orange) ![](https://img.shields.io/badge/unref-yellow) ![](https://img.shields.io/badge/sl-pink)
7. **Towards Holistic and Automatic Evaluation of Open-Domain Dialogue Generation.** *Bo Pang, Erik Nijkamp, Wenjuan Han, Linqi Zhou, Yixian Liu, Kewei Tu.* `ACL 2020` [[pdf]](https://www.aclweb.org/anthology/2020.acl-main.333/) ![](https://img.shields.io/badge/unref-yellow)
8. **Learning an Unreferenced Metric for Online Dialogue Evaluation.** *Koustuv Sinha, Prasanna Parthasarathi, Jasmine Wang, Ryan Lowe, William L. Hamilton, Joelle Pineau.* `ACL 2020` [[pdf]](https://arxiv.org/abs/2005.00583) ![](https://img.shields.io/badge/unref-yellow)
9. **Evaluating Dialogue Generation Systems via Response Selection.** *Shiki Sato, Reina Akama, Hiroki Ouchi, Jun Suzuki, Kentaro Inui.* `ACL 2020` [[pdf]](https://arxiv.org/abs/2004.14302)
10. **Speaker Sensitive Response Evaluation Model.** *JinYeong Bak, Alice Oh.* `ACL 2020` [[pdf]](Speaker Sensitive Response Evaluation Model)
11. **USR: An Unsupervised and Reference Free Evaluation Metric for Dialog Generation.** *Shikib Mehri, Maxine Eskenazi.* `ACL 2020` [[pdf]](https://arxiv.org/abs/2005.00456) ![](https://img.shields.io/badge/unref-yellow)
12. **uBLEU: Uncertainty-Aware Automatic Evaluation Method for Open-Domain Dialogue Systems.** *Tsuta Yuma, Naoki Yoshinaga, Masashi Toyoda.* `ACL 2020` [[pdf]](https://www.aclweb.org/anthology/2020.acl-srw.27/) ![](https://img.shields.io/badge/ref-orange)
13. **Beyond User Self-Reported Likert Scale Ratings: A Comparison Model for Automatic Dialog Evaluation.** *Weixin Liang, James Zou, Zhou Yu.* `ACL 2020` [[pdf]](https://arxiv.org/abs/2005.10716) ![](https://img.shields.io/badge/sl-pink)
14. **Designing Precise and Robust Dialogue Response Evaluators.** *Tianyu Zhao, Divesh Lala, Tatsuya Kawahara.* `ACL 2020 short paper` [[pdf]](https://arxiv.org/abs/2004.04908) ![](https://img.shields.io/badge/unref-yellow)
15. **Unsupervised Evaluation of Interactive Dialog with DialoGPT.** *Shikib Mehri, Maxine Eskenazi.* `SIGDIAL 2020` [[pdf]](https://www.aclweb.org/anthology/2020.sigdial-1.28/) ![](https://img.shields.io/badge/unref-yellow)
16. **Can You Put it All Together: Evaluating Conversational Agents' Ability to Blend Skills.** *Eric Michael Smith, Mary Williamson, Kurt Shuster, Jason Weston, Y-Lan Boureau.* `ACL 2020` [[pdf]](https://arxiv.org/abs/2004.08449)
17. **Bertscore: Evaluating text generation with bert.** *Tianyi Zhang, Varsha Kishore, Felix Wu, Kilian Q. Weinberger, and Yoav Artzi.* `ICLR 2020` [[pdf]](https://openreview.net/forum?id=SkeHuCVFDr) ![](https://img.shields.io/badge/ref-orange)
18. **Predictive Engagement: An Efficient Metric For Automatic Evaluation of Open-Domain Dialogue Systems.** *Sarik Ghazarian, Ralph Weischedel, Aram Galstyan, Nanyun Peng.* `AAAI 2020` [[pdf]](https://arxiv.org/abs/1911.01456) ![](https://img.shields.io/badge/unref-yellow)
19. **Learning to compare for better training and evaluation of open domain natural language generation models.** *Wangchunshu Zhou and Ke Xu.* `AAAI 2020` [[pdf]](https://arxiv.org/abs/2002.05058) ![](https://img.shields.io/badge/ref-orange) ![](https://img.shields.io/badge/unref-yellow)
20. **Improving Dialog Evaluation with a Multi-reference Adversarial Dataset and Large Scale Pretraining.** *Ananya B. Sai, Akash Kumar Mohankumar, Siddhartha Arora, Mitesh M. Khapra.* `TACL 2020` [[pdf]](https://arxiv.org/abs/2009.11321) ![](https://img.shields.io/badge/ref-orange)
21. **How to Evaluate the Next System: Automatic Dialogue Evaluation from the Perspective of Continual Learning.** *Lu Li, Zhongheng He, Xiangyang Zhou, Dianhai Yu.* `arxiv 2019` [[pdf]](https://arxiv.org/abs/1912.04664)
22. **Moverscore: Text generation evaluating with contextualized embeddings and earth mover distance.** *Wei Zhao, Maxime Peyrard, Fei Liu, Yang Gao, Christian M Meyer, and Steffen Eger.* `EMNLP 2019` [[pdf]](https://www.aclweb.org/anthology/D19-1053/) ![](https://img.shields.io/badge/ref-orange)
23. **TIGEr: Text-to-Image Grounding for Image Caption Evaluation.** *Ming Jiang, Qiuyuan Huang, Lei Zhang, Xin Wang, Pengchuan Zhang, Zhe Gan, Jana Diesner, Jianfeng Gao.* `EMNLP 2019` [[pdf]](https://www.aclweb.org/anthology/D19-1220/) ![](https://img.shields.io/badge/ref-orange)
24. **Investigating Evaluation of Open-Domain Dialogue Systems With Human Generated Multiple References.** *Prakhar Gupta, Shikib Mehri, Tiancheng Zhao, Amy Pavel, Maxine Eskenazi, Jeffrey Bigham.* `SIGDIAL 2019` [[pdf]](https://www.aclweb.org/anthology/W19-5944/) ![](https://img.shields.io/badge/ref-orange)
25. **Unifying Human and Statistical Evaluation for Natural Language Generation.** *Tatsunori Hashimoto, Hugh Zhang, Percy Liang.* `NAACL 2019` [[pdf]](https://www.aclweb.org/anthology/N19-1169/) ![](https://img.shields.io/badge/unref-yellow) ![](https://img.shields.io/badge/sl-pink)
26. **Better automatic evaluation of open-domain dialogue systems with contextualized embeddings.** *Sarik Ghazarian, Johnny Wei, Aram Galstyan, and Nanyun Peng.* `NAACL 2019 workshop` [[pdf]](https://www.aclweb.org/anthology/W19-2310.pdf) ![](https://img.shields.io/badge/ref-orange)
27. **Re-evaluating ADEM: A Deeper Look at Scoring Dialogue Responses.** *Ananya B. Sai, Mithun Das Gupta, Mitesh M. Khapra, Mukundhan Srinivasan.* `AAAI 2019` [[pdf]](https://arxiv.org/abs/1902.08832)
28. **Towards a Better Metric for Evaluating Question Generation Systems.** *Preksha Nema, Mitesh M. Khapra.* `EMNLP 2018` [[pdf]](https://www.aclweb.org/anthology/D18-1429/)
29. **The price of debiasing automatic metrics in natural language evaluation.** *Arun Tejasvi Chaganty, Stephen Mussman, Percy Liang.* `ACL 2018` [[pdf]](https://arxiv.org/abs/1807.02202) ![](https://img.shields.io/badge/ref-orange) ![](https://img.shields.io/badge/sl-pink)
30. **Ruse: Regressor using sentence embeddings for automatic machine translation evaluation.** *Hiroki Shimanaka, Tomoyuki Kajiwara, and Mamoru Komachi.* `ACL 2018 workshop` [[pdf]](https://www.aclweb.org/anthology/W18-6456/) ![](https://img.shields.io/badge/ref-orange)
31. **Towards a Metric for Automated Conversational Dialogue System Evaluation and Improvement.** *Jan Deriu, Mark Cieliebak.* `INLG 2018` [[pdf]](https://www.inlg2019.com/assets/papers/132_Paper.pdf) ![](https://img.shields.io/badge/sl-pink)
32. **Ruber: An unsupervised method for automatic evaluation of open-domain dialog systems.** *Chongyang Tao, Lili Mou, Dongyan Zhao, and Rui Yan.* `AAAI 2018` [[pdf]](https://arxiv.org/abs/1701.03079) ![](https://img.shields.io/badge/ref-orange) ![](https://img.shields.io/badge/unref-yellow)
33. **One “Ruler” for All Languages: Multi-Lingual Dialogue Evaluation with Adversarial Multi-Task Learning.** *Xiaowei Tong, Zhenxin Fu, Mingyue Shang, Dongyan Zhao, Rui Yan.* `IJCAI 2018` [[pdf]](https://www.ijcai.org/Proceedings/2018/0616.pdf)
34. **Adversarial Learning for Neural Dialogue Generation.** *Jiwei Li, Will Monroe, Tianlin Shi, Sébastien Jean, Alan Ritter, Dan Jurafsky.* `EMNLP 2017` [[pdf]](https://www.aclweb.org/anthology/D17-1230/) ![](https://img.shields.io/badge/unref-yellow)
35. **Topic-based Evaluation for Conversational Bots.** *Fenfei Guo, Angeliki Metallinou, Chandra Khatri, Anirudh Raju, Anu Venkatesh, Ashwin Ram.* `NeurIPS 2017 workshop` [[pdf]](https://arxiv.org/abs/1801.03622) ![](https://img.shields.io/badge/unref-yellow)
36. **On Evaluating and Comparing Open Domain Dialog Systems.** *Anu Venkatesh, Chandra Khatri, Ashwin Ram, Fenfei Guo, Raefer Gabriel, Ashish Nagar, Rohit Prasad, Ming Cheng, Behnam Hedayatnia, Angeliki Metallinou, Rahul Goel, Shaohua Yang, Anirudh Raju.* `NeurIPS 2017 workshop` [[pdf]](https://arxiv.org/abs/1801.03625) ![](https://img.shields.io/badge/multidim-darkgreen)
37. **Towards an automatic turing test: Learning to evaluate dialogue responses.** *Ryan Lowe, Michael Noseworthy, Iulian Vlad Serban, Nicolas Angelard-Gontier, Yoshua Bengio, and Joelle Pineau.* `ACL 2017 Best Paper` [[pdf]](https://www.aclweb.org/anthology/P17-1103.pdf) ![](https://img.shields.io/badge/sl-pink)
38. **Evaluating Story Generation Systems Using Automated Linguistic Analyses.** *Melissa Roemmele, Andrew S. Gordon, Reid Swanson.* `ACM SIGKDD 2017` [[pdf]](https://people.ict.usc.edu/gordon/public_html/publications/KDD-WS17.PDF) ![](https://img.shields.io/badge/multidim-darkgreen)
39. **Adversarial evaluation of dialogue models.** *Anjuli Kannan and Oriol Vinyals.* `arxiv 2017` [[pdf]](https://arxiv.org/abs/1701.08198) ![](https://img.shields.io/badge/unref-yellow)
40. **deltaBLEU: A Discriminative Metric for Generation Tasks with Intrinsically Diverse Targets.** *Michel Galley, Chris Brockett, Alessandro Sordoni, Yangfeng Ji, Michael Auli, Chris Quirk, Margaret Mitchell, Jianfeng Gao, Bill Dolan.* `ACL 2015` [[pdf]](https://www.aclweb.org/anthology/P15-2073/) ![](https://img.shields.io/badge/ref-orange)
41. **ROUGE: A package for automatic evaluation of summaries.** `Chin-Yew Lin.` `ACL 2004` [[pdf]](https://www.aclweb.org/anthology/W04-1013) ![](https://img.shields.io/badge/ref-orange)
42. **Bleu: a method for automatic evaluation of machine translation.** *Kishore Papineni, Salim Roukos, Todd Ward, and WeiJing Zhu.* `ACL 2002` [[pdf]](https://www.aclweb.org/anthology/P02-1040/) ![](https://img.shields.io/badge/ref-orange)



### 3.2 Protocol for human evaluation

1. **STORIUM: A Dataset and Evaluation Platform for Machine-in-the-Loop Story Generation.** *Nader Akoury, Shufan Wang, Josh Whiting, Stephen Hood, Nanyun Peng, Mohit Iyyer.* `EMNLP 2020` [[pdf]](https://arxiv.org/abs/2010.01717) 
2. **Spot The Bot: A Robust and Efficient Framework for the Evaluation of Conversational Dialogue Systems.** *Jan Deriu, Don Tuggener, Pius von Däniken, Jon Ander Campos, Alvaro Rodrigo, Thiziri Belkacem, Aitor Soroa, Eneko Agirre, Mark Cieliebak.* `EMNLP 2020` [[pdf]](https://arxiv.org/abs/2010.02140)
3. **Towards Best Experiment Design for Evaluating Dialogue System Output.** *Sashank Santhanam, Samira Shaikh.* `INLG 2019` [[pdf]](https://arxiv.org/abs/1909.10122)
4. **Communication-based Evaluation for Natural Language Generation.**  `SCiL 2019` [[pdf]](https://arxiv.org/abs/1909.07290)
5. **Domain-Independent turn-level Dialogue Quality Evaluation via User Satisfaction Estimation.**  `SIGDIAL 2019`[[pdf]](https://arxiv.org/pdf/1908.07064.pdf)
6. **ACUTE-EVAL: Improved Dialogue Evaluation with Optimized Questions and Multi-turn Comparisons.** *Margaret Li, Jason Weston, Stephen Roller.* `AAAI 2019` [[pdf]](https://arxiv.org/abs/1909.03087) 
7. **ChatEval: A Tool for the Systematic Evaluation of Chatbots.** *João Sedoc, Daphne Ippolito, Arun Kirubarajan, Jai Thirani, Lyle Ungar, Chris Callison-Burch.* `ACL 2018` [[pdf]](https://www.aclweb.org/anthology/W18-6709.pdf) 
8. **Towards a Method For Evaluating Naturalness in Conversational Dialog Systems.** *Victor Hung, Miguel Elvir, Avelino Gonzalez, Ronald DeMara.* `IEEE ICSMC 2009` [[pdf]](https://ieeexplore.ieee.org/abstract/document/5345904/) 
9. **Empirical Methods for Evaluating Dialog Systems.** *Tim Paek.* `ACL 2001` [[pdf]](https://www.aclweb.org/anthology/W01-0902.pdf)



## 4. Others

1. **If beam search is the answer, what was the question?** *Clara Meister, Tim Vieira, Ryan Cotterell.* `EMNLP 2020` [[pdf]](https://arxiv.org/abs/2010.02650)
2. **A Systematic Characterization of Sampling Algorithms for Open-ended Language Generation.** *Moin Nadeem, Tianxing He, Kyunghyun Cho, James Glass.* `AACL 2020` [[pdf]](https://arxiv.org/abs/2009.07243)

