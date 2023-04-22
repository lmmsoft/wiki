# 微信的各种资料

# Part1: 微信使用技巧
- 手机号，已经被其他人注册，怎么办？
  - 登陆后，需要旧手机扫码or两个好友帮忙验证，微信号不是自己的，做不了
  - 正确的方法是用新手机号注册，注册完提示已有微信，选择“不是我的，继续注册新微信”
  - 正常情况下，新微信可以直接注册，如果还是不行的话
  - 1. 找客服申诉，4小时候一般可以解决 https://zhuanlan.zhihu.com/p/561114796
  - 2. 微信官方人工电话：4006 700 700 客服电话，然后发下移动掌上营业厅的截图，24h之后即可
- 微信网页版
  - 先用文件传输助手登陆 https://filehelper.weixin.qq.com/ 传个文件
  - 再去登录网页版 https://wx.qq.com/
  - 亲测：文件传输助手都能登陆
  - 老号码，2013年注册的，可以登陆网页版
  - 新号码，2022年重新注册的，不能登陆网页版

# Part2： 微信文章爬虫项目汇总
- https://github.com/chyroc/WechatSogou

# Part3: 微信公众号后端开发

- 官方接入文档
  - https://developers.weixin.qq.com/doc/offiaccount/Basic_Information/Access_Overview.html
- wechatpy库
  - https://wechatpy.readthedocs.io/zh_CN/stable/quickstart.html 

- https://github.com/littlecodersh/itchatmp
  - itchat的兄弟库
  - python
  - 1.4k star 六年没更新 
  
# Part4: 微信聊天相关开发
- https://github.com/littlecodersh/itchat
  - 27k star
  - python 需要能登陆网页版
  - 文档 https://itchat.readthedocs.io/zh/latest/#_16
- https://github.com/why2lyj/ItChat-UOS
  - fork自上个项目的复刻版
- https://gitee.com/lihaitao/ItChat/
  - 据说上面的复刻版也不能用了，这个也是和复刻版本同样的技术，可惜了
- https://github.com/liuwons/wxBot
  - 5.3k star
  - python2 网页版 六年没更新了 
- https://github.com/wechaty/wechaty
- https://github.com/wechaty/puppet-wechat
  - wechaty 家族

# Part5: 微信 telegram项目
- Telegram bot <> EFB <> 微信网页版 <> 微信
- 好处
  - 直接数据上云
  - 可以同时再多台手机、电脑、iPad上面登录TG
  - 一个TG号上登录无数个微信，可以同时管理使用
  - 定时发送

## 项目
- https://github.com/ehForwarderBot/ehForwarderBot
  - https://ehforwarderbot.readthedocs.io/en/latest/
## 教学文章
- https://jkboy.com/archives/5128.html
- https://specialhua.top/20190910/cid=8.html (这篇不错，教你怎么的用docker搞的)
- https://github.com/talkgo/night/issues/137
- https://www.appinn.com/efb-tutorial-with-docker/

## Part6: 登陆网页版微信
- 之前扫码网页登陆，总是提示：
```
<error>
<ret>1203</ret>
<message>由于安全原因，此微信号不能使用网页版微信。你可以使用 Windows 版微信或 Mac 版微信登录。Windows 版微信下载地址：https://pc.weixin.qq.com  Mac 版微信下载地址：https://mac.weixin.qq.com</message>
</error>
```

- 通过以下方法尝试真的可以了

微信扫码 https://filehelper.weixin.qq.com/ 随便传个文件

然后再去登录 
- https://wx.qq.com/
- https://wx2.qq.com/

消息来自：https://hostloc.com/thread-946732-1-2.html

马甲亲测真的可以！

参考Chrome(辅助登陆网页版微信) https://github.com/adamyi/wechrome

## Part7: 导出微信聊天记录
- 楼月工具
  - 从安卓中导出，需要 root 手机，感觉是 hack 了手机里的数据，有点危险
  - http://www.winwin7.com/soft/20482.html
- 开源工具 iOS
  - https://github.com/BlueMatthew/WechatExporter
  - 原理： icloud 备份，不加密，可以拿到手机原始数据，解析出来即可！
  - 有 Mac APP，方便使用
- 开源工具 iOS + python
  - python 写的，搞二次开发方便
  - https://github.com/12425/wechat-exporter
- 开源工具 iOS 备份
  - 这里有介绍解密的原理
  - https://github.com/allen1881996/WeChat-Data-Analysis
- 开源工具 Android
  - 安卓数据是加密的，以前需要用IMEI解密，现在秘钥固定
  - https://github.com/ppwwyyxx/wechat-dump
- 文档介绍 Android 文字+资源文件
  - https://blog.greycode.top/posts/android-wechat-bak/
  - https://github.com/greycodee/wechat-backup  (配套代码)
- 其他工具
  - 这个帖子里有较多付费工具的汇总
  - https://github.com/BlueMatthew/WechatExporter/issues/120
- 知乎汇总贴，免费的，付费的，很全
  - https://zhuanlan.zhihu.com/p/212901830
