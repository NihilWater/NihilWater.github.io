# loss 函数

| 函数名         | 接口                        | 使用说明 |
| -------------- | -------------------------- | -------- |
| 二分类交叉熵   | torch.nn.BCELoss            | --       |
| 均方差函数    | torch.nn.MSELoss()          | --       |
| 平均绝对值函数 | torch.nn.L1Loss()           | --       |
| 交叉熵损失函数 | torch.nn.CrossEntropyLoss() | --       |




## 二次损失函数

## sigmoid_focal_loss_jit
```python
sigmoid_focal_loss_jit(
            pred,
            class_target,
            alpha=,
            gamma=,
            reduction="sum"
        )
```

