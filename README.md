

# 调研思路

> NLP顶会：ACL EMNLP AAAI
>
> 调研：基于知识的对话系统 （Long paper )
>
> Keyword：dialogue / conversation/interaction
>
> 论文题目地址+摘要总结
>
> 以及dialogue的综述:[Recent advances in deep learning based dialogue systems: a systematic survey](https://sentic.net/dialogue-systems-survey.pdf)



## 1. Papers

> 1. [Summary of ACL about dialogue](./1ACL-Dialogue.md)：共81篇
> 2. [Summary of EMNLP about dialogue](./2EMNLP-Dialogue.d)：共 篇
> 3. [Summary of AAAI about dialogue](3AAAI-Dialogue.md)：共26篇



## 2. Survey on dialogue

​	**Abstract:** In this survey, we mainly focus on the **deep learning** based dialogue systems.
​	From the angle of **model type**：we discuss the principles, characteristics, and applications of diferent models that are widely used in dialogue systems（在对话系统中广泛使用的不同模型的原理、特点和应用）.
​	From the angle of **system type**：we discuss **task-oriented and open-domain**  dialogue systems as two streams of research（面向任务和开放域的对话系统）.
​	Furthermore, we comprehensively review the **evaluation methods and datasets** for dialogue systems to pave the way for future research.

| Category      | User message (U)                                             | Agent response (R)                                           | External knowledge (K) |
| ------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------------------- |
| Task-oriented | I need to fnd a nice restaurant in Madrid that serves expensive Thai food | There is a restaurant called Bangkok City locating at 9 Red Ave. | Restaurant database    |
| Open-domain   | I love the grilled fish so much!                             | Yeah. it’s a famous Chinese dish                             | Commonsense KG         |

​	A Summary diagram:

<img src="https://raw.githubusercontent.com/yangxze/Pictures_Bed/main/Pictures/image-20231020205306559.png" alt="image-20231020205306559" style="zoom: 67%;" />



## 3. Others

> 1. long paper：也可分oral和poster paper，**oral**，需要作者上台讲一讲；**poster**海报论文，作者制作一张海报与参会者交流，很难区分oral和poster这两种，但高分论文才有可能中oral。这两种都是**long paper**了，也就是全文收录，正儿八经的顶会本会，一般是成熟完善的工作。
> 2. short paper：可以是没有完成的工作，甚至是负面结果，或者提出新问题，挖个新坑，对完成度不做要求，和long paper的直观区别就是看篇幅。
> 3. Workshop：和大会一起召开的，挂大会（或主办方）名字，但会注明是哪个workshop，比如:4th CASE @ ACL2021，workshop就像一个专注于某一个热点的研讨会，如果是某个方面大佬召集质量就比较高，但有时候稿件都收不够，质量参差不齐。
> 4. Findings：中long paper差点意思，但是确实有一定质量，就是review分数低一些，但也是经过会议同行评议的，ACL会放入官方存档，比Arxiv预印本强很多。
