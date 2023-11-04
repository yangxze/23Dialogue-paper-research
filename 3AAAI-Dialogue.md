# 一、AAAI介绍

​	AAAI的全称是**人工智能促进协会**（Association for the Advancement of Artificial Intelligence），它是人工智能领域的主要学术组织之一。该组织成立于1979年，原名“美国人工智能协会(American Association for Artificial Intelligence)”，并于2007年更名为“人工智能促进协会（AAAI）”。 它在全球拥有超过6000名成员。 汇集了全球最顶尖的人工智能领域专家学者，一直是人工智能界的研究风向标，在学术界久负盛名。
​	AAAI是一个非营利科学协会，致力于推动对思想和智能行为及其在机器中体现的机制的科学理解。AAAI为人工智能社区提供许多服务。AAAI每年主办许多会议和研讨会，并为人工智能领域的14种期刊提供支持，旨在促进人工智能的研究和负责任的使用。AAAI还旨在增加公众对人工智能的理解，改善人工智能从业者的教学和培训，并就当前人工智能发展和未来方向的重要性和潜力为研究计划者和资助者提供指导。**AAAI主办的“AAAI人工智能会议”，被认为是人工智能领域的顶级会议之一。**



# 二、论文调研-2023对话

[Proceedings of the AAAI Conference on Artificial Intelligence](https://ojs.aaai.org/index.php/AAAI/index)

Issue：[Vol. 37 No. 11: AAAI-23 Technical Tracks 11](https://ojs.aaai.org/index.php/AAAI/issue/view/558)

section：AAAI Technical Track on Speech & Natural Language Processing

**Published:** 2023-06-27



## 1.Dialogue

| Num  | Paper                                                        | Summary                                                      |
| :--: | ------------------------------------------------------------ | ------------------------------------------------------------ |
|  1   | [Learning to Memorize Entailment and Discourse Relations for Persona-Consistent Dialogues](https://ojs.aaai.org/index.php/AAAI/article/view/26489)<br />学习记忆蕴涵和语篇关系实现角色一致对话 | 背景：现有的研究通过复杂网络结构学习对话者角色来提高了对话系统的性能。但需要更多有标注的个人语料库，此外模型通常执行下一个话语预测来生成回应，忽略了整个对话中话语连贯。<br />Method：1是利用NLP数据集中的蕴涵文本对，通过前提-假设生成任务学习潜在的蕴涵关系作为外部记忆。2将具有相似结构的内部记忆应用于对话中的话语信息。通过两种记忆相互协作，以获得代的蕴涵和话语表征。在PersonaChat 和DSTC7-AVSD测试在角色一致性和响应一致性方面优于base。[code](https://github.com/Chenrj233/LMEDR)【QA】 |
|  2   | [Learning towards Selective Data Augmentation for Dialogue Generation](https://ojs.aaai.org/index.php/AAAI/article/view/26491)<br />学习用于对话生成的选择性数据增强 | Background：目前关于对话生成任务的数据增强技术大多是增强训练数据集中的所有案例，而没有考虑不同案例之间的内在属性。<br />作者认为适合增强的情况应遵循以下两个属性：低质量和代表性。提出一个采用双对抗网络的SDA来选择最低质量和最具代表性的数据。实验显示在DailyDialog 和OpenSubtitles上改进了响应生成性能。【Data Augmentation】 |
|  3   | [Learning to Imagine: Distillation-Based Interactive Context Exploitation for Dialogue State Tracking](https://ojs.aaai.org/index.php/AAAI/article/view/26510)<br />学习想象：基于蒸馏的DST交互式上下文利用 | Background：由于“先选择，后使用”机制显式地过滤了传递给下游状态预测的分散信息，也不可避免的过滤掉了关键信息。<br />提出了一种模型无关模块DICE-DST应用于部分历史DST，来增强DST模型编码器的上下文利用能力。设计一个教师encoder学习知识，再通过一种回合级注意对齐蒸馏将上下文知识从教师encoder转移到学生encoder。此方法大大提高了部分历史DST模型性能。【DST】 |
|  4   | [Personalized Dialogue Generation with Persona-Adaptive Attention](https://ojs.aaai.org/index.php/AAAI/article/view/26518)<br />用角色适应的注意力来个性对话生成 | Background：基于角色的对话需要在情境和角色之间保持微妙的权重平衡。<br />提出了一个有效的角色适应注意(PAA)框架，来自适应地整合integrate人物角色和语境信息的权重。在PAA中应用了动态掩蔽机制，去除的冗余信息和避免过拟合。实验显示与在全数据环境中训练的更大型模型相比，仅使用20%到30%的数据就能获得类似的结果。【Dialogue Generation】 |
|  5   | [Explaining (Sarcastic) Utterances to Enhance Affect Understanding in Multimodal Dialogues](https://ojs.aaai.org/index.php/AAAI/article/view/26526)<br />在多模态对话中解释(讽刺)话语以加强情感理解 | 作者探讨了对话中的讽刺解释任务，旨在揭示讽刺话语背后隐藏的反讽。提出了一个深度神经网络MOSES，它以一个多模态(讽刺)对话实例作为输入，并生成一个自然语言句子作为其解释。在不同的评估指标上，MOSES比最先进的SED系统平均高出约2%。【Multimodal Dialogues】 |
|  6   | [Mitigating Negative Style Transfer in Hybrid Dialogue System](https://ojs.aaai.org/index.php/AAAI/article/view/26539)<br />减轻混合对话系统中的消极风格迁移 | Background：现有研究利用多任务融合技术同时学习两种任务，但忽略了独特的语篇风格差异所导致的负迁移现象。<br />作者为不同的数据集设计了监督和自监督的正样本和负样本结构。为了利用解耦潜在变量中包含的样式信息，使用了一个包含潜在变量的样式前缀来进一步控制具有不同样式的响应的生成。【Dialogue Systems】 |
|  7   | [Heterogeneous-Branch Collaborative Learning for Dialogue Generation](https://ojs.aaai.org/index.php/AAAI/article/view/26544)<br />对话生成的异构分支协作学习 | 协作学习，是在缺乏训练效果好的大教师模型的情况下进行一阶段蒸馏的有效方式。然而，由于训练目标相和训练集独立相同，存在严重的分支同质性问题。<br />作者在网络分支训练中考虑了对话属性。每个分支根据选择的子集学习与属性相关的特征。提出了一种基于双群的知识蒸馏方法，包括正蒸馏和负蒸馏，以稳定和可解释的方式进一步丰富不同分支的特征。【Dialogue Generation】 |
|  8   | [Learning to Know Myself: A Coarse-to-Fine Persona-Aware Training Framework for Personalized Dialogue Generation](https://ojs.aaai.org/index.php/AAAI/article/view/26545)<br />面向个性化对话生成的从粗到精的人物感知训练框架 | 以前使用最大似然估计训练的基于人物角色的对话代理倾向于忽略给定的人物角色，并生成与人物角色无关或不一致的响应。<br />提出了一个由粗到精的两阶段角色感知训练框架。首先训练对话代理回答构建的人物角色感知问题，然后，通过显式感知一致响应和生成的不一致响应之间的差异，使用对比学习范式进一步训练对话代理。在生成响应的一致性上显著提高。【Personalized Dialogue Generation】 |
|  9   | [A Disentangled-Attention Based Framework with Persona-Aware Prompt Learning for Dialogue Generation](https://ojs.aaai.org/index.php/AAAI/article/view/26556)<br />具有人物感知提示学习的解耦注意力框架的对话生成 | 提出了一种基于解耦注意力的预训练架构，该架构结合了角色感知的提示学习，以联系所选角色和响应生成。首先利用会话流来选择与上下文相关的人物角色。再通过角色感知提示丰富肤浅的角色描述，增加额外的个性特征。最后利用解耦注意力机制和类似A *的基于关键字的启发式估计来实现可控生成。在PERSONA-CHAT数据集上提供更一致和更吸引人的响应。【Dialogue Generation】 |
|  10  | [Towards Complex Scenarios: Building End-to-End Task-Oriented Dialogue System across Multiple Knowledge Bases](https://ojs.aaai.org/index.php/AAAI/article/view/26581)<br />面向复杂场景:跨多个知识库构建端到端的面向任务的对话系统 | 大多数现有的etod仅限于单个KB设置，作者考虑了etod中的多kb场景，并引入了KB-over-KB异构图注意网络(kk - han)来促进模型对多个kb的推理。核心模块是一个三重连接图交互层，可以跨不同kb(即kb内连接、kb间连接和对话- kb连接)对不同粒度级别的交互信息进行建模。实验结果证实了该模型在多KBs推理中的优越性。【Task-Oriented Dialogue】 |
|  11  | [Towards Diverse, Relevant and Coherent Open-Domain Dialogue Generation via Hybrid Latent Variables](https://ojs.aaai.org/index.php/AAAI/article/view/26594)<br />通过混合潜在变量生成多样、相关和连贯的开放域对话 | 作者结合连续潜变量和离散潜变量的优点，提出了一种混合潜变量(HLV)方法。在DailyDialog和Opensubtitles上的实验表明，CHVT比传统的基于transformer的变分机制(包括多样性、相关性和相干性指标)更优。【Open-Domain】 |
|  12  | [Taming Continuous Posteriors for Latent Variational Dialogue Policies](https://ojs.aaai.org/index.php/AAAI/article/view/26602)<br />潜在变分对话策略的连续后验驯服 | 绝对后验一直被认为是表现的主要驱动因素之一。作者重新审视了潜在动作强化学习的高斯变分后验，并表明它们可以产生比分类更好的性能。使用连续潜表示，我们的模型在MultiWOZ基准上实现了最先进的对话成功率。【Task-oriented Dialogue】 |
|  13  | [Dialogue Rewriting via Skeleton-Guided Generation](https://ojs.aaai.org/index.php/AAAI/article/view/26619)<br />对话重写通过框架引导生成 | 现实世界对话经常是嘈杂的并且带有各种各样的错误。因此提出了现实世界对话重写语料库(RealDia)，一个新的基准用于评估当前对话重写系统如何处理现实世界中嘈杂和无信息的对话。RealDia包含来自真实场景的注释多回合对话，其中包含ASR错误，拼写错误，冗余等噪音。提出了框架引导重写SGR算法，来引导生成范式解决对话重写问题。【Dialogue rewriting 】 |
|  14  | [Dialogue State Distillation Network with Inter-slot Contrastive Learning for Dialogue State Tracking](https://ojs.aaai.org/index.php/AAAI/article/view/26620)<br />DST上的基于槽间对比学习的对话状态蒸馏网络 | 不同slots的更新之间的关系为DST提供了重要的线索，现有的方法仅依赖于预定义的图来间接捕获关系。作者提出了一种对话状态蒸馏网络(DSDN)来利用以前对话状态的相关信息，弥补训练和测试之间的利用差距。还提出了一个槽间对比学习损失，以有效地捕获对话上下文中的槽共同更新关系。在MultiWOZ 2.0/2.1达到SOTA。【DST】 |
|  15  | [Balanced Meta Learning and Diverse Sampling for Lifelong Task-Oriented Dialogue Systems](https://ojs.aaai.org/index.php/AAAI/article/view/26621)<br />终身任务导向对话系统的平衡元学习和多样化采样 | 作者提出了一种两阶段终身任务导向的对话生成方法，以减轻灾难性遗忘并同时鼓励知识转移。设计了一种平衡的元学习策略，用于终身学习过程中的前向和后向知识转移。采用基于不确定性的采样策略，选择并存储有代表性的对话样本到情景记忆中以进行向后知识迁移。[code](https: //github.com/travis-xu/MetaLTDS.)【 lifelong Task-Oriented Dialogue 】 |



## 2.Conversation

| Num  | Paper                                                        | Summary                                                      |
| :--: | ------------------------------------------------------------ | ------------------------------------------------------------ |
|  1   | [End-to-End Deep Reinforcement Learning for Conversation Disentanglement](https://ojs.aaai.org/index.php/AAAI/article/view/26480)<br />端到端深度强化学习对话解纠缠 | 对话分离的任务是将这些混杂的信息聚类到对话中。提出了一种直接优化全局度量的端到端强化学习(RL)方法。观察到使用现有的全局指标，如信息变化和调整后的rand指数作为RL代理的奖励，会使其性能恶化。因此提出了一种新的线程级奖励函数，它在不忽略局部决策的情况下捕获全局度量。【Conversation Disentanglement】 |
|  2   | [CP-Rec: Contextual Prompting for Conversational Recommender Systems](https://ojs.aaai.org/index.php/AAAI/article/view/26487)<br />对话推荐系统的上下文提示 | 作者提出了一个新的对话管理上下文提示框架，它基于上下文、主题和用户配置文件优化提示。并进一步采用外部知识来丰富用户档案，并提供基于知识的推荐。结合这些技术，提出了一个具有上下文提示的会话推荐系统CP-Rec。【Recommender Systems】 |
|  3   | [MIGA: A Unified Multi-Task Generation Framework for Conversational Text-to-SQL](https://ojs.aaai.org/index.php/AAAI/article/view/26504)<br />对话文本到sql的统一多任务生成框架 | 作者提出了一个两阶段统一的多任务生成框架(MIGA)，它利用plm的能力来处理对话文本到sql。在预训练阶段，MIGA先将主任务分解为多个相关的子任务，然后使用特定于任务的自然语言提示将它们统一为同一个Seq2Seq范式，从而从多任务训练中提升主任务。微调阶段，提出了四种SQL扰动来减轻错误传播问题。【Conversational Text-to-SQL】 |
|  4   | [SKIER: A Symbolic Knowledge Integrated Model for Conversational Emotion Recognition](https://ojs.aaai.org/index.php/AAAI/article/view/26541) | 作者通过建模话语之间的话语关系并将符号知识纳入多方对话来解决这些ERC挑战。首先在ERC中引入了一种对话解析算法，并通过迁移学习的方法进一步改进。并利用不同的符号知识图关系来学习ERC任务的知识增强特征。【Emotion recognition】 |
|  5   | [SPRING: Situated Conversation Agent Pretrained with Multimodal Questions from Incremental Layout Graph](https://ojs.aaai.org/index.php/AAAI/article/view/26562)<br />基于增量布局图的多模态问题预训练情境对话代理 | 作者提出SPRING，该agent具有在拥挤情境中推理多跳空间关系并将其与视觉属性连接起来的能力。设计了两种类型的多模式问答(MQA)任务来预训练agent。在预训练中使用的所有QA对都是由新的增量布局图(ILG)生成的，利用ILG自动标注的QA对难度标签，促进基于mqa的课程学习。【Conversation Agent】 |
|  6   | [BERT-ERC: Fine-Tuning BERT Is Enough for Emotion Recognition in Conversation](https://ojs.aaai.org/index.php/AAAI/article/view/26582)<br />微调BERT是足够的对于对话情感识别 | 作者提出了一种新的范式，即在微调步骤中探索上下文信息和对话结构信息，并在输入文本、分类结构和训练策略方面使PLM适应ERC任务。根据提此范式开发了BERT-ERC模型，从暗示性文本、细粒度分类模块和两阶段训练三个方面提高ERC性能。大量实验表明，所提出的范式明显优于先前的范式，并且可以适应各种场景。【Emotion Recognition】 |
|  7   | [ConvNTM: Conversational Neural Topic Model](https://ojs.aaai.org/index.php/AAAI/article/view/26595)<br />对话神经主题模型 | 作者假设在不同的文本分析任务中，建模主题具有不同的特征。并提出了一个专门针对会话场景设计的会话神经主题模型ConvNTM，与一般文档主题建模不同，会话持续多个回合并有多个角色参与。通过多回合和多角色的表述来模拟对话中的话题，还利用词共现关系作为新的训练目标，进一步提高主题质量。【 Neural Topic Model】 |
|  8   | [Contrastive Learning Reduces Hallucination in Conversations](https://ojs.aaai.org/index.php/AAAI/article/view/26596)<br />对比学习减少对话中的幻觉 | 作者提出了一个对比学习方案MixCL。一种新型的混合对比目标提出以显式优化lm的内隐知识获取过程，从而减少他们在对话中的幻觉。还研究了检索硬底片和模型生成底片的负抽样策略。在Wizard-of-Wikipedia上进行了实验，并评估了MixCL的有效性。【Conversations Hallucination】 |





## 3.Interaction

| Num  | Paper                                                        | Summary                                                      |
| :--: | ------------------------------------------------------------ | ------------------------------------------------------------ |
|  1   | [Improving Interpretability via Explicit Word Interaction Graph Layer](https://ojs.aaai.org/index.php/AAAI/article/view/26586)通过显式词交互图层提高可解释性 | 提出了一个可训练的WIGRAP，学习单词之间的全局交互图，然后使用学习到的单词交互来选择更多信息丰富的单词。并且可以在它的词嵌入层之后插入任何基于神经网络的NLP文本分类器。实验表明添加WIGRAPH层可以显著提高NLP模型的可解释性，同时增强模型的预测性能。**【model interpretability】** |
|  2   | [Improving Biomedical Entity Linking with Cross-Entity Interaction](https://ojs.aaai.org/index.php/AAAI/article/view/26624)<br />以跨实体交动改善生物医学实体链接 | 生物医学EL是将生物医学文档中的提及与知识库中的相应实体链接起来的任务。重排模型在候选项之间缺乏细粒度的交互，并且在面对高度词汇相似性的候选项时可能无法处理模糊提及。提出基于提示调优的重排模型来处理这个问题，还提出了一种kb增强的自监督预训练策略。在NCBI disease, BC5CDR and COMETA达到SOTA。[code](https://github.com/HITsz-TMG/Prompt-BioEL)**【Entity Linking】** |
|  3   | [Knowledge-Bridged Causal Interaction Network for Causal Emotion Entailment](https://ojs.aaai.org/index.php/AAAI/article/view/26641)<br />面向因果情感蕴涵的知识桥式因果互动网络 | 作者提出了以常识知识(CSK)为杠杆的知识桥式因果交互网络KBCIN。为每个会话构建一个会话图，并利用以事件为中心的CSK作为语义级桥(S-bridge)，通过CSK增强的图注意模块捕获会话上下文中的深层话语间依赖关系。[code](https://github.com/circle-hit/KBCIN)**【Causal Emotion Entailmen】** |



