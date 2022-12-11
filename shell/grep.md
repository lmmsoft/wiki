# grep 相关命令

# 搜索单个目录下面的字符串

- 搜索目录但不搜索在.目录下的.svg目录中包含“string”字符串的文件

> grep -E "string"  . -R  --exclude-dir=.svg123
