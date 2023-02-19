# ubuntu 相关文档

## How To Set or Change Timezone on Ubuntu 20.04
- https://linuxize.com/post/how-to-set-or-change-timezone-on-ubuntu-20-04/
```
# 先检查
> timedatectl
                      Local time: Sun 2023-02-19 17:30:18 CST
                  Universal time: Sun 2023-02-19 09:30:18 UTC
                        RTC time: Sun 2023-02-19 09:30:18
                       Time zone: Asia/Shanghai (CST, +0800)
       System clock synchronized: yes
systemd-timesyncd.service active: yes
                 RTC in local TZ: no
                 
> cat /etc/timezone
Asia/Shanghai

> ls -l /etc/localtime
lrwxrwxrwx 1 root root 33 Feb 10 04:34 /etc/localtime -> /usr/share/zoneinfo/Asia/Shanghai

# 查看各时区的写法
> timedatectl list-timezones | grep Shanghai
Asia/Shanghai

# 修改
> sudo timedatectl set-timezone America/New_York

# 验证
> timedatectl

```
