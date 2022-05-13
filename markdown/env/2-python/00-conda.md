# conda 安装虚拟环境

## 介绍
Anaconda提供了在一台机器上执行Python / R数据科学和机器学习的最简单方法。通过使用Anaconda，可以方便的进行python 环境的创建，多版本间python的切换，以及更加简单的pip包安装。

【意义】多版本python控制让用户在一台电脑上运行多个python环境，防止出现pip包的版本冲突。例如在深度学习任务中，一个常用的pip包叫做`pytorch`, 用户如果想要研究前期使用低版本`pythorch`开发的网络时，而用户电脑上又存在新版本`pytorch`的项目，由于一个python环境只能存在一个`pythorch`包，所以一个解决办法就是安装连个python 环境，而Anaconda就为用户提供了这样的功能，并且可以通过简单的命令进行python 环境的切换。

## 创建虚拟环境

可以简单的使用如下的命令来创建一个虚拟环境。

```shell
conda create -n environment_name python=3.6
```

如果要将虚拟环境放置到指定位置需要使用到 `--prefix` 参数。如下的命令将会在`D:/environment/` 目录下创建一个名为Python的虚拟环境。

```shell
conda create --prefix=D:/environment/Python python=3.8
```

克隆一个虚拟环境
```
conda create -n env2 --clone env1 
```




