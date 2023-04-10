# 保存和 mac 系统相关的操作文档

## mac电脑访达finder如何按照照片的拍摄时间排序？
- my blog post link:  https://lmmsoft.github.io/mac_finder_sort_photos_by_taken_time/ 
- 结论，不行，必须通过第三方软件
- 推荐个免费的小工具：
  - 官方网站： https://www.qdev.de/?location=mac/exifrenamer
  - 下载地址： https://www.qdev.de/download.php?file=ExifRenamer.dmg
- 特性：可以自定义文件名格式，比如我是 [时间+原始文件名]，然后批量重命名

## NTFS for Mac
- 如果是新买的移动硬盘，建议直接格式化成 ExFAT 格式， Windows/Mac 都支持，可以在 Mac 机器上格 只读的 NTFS 盘，不需要重启电脑
  - 参考希捷的文档 https://www.seagate.com/cn/zh/support/kb/how-to-format-your-drive-exfat-on-macos-big-sur-and-later/ 
- 如果是旧磁盘，不方便转换格式，就要安装软件了
  - 知乎帖子 https://www.zhihu.com/question/412132741
  - 各种方法似乎都需要重启电脑
  - 原生命令解决的原生的命令解决  https://www.zhihu.com/question/412132741/answer/1386080254
  - 免费的 Omi NTFS ， x86的mac可以直接用， M1/M2 的需要重启，进入恢复模式，给系统插件授权
- 各种 win/mac 磁盘格式优劣对比
  - https://www.seagate.com/cn/zh/support/kb/how-to-format-your-hard-drive-220151en/?language=zh-cn
