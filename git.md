# git 相关wiki

## 解决 git status 显示中文文件名为乱码
> git config --global core.quotepath false

## 删除远程分支
> git push origin :branch-name

# 设置用户名

```shell
git config --global user.name "name"
git config --global user.email "a@b.com"

git config --local user.name "name"
git config --local user.email "a@b.com"
```
## Android 发布自动版本号方案 （ gradle + git ）/ git rev-list HEAD/git describe --tags

### 参考文章
- https://blog.csdn.net/sinat_31057219/article/details/117562178
- https://blog.csdn.net/weixin_34062329/article/details/92064079

### 参考命令

```
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
```
