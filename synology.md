# 群晖相关内容

# 反向代理设置
- 控制面板 - 应用程序门户 -反向代理服务器 这里可以设置反向代理，比如
  - 参考 https://post.smzdm.com/p/apvp3kl2/
  - xxx.i234.me:2999 代理到 192.168.1.90:3000 上 (可以转发到内网其他服务器)
  - a.xxx.i234.me:2999 代理到 localhost:3000 上 (可以做二级域名)
  - a.xxx.i234.me 代理到 localhost:3000 上 (这是80端口的二级域名，不成功是因为运营商屏蔽了80端口)
- 上述可视化编辑，实际修改的是 /usr/syno/etc/www 目录下的 ReverseProxy.json 文件

# 安装pip3
- https://blog.csdn.net/xiaokai1999/article/details/121070867


```shell

part1: 安装配置Python和pip

在套件中心找到python3并且下载安装
在控制面板->终端机和SNMP中启用SSH功能

安装pip
$ sudo su
$ wget https://bootstrap.pypa.io/get-pip.py
$ python3 get-pip.py


part2: 创建软链

全局查找pip

# find / -name pip2*
# find / -name pip3*

输出

# find / -name pip2*
/volume1/@appstore/python/bin/pip2
/volume1/@appstore/python/bin/pip2.7
/volume1/@appstore/gateone/env/bin/pip2
/volume1/@appstore/gateone/env/bin/pip2.7

ash-4.3# find / -name pip3*
/volume1/@appstore/py3k/usr/local/bin/pip3
/volume1/@appstore/py3k/usr/local/bin/pip3.8

创建软链

ln -s /volume1/@appstore/python/bin/pip2 /usr/bin/pip2
ln -s /volume1/@appstore/py3k/usr/local/bin/pip3 /usr/bin/pip3

# 执行pip -V 可看到输出信息

# pip2 -V
pip 20.0.2 from /var/packages/python/target/lib/python2.7/site-packages/pip (python 2.7)

pip3 -V
pip 22.3.1 from /var/packages/py3k/target/usr/local/lib/python3.8/site-packages/pip (python 3.8)
```

## lxqt, 基于web的 Chrome + terminal
- 项目官网，lightweight QT desktop environment
  - https://lxqt-project.org/
  - 官方更新页 https://lxqt-project.org/releases/
    - 最近更新是 2022-11 的 LXQt 1.2.0
- 群晖官网插件, 6.2才有，升级到7.1就没啦
  - 群晖介绍页 https://www.synology.cn/zh-cn/dsm/packages/Docker-LXQt?os_ver=6.2&search=lxqt
  - 群晖更新历史页 https://www.synology.cn/zh-cn/releaseNote/Docker-LXQt?model=RS18017xs%2B
    - 最近一次更新是 LXQT 0.10.0-0015 (2021-12-07) 0.10.0 是非常老的lxqt版本，0015应该是小更新了15次，但大版本没变化
  - LXQt 是一款用部分 Razor-qt 和 LXDE 组件以 QT 构建的桌面实用程序。它配备了基本的图形用户界面，让用户能够利用特定的操作系统功能，如网页浏览。它有大量的功能并可通过 Docker 在 Synology NAS 上运行。
- 安装方法：套件中心，一键下载安装即可
![image](https://user-images.githubusercontent.com/1109198/226795469-1219fc36-e3be-490f-bd2a-0174beba94c8.png)
- 使用方法 默认LXQT使用的是NAS的30006端口，也可以到Docker的容器配置中查看
  - ip:30006
- Chrome是v55，很旧的版本了，现在已经到v110了

## oldiy大神的 chrome浏览器
- 容器 里搜 oldiy， 有很多好东西
- 浏览器有火狐和Chrome，据说火狐更稳定
- chrome 是 v72, 飞书要求最低v58,lxqt太老了，不行
- 用UI创建容器的教程：https://www.toutiao.com/article/7109476620066423336/
- 大神原版的加密码教程：《给Docker镜像运行的chrome镜像添加访问密码》 https://odcn.top/2019/03/09/2902/
