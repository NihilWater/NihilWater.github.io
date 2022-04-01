# SETR

## 基础信息

论文题目：Rethinking Semantic Segmentation from a Sequence-to-Sequence Perspective with Transformers

文章链接：[https://arxiv.org/abs/2012.15840](https://arxiv.org/abs/2012.15840)

发表时间：2020-12 

## 创新点简介
SETR使用transformer设计了一个端到端的语义分割网络，首先将原图切割为若干 16x16 个窗口，把其中的像素进行线性映射，得到一维编码，然后使用24层transformer的编码器来完成对于图像特征的提取，然后使用卷积做上采样操作，得到最终结果。

![](../../../img/article/2022-03-11-14-59-06.png)

## 优点
是语义分割领域的一次创行，将transformer引入到了语义分割领域中。

## 存在的问题
切割的窗口过大，语义信息不仅准。
