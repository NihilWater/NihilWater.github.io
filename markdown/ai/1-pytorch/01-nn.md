# Pytouch.nn 相关函数对照

## nn.Embedding
【功能】<br/>
产生一组存储固定大小的词典的嵌入向量的查找表。
【初始化】
```py
embed = torch.nn.Embedding(num_embeddings,embedding_dim)
```
> num_embeddings (python:int) – 词典的大小尺寸
> embedding_dim (python:int) – 嵌入向量的维度，即用多少维来表示一个符号。

有时在初始化时会被赋值会伴随着初始化过程。
```py
self.init_proposal_boxes = nn.Embedding(300, 4)
nn.init.constant_(self.init_proposal_boxes.weight[:, :2], 0.5)
nn.init.constant_(self.init_proposal_boxes.weight[:, 2:], 1.0)
```

【使用】<br />
使用过程中，将`embed`直接当作向量来是使用即可。

## nn.MultiheadAttention
【功能】<br/>
产生多头注意力模型
【初始化】
```py
 self.self_attn = nn.MultiheadAttention(d_model, nhead, dropout=dropout)
```
> num_embeddings (python:int) – 词典的大小尺寸
> embedding_dim (python:int) – 嵌入向量的维度，即用多少维来表示一个符号。

有时在初始化时会被赋值会伴随着初始化过程。
```py
self.init_proposal_boxes = nn.Embedding(300, 4)
nn.init.constant_(self.init_proposal_boxes.weight[:, :2], 0.5)
nn.init.constant_(self.init_proposal_boxes.weight[:, 2:], 1.0)
```

【使用】<br />
使用过程中，将`embed`直接当作向量来是使用即可。