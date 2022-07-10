# trojan 工具

## trojan多用户管理部署程序
- https://github.com/Jrohy/trojan
- 有web工具

## 使用方法
- 按照 gihhub readme 操作

## 问题，证书过期
- 此服务器无法证明其所在网域是 xxx.westus2.cloudapp.azure.com；其安全证书已在 17 天前过期。出现此问题的原因可能是配置有误，或是有攻击者拦截您的连接。计算机的时钟目前已设为 2022年3月8日星期二，请问是否正确？如果不正确，请更正系统的时钟，然后刷新此页面。
- 证书续期，正常是有定时任务的
- 可以通过 crotab -l 查看
> 0 19 * * * systemctl stop trojan-web; "/root/.acme.sh"/acme.sh --cron --home "/root/.acme.sh" > /dev/null; systemctl start trojan-web

- 但是有时候 定时任务会出问题，需要手动申请证书
```
# 先进入容器
docker exec -it trojan bash

# 再申请证书
systemctl stop trojan-web
acme.sh --renew-all --force
systemctl start trojan-web

# 最后退出，并重启容器(2022-03-08 上面重启了还不行，然后重启容器就好了)
exit
docker restart trojan
```
