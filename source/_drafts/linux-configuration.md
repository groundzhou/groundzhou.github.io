---
title: Linux系统及软件常用配置
description: 记录日常使用Linux及部分软件时的常用配置。
tags: Linux
---

# 1. 硬盘挂载

配置文件：`/etc/fstab`

`UUID=3640EF3040EEF611 /home/ground/share ntfs-3g uid=ground,gid=ground,hide_hid_files,dmask=022,fmask=033 0 0`

# 2. 科学上网

## 2.1 服务器端

## 2.2 客户端

软件：shadowsocks-libev

配置文件位置：`/etc/shadowsocks/config.json`

```js
{
    "server":"server_ip",
    "server_port":2020,
    "local_address": "127.0.0.1",
    "local_port":1080,
    "password":"password",
    "timeout":300,
    "method":"chacha20-ietf-poly1305",
    "fast_open": false,
    "workers": 1,
    "prefer_ipv6": false
}
```

启动命令：`ss-local -c /etc/shadowsocks/config.json`


