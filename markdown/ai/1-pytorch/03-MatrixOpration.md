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
| 增加维度 | tensor.unsqueeze(dim) | 增加一个维度，周长为1 |
| 矩阵拼接 | torch.cat((a,b),dim=)  | 矩阵拼接， 在第n个维度上进行拼接，dim从0开始|
| 矩阵堆叠 | torch.stack(\[a,b\],dim=) | 堆叠矩阵，不同于cat，他会创建一个新的维度|
| 重复函数 | tensor.repeat(dim1, dim2) | 矩阵重复|
| 线性递增 | torch.arange(start, end, step) | 生成从start（包含）到end(不包含) 步长为step的线性tensor |
| 维度置换 | tensor.permute(0,1,3,2) | 将3和2 维度进行交换，x.permute(i).permute(i) = x  | 
| 改变维度 | tensor.reshape() | reshape可以改变tensor的维度 | 
