# 群晖相关内容

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

