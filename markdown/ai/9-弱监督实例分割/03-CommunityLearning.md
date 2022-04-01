# CommunityLearning

## 基础信息

文章标题：Weakly Supervised Instance Segmentation by Deep Community Learning

文章链接：[https://arxiv.org/pdf/2001.11207.pdf](https://arxiv.org/pdf/2001.11207.pdf)

发表时间：2020-01


## 背景


## 创新点简介
(社区学习， community learning)这篇文章通过训练多个子模型用于多个子任务，end-to-end trainable deep neural network with active interactions between multiple tasks。

社区学习与多任务学习不同，后者试图在没有参与模块之间紧密互动的情况下平行实现多个目标。
The community learning is different from multi-task learning that attempts to achieve multiple objectives in parallel without tight interaction between participating modules.

![](../../../img/article/2021-12-10-14-59-50.png)


## trick
在使用有实例框的标注中，可以不使用全局平均池化，而是适当的提高中间的权重。
使用log(1+f)作为CAM的输入，这样可以抑制峰值。