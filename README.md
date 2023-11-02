

调研-idea/实验-论文（会议->期刊->杂志）

> NLP顶会：ACL EMNLP AAAI
>
> 调研：基于知识的对话系统 （Long paper )
>
> keyword：dialogue / conversation/interaction
>
> 题目+年份+会议+总结





[Recent advances in deep learning based dialogue systems: a systematic survey](https://sentic.net/dialogue-systems-survey.pdf)

## Abstract

> In this survey, we mainly focus on the ==deep learning based dialogue systems.==
>
> From the angle of ==model type==：we discuss the principles, characteristics, and applications of diferent models that are widely used in dialogue systems（在对话系统中广泛使用的不同模型的原理、特点和应用）
>
> From the angle of ==system type==：we discuss ==task-oriented and open-domain==  dialogue systems as two streams of research（面向任务和开放域的对话系统）
>
> Furthermore, we comprehensively review the ==evaluation methods and datasets== for dialogue systems to pave the way for future research.

​						Table 1 Examples of inputs and outputs of task-oriented and open-domain dialogue systems in datasets

| Category      | User message (U)                                             | Agent response (R)                                           | External knowledge (K) |
| ------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------------------- |
| Task-oriented | I need to fnd a nice restaurant in Madrid that serves expensive Thai food | There is a restaurant called Bangkok City locating at 9 Red Ave. | Restaurant database    |
| Open-domain   | I love the grilled fish so much!                             | Yeah. it’s a famous Chinese dish                             | Commonsense KG         |

​	Some datasets provide external knowledge annotations for each dialogue pair, e.g., in task-oriented dialogue systems, the external knowledge can be retrieved from restaurant databases; in open-domain dialogue systems, it can be retrieved from commonsense knowledge graphs (KG)

## 1 Introduction

<img src="https://raw.githubusercontent.com/yangxze/Pictures_Bed/main/Pictures/image-20231020205306559.png" alt="image-20231020205306559" style="zoom: 67%;" />

## 2 Neural models in dialogue systems

> 1. Convolutional Neural Networks (CNNs)
> 2. Recurrent Neural Networks (RNNs)
> 3. Vanilla Sequence-to-sequence Models,
> 4. Hierarchical Recurrent Encoder-Decoder (HRED),
> 5. Memory Networks
> 6. Attention Networks, Transformer
> 7. Pointer Net and CopyNet
> 8. Deep Reinforcement Learning models,
> 9. Generative Adversarial Networks (GANs),
> 10. Knowledge Graph Augmented Neural Networks.



## 3 Task‑oriented dialogue systems

> 1. NLU  Natural language understanding
> 2. DST  Dialogue state tracking
> 3. Policy learning
> 4. NLG Natural language generation
> 5. End‑to‑end methods
> 6. Research challenges and hot topics
>    * 

## 4 Open‑domain dialogue systems

> 1.  Context awareness
> 2. Response coherence
> 3. Response diversity
> 4. Speaker consistency and personality‑based response
> 5. Empathetic response
> 6.  Controllable generation
> 7. Conversation topic
> 8. Knowledge‑grounded system
> 9.  Interactive training
> 10. Visual dialogue

## 5 Evaluation approaches

> 

## 6 Datasets



## 7 Conclusions and trends

> 1. Multimodal dialogue systems 
> 2. Multitask dialogue systems 
> 3. Corpus exploration 
> 4. User modeling
> 5. Dialogue generation 