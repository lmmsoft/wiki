# 存放 feign 相关文档

- 官网 https://github.com/OpenFeign/feign
## What is Feign?

- Feign is a Java to HTTP client binder inspired by Retrofit, JAXRS-2.0, and WebSocket. Feign's first goal was reducing the complexity of binding Denominator uniformly to HTTP APIs regardless of ReSTfulness.

- Feign 是⼀个 HTTP 请求的轻量级客户端框架。通过 接口 + 注解的方式发起 HTTP 请求调用，面向接口编程，而不是像 Java 中通过封装 HTTP 请求报文的方式直接调用。服务消费方拿到服务提供方的接⼝，然后像调⽤本地接⼝⽅法⼀样去调⽤，实际发出的是远程的请求。让我们更加便捷和优雅的去调⽤基于 HTTP 的 API，被⼴泛应⽤在 Spring Cloud 的解决⽅案中。开源项目地址：Feign，官方描述如下：


## Why Feign? 
- Feign 封装了 HTTP 请求调用的流程，而且会强制使用者去养成面向接口编程的习惯
- ![image](https://user-images.githubusercontent.com/1109198/206890976-ab2e6319-0d7b-46c4-9d98-807587f07f7b.png)
