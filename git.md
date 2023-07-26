# 本文档记录 git 相关的常见操作命令


# 解决 git status 显示中文文件名为乱码
> git config --global core.quotepath false

如果运行上述命令弹出提示： 
> error: could not lock config file /Users/lmm333/.gitconfig: File exists

则可以手动编辑配置文件
> vim /Users/lmm333/.gitconfig

在 [core] 下增加 quotepath = false

```
[core]
quotepath = false
```

原理：core.quotepath 设为 false 的话，就不会对 0x80 以上的字符进行quote, 故中文可以正常显示, 此时, 如果你查看 git 的配置文件, 就会发现在 [core] 的分类下多处一条 quotepath = false的选项.

# 清理本地分支
清理本地 tracking branches not on the remote
> git remote prune origin 

# 删除远程分支
> git push origin :branch-name

# 查看用户名
```shell
git config user.email
git config --global user.email
git config --local user.email
```

# 设置用户名

```shell
git config --global user.name "name"
git config --global user.email "a@b.com"

git config --local user.name "name"
git config --local user.email "a@b.com"
```

# 不同目录设置不同用户名
- 查看根目录是否有 .gitconfig 文件，没有创建一个

```shell
ls -a ~/
cat ~/.gitconfig
```

- Since git 2.13, it is possible to solve this using newly introduced Conditional includes.
- An example:
- Global config ~/.gitconfig
```
[user]
    name = John Doe
    email = john@doe.tld

[includeIf "gitdir:~/work/"]
    path = ~/work/.gitconfig
```

- Work specific config ~/work/.gitconfig
```
[user]
    name = Work Name
    email = john.doe@company.tld
```
- Remember that [includeIf...] should follows default [user] at the top.


## 参考文章
- https://www.freecodecamp.org/news/how-to-handle-multiple-git-configurations-in-one-machine/

# Android 发布自动版本号方案 （ gradle + git ）/ git rev-list HEAD/git describe --tags

## 参考文章
- https://blog.csdn.net/sinat_31057219/article/details/117562178
- https://blog.csdn.net/weixin_34062329/article/details/92064079

## 参考命令

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
