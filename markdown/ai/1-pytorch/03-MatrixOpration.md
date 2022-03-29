# 常用pytorch矩阵操作
| 操作 | 指令 | 备注 |
|-----|-----|-----|
| 从list转变 | torch.cat($list) | 往往这类操作后面接列表生成式|
| 获取邻域 |F.unfold( x, kernel_size=kernel_size, padding=padding, dilation=dilation ) | kernel_size领域大小，padding边距，dilation填充，padding = (kernel_size + (dilation - 1) * (kernel_size - 1)) // 2|
| 邻域->图像 |F.fold( x, kernel_size=kernel_size, padding=padding, dilation=dilation ) | kernel_size领域大小，padding边距，dilation填充，padding = (kernel_size + (dilation - 1) * (kernel_size - 1)) // 2|
|出现过的量|torch.unique()| 获取矩阵中出现过的量 |
|resize|t = transforms.Compose([transforms.Resize((w,h))])<br/> new = t(old)| 需要导库：import torchvision.transforms as transforms|
|满足条件的索引|torch.nonzero(条件矩阵)|e.g. torch.nonzero(labels != num_classes) |
|指定位置值|a = torch.tensor([[1, 2],[3, 4]])<br/>b = torch.tensor([[True, False],[True, False]])<br/>a[b] | 输出结果为tensor([1, 3]) |
| 维度合并|tensor.flatten(dim1, dim2) | 可以将维度进行结合 |