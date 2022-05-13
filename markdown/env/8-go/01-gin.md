# Gin 框架快速上手

## Gin的安装

【设置代理】

```shell
# 取消校验，为了保证安全，Go官方设定的module校验数据库，服务器地址为：sum.golang.org，如果不关闭还是无法使用代理
go env -w GOSUMDB=off

# 更换代理
go env -w GOPROXY="https://goproxy.io"
```

【安装Gin】
```shell
# go get 下载的包会在C:\user\你的用户名\go 里， -u 参数表示更新
go get -u github.com/gin-gonic/gin
```

## Gin的使用
```go
package main

import "github.com/gin-gonic/gin"

func main() {
	r := gin.Default()
	r.GET("/ping", func(c *gin.Context) {
		c.JSON(200, gin.H{
			"message": "pong",
		})
	})
	r.Run() // listen and serve on 0.0.0.0:8080
}
```