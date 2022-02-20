---
title: 薅小羊毛教程
date: 2022-02-20 16:50:00
updated: 
tags: 羊毛
categories: 脚本
description: 
keywords:
top_img: https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/羊毛/202202201549248.png
cover: https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/羊毛/202202201558810.png
sticky:
toc: true
toc_number: 
toc_style_simple: 
copyright: true
copyright_author:
copyright_author_href:
copyright_url:
copyright_info:
mathjax:
katex:
aplayer:
highlight_shrink:
aside:
---

## 准备材料

 - 一枚vps
 - 青龙面板
 - 脚本仓库

## 安装青龙面板

1. 连接vps 
2. 输入以下命令，如果第一个出现错误，可选用第二个
```
curl -sSL https://get.daocloud.io/docker | sh
```
```
curl -fsSL https://get.docker.com | bash -s docker --mirror Aliyun
```
3. 拉取青龙镜像
```
docker run -dit \
    -v $PWD/ql/config:/ql/config \
    -v $PWD/ql/log:/ql/log \
    -v $PWD/ql/db:/ql/db \
    -v $PWD/ql/repo:/ql/repo \
    -v $PWD/ql/raw:/ql/raw \
    -v $PWD/ql/scripts:/ql/scripts \
    -p 5700:5700 \
    --name qinglong \
    --hostname qinglong \
    --restart unless-stopped \
    whyour/qinglong:latest
```
4. 登录青龙面板：`http://ip:5700`，若为ipv6地址，输入`http://[ipv6地址]:5700`，登录之后安装面板，消息推送可参考本博客其他文章。

## 拉库命令

 - 可以参考这些仓库的
>[https://github.com/Yiov/wool.git](https://github.com/Yiov/wool.git)
>[https://gitee.com/xiecoll/radish-script.git](https://gitee.com/xiecoll/radish-script.git)
>[https://gitee.com/sitoi/dailycheckin.git](https://gitee.com/sitoi/dailycheckin.git)

 - 简单说明： 青龙面板 => 定时任务 => 新建任务
```
ql repo https://github.com/Yiov/wool.git "" "COOKIE"
```
  ![](https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/羊毛/202202201527605.png)

## 青龙命令

1. 查看容器
```
docker ps -a
```
2. 重启容器
```
docker restart qinglong
```
3. 更新青龙
```
docker exec -it qinglong ql update
```
4. 重启青龙
```
docker exec -it qinglong ql restart
```
5. 拉取自定义仓库
```
docker exec -it qinglong ql repo https://github.com/whyour/hundun.git "quanx" "tokens|caiyun|didi|donate|fold|Env"
```
6. 拉取单个脚本
```
docker exec -it qinglong ql raw https://raw.githubusercontent.com/Yiov/wool/main/xmsb.py
```
7. 删除7天前的所有日志
```
docker exec -it qinglong ql rmlog 7
```
8. 通知测试
```
docker exec -it qinglong notify test test
```
9.  立即执行脚本
```
docker exec -it qinglong task test.js now
```
10. 并行执行脚本
```
docker exec -it qinglong task test.js conc
```
11. 启动青龙bot 前提你已配置好青龙BOT
```
docker exec -it qinglong ql bot
```
12. 查看账号和密码
```
docker exec -it qinglong cat /ql/config/auth.json
```
ps：拉取仓库命令可以在青龙面板中定时任务那里运行