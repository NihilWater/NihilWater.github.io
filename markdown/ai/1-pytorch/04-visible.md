# pytorch 可视化

## 图片可视化
```python 
from matplotlib import pyplot as plt
image = $image.cpu().clone()  # detach().numpy() 这里的 $image 要换成自己的变量名
# image = image.permute(1,2,0)    # 这个是可选的，主要是要将图片的维度调正为(w, h, c)的形式
plt.imshow(image)  # 准备图片
plt.show()  # 展示图片
```
