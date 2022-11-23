# 放置spring相关的学习笔记

# 为什么要用 Spring
让使用者只关心核心业务的开发，框架帮你屏蔽原有技术跟业务开发无关的各类技术问题

## 演进
- JAVA从业经验中，经历了SSH，SSM，SpringMVC＋M，Spring boot和Spring cloud，等等框架，核心都是Spring，都离不开spring！
- servlet: 根据 request自己处理返回response，很多基础的工作需要自己做
- SpringMVC 做了很多封装，基于IOC AOP(控制反转, 依赖注入)

## 好处
- spring设计伊始就是为了解决对象的创建和管理！后来功能愈发的完善，变成了垄断性的框架！

1. 控制反转（IOC）的思想，运用依赖注入(DI)的技术，让我们管理对象的时候再也不用new new new了！防止大量对象的创建！防止组件之间的强依赖！
2. 运用了大量的反射，代理，工厂方法，是我们学习编码技巧的最好模范！
3. AOP(面向切面编程)技术，能够使用少量代码搭建完美的的日志管理，权限管理，运行期监控！
4. 低侵入性！让我们可以轻松耦合诸如struts，hibernate，mybatis，redis，memcache，amoeba，actibemq等包括数据层，控制层，缓存，数据中间件，消息中间件的中间件！
5. 低耦合特性:通过依赖注入特性，可以借助spring容器创建，管理对象，防止在代码中硬性注入对象，防止对象混乱！
6. 通过@transaction注解，可以实现声明式事务，在注解中的代码都可以在一个事务当中，实现最简单的事务控制，异常回滚！
7. spring源码使用了诸如工厂，单例，代理，构造者，策略，模板等多种设计模式，是JAVA程序员写出优良代码的不二范例！
8. 提供大量诸如beanUtils，qstringUtils等优秀工具类！

- 但是spring 4之前，用spring开发web配置过于繁杂，笨重！让程序员不用专注于业务代码开发，spring boot ，spring cloud由此诞生，将spring再次推向辉煌神坛！
- https://blog.csdn.net/Melod_bc/article/details/53414900

## 另一篇讲好处的文章
- https://blog.csdn.net/xiao2shiqi/article/details/97368779
- https://www.zhihu.com/question/470828417/answer/1987550231
1. Spring框架为我们做了什么，没有Spring框架前我们的程序是什么样的？
1. 为什么要把对象放在Spring容器里面，为什么我不能直接new对象？
1. 为什么要把Sevlet交给Spring MVC管理，我自己写Sevlet处理HTTP请求不行吗？
1. Spring为什么要封装这么多的 Template（JDBCTemplate，RestTemplate等……）它想要干什么？
