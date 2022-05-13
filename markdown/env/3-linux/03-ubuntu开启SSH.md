# Ubuntu 开启 SSH 服务

## 1. 安装 openssh-server
```shell
sudo apt-get install openssh-server
```

## 2. 查看是否开启了ssh

```shell
ps -e |grep ssh
```

## 3. 开启SSH
如果服务没有开器可以使用以下的命令来进行开启
```shell
sudo /etc/init.d/ssh start
```

## 4. 连接部分
在Ubuntu 命令行使用`ifconfig` 命令查看网络地址ip地址

![](../../../img/article/2022-04-11-14-45-30.png)

之后在xshell 中填写ip，端口号，用户名和密码就可以对虚拟机进行连接了。

![](../../../img/article/2022-04-11-14-48-33.png)

![](../../../img/article/2022-04-11-14-47-36.png)