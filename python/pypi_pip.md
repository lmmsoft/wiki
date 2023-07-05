# pypi 国内镜像
- https://mirrors.tuna.tsinghua.edu.cn/help/pypi/ 清华源的教程
- https://blog.csdn.net/u011107575/article/details/109901086 其他源
- pip config set global.index-url https://mirrors.aliyun.com/pypi/simple  阿里云源

# pip 命令
> pip install --upgrade --upgrade-strategy eager revChatGPT
> 
--upgrade-strategy with options "eager" and "only-if-needed". 

The default is "only-if-needed". 

Choosing the "eager" option forces installation of the newest available versions of the dependencies.

Ref: https://pip.pypa.io/en/stable/development/architecture/upgrade-options/

# 有趣的库

## 个人信息随机生成
- 姓名，地址，身份证号，手机号等，支持中国（有点像美国地址随机生成器，哈哈）
- https://juejin.cn/post/7064457994540417038
- pip install Faker -i https://pypi.tuna.tsinghua.edu.cn/simple/

