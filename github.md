# gitbub 相关的问题

# http 无法 push 了
- github 提高了安全级别，原有 http 的无法push了
- 两种方法
- 方法一： 改用 ssh
  - 在 https://github.com/settings/keys 做ssh key 的设置
  - 在本机做ssh key 的设置 (我的 milou_mac/ pythonanywhere 已经设置好)
  - 更新仓库的origin链接:
    - git remote set-url origin git@github.com:lmmsoft/[xxx].git
    - eg: git remote set-url origin git@github.com:lmmsoft/LeetCode.git
- 方法二： 使用 token
  - 参考 https://mp.weixin.qq.com/s/56Dp3pM0BMyH2GZMGEsmCQ

# github action
- 非常强大的工具，除了 cicd 的构建发布工具外，还可以跑cron定时脚本，脚本还能与 iPhone 的快捷打通，完成更多的自定义任务（比如关闭闹钟，比如关闭app等）
- 官方教程
  - https://support.github.com/features/actions
- 其他教程
  - 介绍几个技巧，值得一看 https://zhuanlan.zhihu.com/p/348381477
- action 市场，搜索现成的任务
  - sh
- 各种好的idea
  - 如何用一个仓库记录自己的一年
    - https://github.com/yihong0618/gitblog/issues/209  
  - 利用 GitHubPoster 和 GitHub Actions 备份任意用户推特(这个项目里有大量的cron脚本，各种平台)
    - https://github.com/yihong0618/gitblog/issues/252
  - 知乎回答，打通了 github + iPhone快捷
    - https://www.zhihu.com/question/472267975/answer/2296132239
  - 自动生成github about me 首页
    - https://github.com/dejavudwh/dejavudwh
- 飞书action
  - https://github.com/xiachufang/actions-feishu/blob/main/action.yml

# github action 技巧
1. 初次调试时，可以加上 push 就触发的功能，方便调试
```
on:
  push:
    branches: [ main ]
```

2. 提交代码时，可以加上date格式化后的时间 %z %Z 是时区
```
git commit -m "Action: `date +'%Y-%m-%d %H:%M %z %Z'`"
# Action: 2022-12-16 08:57 +0000 UTC

# 默认 date 可读性差一点： action: Thu Dec 15 06:31:18 UTC 2022
```
3. crontab 格式

![image](https://user-images.githubusercontent.com/1109198/208071620-fc187be3-4b8d-43b0-ac94-7533875d76c6.png)

特殊字符	代表意义

**(星号)	代表任何时刻都接受的意思。举例来说，范例一内那个日、月、周都是*，就代表着不论何月、何日的礼拜几的12：00都执行后续命令的意思。

,(逗号)	代表分隔时段的意思。举例来说，如果要执行的工作是3：00与6：00时，就会是：0 3,6 * * * command时间还是有五列，不过第二列是 3,6 ，代表3与6都适用

-(减号)	代表一段时间范围内，举例来说，8点到12点之间的每小时的20分都进行一项工作：20 8-12 * * * command仔细看到第二列变成8-12.代表 8,9,10,11,12 都适用的意思

/n(斜线)	那个n代表数字，即是每隔n单位间隔的意思，例如每五分钟进行一次，则：*/5 * * * * command用*与/5来搭配，也可以写成0-59/5，意思相同

4. 想要有手动触发按钮，得加上 `on workflow_dispatch`
