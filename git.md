# git 相关wiki

## Android 发布自动版本号方案 （ gradle + git ）/ git rev-list HEAD/git describe --tags

- https://blog.csdn.net/sinat_31057219/article/details/117562178
- 参考命令

···
# 获取当前分支的提交总次数：
> git rev-list HEAD --count
1042

# 使用commit的哈希值作为版本号也是可以的，获取最新的一次提交的哈希值的前七个字符
> git rev-list HEAD --abbrev-commit --max-count=1
cc450c1de

# 获取最新的一个tag信息
> git describe --tags
v1.9.0-4-gcc450c1de
# v1.9.0 : tag名
# 4 : 打tag之后又有四次提交
# gcc450c1de ：开头 g 为git的缩写，在多种管理工具并存的环境中很有用处
# cc450c1de ： 当前分支最新的commitID前几位
···
