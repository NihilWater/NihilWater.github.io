# MEInst

## 信息

文章标题：Mask Encoding for Single Shot Instance Segmentation

文章链接：[https://arxiv.org/abs/2003.11712](https://arxiv.org/abs/2003.11712)

发表时间：2020-03


## 背景
本文采用了紧凑掩膜编码，来进行单阶段实例分割任务，任务表面，使用了紧凑掩膜，对小目标的分割的效果相较二阶段无紧密掩膜的有较大提高，但对大目标，精度会少许的损失。

## 创新点简介
论文中指出，决定一个目标掩膜的关键像素主要分布在一个实例的边缘，而实例中占有大面积的部分是图像的主体部分，导致了信息的冗余。所以需要进行编码处理。
> The discriminative pixels are mainly distributed along the object boundaries while most pixels in its body hold the properties of being category-continuous and category-consistent. In other words, the existing mask representations contains redundant information and it may be highly compressed with negligible loss. 

## 详细内容

### Encoder 和 Decoder 的生成
这里会先通过Mask来直接训练编解码矩阵（压缩矩阵），而在后面的模型训练中，就不在改变之前训练好的编解码矩阵了。编解码矩阵的训练方法是`PCA`(主成分分析)使用的包是`sklearn.decomposition import IncrementalPCA`（为什么用`PCA`:作者在文中提到，我们将二维的数据变成了一维，这与主成分分析压缩很有关系，如下图，就看将一个二维数据，压缩到一维，而我们需要保留的就是中心，和方向）

![](../../../img/article/2021-12-03-16-00-40.png)
