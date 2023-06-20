# 这个文档放置 MySQL 相关的资料

## 异地多活方案 by Claude
```
MySQL 异地双活主要有以下几种方案:
1. MySQL Replication:通过主从复制,在不同地点部署主数据库和从数据库,应用连接从数据库提供服务。如果主数据库下线,可以 Failover 到从库,实现高可用。缺点是无法实现读写分离,有数据一致性问题。
2. MySQL Group Replication:MySQL 5.7 版本引入的新特性,可以实现异地多主复制,所有主库都可以读写,并自动同步数据。缺点是部署和管理比较复杂。
3. DRBD + Corosync + Pacemaker:通过 DRBD 实现存储层面的主从复制和同步,Corosync + Pacemaker 实现自动 Failover,当主数据库不可用时自动切换到从库。缺点是部署和管理也比较复杂。
4. TungstenCluster:一站式的 MySQL 异地双活方案,实现异地多主复制,自动数据中心和 MySQL 角色切换,以及恢复。缺点是企业版本收费较高。
5. 搭建 MySQL 代理中间层:通过 Proxy 层实现读写分离,主库负责写,从库负责读。同时 Proxy 实现自动检测主库健康状态,一旦主库下线可以快速切换到从库。缺点是代理层的维护成本较高,数据一致性也无法保证。
综上,异地双活方案的选择一般根据公司的资源情况及数据安全要求来定。简单方案部署容易但安全性能弱,复杂方案实现效果好但难以维护。选择最恰当的方案并妥善测试与实施是关键。
```

## 介绍下 MySQL Group Replication方案 by Claude
```
MySQL Group Replication 是 MySQL 5.7 版本引入的新特性,可以实现异地多主复制。它的主要特点是:
1. 多主复制:组中的所有成员都可以同时处理读写请求,自动同步数据。
2. 数据冲突检测与解决:Group Replication 可以检测同一事务内的数据冲突,并根据一定策略解决。
3. 自动节点故障检测与恢复:Group Replication 能自动检测节点故障,并从备份节点恢复。
4. 一致性保证:Group Replication 可以在线更改组成员关系,保证了最终数据一致性。
Group Replication 的基本工作原理是:
1. 组成员之间通过复制通道交换消息,同步提交的事务。
2. 当一个成员提交事务后,会将事务消息广播给其他成员。
3. 其他成员接收到消息后,会在本地执行事务,然后进行投票。
4. 如果超过半数成员投了同意票,则事务最终提交,否则回滚。
5. 通过这种机制,保证了组内数据的强一致性。
Group Replication 部署大致步骤:
1. MySQL 版本大于等于 5.7,并打开 Group Replication 插件
2. 为每台 MySQL服务器配置唯一的服务器 ID
3. 在所有服务器上创建用于复制的 MySQL 用户并授权
4. 配置组复制相关参数,指定组名、节点信息等
5. 启动组复制插件并添加种子节点,其他节点自动加入组
6. 验证组复制功能是否正常工作
Group Replication 提供了较为完善的异地多主方案,但其复杂性也较高,适合有专业 DBA 运维的企业使用。 
```
## CloudCanal
- 一句话，异构的数据库复制
- eg: 
```
5分钟搞定 MySQL 到 TiDB 迁移同步-CloudCanal 实战
5分钟搞定 MySQL 到 ElasticSearch 迁移同步-CloudCanal 实战
5分钟搞定 MySQL 到 MySQL 异构在线数据迁移同步-CloudCanal 实战
5分钟搞定 MySQL 到 ClickHouse 实时数据同步-CloudCanal 实战
```
- claude
```
CloudCanal 是阿里巴巴开源的一款基于 Canal 的 MySQL 数据库增量订阅&消费组件。它主要用于实现 MySQL 数据库增量数据的订阅和消费,常用于构建数据库异构迁移、异构复制、实时业务 cache 刷新等场景。
CloudCanal 的主要功能是:
1. 基于 MySQL binlog 增量订阅 canal 客户端
2. 支持 RDS MySQL 与自建 MySQL 订阅
3. 支持业务去重和异常重试
4. 支持增量消费接口调用(支持同步和异步两种消费模式)
5. 支持并发消费和顺序消费两种消费模式
6. 支持定时任务方式和长轮询方式两种消费触发方式
7. 支持数据落地到 MQ、Redis、ES、MySQL 等多种方式
CloudCanal 的工作原理是:
1. 启动 canal 实例,连接 MySQL 获得 binlog 事件流
2. 添加消费者组,消费者组定义具体的 binlog 事件订阅规则和消费方式
3. canal 实例根据订阅规则,筛选 binlog 事件并推送给消费者组
4. 消费者组中的消费实例接收 binlog 事件,并进行消费(调用接口,落地到 MQ 等)
5. 支持消费实例水平扩展,规则同步到新实例
所以,CloudCanal 的主要应用场景是实现 MySQL 数据的实时同步到其他异构系统中,常用于构建数据库异构迁移、数据库复制、业务 Cache 刷新的解决方案。
总体来说,CloudCanal 是一个相对成熟和易用的 Canal 企业级封装,值得在项目中应用。
```
## MySQL 数据迁移，导入导出教程
- workbench 和 mysqldump 都有
- https://learn.microsoft.com/zh-cn/azure/mysql/migrate/how-to-decide-on-right-migration-tools
