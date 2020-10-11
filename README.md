1. #Paper List for Open-eNded Language Generation (ONLG)

  ![](https://img.shields.io/github/last-commit/thu-coai/PaperForONLG?color=blue) ![](https://img.shields.io/badge/PaperNumber-65-brightgreen) ![](https://img.shields.io/badge/PRs-Welcome-red) 

  Contributed by [Jian Guan](https://jianguanthu.github.io/), Zhexin Zhang, Zhuoer Feng

  ### Introduction

  **O**pen-e**N**ded **L**anguage **G**eneration (ONLG) refers to those generation tasks where only very limited information is given in the input and there are many plausible output for the same input (also known as one-to-many). ONLG roughly includes chit-chat dialog generation, story generation, review generation, essay generation etc.

  

  ### Some active authors in the list

  [Noah A. Smith](https://homes.cs.washington.edu/~nasmith/), [Minlie Huang](http://coai.cs.tsinghua.edu.cn/hml/), [Stephen Roller](https://stephenroller.com/), [Nanyun Peng](https://violetpeng.github.io//), [Jianfeng Gao](https://www.microsoft.com/en-us/research/people/jfgao/?from=http%3A%2F%2Fresearch.microsoft.com%2Fen-us%2Fum%2Fpeople%2Fjfgao%2F), [Joelle Pineau](https://scholar.google.com/citations?user=CEt6_mMAAAAJ&hl=zh-CN), [Angela Fan](https://ai.facebook.com/people/angela-fan/), [Jason Weston](http://www.thespermwhale.com/jaseweston/), [Ryan Lowe](https://scholar.google.ca/citations?user=iRgYMuEAAAAJ&hl=en) ...

  

  ### Contents

  * [0. Resource](#0-resource)
  * [1. Survey](#1-survey)
  * [2. Generative Model](#2-generative-model)
    * [2.1 Story](#21-story)
    * [2.2 Dialog](#22-dialog) 
    * [2.3 Others](#23-others)
  * [3. Evaluation](#3-evaluation)
    * [3.1 Metric](3-1-metric)
    * [3.2 Protocol](protocol)
  * [4. Others](#4-others)

  

  ## 0. Resource

  1. **STORIUM: A Dataset and Evaluation Platform for Machine-in-the-Loop Story Generation.** *Nader Akoury, Shufan Wang, Josh Whiting, Stephen Hood, Nanyun Peng, Mohit Iyyer.* <u>EMNLP 2020</u> [[pdf]](https://arxiv.org/abs/2010.01717)
  2. **GLUCOSE: GeneraLized and COntextualized Story Explanations.** *Nasrin Mostafazadeh, Aditya Kalyanpur, Lori Moon, David Buchanan, Lauren Berkowitz, Or Biran, Jennifer Chu-Carroll.* <u>EMNLP 2020</u> [[pdf]](https://arxiv.org/abs/2009.07758)
  3. **CommonGen: A Constrained Text Generation Challenge for Generative Commonsense Reasoning.** *Bill Yuchen Lin, Wangchunshu Zhou, Ming Shen, Pei Zhou, Chandra Bhagavatula, Yejin Choi, Xiang Ren.* <u>Findings of EMNLP 2020</u> [[pdf]](https://arxiv.org/abs/1911.03705)
  4. **A Large-Scale Chinese Short-Text Conversation Dataset.** *Yida Wang, Pei Ke, Yinhe Zheng, Kaili Huang, Yong Jiang, Xiaoyan Zhu, Minlie Huang.* <u>NLPCC 2020</u> [[pdf]](https://arxiv.org/abs/2008.03946)
  5. **Storytelling with Dialogue: A Critical Role Dungeons and Dragons Dataset.** *Revanth Rameshkumar, Peter Bailey.* <u>ACL 2020</u> [[pdf]](https://www.aclweb.org/anthology/2020.acl-main.459/)
  6. **MuTual: A Dataset for Multi-Turn Dialogue Reasoning.** *Leyang Cui, Yu Wu, Shujie Liu, Yue Zhang, Ming Zhou.* <u>ACL 2020</u> [[pdf]](https://arxiv.org/abs/2004.04494)
  7. **Designing Precise and Robust Dialogue Response Evaluators.** *Tianyu Zhao, Divesh Lala, Tatsuya Kawahara.* <u>ACL 2020 short paper</u> [[pdf]](https://arxiv.org/abs/2004.04908)
  8. **Recollection versus Imagination: Exploring Human Memory and Cognition via Neural Language Models.** *Maarten Sap, Eric Horvitz, Yejin Choi, Noah A. Smith, James Pennebaker.* <u>ACL 2020</u> [[pdf]](https://www.aclweb.org/anthology/2020.acl-main.178/)
  9. **Exploring the Effect of Author and Reader Identity in Online Story Writing: the STORIESINTHEWILD Corpus.** <u>Tal August, Maarten Sap, Elizabeth Clark, Katharina Reinecke, Noah A. Smith.</u> <u>ACL 2020</u> [[pdf]](https://www.aclweb.org/anthology/2020.nuse-1.6/)
  10. **Counterfactual Story Reasoning and Generation.** *Lianhui Qin, Antoine Bosselut, Ari Holtzman, Chandra Bhagavatula, Elizabeth Clark, Yejin Choi.* <u>EMNLP 2019</u> [[pdf]](https://arxiv.org/abs/1909.04076)
  11. **Hierarchical neural story generation.** *Angela Fan, Mike Lewis, and Yann Dauphin.* <u>ACL 2018</u> [[pdf]](https://www.aclweb.org/anthology/P18-1082.pdf)
  12. **LSDSCC: a Large Scale Domain-Specific Conversational Corpus for Response Generation with Diversity Oriented Evaluation Metrics.** *Zhen Xu, Nan Jiang, Bingquan Liu, Wenge Rong, Bowen Wu, Baoxun Wang, Zhuoran Wang, Xiaolong Wang.* <u>NAACL 2018</u> [[pdf]](https://www.aclweb.org/anthology/N18-1188/)
  13. **A Corpus and Cloze Evaluation for Deeper Understanding of Commonsense Stories.** *Nasrin Mostafazadeh, Nathanael Chambers, Xiaodong He, Devi Parikh, Dhruv Batra, Lucy Vanderwende, Pushmeet Kohli, James Allen.* <u>NAACL 2016</u> [[pdf]](https://www.aclweb.org/anthology/N16-1098/)

  

  ## 1. Survey

  1. **Automatic Story Generation: State of the Art and Recent Trends.**  *Brian Daniel Herrera-González, Alexander Gelbukh, and Hiram Calvo.* <u>MICA 2020</u> [[pdf]](https://link.springer.com/chapter/10.1007%2F978-3-030-60887-3_8)
  2. **Towards Unified Dialogue System Evaluation: A Comprehensive Analysis of Current Evaluation Protocols.** *Sarah E. Finch, Jinho D. Choi.* <u>SIGDIAL 2020</u> [[pdf]](https://arxiv.org/abs/2006.06110)
  3. **Challenges in Building Intelligent Open-domain Dialog Systems.** *Minlie Huang, Xiaoyan Zhu, Jianfeng Gao.* <u>TOIS 2020</u> [[pdf]](https://dl.acm.org/doi/abs/10.1145/3383123)
  4. **Open-Domain Conversational Agents: Current Progress, Open Problems, and Future Directions.** *Stephen Roller, Y-Lan Boureau, Jason Weston, Antoine Bordes, Emily Dinan, Angela Fan, David Gunning, Da Ju, Margaret Li, Spencer Poff, Pratik Ringshia, Kurt Shuster, Eric Michael Smith, Arthur Szlam, Jack Urbanek, Mary Williamson.* <u>arxiv 2020</u> [[pdf]](https://arxiv.org/abs/2006.12442)
  5. **A Survey of Evaluation Metrics Used for NLG Systems.** *Ananya B. Sai, Akash Kumar Mohankumar, Mitesh M. Khapra.* <u>arxiv 2020</u> [[pdf]](https://arxiv.org/abs/2008.12009)
  6. **Evaluation of Text Generation: A Survey.** *Asli Celikyilmaz, Elizabeth Clark, Jianfeng Gao.* <u>arxiv 2020</u> [[pdf]](https://arxiv.org/abs/2006.14799)
  7. **Survey on evaluation methods for dialogue systems.** *Jan Deriu, Alvaro Rodrigo, Arantxa Otegi, Guillermo Echegoyen, Sophie Rosset, Eneko Agirre & Mark Cieliebak.* <u>Artificial Intelligence Review 2020</u> [[pdf]](https://link.springer.com/article/10.1007/s10462-020-09866-x)
  8. **Judge the Judges: A Large-Scale Evaluation Study of Neural Language Models for Online Review Generation.** *Cristina Garbacea, Samuel Carton, Shiyan Yan, Qiaozhu Mei.* <u>arxiv 2019</u> [[pdf]](https://arxiv.org/abs/1901.00398)
  9. **How NOT To Evaluate Your Dialogue System: An Empirical Study of Unsupervised Evaluation Metrics for Dialogue Response Generation.** *Chia-Wei Liu, Ryan Lowe, Iulian Serban, Mike Noseworthy, Laurent Charlin, Joelle Pineau.* <u>EMNLP 2016</u> [[pdf]](https://www.aclweb.org/anthology/D16-1230/)
  10. **对话系统评价方法综述** *张伟男, 张杨子, 刘挺.* <u>中国科学 : 信息科学</u> [[pdf]](http://scis.scichina.com/cn/2017/N112017-00125.pdf)
  11. **A Survey of Available Corpora for Building Data-Driven Dialogue Systems.** *Iulian Vlad Serban, Ryan Lowe, Peter Henderson, Laurent Charlin, Joelle Pineau.* <u>arxiv 2015</u> [[pdf]](https://arxiv.org/abs/1512.05742)

  

  ##2. Generative Model

  ###2.1 Story

  1. **Content Planning for Neural Story Generation with Aristotelian Rescoring** *Seraphina Goldfarb-Tarrant, Tuhin Chakrabarty, Ralph Weischedel, Nanyun Peng.* <u>EMNLP 2020</u> [[pdf]](https://arxiv.org/abs/2009.09870)
  2. **MEGATRON-CNTRL: Controllable Story Generation with External Knowledge Using Large-Scale Language Models.** *Peng Xu, Mostofa Patwary, Mohammad Shoeybi, Raul Puri, Pascale Fung, Anima Anandkumar, Bryan Catanzaro.* [[pdf]](https://arxiv.org/abs/2010.00840)
  3. **A Knowledge-Enhanced Pretraining Model for Commonsense Story Generation.** *Jian Guan, Fei Huang, Zhihao Zhao, Xiaoyan Zhu, Minlie Huang*. <u>TACL 2020</u> [[pdf]](https://www.mitpressjournals.org/doi/pdf/10.1162/tacl_a_00302)
  4. **Narrative Interpolation for Generating and Understanding Stories.** *Su Wang, Greg Durrett, Katrin Erk.* <u>arxiv 2020</u> [[pdf]](https://arxiv.org/abs/2008.07466)
  5. **Strategies for structuring story generation. ** *Angela Fan, Mike Lewis, and Yann Dauphin.* <u>ACL 2019</u> [[pdf]](https://www.aclweb.org/anthology/P19-1254.pdf)
  6. **Plan-and-write: Towards better automatic storytelling.** *Lili Yao, Nanyun Peng, Ralph Weischedel, Kevin Knight, Dongyan Zhao, and Rui Yan.* <u>AAAI 2019</u> [[pdf]](https://www.aaai.org/ojs/index.php/AAAI/article/view/4726)
  7. **Story ending generation with incremental encoding and commonsense knowledge.** *Jian Guan, Yansen Wang, and Minlie Huang.* <u>AAAI 2019</u> [[pdf]]((https://www.aaai.org/ojs/index.php/AAAI/article/view/4612))
  8. **Hierarchical neural story generation.** *Angela Fan, Mike Lewis, and Yann Dauphin.* <u>ACL 2018</u> [[pdf]](https://www.aclweb.org/anthology/P18-1082.pdf)
  9. **A skeleton-based model for promoting coherence among sentences in narrative story generation.** *Jingjing Xu, Xuancheng Ren, Yi Zhang, Qi Zeng, Xiaoyan Cai, and Xu Sun.* <u>EMNLP 2018</u> [[pdf]](https://www.aclweb.org/anthology/D18-1462/)
  10. **Event representations for automated story generation with deep neural nets.** *Lara Martin, Prithviraj Ammanabrolu, Xinyu Wang, William Hancock, Shruti Singh, Brent Harrison, and Mark Riedl.* <u>AAAI 2018</u> [[pdf]](https://arxiv.org/abs/1706.01331)

  

  ### 2.2 Dialog

  1. **Learning to Plan and Realize Separately for Open-Ended Dialogue Systems.** *Sashank Santhanam, Zhuo Cheng, Brodie Mather, Bonnie Dorr, Archna Bhatia, Bryanna Hebenstreit, Alan Zemel, Adam Dalton, Tomek Strzalkowski, Samira Shaikh.* <u>Findings of EMNLP 2020</u> [[pdf]](https://arxiv.org/abs/2009.12506)
  2. **A Large-Scale Chinese Short-Text Conversation Dataset.** *Yida Wang, Pei Ke, Yinhe Zheng, Kaili Huang, Yong Jiang, Xiaoyan Zhu, Minlie Huang.* <u>NLPCC 2020</u> [[pdf]](https://arxiv.org/abs/2008.03946)
  3. **DIALOGPT : Large-Scale Generative Pre-training for Conversational Response Generation.** *Yizhe Zhang, Siqi Sun, Michel Galley, Yen-Chun Chen, Chris Brockett, Xiang Gao, Jianfeng Gao, Jingjing Liu, Bill Dolan.* <u>ACL 2020</u> [[pdf]](https://www.aclweb.org/anthology/2020.acl-demos.30/)
  4. **Recipes for building an open-domain chatbot.** *Stephen Roller, Emily Dinan, Naman Goyal, Da Ju, Mary Williamson, Yinhan Liu, Jing Xu, Myle Ott, Kurt Shuster, Eric M. Smith, Y-Lan Boureau, Jason Weston.* <u>arxiv 2020</u> [[pdf]](https://arxiv.org/abs/2004.13637)
  5. **Towards a Human-like Open-Domain Chatbot.** *Daniel Adiwardana, Minh-Thang Luong, David R. So, Jamie Hall, Noah Fiedel, Romal Thoppilan, Zi Yang, Apoorv Kulshreshtha, Gaurav Nemade, Yifeng Lu, Quoc V. Le.*  <u>arxiv 2020</u> [[pdf]](https://arxiv.org/abs/2001.09977)

  

  ### 2.3 Others

  1. **Long and Diverse Text Generation with Planning-based Hierarchical Variational Model.** *Zhihong Shao, Minlie Huang, Jiangtao Wen, Wenfei Xu, Xiaoyan Zhu.* <u>EMNLP 2019</u> [[pdf]](https://arxiv.org/abs/1908.06605)
  2. **Chinese poetry generation with planning based neural network.** *Zhe Wang, Wei He, Hua Wu, Haiyang Wu, Wei Li, Haifeng Wang, Enhong Chen.* <u>COLING 2016</u> [[pdf]](https://arxiv.org/abs/1610.09889)

  

  ##3. Evaluation

  ###3.1 Metric

  1. **UNION: An Unreferenced Metric for Evaluating Open-ended Story Generation.** *Jian Guan, Minlie Huang.* <u>EMNLP 2020</u> [[pdf]](https://arxiv.org/pdf/2009.07602.pdf)
  2. **GRUEN for Evaluating Linguistic Quality of Generated Text.** *Wanzheng Zhu and Suma Bhat.* <u>Findings of EMNLP 2020</u> [[pdf]](https://arxiv.org/abs/2010.02498)
  3. **Spot The Bot: A Robust and Efficient Framework for the Evaluation of Conversational Dialogue Systems.** *Jan Deriu, Don Tuggener, Pius von Däniken, Jon Ander Campos, Alvaro Rodrigo, Thiziri Belkacem, Aitor Soroa, Eneko Agirre, Mark Cieliebak.* <u>EMNLP 2020</u> [[pdf]](https://arxiv.org/abs/2010.02140)
  4. **How To Evaluate Your Dialogue System: Probe Tasks as an Alternative for Token-level Evaluation Metrics.** *Prasanna Parthasarathi, Joelle Pineau, Sarath Chandar.* <u>arxiv 2020</u> [[pdf]](https://arxiv.org/abs/2008.10427)
  5. **BLEURT: Learning robust metrics for text generation.** *Thibault Sellam, Dipanjan Das, and Ankur Parikh.* <u>ACL 2020</u> [[pdf]](https://doi.org/10.18653/v1/2020.acl-main.704)
  6. **Towards Holistic and Automatic Evaluation of Open-Domain Dialogue Generation.** *Bo Pang, Erik Nijkamp, Wenjuan Han, Linqi Zhou, Yixian Liu, Kewei Tu.* <u>ACL 2020</u> [[pdf]](https://www.aclweb.org/anthology/2020.acl-main.333/)
  7. **Learning an Unreferenced Metric for Online Dialogue Evaluation.** *Koustuv Sinha, Prasanna Parthasarathi, Jasmine Wang, Ryan Lowe, William L. Hamilton, Joelle Pineau.* <u>ACL 2020</u> [[pdf]](https://arxiv.org/abs/2005.00583)
  8. **Evaluating Dialogue Generation Systems via Response Selection.** *Shiki Sato, Reina Akama, Hiroki Ouchi, Jun Suzuki, Kentaro Inui.* <u>ACL 2020</u> [[pdf]](https://arxiv.org/abs/2004.14302)
  9. **Speaker Sensitive Response Evaluation Model.** *JinYeong Bak, Alice Oh.* <u>ACL 2020</u> [[pdf]](Speaker Sensitive Response Evaluation Model)
  10. **USR: An Unsupervised and Reference Free Evaluation Metric for Dialog Generation.** *Shikib Mehri, Maxine Eskenazi.* <u>ACL 2020</u> [[pdf]](https://arxiv.org/abs/2005.00456)
  11. **uBLEU: Uncertainty-Aware Automatic Evaluation Method for Open-Domain Dialogue Systems.** *Tsuta Yuma, Naoki Yoshinaga, Masashi Toyoda.* <u>ACL 2020</u> [[pdf]](https://www.aclweb.org/anthology/2020.acl-srw.27/)
  12. **Beyond User Self-Reported Likert Scale Ratings: A Comparison Model for Automatic Dialog Evaluation.** *Weixin Liang, James Zou, Zhou Yu.* <u>ACL 2020</u> [[pdf]](https://arxiv.org/abs/2005.10716)
  13. **Designing Precise and Robust Dialogue Response Evaluators.** *Tianyu Zhao, Divesh Lala, Tatsuya Kawahara.* <u>ACL 2020 short paper</u> [[pdf]](https://arxiv.org/abs/2004.04908)
  14. **Unsupervised Evaluation of Interactive Dialog with DialoGPT.** *Shikib Mehri, Maxine Eskenazi.* <u>SIGDIAL 2020</u> [[pdf]](https://www.aclweb.org/anthology/2020.sigdial-1.28/)
  15. **Can You Put it All Together: Evaluating Conversational Agents' Ability to Blend Skills.** *Eric Michael Smith, Mary Williamson, Kurt Shuster, Jason Weston, Y-Lan Boureau.* <u>ACL 2020</u> [[pdf]](https://arxiv.org/abs/2004.08449)
  16. **Bertscore: Evaluating text generation with bert.** *Tianyi Zhang, Varsha Kishore, Felix Wu, Kilian Q. Weinberger, and Yoav Artzi.* <u>ICLR 2020</u> [[pdf]](https://openreview.net/forum?id=SkeHuCVFDr)
  17. **Predictive Engagement: An Efficient Metric For Automatic Evaluation of Open-Domain Dialogue Systems.** *Sarik Ghazarian, Ralph Weischedel, Aram Galstyan, Nanyun Peng.* <u>AAAI 2020</u> [[pdf]](https://arxiv.org/abs/1911.01456)
  18. **Learning to compare for better training and evaluation of open domain natural language generation models.** *Wangchunshu Zhou and Ke Xu.* <u>AAAI 2020</u>
  19. **Improving Dialog Evaluation with a Multi-reference Adversarial Dataset and Large Scale Pretraining.** *Ananya B. Sai, Akash Kumar Mohankumar, Siddhartha Arora, Mitesh M. Khapra.* <u>TACL 2020</u> [[pdf]](https://arxiv.org/abs/2009.11321)
  20. **How to Evaluate the Next System: Automatic Dialogue Evaluation from the Perspective of Continual Learning.** *Lu Li, Zhongheng He, Xiangyang Zhou, Dianhai Yu.* <u>arxiv 2019</u> [[pdf]](https://arxiv.org/abs/1912.04664)
  21. **Moverscore: Text generation evaluating with contextualized embeddings and earth mover distance. ** *Wei Zhao, Maxime Peyrard, Fei Liu, Yang Gao, Christian M Meyer, and Steffen Eger.* <u>EMNLP 2019</u>
  22. **TIGEr: Text-to-Image Grounding for Image Caption Evaluation.** *Ming Jiang, Qiuyuan Huang, Lei Zhang, Xin Wang, Pengchuan Zhang, Zhe Gan, Jana Diesner, Jianfeng Gao.* <u>EMNLP 2019</u> [[pdf]](https://www.aclweb.org/anthology/D19-1220/)
  23. **Investigating Evaluation of Open-Domain Dialogue Systems With Human Generated Multiple References.** *Prakhar Gupta, Shikib Mehri, Tiancheng Zhao, Amy Pavel, Maxine Eskenazi, Jeffrey Bigham.* <u>SIGDIAL 2019</u> [[pdf]](https://www.aclweb.org/anthology/W19-5944/)
  24. **Unifying Human and Statistical Evaluation for Natural Language Generation.** *Tatsunori Hashimoto, Hugh Zhang, Percy Liang.* <u>NAACL 2019</u> [[pdf]](https://www.aclweb.org/anthology/N19-1169/)
  25. **Better automatic evaluation of open-domain dialogue systems with contextualized embeddings.** *Sarik Ghazarian, Johnny Wei, Aram Galstyan, and Nanyun Peng.* <u>NAACL 2019 workshop</u>
  26. **Re-evaluating ADEM: A Deeper Look at Scoring Dialogue Responses.** *Ananya B. Sai, Mithun Das Gupta, Mitesh M. Khapra, Mukundhan Srinivasan.* <u>AAAI 2019</u> [[pdf]](https://arxiv.org/abs/1902.08832)
  27. **The price of debiasing automatic metrics in natural language evaluation.** *Arun Tejasvi Chaganty, Stephen Mussman, Percy Liang.* <u>ACL 2018</u> [[pdf]](https://arxiv.org/abs/1807.02202)
  28. **Ruse: Regressor using sentence embeddings for automatic machine translation evaluation.** *Hiroki Shimanaka, Tomoyuki Kajiwara, and Mamoru Komachi.* <u>ACL 2018 workshop</u>
  29. **Towards a Metric for Automated Conversational Dialogue System Evaluation and Improvement.** *Jan Deriu, Mark Cieliebak.* <u>INLG 2018</u> [[pdf]](https://www.inlg2019.com/assets/papers/132_Paper.pdf)
  30. **Ruber: An unsupervised method for automatic evaluation of open-domain dialog systems.** *Chongyang Tao, Lili Mou, Dongyan Zhao, and Rui Yan.* <u>AAAI 2018</u> [[pdf]](https://arxiv.org/abs/1701.03079)
  31. **One “Ruler” for All Languages: Multi-Lingual Dialogue Evaluation with Adversarial Multi-Task Learning.** *Xiaowei Tong, Zhenxin Fu, Mingyue Shang, Dongyan Zhao, Rui Yan.* <u>IJCAI 2018</u> [[pdf]](https://www.ijcai.org/Proceedings/2018/0616.pdf)
  32. **Topic-based Evaluation for Conversational Bots.** *Fenfei Guo, Angeliki Metallinou, Chandra Khatri, Anirudh Raju, Anu Venkatesh, Ashwin Ram.* <u>NeurIPS 2017 workshop</u> [[pdf]](https://arxiv.org/abs/1801.03622)
  33. **On Evaluating and Comparing Open Domain Dialog Systems.** *Anu Venkatesh, Chandra Khatri, Ashwin Ram, Fenfei Guo, Raefer Gabriel, Ashish Nagar, Rohit Prasad, Ming Cheng, Behnam Hedayatnia, Angeliki Metallinou, Rahul Goel, Shaohua Yang, Anirudh Raju.* <u>NeurIPS 2017 workshop</u> [[pdf]](https://arxiv.org/abs/1801.03625)
  34. **Towards an automatic turing test: Learning to evaluate dialogue responses.** *Ryan Lowe, Michael Noseworthy, Iulian Vlad Serban, Nicolas Angelard-Gontier, Yoshua Bengio, and Joelle Pineau.* <u>ACL 2017 Best Paper</u> [[pdf]](https://www.aclweb.org/anthology/P17-1103.pdf)
  35. **Evaluating Story Generation Systems Using Automated Linguistic Analyses.** *Melissa Roemmele, Andrew S. Gordon, Reid Swanson.* <u>ACM SIGKDD 2017</u> [[pdf]](https://people.ict.usc.edu/gordon/public_html/publications/KDD-WS17.PDF)
  36. **Adversarial evaluation of dialogue models. ** *Anjuli Kannan and Oriol Vinyals.* <u>arxiv 2017</u>
  37. **deltaBLEU: A Discriminative Metric for Generation Tasks with Intrinsically Diverse Targets.** <u>ACL  2015</u> [[pdf]](Michel Galley, Chris Brockett, Alessandro Sordoni, Yangfeng Ji, Michael Auli, Chris Quirk, Margaret Mitchell, Jianfeng Gao, Bill Dolan)
  38. **ROUGE: A package for automatic evaluation of summaries.** <u>Chin-Yew Lin.</u> <u>ACL 2004</u> [[pdf]](https://www.aclweb.org/anthology/W04-1013)
  39. **Bleu: a method for automatic evaluation of machine translation.** *Kishore Papineni, Salim Roukos, Todd Ward, and WeiJing Zhu.* <u>ACL 2002</u>

  

  ### 3.2 Protocol for human evaluation

  1. **Towards Best Experiment Design for Evaluating Dialogue System Output.** *Sashank Santhanam, Samira Shaikh.* <u>INLG 2019</u> [[pdf]](https://arxiv.org/abs/1909.10122)
  2. **Communication-based Evaluation for Natural Language Generation.**  <u>SCiL 2019</u> [[pdf]](https://arxiv.org/abs/1909.07290)
  3. **Domain-Independent turn-level Dialogue Quality Evaluation via User Satisfaction Estimation.**  <u>SIGDIAL 2019</u>[[pdf]](https://arxiv.org/pdf/1908.07064.pdf)
  4. **ACUTE-EVAL: Improved Dialogue Evaluation with Optimized Questions and Multi-turn Comparisons.** *Margaret Li, Jason Weston, Stephen Roller.* <u>AAAI 2019</u> [[pdf]](https://arxiv.org/abs/1909.03087) 
  5. **ChatEval: A Tool for the Systematic Evaluation of Chatbots.** *João Sedoc, Daphne Ippolito, Arun Kirubarajan, Jai Thirani, Lyle Ungar, Chris Callison-Burch.* <u>ACL 2018</u> [[pdf]](https://www.aclweb.org/anthology/W18-6709.pdf) 
  6. **Towards a Method For Evaluating Naturalness in Conversational Dialog Systems.** *Victor Hung, Miguel Elvir, Avelino Gonzalez, Ronald DeMara.* <u>IEEE ICSMC 2009</u> [[pdf]](https://ieeexplore.ieee.org/abstract/document/5345904/) 
  7. **Empirical Methods for Evaluating Dialog Systems.** *Tim Paek.* <u>ACL 2001</u> [[pdf]](https://www.aclweb.org/anthology/W01-0902.pdf)

  

  ## 4. Others

  1. **A Systematic Characterization of Sampling Algorithms for Open-ended Language Generation.** *Moin Nadeem, Tianxing He, Kyunghyun Cho, James Glass.* <u>AACL 2020</u> [[pdf]](https://arxiv.org/abs/2009.07243)