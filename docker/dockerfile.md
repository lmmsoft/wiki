# 本文存放 dockerfile 相关的实践

## 时区
```
For: FROM python:3.8.1-buster

# Add crontab file in the cron directory
ADD crontabfile /etc/cron.d/watcher-cron

# Give execution rights on the cron job
# Create the log file to be able to run tail

RUN apt-get update \
    && apt-get -y install cron openssl \
    && cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
    && echo 'Asia/Shanghai' >/etc/timezone
```

```
for FROM python:3-alpine

RUN sed -i "s|dl-cdn.alpinelinux.org|mirrors.tuna.tsinghua.edu.cn|g" /etc/apk/repositories && \
    apk add -U tzdata make && \
    cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo "Asia/Shanghai" > /etc/timezone && \
    apk add -U -t xxbuild gcc musl-dev g++ libffi-dev openssl-dev && \
    pip install -r /requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple && \
    apk del xxbuild && \
    rm -rf /var/cache/apk/*

RUN apk add -U tzdata && \
    cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo "Asia/Shanghai" > /etc/timezone
```

```
For: FROM python:3.12

# Set the timezone to Shanghai
ENV TZ=Asia/Shanghai

# Use the system's package manager to install tzdata package
RUN apt-get update && apt-get install -y --no-install-recommends tzdata && \
    ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && \
    echo $TZ > /etc/timezone

# Copy the Python requirements file into the container at /app
COPY requirements.txt /app/
```

## RUN 命令
- 在同一个RUN中 yum install 命令之后加上 yum clean all
```
RUN yum install -y git \
    && yum clean all
```

- 在同一个RUN中 apt-get install 请加上--no-install-recommends参数 命令之后加上 apt-get clean && rm -rf /var/lib/apt/lists/*
```
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        git \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* 
```

- 可能会通过COPY/wget/git clone下载一些文件，这些文件在使用完后建议在同一个RUN中删除（deb文件 rpm文件 编译后的源码文件 requirements.txt 等）
```
RUN git clone http://xxx.git \
    && bash xxx/ext/python/install.sh \
    && rm -rf xxx
```
