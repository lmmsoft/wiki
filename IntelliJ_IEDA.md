# 常见 IDE 问题

- 运行项目，出现 Connect to 127.0.0.1:7890 [/127.0.0.1] failed: Connection refused (Connection refused)
  - 初步判断是代理问题
  - 依次检查: 
    - 系统代理软件客户端
    - 系统全局代理
    - IDE的proxy设置
    - app的 gradle.properties 里面的代理设置
    - 系统的 gradle.properties 里面的代理设置
  - 最后发现是 gradle.properties 的全局配置里被写了代理，但是代理软件没启动导致，在 gradle.properties 里删除4行代理即可
    - Windows 在：C:\Users\Administrator.gradle下的gradle.properties中
    - Mac 在：/Users/.{你的用户目录}/.gradle下的gradle.properties中
