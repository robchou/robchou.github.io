---
title: macOS High Sierra搭建rtmp服务器
date: 2017-11-26 22:58:40
tags:
---

### 系统环境
```bash
macOS High Sierra 10.13.6
```

### 安装nginx
```bash
brew tap homebrew/nginx
brew install nginx-full --with-rtmp-module
```

### 修改nginx配置文件

```bash
## /usr/local/etc/nginx/nginx.conf
rtmp {
   server {
        #监听的端口号,rtmp协议的默认端口号是1935
        listen 1935;
        #直播流配置,访问路径是rtmplive
        application rtmplive {
              #开启实时
              live on;
              #为rtmp引擎设置最大连接数.默认为off
              max_connections 1024;
              #不记录数据
             record off;
        }
    }
}

```

### 启动nginx及重新加载配置文件
```bash
nginx
nginx -s reload
```

### 测试nginx
```bash
http://localhost:8080
```

### FFMpeg推流
```bash
ffmpeg -re -i ./sintel.h264 -vcodec libx264 -vprofile baseline -acodec aac -ar 44100 -strict -2 -ac 1 -f flv -s 640x360 -q 10 rtmp://localhost:1935/hls/test
```
### ffplay查看
```bash
ffplay rtmp://localhost:1935/hls/test
```

### 后记

macOS中有一个坑，需要关闭防火墙，否则可能出现推流不成功
