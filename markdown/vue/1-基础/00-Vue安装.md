# Vue 环境配置 


## 使用 nvm 创建合适的npm
```shell
nvm install <version>
```

## 安装cnpm
```shell
npm install cnpm -g
```

## 安装vue相关内容 
```shell
cnpm install -g @vue/cli
```

## 使用vue客户端创建vue应用 
```shell
vue create hello-world
```
或者 使用cli-init 创建，两者创建的启动器是不一样的

```shell
npm install -g @vue/cli-init
# `vue init` 的运行效果将会跟 `vue-cli@2.x` 相同
vue init webpack my-project
```