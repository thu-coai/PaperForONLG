# Paper List for Open-eNded Language Generation (ONLG)

![](https://img.shields.io/github/last-commit/thu-coai/PaperForONLG?color=blue) ![](https://img.shields.io/badge/PaperNumber-221-brightgreen) ![](https://img.shields.io/badge/PRs-Welcome-red) 

Contributed by [Jian Guan](https://jianguanthu.github.io/), [Zhexin Zhang](https://github.com/nonstopfor), Xuekai Zhu, Zhuoer Feng

### Introduction

**O**pen-e**N**ded **L**anguage **G**eneration (ONLG) refers to those generation tasks where only very limited information is given in the input and there are many plausible output for the same input (also known as one-to-many). ONLG roughly includes chit-chat dialog/story/review/essay generation, etc.





### Some active authors in the list

[Minlie Huang](http://coai.cs.tsinghua.edu.cn/hml/), [Stephen Roller](https://stephenroller.com/), [Nanyun Peng](https://violetpeng.github.io//), [Jianfeng Gao](https://www.microsoft.com/en-us/research/people/jfgao/?from=http%3A%2F%2Fresearch.microsoft.com%2Fen-us%2Fum%2Fpeople%2Fjfgao%2F), [Joelle Pineau](https://scholar.google.com/citations?user=CEt6_mMAAAAJ&hl=zh-CN), [Angela Fan](https://ai.facebook.com/people/angela-fan/), [Jason Weston](http://www.thespermwhale.com/jaseweston/), [Ryan Lowe](https://scholar.google.ca/citations?user=iRgYMuEAAAAJ&hl=en), [Noah A. Smith](https://homes.cs.washington.edu/~nasmith/)...



### Contents

* [0. Resource](#0-resource)
* [1. Survey](#1-survey)
* [2. Generative Model](#2-generative-model)
  * [2.1 Long Texts](#21-long-texts)
  * [2.2 Dialog](#22-dialog) 
  * [2.3 MultiModal](#23-multimodal)
  * [2.4 Reasoning](#24-reasoning)
  * [2.5 Pretraining Models](#25-pretraining-models)
  * [2.6 Others](#26-others)
* [3. Evaluation](#3-evaluation)
  * [3.1 Metric](#31-metric)
  * [3.2 Protocol](#32-protocol-for-human-evaluation)
* [4. Others](#4-others)



## 0. Resource

1. **TVRecap: A Dataset for Generating Stories with Character Descriptions.** *Mingda Chen, Kevin Gimpel.* [[pdf]](https://arxiv.org/abs/2109.08833) `arxiv 2021 ` ![](https://img.shields.io/badge/story-navy)
2. **StoryDB: Broad Multi-language Narrative Dataset** *Alexey Tikhonov, Igor Samenko, Ivan P. Yamshchikov.* [[pdf]](https://arxiv.org/abs/2109.14396) `arxiv 2021` ![](https://img.shields.io/badge/story-navy)
3. **Documenting Large Webtext Corpora: A Case Study on the Colossal Clean Crawled Corpus.** *Jesse Dodge, Maarten Sap, Ana Marasović, William Agnew, Gabriel Ilharco, Dirk Groeneveld, Margaret Mitchell, Matt Gardner.* `EMNLP 2021` 
4. **Perturbation CheckLists for Evaluating NLG Evaluation Metrics.** *Ananya B. Sai,Tanay Dixit,Dev Yashpal Sheth,Sreyas Mohan,Mitesh M. Khapra.* [[pdf]](https://arxiv.org/abs/2109.05771) `EMNLP 2021` ![](https://img.shields.io/badge/story-navy)
5. **TURINGBENCH: A Benchmark Environment for Turing Test in the Age of Neural Text Generation.** *Adaku Uchendu, Zeyu Ma, Thai Le, Rui Zhang, Dongwon Lee.* [[pdf]](https://arxiv.org/abs/2109.13296) `Findings of EMNLP 2021` ![](https://img.shields.io/badge/story-navy)
6. **"Let Your Characters Tell Their Story": A Dataset for Character-Centric Narrative Understanding.** *Faeze Brahman, Meng Huang, Oyvind Tafjord, Chao Zhao, Mrinmaya Sachan, Snigdha Chaturvedi.* [[pdf]](https://arxiv.org/abs/2109.05438) `Findings of EMNLP 2021` ![](https://img.shields.io/badge/story-navy)
7. **TellMeWhy: A Dataset for Answering Why-Questions in Narratives.** *Yash Kumar Lal, Nathanael Chambers, Raymond Mooney, Niranjan Balasubramanian.* [[pdf]](https://arxiv.org/abs/2106.06132) `Findings of ACL 2021` ![](https://img.shields.io/badge/story-navy)
8. **Evaluation of Thematic Coherence in Microblogs.** *Iman Munire Bilal, Bo Wang, Maria Liakata, Rob Procter, Adam Tsakalidis.* [[pdf]](https://aclanthology.org/2021.acl-long.530/) `ACL 2021` ![](https://img.shields.io/badge/evaluation-darkred)
9. **Unsupervised Enrichment of Persona-grounded Dialog with Background Stories.** *Bodhisattwa Prasad Majumder, Taylor Berg-Kirkpatrick, Julian McAuley, Harsh Jhamtani.* [[pdf]](https://arxiv.org/abs/2106.08364) `ACL 2021` ![](https://img.shields.io/badge/story-navy) ![](https://img.shields.io/badge/dialog-gold)
10. **TuringAdvice: A Generative and Dynamic Evaluation of Language Use.** *Rowan Zellers, Ari Holtzman, Elizabeth Clark, Lianhui Qin, Ali Farhadi, Yejin Choi.* [[pdf]](https://www.aclweb.org/anthology/2021.naacl-main.386/) `ACL 2021` 
11. **CIDER: Commonsense Inference for Dialogue Explanation and Reasoning.** *Deepanway Ghosal, Pengfei Hong, Siqi Shen, Navonil Majumder, Rada Mihalcea, Soujanya Poria.* [[pdf]](https://arxiv.org/abs/2106.00510) `SIGDIAL 2021` ![](https://img.shields.io/badge/dialog-gold)
12. **OpenMEVA: A Benchmark for Evaluating Open-ended Story Generation Metrics.** *Jian Guan, Zhexin Zhang, Zhuoer Feng, Zitao Liu, Wenbiao Ding, Xiaoxi Mao, Changjie Fan, Minlie Huang.*  [[pdf]](https://arxiv.org/abs/2105.08920) [[toolkit]](https://github.com/thu-coai/OpenMEVA) `ACL 2021` ![](https://img.shields.io/badge/evaluation-darkred)
13. **Is Incoherence Surprising? Targeted Evaluation of Coherence Prediction from Language Models.** *Anne Beyer, Sharid Loáiciga, David Schlangen.* [[pdf]](https://arxiv.org/abs/2105.03495) `NAALC 2021` ![](https://img.shields.io/badge/evaluation-darkred)
14. **CLiMP: A Benchmark for Chinese Language Model Evaluation.** *Beilei Xiang, Changbing Yang, Yu Li, Alex Warstadt, Katharina Kann.* `arxiv 2021` [[pdf]](https://arxiv.org/abs/2101.11131) ![](https://img.shields.io/badge/evaluation-darkred)
15. **MultiTalk: A Highly-Branching Dialog Testbed for Diverse Conversations.** *Yao Dou, Maxwell Forbes, Ari Holtzman, Yejin Choi.* `AAAI 2021` [[pdf]](https://arxiv.org/abs/2102.01263) ![](https://img.shields.io/badge/dialog-gold)
16. **Measuring and Improving Consistency in Pretrained Language Models.** *Yanai Elazar, Nora Kassner, Shauli Ravfogel, Abhilasha Ravichander, Eduard Hovy, Hinrich Schütze, Yoav Goldberg.* `arxiv 2021` [[pdf]](https://arxiv.org/abs/2102.01017) ![](https://img.shields.io/badge/evaluation-darkred)
17. **The GEM Benchmark: Natural Language Generation, its Evaluation and Metrics.** *Sebastian Gehrmann et al.* `ACL 2021 workshop` [[pdf]](https://arxiv.org/abs/2102.01672) ![](https://img.shields.io/badge/evaluation-darkred)
18. **BOLD: Dataset and Metrics for Measuring Biases in Open-Ended Language Generation.** *Jwala Dhamala, Tony Sun, Varun Kumar, Satyapriya Krishna, Yada Pruksachatkun, Kai-Wei Chang, Rahul Gupta.* `FAccT 2021` [[pdf]](https://arxiv.org/abs/2101.11718) ![](https://img.shields.io/badge/story-navy)
19. **GLGE: A New General Language Generation Evaluation Benchmark.** *Dayiheng Liu et al.* `arxiv 2021` [[pdf]](https://arxiv.org/abs/2011.11928) ![](https://img.shields.io/badge/evaluation-darkred) 
20. **Long Range Arena: A Benchmark for Efficient Transformers.** *Yi Tay et al.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2011.04006) 
21. **STORIUM: A Dataset and Evaluation Platform for Machine-in-the-Loop Story Generation.** *Nader Akoury, Shufan Wang, Josh Whiting, Stephen Hood, Nanyun Peng, Mohit Iyyer.* `EMNLP 2020` [[pdf]](https://arxiv.org/abs/2010.01717) ![](https://img.shields.io/badge/story-navy)
22. **GLUCOSE: GeneraLized and COntextualized Story Explanations.** *Nasrin Mostafazadeh, Aditya Kalyanpur, Lori Moon, David Buchanan, Lauren Berkowitz, Or Biran, Jennifer Chu-Carroll.* `EMNLP 2020` [[pdf]](https://arxiv.org/abs/2009.07758) ![](https://img.shields.io/badge/story-navy)
23. **CommonGen: A Constrained Text Generation Challenge for Generative Commonsense Reasoning.** *Bill Yuchen Lin, Wangchunshu Zhou, Ming Shen, Pei Zhou, Chandra Bhagavatula, Yejin Choi, Xiang Ren.* `Findings of EMNLP 2020` [[pdf]](https://arxiv.org/abs/1911.03705) ![](https://img.shields.io/badge/story-navy)
24. **A Large-Scale Chinese Short-Text Conversation Dataset.** *Yida Wang, Pei Ke, Yinhe Zheng, Kaili Huang, Yong Jiang, Xiaoyan Zhu, Minlie Huang.* `NLPCC 2020` [[pdf]](https://arxiv.org/abs/2008.03946) ![](https://img.shields.io/badge/dialog-gold)
25. **Storytelling with Dialogue: A Critical Role Dungeons and Dragons Dataset.** *Revanth Rameshkumar, Peter Bailey.* `ACL 2020` [[pdf]](https://www.aclweb.org/anthology/2020.acl-main.459/) ![](https://img.shields.io/badge/story-navy)
26. **MuTual: A Dataset for Multi-Turn Dialogue Reasoning.** *Leyang Cui, Yu Wu, Shujie Liu, Yue Zhang, Ming Zhou.* `ACL 2020` [[pdf]](https://arxiv.org/abs/2004.04494) ![](https://img.shields.io/badge/dialog-gold)
27. **Designing Precise and Robust Dialogue Response Evaluators.** *Tianyu Zhao, Divesh Lala, Tatsuya Kawahara.* `ACL 2020 short paper` [[pdf]](https://arxiv.org/abs/2004.04908) ![](https://img.shields.io/badge/dialog-gold)
28. **Recollection versus Imagination: Exploring Human Memory and Cognition via Neural Language Models.** *Maarten Sap, Eric Horvitz, Yejin Choi, Noah A. Smith, James Pennebaker.* `ACL 2020` [[pdf]](https://www.aclweb.org/anthology/2020.acl-main.178/) ![](https://img.shields.io/badge/story-navy)
29. **Exploring the Effect of Author and Reader Identity in Online Story Writing: the STORIESINTHEWILD Corpus.** *Tal August, Maarten Sap, Elizabeth Clark, Katharina Reinecke, Noah A. Smith.* `ACL 2020` [[pdf]](https://www.aclweb.org/anthology/2020.nuse-1.6/) ![](https://img.shields.io/badge/story-navy)
30. **Story Realization: Expanding Plot Events into Sentences.** *Prithviraj Ammanabrolu, Ethan Tien, Wesley Cheung, Zhaochen Luo, William Ma, Lara J. Martin, and Mark O. Riedl.* `AAAI 2020` [[pdf]](https://arxiv.org/abs/1909.03480) [[data] ](https://huggingface.co/datasets/lara-martin/Scifi_TV_Shows) ![](https://img.shields.io/badge/story-navy)
31. **Counterfactual Story Reasoning and Generation.** *Lianhui Qin, Antoine Bosselut, Ari Holtzman, Chandra Bhagavatula, Elizabeth Clark, Yejin Choi.* `EMNLP 2019` [[pdf]](https://arxiv.org/abs/1909.04076) ![](https://img.shields.io/badge/story-navy)
32. **Hierarchical neural story generation.** *Angela Fan, Mike Lewis, and Yann Dauphin.* `ACL 2018` [[pdf]](https://www.aclweb.org/anthology/P18-1082.pdf) ![](https://img.shields.io/badge/story-navy)
33. **Modeling Naive Psychology of Characters in Simple Commonsense Stories.** *Hannah Rashkin, Antoine Bosselut, Maarten Sap, Kevin Knight, Yejin Choi.* `ACL 2018` [[pdf]](https://www.aclweb.org/anthology/P18-1213) ![](https://img.shields.io/badge/story-navy)
34. **LSDSCC: a Large Scale Domain-Specific Conversational Corpus for Response Generation with Diversity Oriented Evaluation Metrics.** *Zhen Xu, Nan Jiang, Bingquan Liu, Wenge Rong, Bowen Wu, Baoxun Wang, Zhuoran Wang, Xiaolong Wang.* `NAACL 2018` [[pdf]](https://www.aclweb.org/anthology/N18-1188/) ![](https://img.shields.io/badge/dialog-gold)
35. **Visual storytelling.** *Ting-Hao Kenneth Huang, Francis Ferraro, Nasrin Mostafazadeh, Ishan Misra, Aishwarya Agrawal, Jacob Devlin, Ross Girshick, Xiaodong He, Pushmeet Kohli, Dhruv Batra, C. Lawrence Zitnick, Devi Parikh, Lucy Vanderwende, Michel Galley, Margaret Mitchell.* `NAACL 2016` [[pdf]](https://www.aclweb.org/anthology/N16-1147/) ![](https://img.shields.io/badge/story-navy)
36. **CaTeRS: Causal and Temporal Relation Scheme for Semantic Annotation of Event Structures.** *Nasrin Mostafazadeh, Alyson Grealish, Nathanael Chambers, James Allen, Lucy Vanderwende.* `ACL 2016 workshop` [[pdf]](https://www.aclweb.org/anthology/W16-1007/) ![](https://img.shields.io/badge/story-navy)
37. **A Corpus and Cloze Evaluation for Deeper Understanding of Commonsense Stories.** *Nasrin Mostafazadeh, Nathanael Chambers, Xiaodong He, Devi Parikh, Dhruv Batra, Lucy Vanderwende, Pushmeet Kohli, James Allen.* `NAACL 2016` [[pdf]](https://www.aclweb.org/anthology/N16-1098/) ![](https://img.shields.io/badge/story-navy)
38. **WikiPlots.** *Mark Ridel.* `Github 2017` [[link]](https://github.com/markriedl/WikiPlots) ![](https://img.shields.io/badge/story-navy)

## 1. Survey

1. **Survey of Hallucination in Natural Language Generation.** *Ziwei Ji, Nayeon Lee, Rita Frieske, Tiezheng Yu, Dan Su, Yan Xu, Etsuko Ishii, Yejin Bang, Andrea Madotto, Pascale Fung.* [[pdf]](https://arxiv.org/abs/2202.03629)
2. **Repairing the Cracked Foundation: A Survey of Obstacles in Evaluation Practices for Generated Text.** *Google.* [[pdf]](https://arxiv.org/abs/2202.06935) ![](https://img.shields.io/badge/evaluation-darkred)
3. **State-of-the-Art in Automated Story Generation Systems Research.** *Rebeca Amaya Ansag, Avelino J. Gonzalez.* `Journal of Experimental & Theoretical Artificial Intelligence 2021.` [[pdf]](https://www.tandfonline.com/doi/abs/10.1080/0952813X.2021.1971777) ![](https://img.shields.io/badge/story-navy) 
4. **A Systematic Investigation of Commonsense Understanding in Large Language Models.** *Xiang Lorraine Li, Adhi Kuncoro, Cyprien de Masson d'Autume, Phil Blunsom, Aida Nematzadeh.* [[pdf]](https://arxiv.org/abs/2111.00607) `arxiv 2021`
5. **Retrieving and Reading : A Comprehensive Survey on Open-domain Question Answering.** *Fengbin Zhu, Wenqiang Lei, Chao Wang, Jianming Zheng, Soujanya Poria, Tat-Seng Chua.* [[pdf]](https://arxiv.org/abs/2101.00774) `arxiv 2021`
6. **Automatic story generation: A survey of approaches.** *ARWA I. ALHUSSAIN and AQIL M. AZMI.* `ACM computing surveys 2021` [[pdf]](https://dl.acm.org/doi/abs/10.1145/3453156) ![](https://img.shields.io/badge/story-navy) 
7. **Automatic Story Generation: Challenges and Attempts.** *Amal Alabdulkarim, Siyan Li, Xiangyu Peng.* `ACL 2021` [[pdf]](https://www.aclweb.org/anthology/2021.nuse-1.8/) ![](https://img.shields.io/badge/story-navy)
8. **Eﬃcient Transformers: A Survey.** *Yi Tay, Mostafa Dehghani, Dara Bahri, Donald Metzler.* [[pdf]](https://arxiv.org/abs/2009.06732) `arxiv 2020`
9. **Combining pre-trained language models and structured knowledge.** *Pedro Colon-Hernandez, Catherine Havasi, Jason Alonso, Matthew Huggins, Cynthia Breazeal.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2101.12294) ![](https://img.shields.io/badge/knowledge-red)
10. **A Survey of Knowledge-Enhanced Text Generation.** *Wenhao Yu, Chenguang Zhu, Zaitang Li, Zhiting Hu, Qingyun Wang, Heng Ji, Meng Jiang.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2010.04389) ![](https://img.shields.io/badge/dialog-gold) ![](https://img.shields.io/badge/story-navy) ![](https://img.shields.io/badge/knowledge-red)
11. **Automatic Story Generation: State of the Art and Recent Trends.**  *Brian Daniel Herrera-González, Alexander Gelbukh, and Hiram Calvo.* `MICA 2020` [[pdf]](https://link.springer.com/chapter/10.1007%2F978-3-030-60887-3_8) ![](https://img.shields.io/badge/story-navy)
12. **Towards Unified Dialogue System Evaluation: A Comprehensive Analysis of Current Evaluation Protocols.** *Sarah E. Finch, Jinho D. Choi.* `SIGDIAL 2020` [[pdf]](https://arxiv.org/abs/2006.06110) ![](https://img.shields.io/badge/dialog-gold)
13. **Challenges in Building Intelligent Open-domain Dialog Systems.** *Minlie Huang, Xiaoyan Zhu, Jianfeng Gao.* `TOIS 2020` [[pdf]](https://dl.acm.org/doi/abs/10.1145/3383123) ![](https://img.shields.io/badge/dialog-gold)
14. **Open-Domain Conversational Agents: Current Progress, Open Problems, and Future Directions.** *Stephen Roller, Y-Lan Boureau, Jason Weston, Antoine Bordes, Emily Dinan, Angela Fan, David Gunning, Da Ju, Margaret Li, Spencer Poff, Pratik Ringshia, Kurt Shuster, Eric Michael Smith, Arthur Szlam, Jack Urbanek, Mary Williamson.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2006.12442) ![](https://img.shields.io/badge/dialog-gold)
15. **A Survey of Evaluation Metrics Used for NLG Systems.** *Ananya B. Sai, Akash Kumar Mohankumar, Mitesh M. Khapra.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2008.12009) ![](https://img.shields.io/badge/evaluation-darkred)
16. **Evaluation of Text Generation: A Survey.** *Asli Celikyilmaz, Elizabeth Clark, Jianfeng Gao.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2006.14799) ![](https://img.shields.io/badge/evaluation-darkred)
17. **Survey on evaluation methods for dialogue systems.** *Jan Deriu, Alvaro Rodrigo, Arantxa Otegi, Guillermo Echegoyen, Sophie Rosset, Eneko Agirre & Mark Cieliebak.* `Artificial Intelligence Review 2020` [[pdf]](https://link.springer.com/article/10.1007/s10462-020-09866-x) ![](https://img.shields.io/badge/dialog-gold) ![](https://img.shields.io/badge/evaluation-darkred)  
18. **Judge the Judges: A Large-Scale Evaluation Study of Neural Language Models for Online Review Generation.** *Cristina Garbacea, Samuel Carton, Shiyan Yan, Qiaozhu Mei.* `arxiv 2019` [[pdf]](https://arxiv.org/abs/1901.00398) ![](https://img.shields.io/badge/evaluation-darkred)
19. **How NOT To Evaluate Your Dialogue System: An Empirical Study of Unsupervised Evaluation Metrics for Dialogue Response Generation.** *Chia-Wei Liu, Ryan Lowe, Iulian Serban, Mike Noseworthy, Laurent Charlin, Joelle Pineau.* `EMNLP 2016` [[pdf]](https://www.aclweb.org/anthology/D16-1230/) ![](https://img.shields.io/badge/dialog-gold) ![](https://img.shields.io/badge/evaluation-darkred)
20. **对话系统评价方法综述** *张伟男, 张杨子, 刘挺.* `中国科学 : 信息科学` [[pdf]](http://scis.scichina.com/cn/2017/N112017-00125.pdf) ![](https://img.shields.io/badge/dialog-gold) ![](https://img.shields.io/badge/evaluation-darkred)
21. **A Survey of Available Corpora for Building Data-Driven Dialogue Systems.** *Iulian Vlad Serban, Ryan Lowe, Peter Henderson, Laurent Charlin, Joelle Pineau.* `arxiv 2015` [[pdf]](https://arxiv.org/abs/1512.05742) ![](https://img.shields.io/badge/dialog-gold)
22. **A Survey of Transformers.** *Tianyang Lin, Yuxin Wang, Xiangyang Liu, Xipeng Qiu.* `arxiv 2021` [[pdf]](https://arxiv.org/abs/2106.04554)
23. **Pretrained Language Models for Text Generation: A Survey.** *Junyi Li, Tianyi Tang, Wayne Xin Zhao, Ji-Rong Wen.* `arxiv 2021` [[pdf]](https://arxiv.org/abs/2105.10311)


## 2. Generative Model

![](https://img.shields.io/badge/planning-planning-brightgreen) ![](https://img.shields.io/badge/knowledge-knowledge-red) ![](https://img.shields.io/badge/PreTrainingModel-ptm-blue)

### 2.1 Long Texts

1. **Language modeling via stochastic processes.** *Rose E Wang, Esin Durmus, Noah Goodman, Tatsunori Hashimoto.* `ICLR 2022` [[pdf]](https://openreview.net/forum?id=pMQwKL1yctf) ![](https://img.shields.io/badge/planning-brightgreen)
2. **Towards Coherent and Consistent Use of Entities in Narrative Generation.** *Pinelopi Papalampidi, Kris Cao, Tomas Kocisky.* `arxiv 2022` [[pdf]](https://arxiv.org/abs/2202.01709)
3. **Guiding Neural Story Generation with Reader Models.** *Xiangyu Peng, Kaige Xie, Amal Alabdulkarim, Harshith Kayam, Samihan Dani, Mark O. Riedl* `arixv 2021` [[pdf]](https://arxiv.org/pdf/2112.08596.pdf) ![](https://img.shields.io/badge/knowledge-red)
4. **Goal-Directed Story Generation: Augmenting Generative Language Models with Reinforcement Learning.** *Amal Alabdulkarim, Winston Li, Lara J. Martin, Mark O. Riedl.* `arixv 2021` [[pdf]](https://arxiv.org/abs/2112.08593)
5. **Unsupervised Editing for Counterfactual Stories.** *Jiangjie Chen, Chun Gan, Sijie Cheng, Hao Zhou, Yanghua Xiao, Lei Li.* `AAAI 2022` [[pdf]](https://arxiv.org/abs/2112.05417)
6. **Simple Local Attentions Remain Competitive for Long-Context Tasks.** *Meta AI.* [[pdf]](https://arxiv.org/abs/2112.07210) `arxiv 2021`
7. **TopNet: Learning from Neural Topic Model to Generate Long Stories.** *Yazheng Yang, Boyuan Pan, Deng Cai, Huan Sun.* [[pdf]](https://arxiv.org/abs/2112.07259) `kdd 2021`
8. **Automated Story Generation as Question-Answering.** *Louis Castricato, Spencer Frazier, Jonathan Balloch, Nitya Tarakad, Mark Riedl.* [[pdf]](https://arxiv.org/abs/2112.03808) `arxiv 2021`
9. **Automated Story Generation as Question-Answering.** *Louis Castricato, Spencer Frazier, Jonathan Balloch, Nitya Tarakad, Mark Riedl.* [[pdf]](https://arxiv.org/abs/2112.03808) `AAAI 2022`
10. **DCT: Dynamic Compressive Transformer for Modeling Unbounded Sequence.** *Kai-Po Chang, Wei-Yun Ma.* [[pdf]](https://arxiv.org/abs/2110.04821) `arxiv 2021`
11. **Hierarchical Transformers Are More Efficient Language Models.** *Piotr Nawrot, Szymon Tworkowski, Michał Tyrolski, Łukasz Kaiser, Yuhuai Wu, Christian Szegedy, Henryk Michalewski.* [[pdf]](https://arxiv.org/abs/2110.13711) `arxiv 2021`
12. **GNN-LM: Language Modeling based on Global Contexts via GNN.** *Yuxian Meng, Shi Zong, Xiaoya Li, Xiaofei Sun, Tianwei Zhang, Fei Wu, Jiwei Li.* [[pdf]](https://arxiv.org/abs/2110.08743) `arxiv 2021`
13. **GGP: A Graph-based Grouping Planner for Explicit Control of Long Text Generation.** *Xuming Lin, Shaobo Cui, Zhongzhou Zhao, Wei Zhou, Ji Zhang, Haiqing Chen.* [[pdf]](https://arxiv.org/abs/2108.07998) `CIKM 2021` ![](https://img.shields.io/badge/planning-brightgreen)
14. **Building the Directed Semantic Graph for Coherent Long Text Generation.** *Ziao Wang, Xiaofeng Zhang, Hongwei Du.* `EMNLP 2021` [[pdf]](https://aclanthology.org/2021.emnlp-main.200/) ![](https://img.shields.io/badge/planning-brightgreen)
15. **DiscoDVT: Generating Long Text with Discourse-Aware Discrete Variational Transformer.** *Haozhe Ji, Minlie Huang.* `EMNLP 2021` [[pdf]](https://arxiv.org/abs/2110.05999)![](https://img.shields.io/badge/planning-brightgreen)
16. **A Temporal Variational Model for Story Generation.** *David Wilmot, Frank Keller.* [[pdf]](https://arxiv.org/abs/2109.06807) `arxiv 2021` ![](https://img.shields.io/badge/planning-brightgreen)
17. **Wordcraft: a Human-AI Collaborative Editor for Story Writing.** *Google.* [[pdf]](https://arxiv.org/abs/2107.07430) `arxiv 2021`
18. **Inferring the Reader: Guiding Automated Story Generation with Commonsense Reasoning.** *Xiangyu Peng, Siyan Li, Sarah Wiegreffe, Mark Riedl.* [[pdf]](https://arxiv.org/abs/2105.01311) `arxiv 2021`  ![](https://img.shields.io/badge/knowledge-red)
19. **COINS: Dynamically Generating COntextualized Inference Rules for Narrative Story Completion.** *Debjit Paul, Anette Frank.* [[pdf]](https://arxiv.org/abs/2106.02497) `ACL 2021` ![](https://img.shields.io/badge/planning-brightgreen)
20. **Long Text Generation by Modeling Sentence-Level and Discourse-Level Coherence.** *Jian Guan, Xiaoxi Mao, changjie fan, Zitao Liu, Wenbiao Ding, Minlie Huang.*  [[pdf]](https://arxiv.org/abs/2105.08963) [[code]](https://github.com/thu-coai/HINT)  `ACL 2021` ![](https://img.shields.io/badge/ptm-blue)
21. **Stylized Story Generation with Style-Guided Planning.** *Xiangzhe Kong, Jialiang Huang, Ziquan Tung, Jian Guan and Minlie Huang.* [[pdf]](https://arxiv.org/abs/2105.08625) [[code]](https://github.com/thu-coai/Stylized-Story-Generation-with-Style-Guided-Planning)  `Findings of ACL 2021` ![](https://img.shields.io/badge/planning-brightgreen)
22. **Changing the Mind of Transformers for Topically-Controllable Language Generation.** *Haw-Shiuan Chang, Jiaming Yuan, Mohit Iyyer, Andrew McCallum.* [[pdf]](https://arxiv.org/abs/2103.15335) `EACL 2021` 
23. **Plug-and-Blend: A Framework for Plug-and-Play Controllable Story Generation with Sketches.** *Zhiyu Lin, Mark O. Riedl.* [[pdf]](https://ojs.aaai.org/index.php/AIIDE/article/view/18891) `AAAI 2021` ![](https://img.shields.io/badge/planning-brightgreen)
24. **Sketch and Customize: A Counterfactual Story Generator.** *Changying Hao, Liang Pang, Yanyan Lan, Yan Wang, Jiafeng Guo, Xueqi Cheng.* [[pdf]](https://arxiv.org/abs/2104.00929) `AAAI 2021` ![](https://img.shields.io/badge/planning-brightgreen)
25. **Automated Storytelling via Causal, Commonsense Plot Ordering.** *Prithviraj Ammanabrolu, Wesley Cheung, William Broniec, Mark O. Riedl.* [[pdf]](https://arxiv.org/abs/2009.00829) `AAAI 2021` ![](https://img.shields.io/badge/knowledge-red)
26. **GraphPlan: Story Generation by Planning with Event Graph.** *Hong Chen, Raphael Shu, Hiroya Takamura, Hideki Nakayama.* [[pdf]](https://arxiv.org/abs/2102.02977) `arxiv 2021` ![](https://img.shields.io/badge/planning-brightgreen)
27. **Facts2Story: Controlling Text Generation by Key Facts.** *Eyal Orbach, Yoav Goldberg.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2012.04332) ![](https://img.shields.io/badge/planning-brightgreen)
28. **Story Generation with Rich Details.** *Fangzhou Zhai, Vera Demberg, Alexander Koller.* `COLING 2020`  [[pdf]](https://www.aclweb.org/anthology/2020.coling-main.212/)  ![](https://img.shields.io/badge/planning-brightgreen)
29. **Consistency and Coherency Enhanced Story Generation.** *Wei Wang, Piji Li, Hai-Tao Zheng.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2010.08822) ![](https://img.shields.io/badge/planning-brightgreen)
30. **Narrative Interpolation for Generating and Understanding Stories.** *Su Wang, Greg Durrett, Katrin Erk.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2008.07466) ![](https://img.shields.io/badge/planning-brightgreen)
31. **Plan-CVAE: A Planning-based Conditional Variational Autoencoder for Story Generation.** *Lin Wang, Juntao Li , Dongyan Zhao, Rui Yan.* `CCL 2020` [[pdf]](http://www.cips-cl.org/static/anthology/CCL-2020/CCL-20-083.pdf) ![](https://img.shields.io/badge/planning-brightgreen)
32. **Controllable Multi-Character Psychology-Oriented Story Generation.** *Feifei Xu, Xinpeng Wang, Yunpu Ma, Volker Tresp, Yuyi Wang, Shanlin Zhou, Haizhou Du.* `CIKM 2020` [[pdf]](https://dl.acm.org/doi/pdf/10.1145/3340531.3411937) ![](https://img.shields.io/badge/planning-brightgreen) ![](https://img.shields.io/badge/emotion-cyan)
33. **Creative Storytelling with Language Models and Knowledge Graphs.** *Xinran Yang, Ilaria Tiddi.* `CIKM 2020 workshop` [[pdf]](http://ceur-ws.org/Vol-2699/paper07.pdf) ![](https://img.shields.io/badge/knowledge-red)
34. **Modeling Protagonist Emotions for Emotion-Aware Storytelling.** *Faeze Brahman, Snigdha Chaturvedi.* `EMNLP 2020` [[pdf]](https://arxiv.org/abs/2010.06822) ![](https://img.shields.io/badge/planning-brightgreen) ![](https://img.shields.io/badge/emotion-cyan)
35. **PlotMachines: Outline-Conditioned Generation with Dynamic Plot State Tracking.** *Hannah Rashkin, Asli Celikyilmaz, Yejin Choi, Jianfeng Gao.* `EMNLP 2020` [[pdf]](https://www.aclweb.org/anthology/2020.emnlp-main.349/) ![](https://img.shields.io/badge/planning-brightgreen)
36. **Cue Me In: Content-Inducing Approaches to Interactive Story Generation.** *Faeze Brahman, Alexandru Petrusca, Snigdha Chaturvedi.* `AACL 2020` [[pdf]](https://arxiv.org/abs/2010.09935) ![](https://img.shields.io/badge/planning-brightgreen)
37. **Content Planning for Neural Story Generation with Aristotelian Rescoring.** *Seraphina Goldfarb-Tarrant, Tuhin Chakrabarty, Ralph Weischedel, Nanyun Peng.* `EMNLP 2020` [[pdf]](https://arxiv.org/abs/2009.09870) ![](https://img.shields.io/badge/planning-brightgreen)
38. **MEGATRON-CNTRL: Controllable Story Generation with External Knowledge Using Large-Scale Language Models.** *Peng Xu, Mostofa Patwary, Mohammad Shoeybi, Raul Puri, Pascale Fung, Anima Anandkumar, Bryan Catanzaro.* `EMNLP 2020` [[pdf]](https://arxiv.org/abs/2010.00840) ![](https://img.shields.io/badge/knowledge-red)
39. **A Knowledge-Enhanced Pretraining Model for Commonsense Story Generation.** *Jian Guan, Fei Huang, Zhihao Zhao, Xiaoyan Zhu, Minlie Huang*. `TACL 2020` [[pdf]](https://www.mitpressjournals.org/doi/pdf/10.1162/tacl_a_00302) ![](https://img.shields.io/badge/knowledge-red)
40. **Improving Neural Story Generation by Targeted Common Sense Grounding.** *Huanru Henry Mao, Bodhisattwa Prasad Majumder, Julian McAuley, Garrison Cottrell.* `EMNLP 2020` [[pdf]](https://www.aclweb.org/anthology/D19-1615/) ![](https://img.shields.io/badge/knowledge-red)
41. **A Character-Centric Neural Model for Automated Story Generation.** *Rui Yan et al.* `AAAI 2020` [[pdf]](https://ojs.aaai.org/index.php/AAAI/article/view/5536) ![](https://img.shields.io/badge/planning-brightgreen)
42. **Narrative Interpolation for Generating and Understanding Stories.** *Su Wang, Greg Durrett, Katrin Erk.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2008.07466)
43. **Strategies for structuring story generation.** *Angela Fan, Mike Lewis, and Yann Dauphin.* `ACL 2019` [[pdf]](https://www.aclweb.org/anthology/P19-1254) ![](https://img.shields.io/badge/planning-brightgreen)
44. **Plan-and-write: Towards better automatic storytelling.** *Lili Yao, Nanyun Peng, Ralph Weischedel, Kevin Knight, Dongyan Zhao, and Rui Yan.* `AAAI 2019` [[pdf]](https://www.aaai.org/ojs/index.php/AAAI/article/view/4726) ![](https://img.shields.io/badge/planning-brightgreen)
45. **Story ending generation with incremental encoding and commonsense knowledge.** *Jian Guan, Yansen Wang, and Minlie Huang.* `AAAI 2019` [[pdf]](https://www.aaai.org/ojs/index.php/AAAI/article/view/4612) ![](https://img.shields.io/badge/knowledge-red)
46. **Learning to Write Stories with Thematic Consistency and Wording Novelty**. *Juntao Li, Lidong Bing, Lisong Qiu, Dongmin Chen, Dongyan Zhao, and Rui Yan.* `AAAI 2019` [[pdf]](https://www.aaai.org/ojs/index.php/AAAI/article/view/3993/3871) 
47. **T-CVAE: Transformer-Based Conditioned Variational Autoencoder for Story Completion.** *Tianming Wang and Xiaojun Wan.* `IJCAI 2019` [[pdf]](http://184pc128.csie.ntnu.edu.tw/presentation/20-04-27/T-CVAE-%20Transformer-Based%20Conditioned%20Variational%20Autoencoder%20for%20Story%20Completion.pdf) ![](https://img.shields.io/badge/planning-brightgreen)
48. **Learning to Predict Explainable Plots for Neural Story Generation**. *Gang Chen, Yang Liu, Huanbo Luan, Meng Zhang, Qun Liu, and Maosong Sun.* `arxiv 2019` [[pdf]](https://arxiv.org/abs/1912.02395) ![](https://img.shields.io/badge/planning-brightgreen)
49. **Hierarchical neural story generation.** *Angela Fan, Mike Lewis, and Yann Dauphin.* `ACL 2018` [[pdf]](https://www.aclweb.org/anthology/P18-1082.pdf)
50. **Discourse-Aware Neural Rewards for Coherent Text Generation.** *Antoine Bosselut, Asli Celikyilmaz, Xiaodong He, Jianfeng Gao, Po-Sen Huang, Yejin Choi.* `ACL 2018` [[pdf]](https://www.aclweb.org/anthology/N18-1016/)
51. **A skeleton-based model for promoting coherence among sentences in narrative story generation.** *Jingjing Xu, Xuancheng Ren, Yi Zhang, Qi Zeng, Xiaoyan Cai, and Xu Sun.* `EMNLP 2018` [[pdf]](https://www.aclweb.org/anthology/D18-1462/) ![](https://img.shields.io/badge/planning-brightgreen)
52. **Event representations for automated story generation with deep neural nets.** *Lara Martin, Prithviraj Ammanabrolu, Xinyu Wang, William Hancock, Shruti Singh, Brent Harrison, and Mark Riedl.* `AAAI 2018` [[pdf]](https://arxiv.org/abs/1706.01331)
53. **Discourse-Driven Narrative Generation with Bipartite Planning.** *David R. Winer and R. Michael Young.* `ACL 2016` [[pdf]](https://www.aclweb.org/anthology/W16-6602/) ![](https://img.shields.io/badge/planning-brightgreen)
54. **Story Generation with Crowdsourced Plot Graphs.** *Boyang Li, Stephen Lee-Urban, George Johnston, and Mark O. Riedl.* `AAAI 2012 ` [[pdf]](https://ojs.aaai.org/index.php/AAAI/article/view/8649)  ![](https://img.shields.io/badge/planning-brightgreen)

### 2.2 Dialog

1. **A Joint Model for Dropped Pronoun Recovery and Conversational Discourse Parsing in Chinese Conversational Speech.** *Jingxuan Yang, Kerui Xu, Jun Xu, Si Li, Sheng Gao, Jun Guo, Nianwen Xue, Ji-Rong Wen.* `ACL 2021` [[pdf]](https://arxiv.org/abs/2106.03345) 
2. **Discovering Dialog Structure Graph for Open-Domain Dialog Generation.** *Jun Xu, Zeyang Lei, Haifeng Wang, Zheng-Yu Niu, Hua Wu, Wanxiang Che, Ting Liu.* `ACL 2021` [[pdf]](https://arxiv.org/abs/2012.15543) ![](https://img.shields.io/badge/planning-brightgreen)
3. **CARE: Commonsense-Aware Emotional Response Generation with Latent Concepts,** *Peixiang Zhong, Di Wang, Pengfei Li, Chen Zhang, Hao Wang, Chunyan Miao.* `AAAI 2021` [[pdf]](https://arxiv.org/abs/2012.08377v1) ![](https://img.shields.io/badge/knowledge-red) ![](https://img.shields.io/badge/emotion-cyan)
4. **DiSCoL: Toward Engaging Dialogue Systems through Conversational Line Guided Response Generation.** *Sarik Ghazarian, Zixi Liu, Tuhin Chakrabarty, Xuezhe Ma, Aram Galstyan, Nanyun Peng.* `arxiv 2021` [[pdf]](https://arxiv.org/abs/2102.02191) ![](https://img.shields.io/badge/planning-brightgreen)
5. **Keyword-Guided Neural Conversational Model.** *Peixiang Zhong, Yong Liu, Hao Wang, Chunyan Miao.* `AAAI 2021` [[pdf]](https://arxiv.org/abs/2012.08383) ![](https://img.shields.io/badge/planning-brightgreen)
6. **Learning to Plan and Realize Separately for Open-Ended Dialogue Systems.** *Sashank Santhanam, Zhuo Cheng, Brodie Mather, Bonnie Dorr, Archna Bhatia, Bryanna Hebenstreit, Alan Zemel, Adam Dalton, Tomek Strzalkowski, Samira Shaikh.* `Findings of EMNLP 2020` [[pdf]](https://arxiv.org/abs/2009.12506) ![](https://img.shields.io/badge/planning-brightgreen)
7. **A Large-Scale Chinese Short-Text Conversation Dataset.** *Yida Wang, Pei Ke, Yinhe Zheng, Kaili Huang, Yong Jiang, Xiaoyan Zhu, Minlie Huang.* `NLPCC 2020` [[pdf]](https://arxiv.org/abs/2008.03946) ![](https://img.shields.io/badge/ptm-blue)
8. **DIALOGPT : Large-Scale Generative Pre-training for Conversational Response Generation.** *Yizhe Zhang, Siqi Sun, Michel Galley, Yen-Chun Chen, Chris Brockett, Xiang Gao, Jianfeng Gao, Jingjing Liu, Bill Dolan.* `ACL 2020` [[pdf]](https://www.aclweb.org/anthology/2020.acl-demos.30/) ![](https://img.shields.io/badge/ptm-blue)
9. **Target-Guided Open-Domain Conversation.** *Jianheng Tang, Tiancheng Zhao, Chenyan Xiong, Xiaodan Liang, Eric Xing, Zhiting Hu.* [[pdf]](https://www.aclweb.org/anthology/P19-1565/) 
10. **Recipes for building an open-domain chatbot.** *Stephen Roller, Emily Dinan, Naman Goyal, Da Ju, Mary Williamson, Yinhan Liu, Jing Xu, Myle Ott, Kurt Shuster, Eric M. Smith, Y-Lan Boureau, Jason Weston.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2004.13637) ![](https://img.shields.io/badge/ptm-blue)
11. **Towards a Human-like Open-Domain Chatbot.** *Daniel Adiwardana, Minh-Thang Luong, David R. So, Jamie Hall, Noah Fiedel, Romal Thoppilan, Zi Yang, Apoorv Kulshreshtha, Gaurav Nemade, Yifeng Lu, Quoc V. Le.*  `arxiv 2020` [[pdf]](https://arxiv.org/abs/2001.09977) ![](https://img.shields.io/badge/ptm-blue)
12. **Adversarial Learning for Neural Dialogue Generation.** *Jiwei Li, Will Monroe, Tianlin Shi, Sébastien Jean, Alan Ritter, Dan Jurafsky.* `EMNLP 2017` [[pdf]](https://www.aclweb.org/anthology/D17-1230/)

### 2.3 MultiModal

1. **VisualCOMET: Reasoning about the Dynamic Context of a Still Image** *Jae Sung Park,  Chandra Bhagavatula,  Roozbeh Mottaghi, Ali Farhadi,  Yejin Choi.* `ECCV 2020` [[pdf]](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123500494.pdf)
2. **CapWAP: Image Captioning with a Purpose.** *Adam Fisch, Kenton Lee, Ming-Wei Chang, Jonathan Clark, Regina Barzilay.* `EMNLP 2020` [[pdf]](https://www.aclweb.org/anthology/2020.emnlp-main.705/) ![](https://img.shields.io/badge/dialog-gold)
3. **Transitional Adaptation of Pretrained Models for Visual Storytelling.** *Youngjae Yu, Jiwan Chung, Heeseung Yun, Jongseok Kim, Gunhee Kim.* `CVPR 2021` [[pdf]](https://openaccess.thecvf.com/content/CVPR2021/papers/Yu_Transitional_Adaptation_of_Pretrained_Models_for_Visual_Storytelling_CVPR_2021_paper.pdf)
4. **VinVL: Revisiting Visual Representations in Vision-Language Models.** *Pengchuan Zhang, Xiujun Li, Xiaowei Hu, Jianwei Yang, Lei Zhang, Lijuan Wang, Yejin Choi, Jianfeng Gao.* `CVPR 2021` [[pdf]](https://openaccess.thecvf.com/content/CVPR2021/html/Zhang_VinVL_Revisiting_Visual_Representations_in_Vision-Language_Models_CVPR_2021_paper.html)

### 2.4 Reasoning

1. **Reconstructing Implicit Knowledge with Language Models.** *Maria Becker, Siting Liang, Anette Frank.* [[pdf]](https://aclanthology.org/2021.deelio-1.2/) `NAACL 2021`
2. **Differentiable Open-Ended Commonsense Reasoning.** *Bill Yuchen Lin, Haitian Sun, Bhuwan Dhingra, Manzil Zaheer, Xiang Ren, William W. Cohen.* [[pdf]](https://arxiv.org/abs/2010.14439) `NAACL 2021`
3. **Does External Knowledge Help Explainable Natural Language Inference? Automatic Evaluation vs. Human Ratings.** *Hendrik Schuff, Hsiu-Yu Yang, Heike Adel, Ngoc Thang Vu.* [[pdf]](https://arxiv.org/abs/2109.07833) `EMNLP 2021 workshop`
4. **Salience-Aware Event Chain Modeling for Narrative Understanding.** *Xiyang Zhang, Muhao Chen, Jonathan May.* [[pdf]](https://arxiv.org/abs/2109.10475) `EMNLP 2021`
5. **Text2Event: Controllable Sequence-to-Structure Generation for End-to-end Event Extraction.** *Yaojie Lu, Hongyu Lin, Jin Xu, Xianpei Han, Jialong Tang, Annan Li, Le Sun, Meng Liao, Shaoyi Chen.* [[pdf]](https://arxiv.org/abs/2106.09232) `ACL 2021`
6. **Modeling Event Salience in Narratives via Barthes' Cardinal Functions.** *Takaki Otake, Sho Yokoi, Naoya Inoue, Ryo Takahashi, Tatsuki Kuribayashi, Kentaro Inui.* [[pdf]](https://arxiv.org/abs/2011.01785) `COLING 2020`
7. **EIGEN: Event Influence GENeration using Pre-trained Language Models.** *Aman Madaan, Dheeraj Rajagopal, Yiming Yang, Abhilasha Ravichander, Eduard Hovy, Shrimai Prabhumoye.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2010.11764)
8. **Playing Text-Based Games with Common Sense.** *Sahith Dambekodi, Spencer Frazier, Prithviraj Ammanabrolu, Mark O. Riedl.* [[pdf]](https://arxiv.org/abs/2012.02757) `NeurIPS 2020`
9. **Leap-Of-Thought: Teaching Pre-Trained Models to Systematically Reason Over Implicit Knowledge.** *Alon Talmor, Oyvind Tafjord, Peter Clark, Yoav Goldberg, Jonathan Berant.*  `NeurIPS 2020` [[pdf]](https://arxiv.org/abs/2006.06609)
10. **Back to the Future: Unsupervised Backprop-based Decoding for Counterfactual and Abductive Commonsense Reasoning.** *Lianhui Qin, Vered Shwartz, Peter West, Chandra Bhagavatula, Jena D. Hwang, Ronan Le Bras, Antoine Bosselut, Yejin Choi.* `EMNLP 2020` [[pdf]](https://aclanthology.org/2020.emnlp-main.58/)
11. **Scene Restoring for Narrative Machine Reading Comprehension.** *Zhixing Tian, Yuanzhe Zhang, Kang Liu, Jun Zhao, Yantao Jia, Zhicheng Sheng.* `EMNLP 2020` [[pdf]](https://aclanthology.org/2020.emnlp-main.247/) 

### 2.5 Pretraining Models

Regarding `parameter-efficient tuning (prompt/prefix tuning)`, `plug-and-play`, `adapter` and `general pretraining moddels`

1. **Context-Tuning: Learning Contextualized Prompts for Natural Language Generation.** *Tianyi Tang, Junyi Li, Wayne Xin Zhao.* `arxiv 2022` [[pdf]](https://arxiv.org/abs/2201.08670)
2. **Controllable Generation from Pre-trained Language Models via Inverse Prompting.** *Xu Zou, Da Yin, Qingyang Zhong, Ming Ding, Hongxia Yang, Zhilin Yang, Jie Tang.* [[pdf]](https://arxiv.org/abs/2103.10685) `kdd 2021` 
3. **LongT5: Efficient Text-To-Text Transformer for Long Sequences.** *Google.* [[pdf]](https://arxiv.org/pdf/2112.07916.pdf) `arxiv 2021`
4. **Scaling Language Models: Methods, Analysis & Insights from Training Gopher.** *DeepMind* [[pdf]](https://storage.googleapis.com/deepmind-media/research/language-research/Training%20Gopher.pdf) `arxiv 2021`
5. **Improving language models by retrieving from trillions of tokens.** *DeepMind* [[pdf]](https://arxiv.org/abs/2112.04426) `arxiv 2021`
6. **The Power of Scale for Parameter-Efficient Prompt Tuning.** *Google* [[pdf]](https://arxiv.org/abs/2104.08691) `EMNLP 2021`
7. **Prefix-Tuning: Optimizing Continuous Prompts for Generation.** *Xiang Lisa Li, Percy Liang.* `ACL 2021`  [[pdf]](https://aclanthology.org/2021.acl-long.353/)
8. **A Plug-and-Play Method for Controlled Text Generation.** *Damian Pascual, Beni Egressy, Clara Meister, Ryan Cotterell, Roger Wattenhofer.* [[pdf]](https://arxiv.org/abs/2109.09707) `Findings of EMNLP 2021`
9. **Attribute Alignment: Controlling Text Generation from Pre-trained Language Models.** *Dian Yu, Kenji Sagae, Zhou Yu.* [[pdf]](https://arxiv.org/abs/2103.11070) `Findings of EMNLP 2021` 
10. **ERNIE-Doc: A Retrospective Long-Document Modeling Transformer.** *Siyu Ding, Junyuan Shang, Shuohuan Wang, Yu Sun, Hao Tian, Hua Wu, Haifeng Wang.* [[pdf]](https://arxiv.org/abs/2012.15688) `ACL 2021`
11. **All NLP Tasks Are Generation Tasks: A General Pretraining Framework.** *Zhengxiao Du, Yujie Qian, Xiao Liu, Ming Ding, Jiezhong Qiu, Zhilin Yang, Jie Tang.* `arxiv 2021` [[pdf]](https://arxiv.org/abs/2103.10360) 
12. **GeDi: Generative Discriminator Guided Sequence Generation.** *Ben Krause, Akhilesh Deepak Gotmare, Bryan McCann, Nitish Shirish Keskar, Shafiq Joty, Richard Socher, Nazneen Fatema Rajani.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2009.06367)  
13. **K-Adapter: Infusing Knowledge into Pre-Trained Models with Adapters.** *Ruize Wang, Duyu Tang, Nan Duan, zhongyu wei, Xuanjing Huang, Jianshu Ji, Guihong Cao, Daxin Jiang, Ming Zhou.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2002.01808)
14. **PLUG AND PLAY LANGUAGE MODELS : A SIMPLE APPROACH TO CONTROLLED TEXT GENERATION.** *Sumanth Dathathri, Andrea Madotto, Janice Lan, Jane Hung, Eric Frank, Piero Molino, Jason Yosinski, Rosanne Liu.* `ICLR 2020` [[pdf]](https://arxiv.org/abs/1912.02164) 
15. **Language Models are Few-Shot Learners.** *Tom B. Brown, et al.* `OpenAI blog 2020` [[pdf]](https://arxiv.org/abs/2005.14165) 
16. **BART: Denoising Sequence-to-Sequence Pre-training for Natural Language Generation, Translation, and Comprehension.** *Mike Lewis, Yinhan Liu, Naman Goyal, Marjan Ghazvininejad, Abdelrahman Mohamed, Omer Levy, Veselin Stoyanov, Luke Zettlemoyer.* `ACL 2020` [[pdf]](https://www.aclweb.org/anthology/2020.acl-main.703/) 
17. **Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer.** *Colin Raffel, Noam Shazeer, Adam Roberts, Katherine Lee, Sharan Narang, Michael Matena, Yanqi Zhou, Wei Li, Peter J. Liu.* `JMLR 2020` [[pdf]](https://arxiv.org/abs/1910.10683) 
18. **Improving Language Understanding by Generative Pre-Training.** *Alec Radford, Karthik Narasimhan, Tim Salimans, Ilya Sutskever.* `OpenAI blog 2018` [[pdf]](https://cdn.openai.com/research-covers/language-unsupervised/language_understanding_paper.pdf) 
19. **Language Models are Unsupervised Multitask Learners.** *Alec Radford, Jeffrey Wu, Rewon Child, David Luan, Dario Amodei, Ilya Sutskever.* `OpenAI blog 2019` [[pdf]](https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf) 

### 2.6 Others

1. **Discourse-Aware Prompt Design for Text Generation.** *Facebook.* [[pdf]](https://arxiv.org/pdf/2112.05717.pdf) `arxiv 2021`
2. **Joint Retrieval and Generation Training for Grounded Text Generation.** *Yizhe Zhang, Siqi Sun, Xiang Gao, Yuwei Fang, Chris Brockett, Michel Galley, Jianfeng Gao, Bill Dolan.* [[pdf]](https://arxiv.org/abs/2105.06597) `arxiv 2021`
3. **Disentangling Generative Factors in Natural Language with Discrete Variational Autoencoders.** *Giangiacomo Mercatali, André Freitas.* [[pdf]](https://arxiv.org/abs/2109.07169) `Findings of EMNLP 2021`
4. **Towards Document-Level Paraphrase Generation with Sentence Rewriting and Reordering.** *Zhe Lin, Yitao Cai, Xiaojun Wan.* [[pdf]](https://arxiv.org/abs/2109.07095) `Findings of EMNLP 2021`
5. **Conditional Generation of Temporally-ordered Event Sequences.** *Shih-Ting Lin, Nathanael Chambers, Greg Durrett* [[pdf]](https://arxiv.org/abs/2012.15786) `ACL 2021` 
6. **On Training Instance Selection for Few-Shot Neural Text Generation.** *Ernie Chang, Xiaoyu Shen, Hui-Syuan Yeh, Vera Demberg.* [[pdf]](https://arxiv.org/abs/2107.03176) `ACL 2021`
7. **DYPLOC: Dynamic Planning of Content Using Mixed Language Models for Text Generation.** *Xinyu Hua, Ashwin Sreevatsa, Lu Wang.* [[pdf]](https://arxiv.org/abs/2106.00791) `ACL 2021` ![](https://img.shields.io/badge/planning-brightgreen)
8. **PAIR: Planning and Iterative Reﬁnement in Pre-trained Transformers for Long Text Generation.** *Xinyu Hua, Lu Wang.* `EMNLP 2020` [[pdf]](https://arxiv.org/abs/2010.02301) ![](https://img.shields.io/badge/planning-brightgreen)
9. **Progressive Generation of Long Text.** *Bowen Tan, Zichao Yang, Maruan AI-Shedivat, Eric P. Xing, Zhiting Hu.* `NAACL 2021` [[pdf]](https://www.aclweb.org/anthology/2021.naacl-main.341/)![](https://img.shields.io/badge/planning-brightgreen)
10. **Long and Diverse Text Generation with Planning-based Hierarchical Variational Model.** *Zhihong Shao, Minlie Huang, Jiangtao Wen, Wenfei Xu, Xiaoyan Zhu.* `EMNLP 2019` [[pdf]](https://arxiv.org/abs/1908.06605) ![](https://img.shields.io/badge/planning-brightgreen)
11. **Chinese poetry generation with planning based neural network.** *Zhe Wang, Wei He, Hua Wu, Haiyang Wu, Wei Li, Haifeng Wang, Enhong Chen.* `COLING 2016` [[pdf]](https://arxiv.org/abs/1610.09889) ![](https://img.shields.io/badge/planning-brightgreen)
12. **Sentence-Level Content Planning and Style Specification for Neural Text Generation**. *Xinyu Hua, Lu Wang*.  `EMNLP 2019` [[pdf]](https://arxiv.org/abs/1909.00734) ![](https://img.shields.io/badge/planning-brightgreen)
13. **Summarize, Outline, and Elaborate : Long-Text Generation via Hierarchical Supervision from Extractive Summaries**. *Xiaofei Sun, Chun Fan, Zijun Sun, Yuxian Meng, Fei Wu, JiWei Li*. `arxiv 2020` [[pdf]](https://arxiv.org/abs/2010.07074) ![](https://img.shields.io/badge/planning-brightgreen)



## 3. Evaluation

![](https://img.shields.io/badge/ReferencedMetric-ref-orange) ![](https://img.shields.io/badge/UnreferencedMetric-unref-yellow) ![](https://img.shields.io/badge/WithHumanRatingAsSupervision-sl-pink) ![](https://img.shields.io/badge/EvaluationFromMultipleDimension-multidim-darkgreen)

### 3.1 Metric

1. **DiscoScore: Evaluating Text Generation with BERT and Discourse Coherence.** *Wei Zhao, Michael Strube, Steffen Eger.* `arxiv` [[pdf]](https://arxiv.org/abs/2201.11176) ![](https://img.shields.io/badge/system-green)
2. **MAUVE: Measuring the Gap Between Neural Text and Human Text using Divergence Frontiers.** **Krishna Pillutla, Swabha Swayamdipta, Rowan Zellers, John Thickstun, Sean Welleck, Yejin Choi, Zaid Harchaoui*.* `NeurIPS 2021 distinguished paper` [[pdf]](https://proceedings.neurips.cc/paper/2021/hash/260c2432a0eecc28ce03c10dadc078a4-Abstract.html) ![](https://img.shields.io/badge/system-green)
3. **FrugalScore: Learning Cheaper, Lighter and Faster Evaluation Metrics for Automatic Text Generation.** *Moussa Kamal Eddine, Guokan Shang, Antoine J.-P. Tixier, Michalis Vazirgiannis.* `arxiv 2021` [[pdf]](https://arxiv.org/abs/2110.08559) ![](https://img.shields.io/badge/ref-orange) ![](https://img.shields.io/badge/unref-yellow) ![](https://img.shields.io/badge/sl-pink)
4. **Compression, Transduction, and Creation: A Unified Framework for  Evaluating Natural Language Generation.** *Mingkai Deng,Bowen Tan,Zhengzhong Liu,Eric P. Xing,Zhiting Hu.* [[pdf]](https://arxiv.org/abs/2109.06379) `EMNLP 2021` ![](https://img.shields.io/badge/unref-yellow)
5. **Language Model Augmented Relevance Score.** *Ruibo Liu, Jason Wei, Soroush Vosoughi.* [[pdf]](https://arxiv.org/abs/2108.08485) `ACL 2021`   ![](https://img.shields.io/badge/unref-yellow)
6. **Generating Negative Samples by Manipulating Golden Responses for Unsupervised Learning of a Response Evaluation Model.** *ChaeHun Park, Eugene Jang, Wonsuk Yang, Jong Park.* [[pdf]](https://www.aclweb.org/anthology/2021.naacl-main.120/) `NAACL 2021` ![](https://img.shields.io/badge/unref-yellow)
7. **Towards Quantifiable Dialogue Coherence Evaluation.** *Zheng Ye, Liucun Lu, Lishan Huang, Liang Lin, Xiaodan Liang.* [[pdf]](https://arxiv.org/abs/2106.00507) `ACL 2021` ![](https://img.shields.io/badge/sl-pink)
8. **REAM♯: An Enhancement Approach to Reference-based Evaluation Metrics for Open-domain Dialog Generation.** *Jun Gao, Wei Bi, Ruifeng Xu, Shuming Shi.* [[pdf]](https://arxiv.org/abs/2105.14488) `Findings of ACL 2021` ![](https://img.shields.io/badge/ref-orange)
9. **DynaEval: Unifying Turn and Dialogue Level Evaluation.** *Chen Zhang, Yiming Chen, Luis Fernando D'Haro, Yan Zhang, Thomas Friedrichs, Grandee Lee, Haizhou Li.* `ACL 2021` [[pdf]](https://arxiv.org/abs/2106.01112) ![](https://img.shields.io/badge/unref-yellow)
10. **Plot-guided Adversarial Example Construction for Evaluating Open-domain Story Generation.** *Sarik Ghazarian, Zixi Liu, Akash SM, Ralph Weischedel, Aram Galstyan, Nanyun Peng.* `NAACL 2021` [[pdf]](https://arxiv.org/abs/2104.05801) ![](https://img.shields.io/badge/unref-yellow)
11. **Perception Score, A Learned Metric for Open-ended Text Generation Evaluation.** *Jing Gu, Qingyang Wu, Zhou Yu.* `AAAI 2021` [[pdf]](https://arxiv.org/abs/2008.03082) ![](https://img.shields.io/badge/ref-orange)
12. **UNION: An Unreferenced Metric for Evaluating Open-ended Story Generation.** *Jian Guan, Minlie Huang.* `EMNLP 2020` [[pdf]](https://arxiv.org/pdf/2009.07602.pdf) ![](https://img.shields.io/badge/unref-yellow)
13. **GRADE: Automatic Graph-Enhanced Coherence Metric for Evaluating Open-Domain Dialogue Systems.** *Lishan Huang, Zheng Ye, Jinghui Qin, Liang Lin, Xiaodan Liang.* `EMNLP 2020` [[pdf]](https://arxiv.org/abs/2010.03994) ![](https://img.shields.io/badge/unref-yellow)
14. **GRUEN for Evaluating Linguistic Quality of Generated Text.** *Wanzheng Zhu and Suma Bhat.* `Findings of EMNLP 2020` [[pdf]](https://arxiv.org/abs/2010.02498) ![](https://img.shields.io/badge/multidim-darkgreen)
15. **How To Evaluate Your Dialogue System: Probe Tasks as an Alternative for Token-level Evaluation Metrics.** *Prasanna Parthasarathi, Joelle Pineau, Sarath Chandar.* `arxiv 2020` [[pdf]](https://arxiv.org/abs/2008.10427)
16. **BLEURT: Learning robust metrics for text generation.** *Thibault Sellam, Dipanjan Das, and Ankur Parikh.* `ACL 2020` [[pdf]](https://doi.org/10.18653/v1/2020.acl-main.704) ![](https://img.shields.io/badge/ref-orange) ![](https://img.shields.io/badge/unref-yellow) ![](https://img.shields.io/badge/sl-pink)
17. **Towards Holistic and Automatic Evaluation of Open-Domain Dialogue Generation.** *Bo Pang, Erik Nijkamp, Wenjuan Han, Linqi Zhou, Yixian Liu, Kewei Tu.* `ACL 2020` [[pdf]](https://www.aclweb.org/anthology/2020.acl-main.333/) ![](https://img.shields.io/badge/unref-yellow)
18. **Learning an Unreferenced Metric for Online Dialogue Evaluation.** *Koustuv Sinha, Prasanna Parthasarathi, Jasmine Wang, Ryan Lowe, William L. Hamilton, Joelle Pineau.* `ACL 2020` [[pdf]](https://arxiv.org/abs/2005.00583) ![](https://img.shields.io/badge/unref-yellow)
19. **Evaluating Dialogue Generation Systems via Response Selection.** *Shiki Sato, Reina Akama, Hiroki Ouchi, Jun Suzuki, Kentaro Inui.* `ACL 2020` [[pdf]](https://arxiv.org/abs/2004.14302)
20. **Speaker Sensitive Response Evaluation Model.** *JinYeong Bak, Alice Oh.* `ACL 2020` [[pdf]](Speaker Sensitive Response Evaluation Model)
21. **USR: An Unsupervised and Reference Free Evaluation Metric for Dialog Generation.** *Shikib Mehri, Maxine Eskenazi.* `ACL 2020` [[pdf]](https://arxiv.org/abs/2005.00456) ![](https://img.shields.io/badge/unref-yellow)
22. **uBLEU: Uncertainty-Aware Automatic Evaluation Method for Open-Domain Dialogue Systems.** *Tsuta Yuma, Naoki Yoshinaga, Masashi Toyoda.* `ACL 2020` [[pdf]](https://www.aclweb.org/anthology/2020.acl-srw.27/) ![](https://img.shields.io/badge/ref-orange)
23. **Beyond User Self-Reported Likert Scale Ratings: A Comparison Model for Automatic Dialog Evaluation.** *Weixin Liang, James Zou, Zhou Yu.* `ACL 2020` [[pdf]](https://arxiv.org/abs/2005.10716) ![](https://img.shields.io/badge/sl-pink)
24. **Designing Precise and Robust Dialogue Response Evaluators.** *Tianyu Zhao, Divesh Lala, Tatsuya Kawahara.* `ACL 2020 short paper` [[pdf]](https://arxiv.org/abs/2004.04908) ![](https://img.shields.io/badge/unref-yellow)
25. **Unsupervised Evaluation of Interactive Dialog with DialoGPT.** *Shikib Mehri, Maxine Eskenazi.* `SIGDIAL 2020` [[pdf]](https://www.aclweb.org/anthology/2020.sigdial-1.28/) ![](https://img.shields.io/badge/unref-yellow)
26. **Can You Put it All Together: Evaluating Conversational Agents' Ability to Blend Skills.** *Eric Michael Smith, Mary Williamson, Kurt Shuster, Jason Weston, Y-Lan Boureau.* `ACL 2020` [[pdf]](https://arxiv.org/abs/2004.08449)
27. **Bertscore: Evaluating text generation with bert.** *Tianyi Zhang, Varsha Kishore, Felix Wu, Kilian Q. Weinberger, and Yoav Artzi.* `ICLR 2020` [[pdf]](https://openreview.net/forum?id=SkeHuCVFDr) ![](https://img.shields.io/badge/ref-orange)
28. **Predictive Engagement: An Efficient Metric For Automatic Evaluation of Open-Domain Dialogue Systems.** *Sarik Ghazarian, Ralph Weischedel, Aram Galstyan, Nanyun Peng.* `AAAI 2020` [[pdf]](https://arxiv.org/abs/1911.01456) ![](https://img.shields.io/badge/unref-yellow)
29. **Learning to compare for better training and evaluation of open domain natural language generation models.** *Wangchunshu Zhou and Ke Xu.* `AAAI 2020` [[pdf]](https://arxiv.org/abs/2002.05058) ![](https://img.shields.io/badge/ref-orange) ![](https://img.shields.io/badge/unref-yellow)
30. **Improving Dialog Evaluation with a Multi-reference Adversarial Dataset and Large Scale Pretraining.** *Ananya B. Sai, Akash Kumar Mohankumar, Siddhartha Arora, Mitesh M. Khapra.* `TACL 2020` [[pdf]](https://arxiv.org/abs/2009.11321) ![](https://img.shields.io/badge/ref-orange)
31. **How to Evaluate the Next System: Automatic Dialogue Evaluation from the Perspective of Continual Learning.** *Lu Li, Zhongheng He, Xiangyang Zhou, Dianhai Yu.* `arxiv 2019` [[pdf]](https://arxiv.org/abs/1912.04664)
32. **Moverscore: Text generation evaluating with contextualized embeddings and earth mover distance.** *Wei Zhao, Maxime Peyrard, Fei Liu, Yang Gao, Christian M Meyer, and Steffen Eger.* `EMNLP 2019` [[pdf]](https://www.aclweb.org/anthology/D19-1053/) ![](https://img.shields.io/badge/ref-orange)
33. **TIGEr: Text-to-Image Grounding for Image Caption Evaluation.** *Ming Jiang, Qiuyuan Huang, Lei Zhang, Xin Wang, Pengchuan Zhang, Zhe Gan, Jana Diesner, Jianfeng Gao.* `EMNLP 2019` [[pdf]](https://www.aclweb.org/anthology/D19-1220/) ![](https://img.shields.io/badge/ref-orange)
34. **Investigating Evaluation of Open-Domain Dialogue Systems With Human Generated Multiple References.** *Prakhar Gupta, Shikib Mehri, Tiancheng Zhao, Amy Pavel, Maxine Eskenazi, Jeffrey Bigham.* `SIGDIAL 2019` [[pdf]](https://www.aclweb.org/anthology/W19-5944/) ![](https://img.shields.io/badge/ref-orange)
35. **Unifying Human and Statistical Evaluation for Natural Language Generation.** *Tatsunori Hashimoto, Hugh Zhang, Percy Liang.* `NAACL 2019` [[pdf]](https://www.aclweb.org/anthology/N19-1169/) ![](https://img.shields.io/badge/unref-yellow) ![](https://img.shields.io/badge/sl-pink)
36. **Better automatic evaluation of open-domain dialogue systems with contextualized embeddings.** *Sarik Ghazarian, Johnny Wei, Aram Galstyan, and Nanyun Peng.* `NAACL 2019 workshop` [[pdf]](https://www.aclweb.org/anthology/W19-2310.pdf) ![](https://img.shields.io/badge/ref-orange)
37. **Re-evaluating ADEM: A Deeper Look at Scoring Dialogue Responses.** *Ananya B. Sai, Mithun Das Gupta, Mitesh M. Khapra, Mukundhan Srinivasan.* `AAAI 2019` [[pdf]](https://arxiv.org/abs/1902.08832)
38. **Towards a Better Metric for Evaluating Question Generation Systems.** *Preksha Nema, Mitesh M. Khapra.* `EMNLP 2018` [[pdf]](https://www.aclweb.org/anthology/D18-1429/)
39. **The price of debiasing automatic metrics in natural language evaluation.** *Arun Tejasvi Chaganty, Stephen Mussman, Percy Liang.* `ACL 2018` [[pdf]](https://arxiv.org/abs/1807.02202) ![](https://img.shields.io/badge/ref-orange) ![](https://img.shields.io/badge/sl-pink)
40. **Ruse: Regressor using sentence embeddings for automatic machine translation evaluation.** *Hiroki Shimanaka, Tomoyuki Kajiwara, and Mamoru Komachi.* `ACL 2018 workshop` [[pdf]](https://www.aclweb.org/anthology/W18-6456/) ![](https://img.shields.io/badge/ref-orange)
41. **Towards a Metric for Automated Conversational Dialogue System Evaluation and Improvement.** *Jan Deriu, Mark Cieliebak.* `INLG 2018` [[pdf]](https://www.inlg2019.com/assets/papers/132_Paper.pdf) ![](https://img.shields.io/badge/sl-pink)
42. **Ruber: An unsupervised method for automatic evaluation of open-domain dialog systems.** *Chongyang Tao, Lili Mou, Dongyan Zhao, and Rui Yan.* `AAAI 2018` [[pdf]](https://arxiv.org/abs/1701.03079) ![](https://img.shields.io/badge/ref-orange) ![](https://img.shields.io/badge/unref-yellow)
43. **One “Ruler” for All Languages: Multi-Lingual Dialogue Evaluation with Adversarial Multi-Task Learning.** *Xiaowei Tong, Zhenxin Fu, Mingyue Shang, Dongyan Zhao, Rui Yan.* `IJCAI 2018` [[pdf]](https://www.ijcai.org/Proceedings/2018/0616.pdf)
44. **Adversarial Learning for Neural Dialogue Generation.** *Jiwei Li, Will Monroe, Tianlin Shi, Sébastien Jean, Alan Ritter, Dan Jurafsky.* `EMNLP 2017` [[pdf]](https://www.aclweb.org/anthology/D17-1230/) ![](https://img.shields.io/badge/unref-yellow)
45. **Topic-based Evaluation for Conversational Bots.** *Fenfei Guo, Angeliki Metallinou, Chandra Khatri, Anirudh Raju, Anu Venkatesh, Ashwin Ram.* `NeurIPS 2017 workshop` [[pdf]](https://arxiv.org/abs/1801.03622) ![](https://img.shields.io/badge/unref-yellow)
46. **On Evaluating and Comparing Open Domain Dialog Systems.** *Anu Venkatesh, Chandra Khatri, Ashwin Ram, Fenfei Guo, Raefer Gabriel, Ashish Nagar, Rohit Prasad, Ming Cheng, Behnam Hedayatnia, Angeliki Metallinou, Rahul Goel, Shaohua Yang, Anirudh Raju.* `NeurIPS 2017 workshop` [[pdf]](https://arxiv.org/abs/1801.03625) ![](https://img.shields.io/badge/multidim-darkgreen)
47. **Towards an automatic turing test: Learning to evaluate dialogue responses.** *Ryan Lowe, Michael Noseworthy, Iulian Vlad Serban, Nicolas Angelard-Gontier, Yoshua Bengio, and Joelle Pineau.* `ACL 2017 Best Paper` [[pdf]](https://www.aclweb.org/anthology/P17-1103.pdf) ![](https://img.shields.io/badge/sl-pink)
48. **Evaluating Story Generation Systems Using Automated Linguistic Analyses.** *Melissa Roemmele, Andrew S. Gordon, Reid Swanson.* `ACM SIGKDD 2017` [[pdf]](https://people.ict.usc.edu/gordon/public_html/publications/KDD-WS17.PDF) ![](https://img.shields.io/badge/multidim-darkgreen)
49. **Adversarial evaluation of dialogue models.** *Anjuli Kannan and Oriol Vinyals.* `arxiv 2017` [[pdf]](https://arxiv.org/abs/1701.08198) ![](https://img.shields.io/badge/unref-yellow)
50. **deltaBLEU: A Discriminative Metric for Generation Tasks with Intrinsically Diverse Targets.** *Michel Galley, Chris Brockett, Alessandro Sordoni, Yangfeng Ji, Michael Auli, Chris Quirk, Margaret Mitchell, Jianfeng Gao, Bill Dolan.* `ACL 2015` [[pdf]](https://www.aclweb.org/anthology/P15-2073/) ![](https://img.shields.io/badge/ref-orange)
51. **ROUGE: A package for automatic evaluation of summaries.** `Chin-Yew Lin.` `ACL 2004` [[pdf]](https://www.aclweb.org/anthology/W04-1013) ![](https://img.shields.io/badge/ref-orange)
52. **Bleu: a method for automatic evaluation of machine translation.** *Kishore Papineni, Salim Roukos, Todd Ward, and WeiJing Zhu.* `ACL 2002` [[pdf]](https://www.aclweb.org/anthology/P02-1040/) ![](https://img.shields.io/badge/ref-orange)



### 3.2 Protocol for human evaluation

1. **The Perils of Using Mechanical Turk to Evaluate Open-Ended Text Generation.** *Marzena Karpinska, Nader Akoury, Mohit Iyyer.* `EMNLP 2021` [[pdf]](https://arxiv.org/abs/2109.06835)
2. **Choose Your Own Adventure: Paired Suggestions in Collaborative Writing for Evaluating Story Generation Models.** *Elizabeth Clark, Noah A. Smith.* `NAACL 2021` [[pdf]](https://www.aclweb.org/anthology/2021.naacl-main.279/)
3. **STORIUM: A Dataset and Evaluation Platform for Machine-in-the-Loop Story Generation.** *Nader Akoury, Shufan Wang, Josh Whiting, Stephen Hood, Nanyun Peng, Mohit Iyyer.* `EMNLP 2020` [[pdf]](https://arxiv.org/abs/2010.01717) 
4. **Spot The Bot: A Robust and Efficient Framework for the Evaluation of Conversational Dialogue Systems.** *Jan Deriu, Don Tuggener, Pius von Däniken, Jon Ander Campos, Alvaro Rodrigo, Thiziri Belkacem, Aitor Soroa, Eneko Agirre, Mark Cieliebak.* `EMNLP 2020` [[pdf]](https://arxiv.org/abs/2010.02140)
5. **Towards Best Experiment Design for Evaluating Dialogue System Output.** *Sashank Santhanam, Samira Shaikh.* `INLG 2019` [[pdf]](https://arxiv.org/abs/1909.10122)
6. **Communication-based Evaluation for Natural Language Generation.**  `SCiL 2019` [[pdf]](https://arxiv.org/abs/1909.07290)
7. **Domain-Independent turn-level Dialogue Quality Evaluation via User Satisfaction Estimation.**  `SIGDIAL 2019`[[pdf]](https://arxiv.org/pdf/1908.07064.pdf)
8. **ACUTE-EVAL: Improved Dialogue Evaluation with Optimized Questions and Multi-turn Comparisons.** *Margaret Li, Jason Weston, Stephen Roller.* `AAAI 2019` [[pdf]](https://arxiv.org/abs/1909.03087) 
9. **ChatEval: A Tool for the Systematic Evaluation of Chatbots.** *João Sedoc, Daphne Ippolito, Arun Kirubarajan, Jai Thirani, Lyle Ungar, Chris Callison-Burch.* `ACL 2018` [[pdf]](https://www.aclweb.org/anthology/W18-6709.pdf) 
10. **Towards a Method For Evaluating Naturalness in Conversational Dialog Systems.** *Victor Hung, Miguel Elvir, Avelino Gonzalez, Ronald DeMara.* `IEEE ICSMC 2009` [[pdf]](https://ieeexplore.ieee.org/abstract/document/5345904/) 
11. **Empirical Methods for Evaluating Dialog Systems.** *Tim Paek.* `ACL 2001` [[pdf]](https://www.aclweb.org/anthology/W01-0902.pdf)



## 4. Others

1. **Knowledge Infusion Decoding.** *Ruibo Liu, Guoqing Zheng, Shashank Gupta, Radhika Gaonkar, Chongyang Gao, Soroush Vosoughi, Milad Shokouhi, Ahmed Hassan Awadallah.* `ICLR 2022` [[pdf]](https://openreview.net/forum?id=upnDJ7itech)
2. **A Contrastive Framework for Neural Text Generation.** *Yixuan Su, Tian Lan, Yan Wang, Dani Yogatama, Lingpeng Kong, Nigel Collier.* [[pdf]](https://arxiv.org/abs/2202.06417) `arxiv 2022`
3. **Typical Decoding for Natural Language Generation.** *Clara Meister, Tiago Pimentel, Gian Wiher, Ryan Cotterell.* `arxiv 2022` [[pdf]](https://arxiv.org/abs/2202.00666)
4. **Long-range and hierarchical language predictions in brains and algorithms.** *Facebook* `arxiv 2021` [[pdf]](https://arxiv.org/abs/2111.14232)
5. **Exposure Bias versus Self-Recovery: Are Distortions Really Incremental for Autoregressive Text Generation?** *Tianxing He, Jingzhao Zhang, Zhiming Zhou, James Glass.* `EMNLP 2021` [[pdf]](https://aclanthology.org/2021.emnlp-main.415/)
6. **Don't Take It Literally: An Edit-Invariant Sequence Loss for Text Generation.** *Guangyi Liu, Zichao Yang, Tianhua Tao, Xiaodan Liang, Zhen Li, Bowen Zhou, Shuguang Cui, Zhiting Hu.* `arxiv 2021` [[pdf]](https://arxiv.org/abs/2106.15078)
7. **NEURO LOGIC DECODING : (Un)supervised Neural Text Generation with Predicate Logic Constraints.** *Ximing Lu, Peter West, Rowan Zellers, Ronan Le Bras, Chandra Bhagavatula, Yejin Choi.* `NAACL 2021.` [[pdf]](https://aclanthology.org/2021.naacl-main.339.pdf) 
8. **Boosting coherence of language models.** *Nikolay Malkin, Zhen Wang, Nebojsa Jojic.* `arxiv 2021.` [[pdf]](https://arxiv.org/abs/2110.08294)
9. **If beam search is the answer, what was the question?** *Clara Meister, Tim Vieira, Ryan Cotterell.* `EMNLP 2020` [[pdf]](https://arxiv.org/abs/2010.02650)
10. **A Systematic Characterization of Sampling Algorithms for Open-ended Language Generation.** *Moin Nadeem, Tianxing He, Kyunghyun Cho, James Glass.* `AACL 2020` [[pdf]](https://arxiv.org/abs/2009.07243)
11. **The Curious Case of Neural Text Degeneration.** *Ari Holtzman, Jan Buys, Li Du, Maxwell Forbes, Yejin Choi.* `ICLR 2020` [[pdf]](https://openreview.net/forum?id=rygGQyrFvH)

