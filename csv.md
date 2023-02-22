# 存放 csv 相关问题

## csv 编码问题
- 现象: python 使用 utf8 编码 保存 中文csv 文件，PyChram/文本编辑器/Numbers都能正常打开，但是Excel打开是乱码，钉钉预览是乱码，钉钉编辑是中文
- 解法: python 使用 utf8-sig 编码保存，会带上BOM
- 原因：
### utf-8 与 utf-8-sig 有什么区别？
utf-8 以字节为编码单元，它的字节顺序在所有系统中都是一样的，没有字节序问题，也因此它实际上并不需要 BOM；

uft-8-sig 中 sig 全拼为 signature，即带有签名的 utf-8（UTF-8 with BOM）；

BOM 全称 ByteOrder Mark，字节顺序标记，出现在文本文件头部，Unicode编码标准中用于标识文件是采用哪种格式的编码。

### 为什么写入 csv 文件要用 utf-8-sig 编码？
Excel 在读取 csv 文件的时候是通过读取文件头上的 BOM 来识别编码的，如果文件头无 BOM 信息，则默认按照 Unicode 编码读取。

当我们使用 utf-8 编码来生成 csv 文件的时候，并没有生成 BOM 信息，Excel 就会自动按照 Unicode 编码读取，就会出现乱码问题了。

### 为什么写入 txt 文件要用 utf-8 编码？
在写入 txt 文件时，Windows 会默认转码成 gbk，遇到某些 gbk 不支持的字符就会报错，在打开文件时就声明编码方式为 utf-8 就能避免这个错误。

- 参考：https://blog.csdn.net/qq_36759224/article/details/104417871
