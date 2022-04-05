本文将简单总结一些常用的springboot 配置项
## JSON
```shell
# 配置结果为空时不进行显示
spring.jackson.default-property-inclusion=non_null
```
## mybatis 持久化
```shell
# 配置数据库
spring.datasource.url=jdbc:mysql://localhost:3306/test?serverTimezone=UTC&useAffectedRows=true
# 数据库用户名
spring.datasource.username=user
# 数据库密码
spring.datasource.password=123456
# 将”_小写字母“形式命名的字段与小驼峰命名的变量进行关联
mybatis.configuration.map-underscore-to-camel-case=true
# 实体类的位置
mybatis.typeAliasesPackage=com.nihilwater.permission.entity
# sql配置文件.xml文件的位置
mybatis.mapperLocations=classpath:mapper/*.xml
# 配置sql运行时的输出
mybatis.configuration.log-impl=org.apache.ibatis.logging.stdout.StdOutImpl
```
## SSL 证书
```shell
# 配置服务端口
server.port=443
# 证书名（证书直接放在resources下）
server.ssl.key-store=classpath:nihilwater.com.pfx
# 证书密码
server.ssl.key-store-password=*******
# 证书加密类型
server.ssl.key-store-type= PKCS12
```
## Redis缓存
```shell
# Redis数据库索引（默认为0）
spring.redis.database=0
# Redis服务器地址
spring.redis.host=localhost
# Redis服务器连接端口
spring.redis.port=6379
# Redis服务器连接密码（默认为空）
spring.redis.password=********
# 连接池最大连接数（使用负值表示没有限制）
spring.redis.jedis.pool.max-active=8
# 连接池最大阻塞等待时间（使用负值表示没有限制）
spring.redis.jedis.pool.max-wait=-1
# 连接池中的最大空闲连接
spring.redis.jedis.pool.max-idle=8
# 连接池中的最小空闲连接
spring.redis.jedis.pool.min-idle=0
# 连接超时时间（毫秒）
spring.redis.timeout=300
```