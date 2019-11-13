# 从0到1实战微服务架构

## 前言 

微服务是继SOA后，最流行的服务架构风格之一。

按照微服务对系统进行拆分后，每个服务的业务逻辑都更加简单、清晰。服务之间是松耦合的，模块之间的边界也更加清晰。

微服务有效降低了软件项目的业务复杂程度，为小团队独立开发、持续交付和部署打下了良好的基础。

遗憾的是，微服务并不是银弹。与传统的单一架构相比，微服务架构对团队的组织架构、技术水平、运维能力等方面，都提出了更高的要求。如果没有掌握得当的方法而生搬硬套，微服务架构只会会适得其反－－降低项目的开发效率，这是本书的创作初衷之一。

在国内外的技术社区中，比较推崇现有开源方案，如"Spring Cloud全家桶"或者阿里开源的"Dubbo"。上述框架通常已经实现了服务发现、配置、负载均衡、限流熔断，等微服务架构所必须的的核心功能。

使用开源框架省却了造轮子的过程，但也降低了我们学习、思考的欲望。

为什么需要服务发现，又如何实现它呢？配置中心呢....思考和设计的过程充满了挑战，也是提升自身架构能力的一种手段。这是本书的创作初衷之二。

已有的微服务资料过于重视微服务的开发，忽略了微服务赖以生存的生态系统：工具链、自动化运维。可以说，离开了这两点的支持，微服务架构将难以落地。完善这两方面的思考和实战，是本书的创作初衷之三。

为此，我撰写了这本《从0到1实战微服务架构》。让我们"暂时忘掉"已有的、成熟的开源解决方案。尝试亲自动手，实现微服务架构的各个模块。

我们会从微服务开发、工具链、运维这三个角度，阐述微服务架构的实战方案。

如果本书帮助了你，欢迎在在[github](https://github.com/liheyuan/hands-on-microservices)加Star，但严禁用于商业用途！(参见本页底部版权声明)

由于能力水平所限，本书难免存在各种错误，恳请各位进行指正(Issue or PR)，谢谢！

## 2.0前言

自从去年发布了1.0版本后，已过去一年有余，技术圈又发生了不少变革，其中包括：
* Spring Boot 2.0 正式成为稳定版
* K8S的Operator持续火爆

为此，我开启了本书2.0版的写作计划，除了升级为Spring Boot 2.0之外，也会将K8S的一些最新实战融入进来。

写作水平有限，还请各位多提宝贵意见。

## 读者基础

由于篇幅、精力所限，本书无法写成一本”零起点”教程。我假设读者具有至少2年的服务端工作经验，并且了解以下技术或原理：

* Git
* Maven & Gradle
* Docker & k8s
* Java
* Spring / Spring Boot 
* 数据库: 如MySQL
* 消息队列: 如RabbitMQ
* 缓存系统: 如Memcached 
* 内存数据库: 如Redis

本书可以供架构师、项目经理、高级服务端程序员参考、学习。

动手实战是本书的核心内容，因此本书所涉及的全部代码，都托管到了我的[Github上](https://github.com/liheyuan)(以lmsia-开头的项目)。

这些代码以研讨为主要目的，也可以直接应用于生产，但本人不对其稳定性负责。

## 在线阅读地址

在线阅读: [从0到1实战微服务架构](https://coder4.com/homs_online/)

## 版权

本书虽然在github上公开写作，但版权归本人[Coder4](https://coder4.com)所有。

依照 [署名-非商业性使用-相同方式共享](https://creativecommons.org/licenses/by-nc-sa/2.5/cn/) ，任何人可以在保留署名的情况下转载。但严禁用于商业用途。

This is a book powered by [GitBook](https://github.com/GitbookIO/gitbook).

