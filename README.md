

### 技术架构

![pmhub-系统架构图](https://cdn.tobebetterjavaer.com/stutymore/01.什么是PmHub-20240708113736.png)


### 代码结构

```
com.laigeoffer.pmhub     
├── pmhub-ui              // 前端框架 [1024]
├── pmhub-gateway         // 网关模块 [6880]
├── pmhub-auth            // 认证中心 [6800]
├── pmhub-api             // 接口模块
│       └── pmhub-api-system                          // 系统接口
│       └── pmhub-api-workflow                        // 流程接口
├── pmhub-base          // 通用模块
│       └── pmhub-base-core                           // 核心模块组件
│       └── pmhub-base-datasource                     // 多数据源组件
│       └── pmhub-base-seata                          // 分布式事务组件
│       └── pmhub-base-security                       // 安全模块组件
│       └── pmhub-base-swagger                        // 系统接口组件
│       └── pmhub-base-notice                         // 消息组件组件
├── pmhub-modules         // 业务模块
│       └── pmhub-system                              // 系统模块 [6801]
│       └── pmhub-gen                                 // 代码生成 [6802]
│       └── pmhub-job                                 // 定时任务 [6803]
│       └── pmhub-project                             // 项目服务 [6806]
│       └── pmhub-workflow                            // 流程服务 [6808]
├── pmhub-monitor             						  // 监控中心 [6888]                 
├──pom.xml                                            // 公共依赖
```

### 技术选型

后端技术栈

|         技术          | 说明                   | 官网                                                                                                                         |
|:-------------------:|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Spring & SpringMVC  | Java全栈应用程序框架和WEB容器实现 | [https://spring.io/](https://spring.io/)                                                                                   |
|     SpringBoot      | Spring应用简化集成开发框架     | [https://spring.io/projects/spring-boot](https://spring.io/projects/spring-boot)                                           |
|     SpringCloud     | 微服务框架                | [https://spring.io/projects/spring-cloud](https://spring.io/projects/spring-cloud)                                         |
|    mybatis-plus     | 数据库orm框架             | [https://baomidou.com/](https://baomidou.com/)                                                                             |
| mybatis PageHelper  | 数据库翻页插件              | [https://github.com/pagehelper/Mybatis-PageHelper](https://github.com/pagehelper/Mybatis-PageHelper)                       |
|    elasticsearch    | 近实时文本搜索              | [https://www.elastic.co/cn/elasticsearch/service](https://www.elastic.co/cn/elasticsearch/service)                         |
|        redis        | 内存数据存储               | [https://redis.io](https://redis.io)                                                                                       |
|      rocketmq       | 消息队列                 | [https://rocketmq.apache.org/](https://rocketmq.apache.org/)                                                               |
|       mongodb       | NoSql数据库             | [https://www.mongodb.com/](https://www.mongodb.com/)                                                                       |
|        nginx        | 服务器                  | [https://nginx.org](https://nginx.org)                                                                                     |
|       docker        | 应用容器引擎               | [https://www.docker.com](https://www.docker.com)                                                                           |
|      hikariCP       | 数据库连接                | [https://github.com/brettwooldridge/HikariCP](https://github.com/brettwooldridge/HikariCP)                                 |
|         oss         | 对象存储                 | [https://help.aliyun.com/document_detail/31883.html](https://help.aliyun.com/document_detail/31883.html)                   |
|        https        | 证书                   | [https://letsencrypt.org/](https://letsencrypt.org/)                                                                       |
|         jwt         | jwt登录                | [https://jwt.io](https://jwt.io)                                                                                           |
|       lombok        | Java语言增强库            | [https://projectlombok.org](https://projectlombok.org)                                                                     |
|        guava        | google开源的java工具集     | [https://github.com/google/guava](https://github.com/google/guava)                                                         |
|      thymeleaf      | html5模板引擎            | [https://www.thymeleaf.org](https://www.thymeleaf.org)                                                                     |
|       swagger       | API文档生成工具            | [https://swagger.io](https://swagger.io)                                                                                   |
| hibernate-validator | 验证框架                 | [hibernate.org/validator/](hibernate.org/validator/)                                                                       |
|     quick-media     | 多媒体处理                | [https://github.com/liuyueyi/quick-media](https://github.com/liuyueyi/quick-media)                                         |
|      liquibase      | 数据库版本管理              | [https://www.liquibase.com](https://www.liquibase.com)                                                                     |
|       jackson       | json/xml处理           | [https://www.jackson.com](https://www.jackson.com)                                                                         |
|      ip2region      | ip地址                 | [https://github.com/zoujingli/ip2region](https://github.com/zoujingli/ip2region)                                           |
|      websocket      | 长连接                  | [https://docs.spring.io/spring/reference/web/websocket.html](https://docs.spring.io/spring/reference/web/websocket.html)   |
|   sensitive-word    | 敏感词                  | [https://github.com/houbb/sensitive-word](https://github.com/houbb/sensitive-word)                                         |
|       chatgpt       | chatgpt              | [https://openai.com/blog/chatgpt](https://openai.com/blog/chatgpt)                                                         |
|        讯飞星火         | 讯飞星火大模型              | [https://www.xfyun.cn/doc/spark/Web.html](https://www.xfyun.cn/doc/spark/Web.html#_1-%E6%8E%A5%E5%8F%A3%E8%AF%B4%E6%98%8E) |
copies or substantial portions of the Software.

Copyright (c) 2023-2024 PmHub（苍何、沉默王二）


