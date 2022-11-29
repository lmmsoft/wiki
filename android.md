# Android Related Materials

# Tinker: 安卓热补丁方案
- https://github.com/Tencent/tinker
- https://github.com/Tencent/tinker/wiki
- 官方技术分享
  - https://github.com/WeMobileDev/article/blob/master/Tinker%EF%BC%9A%E6%8A%80%E6%9C%AF%E7%9A%84%E5%88%9D%E5%BF%83%E4%B8%8E%E5%9D%9A%E6%8C%81.md
  - https://mp.weixin.qq.com/s?__biz=MzAwNDY1ODY2OQ==&mid=2649286384&idx=1&sn=f1aff31d6a567674759be476bcd12549&scene=4#wechat_redirect


# Run Linux on Android
- AidLux 带UI的
  - https://github.com/aidlearning/AidLearning-FrameWork
  - with GUI
  - 华人项目，国内应用商店可下载
  - 中文文档 https://docs.aidlux.com/#/
  - 使用问题：
    - 兼容性较差
    - 鸿蒙3系统不支持，32位机器不支持，nexus6是32位，用不了
- Termux 终端仿真
  - https://github.com/termux/termux-app  17k star
  - 生态最好 https://github.com/termux/termux-packages 完美支持 Python、 PHP、 Ruby、 Nodejs、 MySQL等
  - 中文文档 https://termux.dev/cn/index.html (非常烂，感觉是机翻的)
  - 清华/中科大有源，可以半可视化配置 https://mirrors.tuna.tsinghua.edu.cn/help/termux/
  - 2020年之后，Android >= 7，放弃5和6了
  - 蓝牙键盘，快捷键，ssh等等
  - 不需要root(于是也不能用1024以内的端口，有一定限制)，兼容性好
  - 参考文档
    - 详细 https://www.freebuf.com/geek/170510.html
    - https://zhuanlan.zhihu.com/p/32338964
- UserLAnd
  - https://github.com/CypherpunkArmory/UserLAnd
  - 上次是21-10发布Release，有一年多了
  - 可以下载不同的源，但是要翻墙！
  - 不需要 root，需要翻墙！
- Linux Deploy
  - https://github.com/meefik/linuxdeploy
  - 上次发布，2020-02
  - 需要先root

# My Device
- Huawei P20
  - HarmonyOS 2.0 == Android 11(2021.12.1)
  - 6G/128G 2244*1080
- Motorola Nexus 6(2014)
  - Android 7.1.1(2017.10.5)
  - 3G/32G 2560x1440 493ppi
  - Qualcomm Snapdragon 805 4Core 2.7GHz
- Redmi 4X
  - Android 7.1.2(2018.10.1)
  - 3G/32G
  - 8Core 1.4GHz

# 小知识
- tinker: 微信开源的Android热修复框架
- ART（Android Runtime）是Android在4.4版本中引入的新虚拟机环境，在5.0版本正式取代了Dalvik VM
  
