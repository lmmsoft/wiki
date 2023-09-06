# 本文保存 gcp 使用相关的文档

## 免费账号介绍
- https://developers.google.com/maps/billing-credits?hl=zh-cn#monthly
- https://developers.google.com/maps/billing-credits?hl=zh-cn
- 简介：
- 90天，300usd；
- 谷歌地图，另外每个月 200usd。地图相关的API，先扣 $200，再扣  Google Cloud Platform 的 $300。到期前绑定信用卡续订，可以继续使用每月 $200 的费用。 （如上所述，在免费试用结束当天或之前，您必须将第一个 Cloud Billing 帐号升级为付费帐号。升级之后，即使免费试用结束，每月 200 美元的赠金也将继续发放到您的 Cloud Billing 帐号。）

## 免费层级
- 所有账号都享受的免费层级，和赠金无关
  - https://cloud.google.com/free/docs/free-cloud-features?hl=zh_CN#free-tier

## 谷歌地图
- 结算方式 （没看太懂）
    - https://developers.google.com/maps/billing/gmp-billing?hl=zh-cn#billing-overview 

## 其他
- 90 天到期后，用小号再注册谷歌，并绑定到大号上面，可以让大号的资源（比如虚拟机），继续使用小号的 $300 结算。也就是 大号的服务，每个小号续命 3 个月。
  - https://uzbox.com/usa/googlecloud.html

## ChanageLog
- 2023-09-06 免费体验结束前2天，升级到完整账号
![image](https://github.com/lmmsoft/wiki/assets/1109198/12dc71ed-6890-4ec4-875a-069f99a1ae3f)
- 需要删除所有不需要的服务
  - 删了 vetex AI 部署的 stable diffusion 模型
  - 删了 VM 一台
