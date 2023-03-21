# Supervisor进程管理工具

Supervisor是一款用采用Client/Server架构、开源([github地址](https://github.com/Supervisor/supervisor))的进程监控管理工具。

Supervisor稳定、简单、高效、可扩展、兼容性好，可以在大部分类Unix系统(Debian、Solaris、Mac OS、FreeBSD等)上使用

使用步骤
> pip install supervisor

安装完毕后，可以通过echo_supervisord_conf生成一份默认初始配置文件。
> echo_supervisord_conf > your_path/supervisord.conf



## 参考文档
- https://juejin.cn/post/6844903745587773448
