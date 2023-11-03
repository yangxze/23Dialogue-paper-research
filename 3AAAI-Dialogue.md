# 一、AAAI介绍

​	AAAI的全称是**人工智能促进协会**（Association for the Advancement of Artificial Intelligence），它是人工智能领域的主要学术组织之一。该组织成立于1979年，原名“美国人工智能协会(American Association for Artificial Intelligence)”，并于2007年更名为“人工智能促进协会（AAAI）”。 它在全球拥有超过6000名成员。 汇集了全球最顶尖的人工智能领域专家学者，一直是人工智能界的研究风向标，在学术界久负盛名。

​	AAAI是一个非营利科学协会，致力于推动对思想和智能行为及其在机器中体现的机制的科学理解。AAAI为人工智能社区提供许多服务。AAAI每年主办许多会议和研讨会，并为人工智能领域的14种期刊提供支持，旨在促进人工智能的研究和负责任的使用。AAAI还旨在增加公众对人工智能的理解，改善人工智能从业者的教学和培训，并就当前人工智能发展和未来方向的重要性和潜力为研究计划者和资助者提供指导。**AAAI主办的“AAAI人工智能会议”，被认为是人工智能领域的顶级会议之一。**



# 二、论文调研-2023对话

[Proceedings of the AAAI Conference on Artificial Intelligence](https://ojs.aaai.org/index.php/AAAI/index)

Issue：[Vol. 37 No. 11: AAAI-23 Technical Tracks 11](https://ojs.aaai.org/index.php/AAAI/issue/view/558)

section：AAAI Technical Track on Speech & Natural Language Processing

**Published:** 2023-06-27



## 1.Dialogue

| Num  | Paper                                                        | Summary                                                      | Note |
| ---- | ------------------------------------------------------------ | ------------------------------------------------------------ | ---- |
| 1    | [Learning to Memorize Entailment and Discourse Relations for Persona-Consistent Dialogues](https://ojs.aaai.org/index.php/AAAI/article/view/26489)<br />学习记忆蕴涵和语篇关系实现角色一致对话 | 背景：现有的研究通过复杂网络结构学习对话者角色来提高了对话系统的性能。但需要更多有标注的个人语料库，此外模型通常执行下一个话语预测来生成回应，忽略了整个对话中话语连贯。<br />Method：1是利用NLP数据集中的蕴涵文本对，通过前提-假设生成任务学习潜在的蕴涵关系作为外部记忆。2将具有相似结构的内部记忆应用于对话中的话语信息。通过两种记忆相互协作，以获得代的蕴涵和话语表征。在PersonaChat 和DSTC7-AVSD测试在角色一致性和响应一致性方面优于base。[code](https://github.com/Chenrj233/LMEDR)==【QA】== |      |
| 2    | [Learning towards Selective Data Augmentation for Dialogue Generation](https://ojs.aaai.org/index.php/AAAI/article/view/26491)<br />学习用于对话生成的选择性数据增强 | Background：目前关于对话生成任务的数据增强技术大多是增强训练数据集中的所有案例，而没有考虑不同案例之间的内在属性。<br />作者认为适合增强的情况应遵循以下两个属性：低质量和代表性。提出一个采用双对抗网络的SDA来选择最低质量和最具代表性的数据。实验显示在DailyDialog 和OpenSubtitles上改进了响应生成性能。==【Data Augmentation】== |      |
| 3    | [Learning to Imagine: Distillation-Based Interactive Context Exploitation for Dialogue State Tracking](https://ojs.aaai.org/index.php/AAAI/article/view/26510)<br />学习想象：基于蒸馏的DST交互式上下文利用 | Background：由于“先选择，后使用”机制显式地过滤了传递给下游状态预测的分散信息，也不可避免的过滤掉了关键信息。<br />提出了一种模型无关模块DICE-DST应用于部分历史DST，来增强DST模型编码器的上下文利用能力。设计一个教师encoder学习知识，再通过一种回合级注意对齐蒸馏将上下文知识从教师encoder转移到学生encoder。此方法大大提高了部分历史DST模型性能。==【DST】== |      |
| 4    | [Personalized Dialogue Generation with Persona-Adaptive Attention](https://ojs.aaai.org/index.php/AAAI/article/view/26518)<br />用角色适应的注意力来个性对话生成 | Background：基于角色的对话需要在情境和角色之间保持微妙的权重平衡。<br />提出了一个有效的角色适应注意(PAA)框架，来自适应地整合integrate人物角色和语境信息的权重。在PAA中应用了动态掩蔽机制，去除的冗余信息和避免过拟合。实验显示与在全数据环境中训练的更大型模型相比，仅使用20%到30%的数据就能获得类似的结果。==【Dialogue Generation】== |      |
| 5    | [Explaining (Sarcastic) Utterances to Enhance Affect Understanding in Multimodal Dialogues](https://ojs.aaai.org/index.php/AAAI/article/view/26526)<br />在多模态对话中解释(讽刺)话语以加强情感理解 | 作者探讨了对话中的讽刺解释任务，旨在揭示讽刺话语背后隐藏的反讽。提出了一个深度神经网络MOSES，它以一个多模态(讽刺)对话实例作为输入，并生成一个自然语言句子作为其解释。在不同的评估指标上，MOSES比最先进的SED系统平均高出约2%。==【Multimodal Dialogues】== |      |
| 6    | [Mitigating Negative Style Transfer in Hybrid Dialogue System](https://ojs.aaai.org/index.php/AAAI/article/view/26539)<br />减轻混合对话系统中的消极风格迁移 | Background：现有研究利用多任务融合技术同时学习两种任务，但忽略了独特的语篇风格差异所导致的负迁移现象。<br />作者为不同的数据集设计了监督和自监督的正样本和负样本结构。为了利用解耦潜在变量中包含的样式信息，使用了一个包含潜在变量的样式前缀来进一步控制具有不同样式的响应的生成。==【Dialogue Systems】== |      |
| 7    | [Heterogeneous-Branch Collaborative Learning for Dialogue Generation](https://ojs.aaai.org/index.php/AAAI/article/view/26544)<br />对话生成的异构分支协作学习 | 协作学习，是在缺乏训练效果好的大教师模型的情况下进行一阶段蒸馏的有效方式。然而，由于训练目标相和训练集独立相同，存在严重的分支同质性问题。<br />作者在网络分支训练中考虑了对话属性。每个分支根据选择的子集学习与属性相关的特征。提出了一种基于双群的知识蒸馏方法，包括正蒸馏和负蒸馏，以稳定和可解释的方式进一步丰富不同分支的特征。==【Dialogue Generation】== |      |
| 8    | [Learning to Know Myself: A Coarse-to-Fine Persona-Aware Training Framework for Personalized Dialogue Generation](https://ojs.aaai.org/index.php/AAAI/article/view/26545)<br />面向个性化对话生成的从粗到精的人物感知训练框架 | 以前使用最大似然估计训练的基于人物角色的对话代理倾向于忽略给定的人物角色，并生成与人物角色无关或不一致的响应。<br />提出了一个由粗到精的两阶段角色感知训练框架。首先训练对话代理回答构建的人物角色感知问题，然后，通过显式感知一致响应和生成的不一致响应之间的差异，使用对比学习范式进一步训练对话代理。在生成响应的一致性上显著提高。==【Personalized Dialogue Generation】== |      |
| 9    | [A Disentangled-Attention Based Framework with Persona-Aware Prompt Learning for Dialogue Generation](https://ojs.aaai.org/index.php/AAAI/article/view/26556)<br />具有人物感知提示学习的解耦注意力框架的对话生成 | 提出了一种基于解耦注意力的预训练架构，该架构结合了角色感知的提示学习，以联系所选角色和响应生成。首先利用会话流来选择与上下文相关的人物角色。再通过角色感知提示丰富肤浅的角色描述，增加额外的个性特征。最后利用解耦注意力机制和类似A *的基于关键字的启发式估计来实现可控生成。在PERSONA-CHAT数据集上提供更一致和更吸引人的响应。==【Dialogue Generation】== |      |
| 10   | [Towards Complex Scenarios: Building End-to-End Task-Oriented Dialogue System across Multiple Knowledge Bases](https://ojs.aaai.org/index.php/AAAI/article/view/26581)<br />面向复杂场景:跨多个知识库构建端到端的面向任务的对话系统 | 大多数现有的etod仅限于单个KB设置，作者考虑了etod中的多kb场景，并引入了KB-over-KB异构图注意网络(kk - han)来促进模型对多个kb的推理。核心模块是一个三重连接图交互层，可以跨不同kb(即kb内连接、kb间连接和对话- kb连接)对不同粒度级别的交互信息进行建模。实验结果证实了该模型在多KBs推理中的优越性。==【Task-Oriented Dialogue】== |      |
| 11   | [Towards Diverse, Relevant and Coherent Open-Domain Dialogue Generation via Hybrid Latent Variables](https://ojs.aaai.org/index.php/AAAI/article/view/26594)<br />通过混合潜在变量生成多样、相关和连贯的开放域对话 | 作者结合连续潜变量和离散潜变量的优点，提出了一种混合潜变量(HLV)方法。在DailyDialog和Opensubtitles上的实验表明，CHVT比传统的基于transformer的变分机制(包括多样性、相关性和相干性指标)更优。==【Open-Domain】== |      |
| 12   | [Taming Continuous Posteriors for Latent Variational Dialogue Policies](https://ojs.aaai.org/index.php/AAAI/article/view/26602) | ==【Dialogue Policies】==                                    |      |
| 13   | [Dialogue Rewriting via Skeleton-Guided Generation](https://ojs.aaai.org/index.php/AAAI/article/view/26619) | ==【】==                                                     |      |
| 14   | [Dialogue State Distillation Network with Inter-slot Contrastive Learning for Dialogue State Tracking](https://ojs.aaai.org/index.php/AAAI/article/view/26620) | ==【】==                                                     |      |
| 15   | [Balanced Meta Learning and Diverse Sampling for Lifelong Task-Oriented Dialogue Systems](https://ojs.aaai.org/index.php/AAAI/article/view/26621) | ==【】==                                                     |      |



## 2.Conversation

| Num  | Paper                                                        | Summary  |      |
| ---- | ------------------------------------------------------------ | -------- | ---- |
| 1    | [End-to-End Deep Reinforcement Learning for Conversation Disentanglement](https://ojs.aaai.org/index.php/AAAI/article/view/26480) | ==【】== |      |
| 2    | [CP-Rec: Contextual Prompting for Conversational Recommender Systems](https://ojs.aaai.org/index.php/AAAI/article/view/26487) | ==【】== |      |
| 3    | [MIGA: A Unified Multi-Task Generation Framework for Conversational Text-to-SQL](https://ojs.aaai.org/index.php/AAAI/article/view/26504) | ==【】== |      |
| 4    | [SKIER: A Symbolic Knowledge Integrated Model for Conversational Emotion Recognition](https://ojs.aaai.org/index.php/AAAI/article/view/26541) | ==【】== |      |
| 5    | [SPRING: Situated Conversation Agent Pretrained with Multimodal Questions from Incremental Layout Graph](https://ojs.aaai.org/index.php/AAAI/article/view/26562) | ==【】== |      |
| 6    | [BERT-ERC: Fine-Tuning BERT Is Enough for Emotion Recognition in Conversation](https://ojs.aaai.org/index.php/AAAI/article/view/26582) | ==【】== |      |
| 7    | [ConvNTM: Conversational Neural Topic Model](https://ojs.aaai.org/index.php/AAAI/article/view/26595) | ==【】== |      |
| 8    | [Contrastive Learning Reduces Hallucination in Conversations](https://ojs.aaai.org/index.php/AAAI/article/view/26596) | ==【】== |      |
|      |                                                              |          |      |



## 3.Interaction

| Num  | Paper                                                        | Summary  |      |
| ---- | ------------------------------------------------------------ | -------- | ---- |
| 1    | [Improving Interpretability via Explicit Word Interaction Graph Layer](https://ojs.aaai.org/index.php/AAAI/article/view/26586) | ==【】== |      |
| 2    | [Improving Biomedical Entity Linking with Cross-Entity Interaction](https://ojs.aaai.org/index.php/AAAI/article/view/26624) | ==【】== |      |
| 3    | [Knowledge-Bridged Causal Interaction Network for Causal Emotion Entailment](https://ojs.aaai.org/index.php/AAAI/article/view/26641) | ==【】== |      |



