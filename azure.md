# azure 相关知识

- 免费服务清单 https://azure.microsoft.com/zh-cn/free/

## 免费 vm 注意事项

## 免费 mongodb 注意事项
- cosoms db for mongodb api
  - 很烂，不推荐使用，背后是 cosmos db，而不是 mongodb, 兼容性差，各种坑，浪费时间
- 推荐使用 mongodb atlas
  - 在mongodb 官网上申请，可以选 azure/aws/gcp 的服务器
  - 免费用户 500mb 共享空间

## 免费 mysql
- Azure Databas for MySQL
  - 这是真的 MySQL, 可选5.7 或 8.0
  - 免费用户 32G空间，32G备份，750h/月
  - 免费账户创建教程 https://learn.microsoft.com/zh-cn/azure/mysql/flexible-server/how-to-deploy-on-azure-free-account
  - 注意： 选 B1ms (1 个 vCore，2 GiB RAM，32 GiB 存储，396 IOPS)
    - 选择 用户开发项目或者爱好者项目 + 可突发(1-20 vCore) - 最适合不需要持续完全占用 CPU 的工作负载  
    - 有个更小的 B1s(1c 1g 400 IOPS)反而不是免费的
    - 默认20g, 可以提高到32G
    - 免费的不是所有区域都有，比如 southeast asia/japan west 就不行, hk/jp east 可以
