# 保存和 mac 系统相关的操作文档

## 1. Mac 2k 屏幕，字体发飘问题
- 使用 BetterDisplay
  - 下载 https://github.com/waydabber/BetterDisplay
  - 按照教程 https://github.com/waydabber/BetterDisplay/wiki/Fully-scalable-HiDPI-desktop#setting-up-native-smooth-scaling
  - 3440 * 1920 带鱼屏，2K的， 强制开启 HiDPI
  - 开启后发飘消失了，但是字体还是有点糊

## 2. 检查软件是否支持 ARM 架构的网站
- https://isapplesiliconready.com/

## 3. Mac双屏显示时，如何把dock固定在主屏幕？
- https://www.zhihu.com/question/25277698
- 鼠标放在需要固定的显示器底部两秒 (亲测好用，Ventura v13.3.1, 但这个功能设计得太脑残了，之前dock程序坞乱飘，应该就是这个原因，我左下角有锁屏触发角，导致dock总是飘到左边屏幕上  ) 

## 4. mac电脑访达finder如何按照照片的拍摄时间排序？
- my blog post link:  https://lmmsoft.github.io/mac_finder_sort_photos_by_taken_time/ 
- 结论，不行，必须通过第三方软件
- 推荐个免费的小工具：
  - 官方网站： https://www.qdev.de/?location=mac/exifrenamer
  - 下载地址： https://www.qdev.de/download.php?file=ExifRenamer.dmg
- 特性：可以自定义文件名格式，比如我是 [时间+原始文件名]，然后批量重命名

## 5. NTFS for Mac
- 如果是新买的移动硬盘，建议直接格式化成 ExFAT 格式， Windows/Mac 都支持，可以在 Mac 机器上格 只读的 NTFS 盘，不需要重启电脑
  - 参考希捷的文档 https://www.seagate.com/cn/zh/support/kb/how-to-format-your-drive-exfat-on-macos-big-sur-and-later/ 
- 如果是旧磁盘，不方便转换格式，就要安装软件了
  - 知乎帖子 https://www.zhihu.com/question/412132741
  - 各种方法似乎都需要重启电脑
  - 原生命令解决的原生的命令解决  https://www.zhihu.com/question/412132741/answer/1386080254
  - 免费的 Omi NTFS ， x86的mac可以直接用， M1/M2 的需要重启，进入恢复模式，给系统插件授权
  - 免费的 brew 安装方法 https://blog.csdn.net/qq_36071963/article/details/126052367
  - 我有个旧的 paragon 版本太老，不支持 M1，新的要付费
  - 国产的 xx，SEO 做的很好，但是要付费
- 各种 win/mac 磁盘格式优劣对比
  - https://www.seagate.com/cn/zh/support/kb/how-to-format-your-hard-drive-220151en/?language=zh-cn

## 6. 删除文件之后，剩余空间没有增加的问题
- 时间机器的问题，可以删除快照，系统也会根据空间自动删除快照
  - 参考 https://zhuanlan.zhihu.com/p/106320280
```
输入：sudo tmutil listlocalsnapshots /
输入密码+回车 (注意后面 / 要的，是查询目录)

系统会列出文件的名称，主要是日期名，eg:

Snapshots for disk /:
com.apple.TimeMachine.2023-06-11-010732.local
com.apple.TimeMachine.2023-06-11-020925.local
com.apple.TimeMachine.2023-06-11-040319.local


输入：tmutil deletelocalsnapshots 日期名
把不需要的文件都删除后，就可以恢复可用空间了。

eg:
sudo tmutil deletelocalsnapshots 2023-06-11-010732
Deleted local snapshot '2023-06-11-010732'
```

## 7. 查找大目录，清理
> cd Library
> sudo du -sh *
摁下回车，输入密码。
会列出每个目录大小，可以一层层排查

> sudo du -sh *l
> sudo du -sh *

或者
执行open Library,然后调整目录展示位列表展示，再摁下command +J，
在弹出的对话框里，选择计算所有大小。然后找到特别大的没啥样的，就删除掉。
![image](https://github.com/lmmsoft/wiki/assets/1109198/8a3573d4-57e7-423f-b369-cb18bf9ea43f)
