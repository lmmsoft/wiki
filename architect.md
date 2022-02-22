# 架构方面的笔记

## github 系统设计汇总
- https://github.com/donnemartin/system-design-primer

## 微软的云计算设计模式
- https://docs.microsoft.com/en-us/azure/architecture/patterns/

## 限流算法
- 参考文章《高并发之API接口限流》 https://blog.csdn.net/zrg523/article/details/82185088
  - 缓存 缓存的目的是提升系统访问速度和增大系统处理容量
  - 降级 降级是当服务出现问题或者影响到核心流程时，需要暂时屏蔽掉，待高峰或者问题解决后再打开
  - 限流 限流的目的是通过对并发访问/请求进行限速，或者对一个时间窗口内的请求进行限速来保护系统，一旦达到限制速率则可以拒绝服务、排队或等待、降级等处理
- 应用级限流
  - 一、控制并发数量
    - 信号量机制（如Java中的Semaphore）来实现。
  - 二、控制访问速率
    - 漏桶算法
    - 令牌桶算法
  - 三、控制单位时间窗口内请求数
- 分布式限流
  - 自定义注解+拦截器+Redis实现限流 (单体和分布式均适用，全局限流)
- 接入层限流
  - nginx 限流，采用漏桶算法

## 分布式
- coolshell 分布式系统的事务处理
  - https://coolshell.cn/articles/10910.html
