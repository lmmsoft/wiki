# crontab

## 定时删除日志
```shell
#!/bin/bashecho "Cleaning old logs..."find /opt/given/logs/ -mtime +30 -name "*.log" -exec rm -rf {} \;echo "Done for cleaning old logs."
```

## ![crontab_format.png](crontab_format.png)