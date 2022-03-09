# SSH

## 基本步骤
```shell
ssh-keygen
cat .ssh/id_rsa.pub # 显示新生成的公钥

vim authorized_keys # 在远程机上编辑
添加上述 id_rsa.pub到最后

# 次数可以登录了
ssh root@10.67.154.166 -p 52401 # 走隧道
```

## 在跳板机上建隧道
ssh -CNfgL 52401:10.236.24.1:22 root@10.236.24.1