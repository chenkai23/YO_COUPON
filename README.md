## 什么是牛券 oneCoupon？

牛券是一款高性能优惠券系统，与其他网上优惠券系统不同，**牛券能够承受近十万次查询和分发请求的高并发压力**。

项目旨在帮助校招和社招的同学掌握足够的亮点，为获得理想的 offer 助力。此次代码实现非常优雅，甚至细致到参数定义都蕴含深意，值得大家学习借鉴。

其中的一些亮点部分已重点标记，大家可根据实际情况学习即可。该图会持续更新。

![](https://oss.open8gu.com/image-20240723011449928.png)

## 业务架构

从优惠券的业务属性上来说，每个平台都离不开优惠券，优惠券又分为平台券和店铺券，在此之上券类型分为折扣券、满减券以及立减券。当然，优惠券的领取和使用同样具有限制，详情如下：

![](https://oss.open8gu.com/image-20240911201453992.png)

下方的业务架构图全面描述了项目的服务集合、组件库列表和基础设置层等要素，有助于用户快速了解牛券平台的顶层设计和业务细节，从零到一进行构建。

能力层部分虽然涵盖了多个问题解决方案，但与整个项目的亮点相比，这部分内容并非全面展示。随着学习的深入，大家将能够更清楚地理解和掌握这些内容，并从中获得更多的实际应用能力。

![](https://oss.open8gu.com/image-20240822225009816.png)

## 技术架构

我们选择了基于 Spring Boot 3 和 JDK17 进行底层建设，同时组件库的版本大多也是最新的。这样做既能享受新技术带来的性能提升，也能体验到新特性带来的惊喜。

如果用一张图来概括牛券的技术架构，其展现形态如下图所示。

![](https://oss.open8gu.com/image-20240722104707368.png)

技术架构涵盖了 SpringBoot 3、SpringCloudAlibaba、Nacos、Sentinel、Skywalking、RocketMQ 5.x、ElasticSearch、Redis、MySQL、EasyExcel、XXL-Job、Redisson 等技术。

框架技术和版本号关系如下表格所示。

|      | 技术                | 名称               | 版本           | 官网                                                         |
| ---- | ------------------- | ------------------ | -------------- | ------------------------------------------------------------ |
| 1    | Spring Boot         | 基础框架           | 3.0.7          | [https://spring.io/projects/spring-boot](https://spring.io/projects/spring-boot) |
| 2    | SpringCloud Alibaba | 分布式框架         | 2022.0.0.0-RC2 | [https://github.com/alibaba/spring-cloud-alibaba](https://github.com/alibaba/spring-cloud-alibaba) |
| 3    | SpringCloud Gateway | 网关框架           | 2022.0.3       | [https://spring.io/projects/spring-cloud-gateway](https://spring.io/projects/spring-cloud-gateway) |
| 4    | MyBatis-Plus        | 持久层框架         | 3.5.7          | [https://baomidou.com](https://baomidou.com)                 |
| 5    | MySQL               | OLTP 关系型数据库  | 5.7.36         | https://www.mysql.com/cn                                     |
| 6    | Redis               | 分布式缓存数据库   | Latest         | [https://redis.io](https://redis.io)                         |
| 7    | RocketMQ            | 消息队列           | 2.3.0          | [https://rocketmq.apache.org](https://rocketmq.apache.org)   |
| 8    | ShardingSphere      | 数据库生态系统     | 5.3.2          | [https://shardingsphere.apache.org](https://shardingsphere.apache.org) |
| 9    | FastJson2           | JSON 序列化工具    | 2.0.36         | [https://github.com/alibaba/fastjson2](https://github.com/alibaba/fastjson2) |
| 10   | Canal               | BinLog 订阅组件    | 1.1.6          | [https://github.com/alibaba/canal](https://github.com/alibaba/canal) |
| 11   | HuTool              | 小而全的工具集项目 | 5.8.27         | [https://hutool.cn](https://hutool.cn)                       |
| 12   | Maven               | 项目构建管理       | 3.9.1          | [http://maven.apache.org](http://maven.apache.org)           |
| 13   | Redisson            | Redis Java 客户端  | 3.27.2         | [https://redisson.org](https://redisson.org/)                |
| 14   | Sentinel            | 流控防护框架       | 1.8.6          | [https://github.com/alibaba/Sentinel](https://github.com/alibaba/Sentinel) |
| 15   | XXL-Job             | 分布式定时任务框架 | 2.4.1          | [http://www.xuxueli.com/xxl-job](http://www.xuxueli.com/xxl-job) |
| 16   | BizLog              | 操作日志工具       | 3.0.6          | https://github.com/mouzt/mzt-biz-log                         |
| 17   | EasyExcel           | Excel 处理工具     | 4.0.1          | https://easyexcel.opensource.alibaba.com                     |
| 18   | ElasticSearch       | 分布式搜索引擎     | TODO           | https://github.com/elastic/elasticsearch                     |


