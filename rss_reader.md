# 本文记录 rss 阅读器相关的经验

# 1. 在线产品

## [inoreader](http://inoreader.com/)
- 用过 inoreader， UI 和 google reader 类似，功能也不错，问题：1. 现在需要翻墙 2. 开始收费，而且费用相对于中国互联网产品较高 3. 不收费限制订阅数量，我已经超了，无法再使用

# 2. Selfhost

## tiny tiny rss
- https://tt-rss.org/
- https://git.tt-rss.org/fox/tt-rss.git
- https://git.tt-rss.org/fox/ttrss-docker-compose
- php 实现的项目
- 以前在 azure VM 上 self host 过，它作为服务器，再配上其他第三方 API
- 使用体验比 inoreader 差一点，导致使用率比较低，后来VM到期，就没备份，直接再见了
- 现在有 docker-compose 版本的，搭建成本低降低，暂不考虑用

## FreshRSS
- 官网 https://freshrss.org/
- 开源 https://github.com/FreshRSS/FreshRSS
- 官方docker image https://hub.docker.com/r/freshrss/freshrss/ https://github.com/FreshRSS/FreshRSS/tree/edge/Docker
- php 语言实现
- 支持GReader和Fever协议，官方支持的第三方客户端对比，挺全的: https://github.com/FreshRSS/FreshRSS/tree/edge/Docker

# 其他
- 其他的还有很多，不同语言实现，star也不少，没精力摸索了；主要问题是生态不好，FreshRSS支持的客户端最多
- github 直接搜索 rss reader即可，star 1000 以上的挺多了
- https://github.com/Athou/commafeed

# 3. Client

## https://netnewswire.com/
- 开源 https://github.com/Ranchero-Software/NetNewsWire
- Swift 语言实现
- 适合苹果全家桶用户，mac, iPhone, iPad
- 可以 iCloud 同步，也可以连接 inoreader 等第三方服务，还能和 FreshRSS 连接，不支持 tinytiny RSS
- 用户体验还不错
- 目前在用，主要数据 iCloud 同步中 


# 4. 订阅源聚合
- web3订阅源聚合，推荐用 netnewswire  https://github.com/chainfeeds/RSSAggregatorforWeb3
