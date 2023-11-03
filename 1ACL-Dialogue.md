



# 一、ACL介绍

​	国际计算语言学学会（ACL，The Association for Computational Linguistics），1962年成立，ACL是世界上影响力最大、最具活力的国际学术组织，是自然语言处理领域影响力最大、最具活力的顶级国际学术组织，每年举办一次。1982年和1999年，ACL分别成立了欧洲分会（EACL）和北美分会（NAACL）两个区域性分会。2018年7月，国际计算语言学学会亚太地区分会（AACL）成立 。

[AI, NLP, ML领域国际会议、期刊 - 知乎](https://zhuanlan.zhihu.com/p/569964700?utm_id=0)



# 二、论文调研-2023对话

[Proceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)](https://aclanthology.org/events/acl-2023/#2023acl-long)



## 1.Dialogue

| Num          | Paper                                                        | Time      | Summary                                                      |
| ------------ | ------------------------------------------------------------ | --------- | ------------------------------------------------------------ |
| 1            | [Prompter: Zero-shot Adaptive Prefixes for Dialogue State Tracking Domain Adaptation](https://aclanthology.org/2023.acl-long.252/)<br />Prompter: 用于DST领域自适应的零样本自适应前缀 | 2023 july | 对于DST对话状态跟踪，不使用监督数据让模型能够适应于新领域的挑战。文章提出使用目标领域的描述提示词生成动态前缀然后拼接到key和value上在每层的自注意力机制上。Prompter在多领域MultiWOZ和SGD基准测试中都优于以前的方法。**【DST】** |
| 2*           | [A Synthetic Data Generation Framework for Grounded Dialogues](https://aclanthology.org/2023.acl-long.608/)<br />基于对话的合成数据框架 | 2023 july | 提出一种用于生成具体对话的合成数据的框架，称为Synthetic Data Generation Framework（SynDG）。主要用T5和免费可获取知识（wiki，个人资料等）来生成数据，其中设计SynDG的关键思想是在生成过程中考虑对话的流程（使用一种启发式方法并用T5生成数据）和连贯性（分别在流程级别和话语级别进行过滤）。最后在基准上由该框架生成对话数据能够显著提高模型全数据训练和低资源情境中的性能。**【Grounded Dialogues】** |
| 3<br />day1  | [Span-Selective Linear Attention Transformers for Effective and Robust Schema-Guided Dialogue State Tracking](https://arxiv.org/abs/2306.09340) arxiv<br />用于高效和鲁棒的SGDST任务的SPLAT | 2023 june | 介绍了一种新型的对话状态跟踪模型，名为SPLAT，用于处理schema-guided对话状态跟踪任务。它通过将输出限制在有限的预测空间内，实现了更好的泛化和效率。同时，该模型允许在描述和历史之间进行丰富的注意力，此外通过引入线性时间注意力来控制计算成本。在SGD数据集上取得了85.3的JGA。**【DST】** |
| 4            | [Knowledge-enhanced Mixed-initiative Dialogue System for Emotional Support Conversations](https://aclanthology.org/2023.acl-long.225/)<br />情感支持对话的知识增强型混合主动对话系统 | 2023 july | 论文对混合主动ESC系统进行了新颖的分析，将话语分为不同类型的说话者角色和主动类型，并提出了四个情感支持指标，用于评估混合主动互动。该分析揭示了构建混合主动ESC系统的必要和挑战。因此提出了一种知识增强的混合主动框架（KEMI）用于ESC，它从大规模心理健康知识图中检索实际案例知识以生成混合主动响应。**【Dialogue System】** |
| 5            | [Towards Faithful Dialogues via Focus Learning](https://aclanthology.org/2023.acl-long.250/)<br />通过注意学习实现可信对话 | 2023 july | 现有的模型在很大程度上依赖复杂的数据工程或增加模型参数，而忽视跟踪对损失有重大影响的tokens。因此提出了"焦点学习"（FocusL），通过直接缩放相关的目标损失来调整每个token对优化方向贡献。具体来说引入一种定位方法利用知识和每个回答token的相似性分布来定位知识感知tokens。然后设计了一种相似性到权重的转换，为交叉熵损失提供动态的token-level权重。最后使用加权损失鼓励模型更加关注知识利用。**【Faithful Dialogues】** |
| 6            | [Injecting knowledge into language generation: a case study in auto-charting after-visit care instructions from medical dialogue](https://aclanthology.org/2023.acl-long.133/)<br />将知识注入语言生成：医学对话中自动生成随访护理指南的案例研究 | 2023 july | 维护事实准确性的重要要求之一是处理罕见token的能力。对于富含知识的高风险领域，论文利用知识（a）识别源和参考中出现的重要罕见token，以及（b）提高它们的条件概率。再引入“利用率”编码知识并作为正则项通过最大化所选token的边缘概率。通过知识注入方法来纠正具有高利用率的特定医学概念在传统训练的序列到序列模型中被低估的情况。<br />**【Medical Dialogue】** |
| 7*           | [MMDialog: A Large-scale Multi-turn Dialogue Dataset Towards Multi-modal Open-domain Conversation<br />](https://aclanthology.org/2023.acl-long.405/)[MMDialog](https://github.com/victorsungo/MMDialog): 一个面向多模态开放域对话的大规模多轮对话数据集 | 2023 july | MMDialog由经过策划的108万个实际对话组成，并包含了153万个独特的图像，横跨了4184个话题。有两个优势，其一是最大的多模态对话数据集，相比以前的数据集多了88倍，其二是包含了大量的主题。对这个数据集提出并规范化了基于检索和生成场景的两个响应预测任务和一种新颖的评估指标MM-Relevance。此外，也构建了上述任务的两个基线模型。<br />**【Multi-turn/Multi -model Dialogue/DataSet】** |
| 8<br />day2  | [Schema-Guided User Satisfaction Modeling for Task-Oriented Dialogues](https://aclanthology.org/2023.acl-long.116/)<br />任务导向对话的模式引导用户满意度建模 | 2023 july | 提出了一种新的模式引导用户满意度建模框架SG-USM，明确建模用户对任务属性的满足程度，以预测用户满意度水平。SG-USM使用预训练语言模型编码对话和任务属性，接着实现表示层来学习对话中完成了多少任务属性，这是一个用于计算任务属性重要性的重要性预测组件，最后基于任务属性实现度和任务属性重要性预测用户满意度。实验结果显示SG-USM在多个基准数据集上表现更好。框架提高了用户满意度建模的可解释性，具有良好的可扩展性。[Code](https://github.com/amzn/user-satisfaction-modeling)<br />**【Task-Oriented Dialogues】** |
| 9            | [Don’t Forget Your ABC’s: Evaluating the State-of-the-Art in Chat-Oriented Dialogue Systems<br />](https://aclanthology.org/2023.acl-long.839/)不要忘记你的ABC：面向聊天的对话系统的最新评估技术 | 2023 july | 对于对话系统，因为评估受固有主观性的影响，此外对话评估中的方法和标签尚未完全标准化。因此，需要一种可以可靠测量对话能力多个方面的维度评估方法，特别是针对面向聊天的开放领域对话系统。本文提出了一种新颖的人类评估方法，用于估计多个对话系统行为的频率。**【Chat-Oriented Dialogue/Evaluation】** |
| 10           | [On the Compositional Generalization in Versatile Open-domain Dialogue](https://aclanthology.org/2023.acl-long.760/)<br />多功能开放领域对话中的组合泛化 | 2023 july | 开发了一种稀疏激活的模块化网络：（1）我们提出了一套全面的运算符，并使用独立的模块来实例化每个运算符；（2）我们将对话生成的过程构建成执行生成的程序，该程序递归地组合和组装模块。模型仅在10%的数据上训练在4个数据集上表现优于最先进的监督方法。<br />**【Open-domain Dialogue】** |
| 11           | [LiveChat: A Large-Scale Personalized Dialogue Dataset Automatically Constructed from Live Streaming](https://arxiv.org/abs/2306.08401) arxiv<br />LiveChat: 基于直播自动构建的大规模个性化对话数据集 | 2023 june | 引入了LiveChat数据集，该数据集由133万个现实生活中的中文对话组成，有351个角色和其细粒度档案和每个角色有近3800个对话。这个数据集是通过处理互联网上大量的直播视频自动生成。**【DataSet】** |
| 12           | [Reference Matters: Benchmarking Factual Error Correction for Dialogue Summarization with Fine-grained Evaluation Framework](https://aclanthology.org/2023.acl-long.779/)<br />参考关键：使用细粒度评估框架对对话摘要的事实错误修正进行基准测试 | 2023 july | 事实性对于对话摘要至关重要，当前依赖于事实性指标的Factual error correction（FEC）评估既不可靠。论文首次为对话摘要手动注释了包含4000个项目的FEC数据集，并提出了FERRANTI，一种基于参考修正的细粒度评估框架，它可以自动评估FEC模型在不同错误类别上的性能。**【Dialogue Summarization】** |
| 13           | [Dialogue Summarization with Static-Dynamic Structure Fusion Graph](https://aclanthology.org/2023.acl-long.775/)<br />使用静态动态结构融合图的对话摘要 | 2023 july | 在论文中提出了一种基于静态-动态图的对话摘要模型（SDDS），它融合了来自人类专业知识的先验知识，并以端到端的学习方式自适应地学习图结构。为了验证SDDS的有效性，在三个基准数据集（SAMSum、MediaSum和DialogSum）上进行了实验，结果证实了SDDS的优越性。**【Dialogue Summarization】** |
| 14           | [ACCENT: An Automatic Event Commonsense Evaluation Metric for Open-Domain Dialogue Systems](https://aclanthology.org/2023.acl-long.241/)<br />开放领域对话系统的自动事件常识评估指标 | 2023 july | 提出 ACCENT，一种被常识性知识库(CKSBs)授权的事件常识评估指标。ACCENT首先从对话中提取事件-关系元组，然后通过评分这些元组来评估响应与CSKB的兼容性。为了评估ACCENT，构建第一个公共开放领域对话的事件常识评估数据集。<br />**【Open-Domain Dialogue/Evaluation】** |
| 15* day3     | [DAMP: Doubly Aligned Multilingual Parser for Task-Oriented Dialogue](https://aclanthology.org/2023.acl-long.199/)<br />DAMP: 针对任务型对话的双重多语言解析器 | 2023 july | 提出了DAMP，在Spanglish、Hinglish 和多语言任务解析基准上分别将mBERT的转移性能提高3、6和81倍，同时在参数比XLM-R 和 mT5-Large少3.2倍下胜出。<br />**【Task-Oriented Dialogue】** |
| 16           | [A Cognitive Stimulation Dialogue System with Multi-source Knowledge Fusion for Elders with Cognitive Impairment](https://aclanthology.org/2023.acl-long.593/)<br />有认知障碍老人的一个多源知识融合的认知刺激对话系统 | 2023 july | 构建了一个中文认知刺激对话（CSConv）数据集，其中包含约2.6K组对话，带有治疗原则和情感支持策略标签。并以此提出了一种用于认知刺激对话（CSD）的多源知识融合方法，以生成受治疗原则和情感支持策略指导的开放式回应。在CSConv数据集上进行的大量实验表明了所提方法的有效性。**【Dialogue System】** |
| 17           | [Pre-training Multi-party Dialogue Models with Latent Discourse Inference](https://arxiv.org/abs/2305.15175) arxiv<br />基于潜在话语推理的预训练多方对话模型 | 2023 May  | 由于多方对话语料库中缺乏明确的话语标签，以前的工作未能通过忽略未标记的多方对话数据来扩展预训练过程。为了充分利用未标记的数据，提出将话语结构视为潜在变量，然后通过无监督潜在变量推理方法共同推断它们，并通过预训练的方式培养具有话语意识的模型。在多个下游任务达到SOTA。[code](https://github.com/EricLee8/MPD_EMVI)<br />**【Multi-party Dialogue】** |
| 18           | [EM Pre-training for Multi-party Dialogue Response Generation](https://arxiv.org/abs/2305.12412)  arxiv EM 预训练用于多方对话回应生成 | 2023 july | 由于多方对话数据集中缺乏已标记的接受者标签，难以将它们用于为多方对话预训练回应生成模型。因此提出了一种期望最大化（Expectation-Maximization，EM）方法，它迭代执行期望步骤以生成接受者标签，并执行最大化步骤来优化回应生成模型。**【Multi-party Dialogue】** |
| 19           | [DIONYSUS: A Pre-trained Model for Low-Resource Dialogue Summarization](https://arxiv.org/abs/2212.10018) arxiv<br />低资源对话摘要的预训练模型 | 2023 may  | DIONYSUS 一个用于在任何新领域总结对话的预训练编码器-解码器模型。在预训练时，为每个对话示例创建了两个伪摘要：一个是由经过精细调整的摘要模型生成的，另一个是包含重要信息的对话轮次的集合。然后根据不同类型对话中信息分布的差异选择其中一个伪摘要。【Dialogue Summarization】 |
| 20<br />day4 | [White-Box Multi-Objective Adversarial Attack on Dialogue Generation](https://aclanthology.org/2023.acl-long.100/)<br />对话生成上的白盒多目标对抗攻击 | 2023 july | 提出了一种名为DGSlow的白盒多目标攻击方法。DGSlow通过基于梯度的多目标优化器平衡了两个目标——生成准确性和长度，通过自适应搜索机制迭代地制作仅经过少量修改的对抗性样本。【Dialogue Generation】 |
| 21*          | [PaCE: Unified Multi-modal Dialogue Pre-training with Progressive and Compositional Experts](https://aclanthology.org/2023.acl-long.749/)<br />具有渐进和组合专家的统一多模态对话预训练 | 2023 july | 提出了一个统一的、结构化的、组合的多模态对话预训练框架PaCE。它利用几个基本专家的组合来适应多个与对话相关的任务，并且可以使用有限的对话和广泛的非对话多模态数据进行预训练。此外还提出了一种先进式的训练方法，即过去的老专家可以帮助新专家，促进他们的能力扩展。在8个多模态对话基线达到SOTA。【Multi-modal Dialogue】 |
| 22           | [RECAP: Retrieval-Enhanced Context-Aware Prefix Encoder for Personalized Dialogue Response Generation](https://aclanthology.org/2023.acl-long.468/)<br />用于个性化对话回应生成的检索增强上下文感知前缀编码器 | 2023 july | 提出了一个新的检索增强方法对于个性化回应生成。通过设计了一个分层级在对话域数据训的transformer检索器来实现个性化检索，和上下文感知并融合了检索信息的前缀编码器来更有效的解码。【Dialogue Response Generation】 |
| 23           | [One Cannot Stand for Everyone! Leveraging Multiple User Simulators to train Task-oriented Dialogue Systems](https://aclanthology.org/2023.acl-long.1/)<br />一个人不能代表所有人!利用多用户模拟器来训练面向任务的对话系统 | 2023 july | 提出MUST框架通过充分利用多用户模拟器来优化ToD系统。将MUST构建为一个Multi-armed bandits问题，并提供了一种称为MUST adaptive的方法，以平衡i）不同用户模拟器和ToD系统之间的自适应交互的增强适应性，和ii）避免灾难性遗忘问题的统一适应性。在MultiWOZ上通过MUST训练的对话系统在性能上优于单一用户模拟器训练的系统。<br />【Task-oriented Dialogue】 |
| 24           | [PVGRU: Generating Diverse and Relevant Dialogue Responses via Pseudo-Variational Mechanism](https://aclanthology.org/2023.acl-long.185/)<br />通过伪变分机制生成多样而相关的对话响应 | 2023 july | 提出Pseudo-Variational Gated Recurrent Unit (PVGRU)。它的关键创新是一种循环汇总变量，它汇总子序列的累积分布变化。在训练PVGRU时不依赖后验知识，从而避免了训练-推理不一致的问题。VGRU可以通过汇总变量来感知细微的语义变化。<br />【Dialogue Response Generation】 |
| 25<br />day5 | [XDailyDialog: A Multilingual Parallel Dialogue Corpus](https://aclanthology.org/2023.acl-long.684/)<br />多语言平行对话语料库 | 2023 july | 大多数开放域对话数据集是对于单一语言的。提出了XDailyDialog使研究人员能够探索多语言和跨语言开放域对话的挑战性任务。XDailyDialog 包括 4 种语言间对齐的13k 个对话（总计 52k个对话和 410k个话语/回应）。并提出了一个对话生成模型kNN-Chat。它具有新颖的knn搜索机制，支持单语言、多语言和跨语言对话的统一响应检索。【DataSet】 |
| 26           | [DialoGPS: Dialogue Path Sampling in Continuous Semantic Space for Data Augmentation in Multi-Turn Conversations](https://aclanthology.org/2023.acl-long.70/)<br />在连续语义空间中进行对话路径抽样，用于多轮对话中的数据增强 | 2023 july | 传统的对话生成模型在多轮对话中往往表现不佳，因为它们通常采用一对一的上下文-回应映射，而真实的对话往往具有多对多的特性。论文介绍了 DialoGue Path Sampling (DialoGPS) 方法，针对多轮对话的一种多对多增强方法。DialoGPS 提出了一种在连续语义空间中进行对话路径抽样的方法，以生成多对多的增强训练数据。该方法通过将对话映射到特殊的高斯过程，然后在连续空间中采样潜在变量，形成连贯的对话路径。【Multi-Turn Conversations】 |
| 27*          | [Envisioning Future from the Past: Hierarchical Duality Learning for Multi-Turn Dialogue Generation](https://aclanthology.org/2023.acl-long.407/)<br />从过去展望未来：用于多轮对话生成的层次二元学习 | 2023 july | 提出了一种用于对话的层次二元学习（HDLD），来模拟人类在对话中推断未来文本的能力。通过最大化过去和未来话语之间的相互信息，生成既连贯又信息丰富的回应。以前的方法仅在训练期间将未来文本作为辅助信息进行编码，HDLD允许对话历史和未来之间的互动，提高对话数据的利用。【 Dialogue Generation】 |
| 28           | [A Dataset of Argumentative Dialogues on Scientific Papers](https://aclanthology.org/2023.acl-long.425/)科学论文辩论对话数据集 | 2023 july | ArgSciChat数据集，包含在20篇NLP论文中41位科学家之间的辩论对话。它在科学论文的对话话语中包含探索性和论证性的问题和答案。ArgSciChat的大小显示了收集专门领域对话的困难，因此它是一个具有挑战性的任务来评估低资源领域的对话代理。【DataSet】 |
| 29           | [MidMed: Towards Mixed-Type Dialogues for Medical Consultation](https://aclanthology.org/2023.acl-long.453/)<br />面向医疗咨询的混合式对话 | 2023 july | 由于缺乏医学知识，患者通常很难确定明确的目标。先创建一个人对人混合型医疗咨询对话语料库MidMed，包含四种对话类型:诊断、推荐、QA和闲聊的任务导向对话，涵盖耳鼻喉科、眼科、皮肤科、消化科四个科室共8309段对话。提出了一种指导式医学对话生成框架InsMed，用于处理混合类型的对话。【Medical Dialogue】 |
| 30           | [RADE: Reference-Assisted Dialogue Evaluation for Open-Domain Dialogue](https://arxiv.org/abs/2309.08156) arxiv<br />开放域对话的参考辅助对话评价 | 2023 july | 提出了一种基于多任务学习框架的"参考辅助对话评估"（RADE）方法，该方法利用预先创建的话语作为参考，而不仅是黄金回应，以缓解一对多问题。<br />【Open-Domain Dialogue】 |
| 31           | [Learning to Generate Equitable Text in Dialogue from Biased Training Data](https://aclanthology.org/2023.acl-long.163/)<br />学习从偏见的训练数据中生成公平的对话文本 | 2023 july | 论文关注了对话系统中的文本生成的公平性问题。作者提供了文本生成中公平性的正式定义，并证明了学习公平性与学习人类相似性之间存在关联。还提出了一些合理的条件，使文本生成算法能够在不修改有偏训练数据的情况下学习生成公平文本。提出的理论能够准确预测多个算法在生成公平文本方面的性能。<br />【Dialogue Generation】 |
| 32 day6      | [MoralDial: A Framework to Train and Evaluate Moral Dialogue Systems via Moral Discussions](https://aclanthology.org/2023.acl-long.123/)<br />通过道德讨论来训练和评估道德对话系统的框架 | 2023 july | MoralDial 对于训练和评估道德对话系统。通过模拟特定用户和对话系统之间构建道德讨论，包括在对话交流中表达、解释、修正和推断道德观，使对话模型自然地学习道德。并在这个框架下对此提出一种新的评估方法。【Dialogue Systems】 |
| 33           | [Enhancing Dialogue Generation via Dynamic Graph Knowledge Aggregation](https://aclanthology.org/2023.acl-long.253/)<br />通过动态图知识聚合增强对话生成 | 2023 july | 现有模型的训练机制导致了图知识和文本之间的语义差距。通过动态构造了一个带有伪节点的多跳知识图，使语言模型在图内的每一步都参与特征聚合，该框架可以更好地利用来自文本和外部图知识的异构特征。<br />【Dialogue Generation】[code]( https://github.com/tangg555/SaBART) |
| 34           | [Enhancing Personalized Dialogue Generation with Contrastive Latent Variables: Combining Sparse and Dense Persona](https://aclanthology.org/2023.acl-long.299/)<br />对比潜在变量增强个性化对话生成:结合稀疏和密集角色 | 2023 july | 设计了一个基于对比潜在变量的模型(CLV)，该模型将密集的人物角色描述聚类到稀疏的类别中，并将其与历史查询相结合以生成个性化的响应。在中文和英文数据集上的实验结果表明了模型在个性化方面的优越性。<br />【Personalized Dialogue Generation】 |
| 35           | [CORE: Cooperative Training of Retriever-Reranker for Effective Dialogue Response Selection](https://aclanthology.org/2023.acl-long.174/)<br />协同训练检索器和重排器实现有效的对话响应选择 | 2023 july | 提出了一种协同训练方法用于训练响应检索器和再排序器，使它们能够相互学习和共同优化，提高了检索式对话系统的性能。传统方法中，这两个模块通常是独立优化的，或者从一个预训练的再排序器中异步提取知识，导致性能不佳。实验结果表明，该方法在两个基准测试中表现出更好的性能。【Dialogue Response】 |
| 36           | [Divide, Conquer, and Combine: Mixture of Semantic-Independent Experts for Zero-Shot Dialogue State Tracking](https://aclanthology.org/2023.acl-long.114/)<br />划分、征服和合并：零样本DST的语义独立专家混合 | 2023 july | 为了能在零研究迁移学习即在没有领域内数据的情况下提高DST的性能。提出将已见数据分成语义独立的子集，并训练相应的专家，然后使用专家混合机制来处理新出现的数据，以提高性能和稳健性。该方法在MultiWOZ2.1数据集上达到SOTA，并只有10M训练参数【Zero-Shot  DST】 |
| 37           | [Retrieval-free Knowledge Injection through Multi-Document Traversal for Dialogue Models<br />](https://aclanthology.org/2023.acl-long.364/)通过多文档遍历实现无检索知识注入的对话模型 | 2023 july | 为解决对话模型中外部知识注入的成本问题，提出了一种无检索的方法KiDG，通过自动将知识文档转化为模拟的多轮对话，从而构建知识密集型对话模拟。这些模拟数据可用于训练和增强对话模型，用KiDG模拟的数据增强的对话模型在性能上明显优于最先进的无检索方法。【Retrieval-free】 |
| 38           | [VSTAR: A Video-grounded Dialogue Dataset for Situated Semantic Understanding with Scene and Topic Transitions](https://aclanthology.org/2023.acl-long.276/)<br />基于视频的对话数据集，用于场景和主题转换的定位语义理解 | 2023 july | 介绍了Video-grounded Scene&Topic AwaRe dialogue (VSTAR) 数据集，这是一个基于395部电视剧的大规模视频对话理解数据集。基于VSTAR提出了两个视频对话理解的基准情景分割和主题分割，和一个视频对话生成的基准。【Dataset 】 |
| 39* day7     | [BREAK: Breaking the Dialogue State Tracking Barrier with Beam Search and Re-ranking](https://aclanthology.org/2023.acl-long.159/)用bean搜索和重排打破DST障碍 | 2023 july | 引入了一个新的框架BREAK，它执行DST分为两个阶段:(i)用束搜索生成k-最佳对话状态候选;(ii)重新排序候选以选择正确的对话状态。这个简单框架在所有版本的MultiWOZ和M2M数据集上达到SOTA。此外在MultiWOZ 2.1-2.4上将JGA提高到80-90%，分别比以前性能最好的模型提高了23.6%、26.3%、21.7%和10.8%。【DST】[code](https://github.com/tony-won/DST-BREAK) |
| 40           | [Learning New Skills after Deployment: Improving open-domain internet-driven dialogue with human feedback](https://aclanthology.org/2023.acl-long.758/)<br />部署后学习新技能：通过人类反馈改进开放领域的互联网驱动对话 | 2023 july | 论文研究了如何利用互联网检索和人类反馈来改进对话模型的性能。收集各种类型的人类反馈，包括二进制质量测量、自由文本反馈以及详细的失败原因。研究尝试了不同的改进算法，包括标准监督学习、拒绝抽样、模型引导和奖励驱动学习，以确定哪种反馈和算法对性能改进最为有效。结果显示最近的DIRECTOR模型表现出显著的潜力【open-domain】 |
| 41           | [Modeling User Satisfaction Dynamics in Dialogue via Hawkes Process](https://aclanthology.org/2023.acl-long.494/)通过Hawkes过程建模对话中的用户满意度动态 | 2023 july | 假设对话系统的性能可以通过用户满意度来衡量，并使用一个模拟器来模拟用户。提出了一个新的评估器器ASAP（通过Hawkes过程进行满意度估计），将对话中各轮的用户满意度视为事件序列，并采用Hawkes过程来有效地模拟该序列中的动态变化。在四个基准对话数据集上的实验结果表明，ASAP能够明显优于最先进的基线估计器。【Evaluation】 |
| 42           | [FutureTOD: Teaching Future Knowledge to Pre-trained Language Model for Task-Oriented Dialogue](https://arxiv.org/abs/2306.10315) arxiv<br />将未来知识传授给任务导向对话的预训练语言模型 | 2023 july | 提出了一种新颖的对话预训练模型FutureTOD，它使用自训练框架将未来的知识提取到先前对话上下文的表示中。作者认为良好的对话表示应该能够同时学习本地上下文信息并预测未来信息。在各种下游对话任务上的大量实验证明了模型的有效性。【Task-Oriented Dialogue】 |
| 43           | [Seen to Unseen: Exploring Compositional Generalization of Multi-Attribute Controllable Dialogue Generation](https://aclanthology.org/2023.acl-long.793/)<br />从已知到未知：探索多属性可控对话生成的组合泛化 | 2023 july | 提出了一种基于提示的分解式可控对话生成模型DCG，可以从已知属性值中学习并泛化到未知的属性组合。它通过生成属性导向的提示向量来学习属性概念的组合，并使用分解损失来解耦不同属性，以实现更好的泛化。还设计了一个统一的无参考评估框架，可用于多属性的评估。【Dialogue Generation】 |
| 44           | [Dialog-Post: Multi-Level Self-Supervised Objectives and Hierarchical Model for Dialogue Post-Training](https://aclanthology.org/2023.acl-long.564/)<br />多级自监督目标与层次式模型用于对话后训练 | 2023 july | 提出了一种DialPost方法，采用多级自监督目标和层次模型。这些目标利用对话特定属性，并使用自监督信号来充分促进对话的表示和理解。这一新颖模型是一个层次分段自注意力网络，包含内部段和跨段自注意力子层，后面跟随的是一个聚合和更新模块。【】 |
| 45           | [Evaluating Open-Domain Dialogues in Latent Space with Next Sentence Prediction and Mutual Information](https://aclanthology.org/2023.acl-long.33/)<br />用下一句预测和互信息在潜在空间评估开放领域对话 | 2023 july | 开放领域对话的一个重要问题是一对多的问题，即在给定对话上下文的情况下可能存在多个合适的响应，这些响应在语义上不同。因此提出了基于学习的自动评估指标（CMN），通过在条件变分自动编码器（CVAE）中引入下一句预测（NSP）目标和采用互信息（MI）来建模潜在空间中文本的语义相似性，能够强有力地评估开放领域的对话。【Open-Domain Dialogues】 |
| 46 day8      | [Contextual Knowledge Learning for Dialogue Generation](https://arxiv.org/abs/2305.18200) arxiv<br />对话生成的上下文知识学习 | 2023 july | 提出了一种将对话背景和知识加权作为模型训练的一个重要部分。通过一种称为上下文知识学习（CKL）过程来引导模型训练，该过程包括上下文和知识的潜在向量。CKL潜在向量通过弱监督捕捉了对话背景、知识和响应之间的关系，使在训练过程中能够差异化地权衡对话背景话语和知识句子。【Dialogue Generation】 |
| 47           | [SimOAP: Improve Coherence and Consistency in Persona-based Dialogue Generation via Over-sampling and Post-evaluation](https://arxiv.org/abs/2305.11130)<br />通过过度抽样和事后评估提高基于人物的对话生成的连贯性和一致性 | 2023 july | 对于基于人物的对话生成任务，一致性和连贯性是关键因素，提出了一种简单而有效的两阶段SimOAP策略，即过采样和后评价。过采样阶段通过现成的蒸馏和压缩方法有效地从现有训练模型中获得大规模响应。后评价阶段根据多个精心设计的评价指标从大规模候选对象中选择一个好的响应。【Dialogue Generation】 |
| 48           | [PAED: Zero-Shot Persona Attribute Extraction in Dialogues](https://aclanthology.org/2023.acl-long.544/)<br />在对话中的零样本角色属性提取 | 2023 july | 现有的数据集存在标签不明确和标注不一致。因此作者提出了一种更可靠的文本-标签匹配标准，用于生成高质量的个性属性提取数据。此外还提出了一种对比学习和生成的模型，以及一种新颖的硬负采样策略用于广义零样本个性属性提取。<br />【 Zero-Shot】 |
| 49           | [Annotating and Detecting Fine-grained Factual Errors for Dialogue Summarization](https://aclanthology.org/2023.acl-long.377/)<br />为对话摘要标注和检测细粒度事实错误 | 2023 july | 提出了第一个具有细粒度事实错误注释的数据集DIASUMFACT。将细粒度事实错误检测定义为句子级多标签分类问题。进一步利用预训练的编码器-解码器模型通过候选排序提出了一个无监督模型ENDERANKER，性能与SOTA模型相当同时需要更少的资源。【Dialogue Summarization】== |
| 50           | [Towards Understanding Omission in Dialogue Summarization](https://aclanthology.org/2023.acl-long.798/)<br />对对话摘要中省略的理解 | 2023 july | 遗漏是影响摘要质量的主要因素之一，提出了OLDS数据集，为对话摘要提供了高质量的遗漏标签。通过分析这个数据集，发现通过为摘要模型提供真实遗漏标签以恢复遗漏信息，可以大大提高摘要质量，这证明了遗漏检测对于在对话摘要中减少遗漏的重要性。并提出了一个遗漏检测任务，并展示了我们提出的数据集可以很好地支持这个任务的训练和评估。【Dialogue Summarization】 |
| 51 short     | [Controllable Mixed-Initiative Dialogue Generation through Prompting](https://aclanthology.org/2023.acl-short.82/)<br />通过提示的可控混合主动对话生成 | 2023 july | 使用提示大型语言模型作为微调条件生成的可替代方法。为可控的混合主动对话形式化了提示构建。在两个任务PersuasionForGood和Emotional Support Conversations中相对于微调和人工标注的响应表现出了改进。<br />【Dialogue Summarization】 |
| 52**         | [ChatGPT for Zero-shot Dialogue State Tracking: A Solution or an Opportunity?](https://aclanthology.org/2023.acl-short.81/)<br />ChatGPT用于零样本DST：解决方案还是机会？ | 2023 july | DST性能提升严重依赖于对数据增强和对更大的语言模型结构的微调。通用语言模型，经过大量多样化数据训练，有望解决任何类型的任务而无需专门的任务训练。因此在ChatGPT研究并提供了初步的实验结果，显示ChatGPT在零样本DST方面达到了最先进的性能。【Zero-shot DST】 |
| 53 day9      | [Towards Fewer Hallucinations in Knowledge-Grounded Dialogue Generation via Augmentative and Contrastive Knowledge-Dialogue](https://aclanthology.org/2023.acl-short.148/)通过增强和对比知识对话向更少的幻觉在基于知识的对话生成 | 2023 july | 提出了一个增强和对比的知识对话扩展框架ACK-DEF。ACK-DEF包括不同程度错误的知识和手工设计的响应，以扩展原始的训练集，并平滑极化的优化目标，使模型能够生成有或没有黄金知识的真实结果。在Wikipedia Wizard数据集上表明ACK-DEF对减轻虚构问题是有效的。【Dialogue Generation】 |



## 2.Conversation

| Num       | Paper                                                        | Time      | Summary                                                      |
| --------- | ------------------------------------------------------------ | --------- | ------------------------------------------------------------ |
| 1         | [MPCHAT: Towards Multimodal Persona-Grounded Conversation](https://aclanthology.org/2023.acl-long.189/)<br />面向多模态基于角色的对话 | 2023 july | 将基于人物的对话扩展到多模态领域并做出了两个主要贡献。第一是提出了第一个名为MPCHAT的多模态基于人物角色的对话数据集，将人物角色扩展为文本和图像以包含情景记忆。第二结合多模态角色，通过三个提出的基于多模态角色的对话任务来衡量，在统计上显著提高了所有任务效果。【Multi modal conversation】 |
| 2         | [Query Enhanced Knowledge-Intensive Conversation via Unsupervised Joint Modeling](https://aclanthology.org/2023.acl-long.97/)<br />通过无监督联合建模实现查询增强的知识密集对话 | 2023 july | 提出了一种针对知识密集型对话的无监督查询增强方法QKConv，QKConv中有三个模块:查询生成器、现成的知识选择器和响应生成器。通过联合训练进行优化，通过探索多个候选查询并利用相应的选择知识来产生响应。联合训练仅依赖于对话上下文和目标响应，不需要额外的查询注释或知识来源。【Knowledge-Intensive Conversation】 |
| 3         | [Modeling What-to-ask and How-to-ask for Answer-unaware Conversational Question Generation](https://aclanthology.org/2023.acl-long.603/)<br />建模问什么和如何问的答案不知道对话问题的生成 | 2023 july | 在不知答案的情境下，提出什么问题和如何提问成为主要挑战。因此提出了SG-CQG框架，分为两个阶段：在“问什么”阶段，从构建的语义图中选择一个句子作为基本原理，并从中提取答案跨度。在"如何问"阶段，分类器在生成和过滤之前通过两个显式控制信号确定问题的目标答案类型。此外还提出了Conv-Distinct评估度量来评估生成的对话多样性，与现有的CQG模型相比，本文提出的SG-CQG达到SOTA。【Conversational Question Generation】 |
| 4         | [GIFT: Graph-Induced Fine-Tuning for Multi-Party Conversation Understanding](https://aclanthology.org/2023.acl-long.651/)<br />基于图微调的多方对话理解 | 2023 july | 提出了一种即插即用和轻量级的方法图诱导微调(GIFT)，它可以适应各种基于变压器的预训练语言模型(plm)，以实现通用MPC理解。GIFT可以显著提高plm下游任务和基准上的性能，每个编码层仅增加4个参数。【multi-party conversation】 |
| 5         | [Supervised Adversarial Contrastive Learning for Emotion Recognition in Conversations](https://aclanthology.org/2023.acl-long.606/)<br />情感识别对话中的监督对抗对比学习 | 2023 july | 提出了一种监督对抗对比学习（SACL）框架，以有监督的方式学习类别分布结构化表示。设计了一种上下文对抗训练（CAT）策略，以从上下文中学习更多多样性特征。并开发了一种基于序列的SACL-LSTM，用于学习ERC的标签一致和上下文鲁棒特征。【Emotion Recognition】 |
| 6         | [Improved Instruction Ordering in Recipe-Grounded Conversation](https://arxiv.org/abs/2305.17280)<br />在基于食谱的对话中改进指令顺序 | 2023 july | 揭示了基于食谱的对话系统的主要挑战是如何以正确的顺序提供指令。先假设是由于模型缺乏对用户意图的理解和无法跟踪指令状态，因此探索两个辅助子任务，即用户意图检测和指令状态跟踪，以支持改进指令接地的响应生成。通过对我们新收集的数据集ChattyChef的实验表明，结合用户意图和指令状态信息有助于响应生成模型减轻错误顺序问题。[ChattyChef ](https://github.com/octaviaguo/ChattyChef)**【Recipe-Grounded Conversation】** |
| 7         | [TREA: Tree-Structure Reasoning Schema for Conversational Recommendation](https://aclanthology.org/2023.acl-long.167/)<br />基于树结构推理模式的会话推荐 | 2023 july | 会话推荐系统(CRS)旨在通过对话及时跟踪用户的动态兴趣，并生成相关的项目推荐。提出了一种新的树结构推理模式TREA。TREA构建了一个多层可扩展的树作为推理结构，阐明被提及实体之间的因果关系，并充分利用历史对话，对推荐结果产生更合理、更合适的响应。**【Conversational Recommendation】** |
| 8         | [ConvGQR: Generative Query Reformulation for Conversational Search](https://aclanthology.org/2023.acl-long.274/)<br />会话搜索的生成查询重构 | 2023 july | 提出了ConvGQR，这是一个基于生成式预训练语言模型（PLM）的新框架，其中一个用于查询重写，另一个用于生成潜在答案。通过结合两者，ConvGQR能够生成更好的搜索查询，并提出了一种知识注入机制来优化查询重构和检索。【Conversational Search】 |
| 9         | [Compositional Data Augmentation for Abstractive Conversation Summarization](https://aclanthology.org/2023.acl-long.82/)<br />用于抽象对话摘要的组合数据增强 | 2023 july | 提出了一种子结构级组合数据增强方法，Compo，用于生成多样化和高质量的对话和摘要对。Compo首先提取会话结构，然后将语义上有意义的会话片段组合起来创建新的训练实例。在SAMSum和DialogSum上的实验表明，Compo在有限数据下的ROUGE分数提高了近10%.[code](https://github.com/ozyyshr/Compo)【Conversation Summarization】 |
| 10        | [A Survey on Asking Clarification Questions Datasets in Conversational Systems](https://aclanthology.org/2023.acl-long.152/)<br />对话系统中提问澄清问题数据集的综述 | 2023 july | 在对于有限的用户输入来理解用户的潜在需求领域中，提出澄清问题(ACQs)来揭示用户的查询或话语的真实意图是一项必不可少的任务。为了协助ACQ技术的发展，全面分析了当前ACQ研究的现状，提供了公开可用数据集的详细比较，并讨论了应用的评估指标，同时为多个ACQ相关任务提供了基准。【Conversational Systems】 |
| 11 day10  | [MultiEMO: An Attention-Based Correlation-Aware Multimodal Fusion Framework for Emotion Recognition in Conversations](https://aclanthology.org/2023.acl-long.824/)<br />面向对话情感识别的基于注意力关联感知的多模态融合框架 | 2023 july | 提出了名为MultiEMO的新型基于注意力和关联感知的多模态融合框架，通过双向多头跨模态注意力层捕获文本、音频和视觉模态之间的跨模态映射关系，有效地整合多模态线索。还提出了Sample-Weighted Focal Contrastive (SWFC) 损失来减轻识别少数和语义上难以区分的情感类别的困难。【Emotion Recognition】 |
| 12        | [History Semantic Graph Enhanced Conversational KBQA with Temporal Information Modeling](https://aclanthology.org/2023.acl-long.195/)<br />历史语义图增强的具有时间信息建模的对话式知识库问答 | 2023 july | 提出了一种历史语义图增强的KBQA模型(HSGE)，该模型能够有效地对会话历史中的远程语义依赖进行建模，同时保持较低的计算成本。该框架包含一个上下文感知编码器，该编码器采用动态内存衰减机制，并在不同粒度级别上对上下文进行建模。【KBQA】 |
| 13        | [Synthesize, Prompt and Transfer: Zero-shot Conversational Question Generation with Pre-trained Language Model](https://aclanthology.org/2023.acl-long.500/)<br />合成、提示和迁移：用预训练语言模型进行零样本对话问题生成 | 2023 july | 提出ZeroCQG，要求它不需要人工标记的对话进行训练。因此提出了一个多阶段的知识转移框架，即综合、提示和转移预训练语言模型(SPARTA)，以有效地利用单轮问题生成实例中的知识。通过从三个单轮数据集(MS MARCO, NewsQA和SQuAD)转移知识，在三个对话数据集(CoQA, QuAC和DoQA)上进行了广泛的实验证明了该方法的优越性。【Conversational Question Generation】 |
| 14        | [DualGATs: Dual Graph Attention Networks for Emotion Recognition in Conversations](https://aclanthology.org/2023.acl-long.408/)<br />对话中情绪识别的双图注意网络 | 2023 july | 引入双图注意网络 DualGATs来同时考虑话语结构和说话人感知上下文的互补方面。设计了一个话语感知GAT (DisGAT)模块，通过分析话语之间的话语依赖关系来整合话语结构信息。开发了一个说话人感知GAT (SpkGAT)模块，通过考虑话语之间的说话人依赖关系来整合说话人感知的上下文信息。【Emotion Recognition】 |
| 15        | [SafeConv: Explaining and Correcting Conversational Unsafe Behavior](https://aclanthology.org/2023.acl-long.2/)<br />解释和纠正对话不安全行为 | 2023 july | 现有的对话数据集没有提供足够的注释来解释和纠正这种不安全行为。构建了一个SafeConv的新数据集，用于研究对话安全性。(1)除了话语级别的安全标签，SafeConv还提供了话语中的不安全跨度，这些信息能够表明哪些单词导致了检测到的不安全行为;(2)当检测到不安全行为时，SafeConv提供安全的替代响应以继续对话，引导对话进入温和的轨道。[dataset](https://github.com/mianzhang/SafeConv)【Conversational Unsafe Behavior】 |
| 16        | [Bridging The Gap: Entailment Fused-T5 for Open-retrieval Conversational Machine Reading Comprehension](https://aclanthology.org/2023.acl-long.857/)<br />蕴涵融合t5用于开放式检索对话机器阅读理解 | 2023 july | 机器需要根据检索到的规信息，做出“是/否/查询”的决定，最近的研究试图减少决策和问题生成之间的信息差距。决策和问题生成是分开执行的，这使得很难在所有阶段共享决策中使用的蕴涵推理。提出了一种新的单阶段端到端框架EFT，以一种全局理解的方式弥合决策和问题生成之间的信息鸿沟。【Open-retrieval 】 |
| 17        | [A Cross-Modality Context Fusion and Semantic Refinement Network for Emotion Recognition in Conversation](https://aclanthology.org/2023.acl-long.732/)<br />用于对话情感识别的跨模态上下文融合和语义精炼网络 | 2023 july | 以往的研究大多是简单地将多模态表征连接起来，导致冗余信息的积累和模态之间的上下文交互作用有限。因此提出CMCF-SRNet，先设计了一个跨模态位置约束transformer来探索多模态相互作用。再研究了一种基于图的语义精炼transformer，解决了话语间语义关系信息不足的局限性。[code]( https://github.com/zxiaohen/CMCF-SRNet)【Emotion Recognition】 |
| 18        | [CHBias: Bias Evaluation and Mitigation of Chinese Conversational Language Models](https://aclanthology.org/2023.acl-long.757/)<br />CHBias：用于中文对话语言模型的偏见评估和缓解 | 2023 july | 引入了一个新的中文数据集CHBias，用于中文对话语言模型的偏见评估和缓解。加入了一些其他偏见类别，如如年龄歧视和外貌偏见。使用CHBias评估了CDial-GPT和EVA2.0，实验表明，这些中文预训练模型在生成包含社会偏见的文本时存在潜在风险，并对模型应用了几种去偏方法减少了生成的偏见【Bias Conversationa】 |
| 19*       | [A Facial Expression-Aware Multimodal Multi-task Learning Framework for Emotion Recognition in Multi-party Conversations](https://aclanthology.org/2023.acl-long.861/)<br />在多方对话中面部表情感知的多模态多任务学习框架 | 2023 july | 以往的MERMC研究大多侧重于文本和音频模式，而忽略了视觉信息。给定一个话语，以前的方法提取的人脸序列可能包含多个人脸，提出了一个两阶段的框架，称为面部表情感知多模态多任务学习(FacialMMT)。先提取每个话语的真实说话人的面部序列，再多模态面部表情感知情感识别模型利用帧级面部情绪分布来帮助改进基于多任务学习的话语级情感识别。[code](https://github.com/NUSTM/FacialMMT)【Emotion Recognition/ Multi-party】 |
| 20        | [Facilitating Multi-turn Emotional Support Conversation with Positive Emotion Elicitation: A Reinforcement Learning Approach](https://aclanthology.org/2023.acl-long.96/)<br />通过积极情感引发促进多轮情感支持对话：一种强化学习方法 | 2023 july | 引入了一个新的范式，将多回合ESC形式化为一个积极情绪激发的过程。要完成这一任务，需要在保持连贯等会话目标的同时，随着对话的进行，精细地调整ES中的引出强度。提出了一个基于混合专家的强化学习模型，并设计了ES和对话一致性奖励来指导政策的响应学习。【Emotional support conversation 】 |
| 21 short  | [Learning Neuro-Symbolic World Models with Conversational Proprioception](https://aclanthology.org/2023.acl-short.57/)<br />使用对话式自体感知学习神经符号世界模型 | 2023 july | 为了学习有用的世界模型，利用了最近的神经符号架构逻辑神经网络(LNN)。在文中描述了一种可以在TextWorld-Commonsense游戏集上学习神经符号世界模型的方法。这极大地提高了TextWorld环境中解决游戏的代理的性能，相对于基线的优势是平均减少了85%的步数和x2.3的平均分数。。【】 |
| 22* day11 | [AutoConv: Automatically Generating Information-seeking Conversations with Large Language Models](https://aclanthology.org/2023.acl-short.149/)<br />AutoConv：使用大型语言模型自动生成信息寻找对话 | 2023 july | ISC其目的是帮助用户通过会话收集信息，但训练数据的缺乏。提出AutoConv用于合成会话生成，它利用了大型语言模型(LLM)的少样本学习和生成能力。将对话生成问题作为语言建模任务，然后用一些人类对话对LLM进行微调，以捕获信息寻找过程的特征，来生成高质量的合成对话。【Information-seeking conversation】 |



## 3.Interaction

| Num      | Paper                                                        | Time      | Summary                                                      |
| -------- | ------------------------------------------------------------ | --------- | ------------------------------------------------------------ |
| 1        | [Modeling Instance Interactions for Joint Information Extraction with Neural High-Order Conditional Random Field](https://aclanthology.org/2023.acl-long.766/)<br />利用神经高阶条件随机场建模实例间的交互进行联合信息抽取 | 2023 july | 以前的模型通常考虑一对实例的二元依赖评分，并利用局部搜索(如波束搜索)来近似全局解。为了更好地集成跨实例交互，引入了一个联合IE框架(CRFIE)，设计了二元因子和三元因子来直接模拟一对实例之间以及三元组之间的相互作用。然后利用这些因素共同预测所有实例的标签。【 Information Extraction】 |
| 2        | [MS-DETR: Natural Language Video Localization with Sampling Moment-Moment Interaction](https://aclanthology.org/2023.acl-long.77/)<br />MS-DETR：使用采样时刻-时刻交互进行自然语言视频定位 | 2023 july | 给定一个文本查询，NLVL的任务是在语义上匹配查询的未修剪视频中定位时间时刻。作者采用基于提议的解决方案，生成提议(即候选矩)，然后选择最匹配的提议。其核心思想是使用采用的DETR框架对可学习模板指导的时刻子集进行采样。【Natural Language Video Localization】 |
| 3        | [BIC: Twitter Bot Detection with Text-Graph Interaction and Semantic Consistency](https://aclanthology.org/2023.acl-long.575/)<br />基于文本-图交互和语义一致性的Twitter Bot检测 | 2023 july | 推特机器人是由恶意行为者操作的自动程序，用于操纵公众舆论和传播错误信息。 Twitter机器人在不断发展，高级机器人窃取真正用户的推文并稀释其恶意内容以逃避检测。因此提出了BIC，一个具有文本-图形交互和语义一致性的Twitter Bot检测框架。【text-graph】 |
| 4        | [CITADEL: Conditional Token Interaction via Dynamic Lexical Routing for Efficient and Effective Multi-Vector Retrieval](https://arxiv.org/abs/2211.10411)<br />基于动态词法路由的条件令牌交互高效多向量检索 | 2023 july | 由于现有的多向量检索方法速度比单向量慢几个数量级，因此作者从令牌路由的角度统一了不同的多向量检索模型，提出了基于动态词法路由(CITADEL)的条件令牌交互，以实现高效的多向量检索。在保持了较高的精度同时速度对比以往最先进的ColBERT-v2快了近40倍。[code](https://github.com/facebookresearch/dpr-scale)【Retrieval】 |
| 5        | [Causality-Guided Multi-Memory Interaction Network for Multivariate Stock Price Movement Prediction](https://aclanthology.org/2023.acl-long.679/)<br />多元股价走势预测的因果导向多记忆交互网络 | 2023 july | 在预测某只股票时，作者假设来自其他股票的信息也应该被用作辅助数据来提高业绩。提出了一种新的端到端深度神经网络——因果关系引导的多记忆交互网络(CMIN)，该网络首次将金融文本数据与因果关系增强的股票相关性之间的多模态建模，以达到更高的预测精度。【Stock Price Prediction】 |
| 6        | [LAIT: Efficient Multi-Segment Encoding in Transformers with Layer-Adjustable Interaction](https://aclanthology.org/2023.acl-long.571/)<br />LAIT：具有可调层交互的transformer中的高效多段编码 | 2023 july | 在实践中，许多NLP任务的输入文本可以被视为相关片段的序列(例如，段落中的句子序列，或NLI中的假设和前提)。虽然参与这些片段对许多任务非常有益，作者假设这种相互作用可以延迟到稍后的编码阶段。引入了变压器层可调交互作用(LAIT)，LAIT能够在保持高精度的同时减少30-50%的注意力FLOPs。==【Transformer】== |
| 7        | [Cognitive Reframing of Negative Thoughts through Human-Language Model Interaction](https://aclanthology.org/2023.acl-long.555/)<br />通过人-语言模型互动对消极思想的认知重构 | 2023 july | 以人为中心研究语言模型如何帮助人们重构消极思想。作者定义了一个由七个语言属性组成的框架，可以用来重新构建一个思想，开发了自动化的指标来衡量这些属性，并通过心理健康从业者的专家判断来验证它们。实验发现人们更喜欢高度共情或特定的框架，而不是过于积极的框架。==【】== |
| 8        | [We Understand Elliptical Sentences, and Language Models should Too: A New Dataset for Studying Ellipsis and its Interaction with Thematic Fit](https://aclanthology.org/2023.acl-long.188/)<br />用于研究省略句及其与主题契合交互的新数据集 | 2023 july | 作者探讨了事件参与者的原型性如何影响语言模型(LMs)处理省略句和识别不同主题契合度的省略参数的能力，范围从高度典型的参与者到语义异常的参与者。因此构建了ELLie，这是第一个完全由包含不同类型椭圆结构的话语组成的数据集，在结构上适合于评估论点主题拟合在解决省略和重建缺失元素方面的效果。==【Ellipsis DataSet】== |
| 9        | [LayoutMask: Enhance Text-Layout Interaction in Multi-modal Pre-training for Document Understanding](https://aclanthology.org/2023.acl-long.847/)<br />增强文本布局交互在多模态预训练中为了文档理解 | 2023 july | 可视化富文档理解，主要的挑战是如何将文档的不同模式(文本、布局和图像)融合到具有不同预训练任务的统一模型中。提出了一种新的多模态预训练模型LayoutMask，增强统一模型中文本和布局模态之间的交互，并为下游任务产生自适应和鲁棒的多模态表示。==【Document Understanding】== |
| 10       | [Weakly-Supervised Spoken Video Grounding via Semantic Interaction Learning](https://aclanthology.org/2023.acl-long.611/)<br />通过语义交互学习的弱监督口述视频定位 | 2023 july | 作者研究了弱监督的语音视频定位，即学习在没有昂贵的时间注释的情况下定位时刻。为了有效表征跨模态语义提出了一种由声-语义预训练(ASP)和声-视觉对比学习(AVCL)组成的语义交互学习(SIL)框架。==【Spoken Video Grounding】== |
| 11 day12 | [Constrained Tuple Extraction with Interaction-Aware Network](https://aclanthology.org/2023.acl-long.640/)<br />基于交互感知网络的约束元组提取 | 2023 july | 在实践中，知识三元组的有效性与空间、时间或其他类型的约束相关并随其变化。因此提出了一种约束元组提取(CTE)任务来保证知识元组的有效性。并构建了一个交互感知网络来挖掘约束。此外作者建立了一个新的数据集，其中总共包含1,748,826个约束元组用于训练和3656个约束元组用于评估。==【constrained tuple extraction】== |
| 12 short | [LI-RAGE: Late Interaction Retrieval Augmented Generation with Explicit Signals for Open-Domain Table Question Answering](https://aclanthology.org/2023.acl-short.133/)<br />后期交互检索增强生成用开放域表问答的显式信号 | 2023 july | 【】                                                         |









# 三、Others

> 1. Chat-Oriented Dialogu：系统主要目标是进行自由对话和提供用户娱乐、社交互动或一般性的信息交流。通常用于聊天机器人、虚拟助手、社交媒体机器人等应用，其中用户可以提出各种问题、分享故事、进行闲聊等。
>
> 2. Task-Oriented Dialogue：系统帮助用户完成特定任务或目标，例如预订机票、在线购物、查询天气、旅游预订等需要与用户进行任务导向对话以满足其需求的应用。
>
> 3. Multi-party Dialogue：是指在一个对话或交流中涉及多个参与者或对话方的对话形式。多方对话可以包括三个或更多的对话参与者。这些对话参与者可以是人类用户，也可以是自动化的对话代理（例如聊天机器人、虚拟助手等）。
>
> 4. Dialogue Summarization：对话摘要任务，其目标是将对话中的内容精炼、概括成较短的文本，以捕捉对话的主要信息和关键要点。对话摘要模型需要能够从对话历史中筛选和总结最相关的信息，以便生成紧凑而有信息价值的摘要。一般分单轮（Single-Turn）和多轮（Multi-Turn）对话摘要。
>
> 5. Dialogue Generation：即根据用户的输入生成相关的自然语言响应。
>
> 6. NLP = NLU + NLG，NLU-Neural Language Understanding指的自然语言理解，NLG-Neural Language Generation指的自然语言生成。两者是相辅相成的，只有做好NLU才能做好NLG，做好NLG就可以做很多有趣的落地。
>
> 7. [认真的聊一聊对话系统（任务型、检索式、生成式对话论文与工具串讲） - 知乎 夕小瑶](https://zhuanlan.zhihu.com/p/83825070) 还没细看
>
> 8. DST：Dialogue State Tracking对话状态跟踪，帮助系统理解用户的请求并采取适当的行动。数据示例：**用户：**你好，我需要找一家附近的中餐馆，我想预订明天晚上8点的桌子。**系统：**当地有很多中餐馆可供选择。请告诉我您有任何特殊需求，比如地点、价格范围或者餐厅类型。**用户：**我希望附近并且价格适中的中餐馆。**系统：**好的，我会为您找到附近且价格适中的中餐馆。请稍等片刻。**系统（DST 更新）：**领域(domain)：餐厅；意图(intention)：餐厅预订；槽值对(slot-value pairs)
>
>    ：时间：明天晚上8点/地点：附近/价格范围 适中/餐厅类型：中餐馆
>
> 9. JGA："Joint Goal Accuracy" 的缩写，是一种用于评估对话状态跟踪（DST）模型性能的度量标准，包括**Domain** ，**Slot** 和**Goal** 准确性的综合性能。

> 1. [MultiWOZ](https://github.com/budzianowski/multiwoz)：全称Multi-domain Wizard-Of-Oz， Wizard-Of-Oz（绿野仙踪）。一个完全标记的人与人书面对话的集合，跨越多个领域和主题。
> 2. [SGD](https://github.com/google-research-datasets/dstc8-schema-guided-dialogue) ：The Schema-Guided Dialogue Dataset，模式引导对话，带注释的 人与虚拟之间的多域、面向任务的对话 助理。这些对话涉及与服务和 API 的交互跨越20个领域，例如银行、活动、媒体、日历、旅行和 天气。



> 1. BLEU（Bilingual Evaluation Understudy）：BLEU是一种用于机器翻译和对话生成任务的常见自动评估指标。它通过比较生成的文本与参考文本之间的 n-gram 重叠来度量生成文本的质量。较高的BLEU分数表示更好的性能。
>
>    $BLEU = BP * exp(1/n * (log(p1) + log(p2) + log(p3) + log(p4))$
>
> 2. ROUGE（Recall-Oriented Understudy for Gisting Evaluation）：ROUGE是一种用于评估文本摘要和对话生成的自动评估指标。它衡量生成文本与参考文本之间的词语、短语和句子重叠。ROUGE指标包括ROUGE-1、ROUGE-2和ROUGE-L等不同的变体。
>    $ROUGE-N = (Count of overlapping n-grams) / (Total n-grams in reference)$
>
> 3. CIDEr（Consensus-based Image Description Evaluation）：CIDEr是一种用于图像描述生成和对话生成的评估指标。它考虑了多样性和一致性，通过比较生成文本与多个参考文本来评估性能。CIDEr-D 衡量多样性，包括不同n-gram的分布。CIDEr-S 衡量一致性，包括参考文本的相似性。
>
>    $IDEr = α * {CIDEr-D} + (1 - α) * CIDEr-S$
>
> 4. Human Evaluation（人工评估）：除了自动评估指标，人工评估也是一种常见的评测方法。人工评估通常包括主观评分，包括流畅性、相关性、信息量等方面的评价。人工评估可以提供更综合的性能评估。




