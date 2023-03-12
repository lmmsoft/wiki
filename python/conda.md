# conda

## install by brew
```
brew install --cask anaconda

echo 'export PATH="/opt/homebrew/anaconda3/bin:$PATH"' >> ~/.bash_profile
source ~/.bash_profile 

echo 'export PATH="/opt/homebrew/anaconda3/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```
- 通过brew安装，目录在 /opt/homebrew/anaconda3 这里，仔细看安装日志，能找到这个目录的，乱搜教程，大部分目录都不对
- ref: https://blog.csdn.net/young_kp/article/details/119765752

## 常用的命令
查看conda版本
> $ conda --version

更新conda版本
> $ conda update conda

查看都安装了那些依赖库
> $ conda list

创建新的python环境
> $ conda create --name myenv

并且还可以指定python的版本

> $ conda create -n myenv python=3.7

创建新环境并指定包含的库
> $ conda create -n myenv scipy

并且还可以指定库的版本

> $ conda create -n myenv scipy=0.15.0

复制环境
> $ conda create --name myclone --clone myenv

查看是不是复制成功了

> $ conda info --envs

激活、进入某个环境
> $ source activate myenv

退出环境
> $ source deactivate

删除环境
> $ conda remove --name myenv --all

查看当前的环境列表
> $ conda info --envs or $ conda env list

查看某个环境下安装的库
> $ conda list -n myenv

查找包
> $ conda search XXX

安装包
> $ conda install XXX

更新包
> $ conda update XXX

删除包
> $ conda remove XXX

安装到指定环境
> $ conda install -n myenv XXX

好以上就是Anaconda的安装和基本的使用了。
