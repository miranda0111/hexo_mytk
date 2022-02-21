---
title: 薅小羊毛教程之alexamaster
date: 2022-02-21 11:50:00
updated: 
tags: 羊毛
categories: 脚本
description: 这个网站非常坑，不建议用来作为薅羊毛提现的网站，不过它可以发布浏览网页的任务，从而为站点获取访问量。
keywords:
top_img: https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/羊毛/202202211141248.png
cover: https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/羊毛/202202211141248.png
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

 - [注册账号](https://www.alexamaster.net/)，注意：不要用QQ邮箱
 - 一枚挂机服务器（两个左右够了）

## alexamaster简要说明
![](https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/羊毛/202202211146271.png)
 - 不要企图能获取1\$的报酬，到了1\$就会封号
 - Good Votes在![](https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/羊毛/202202211148002.png)处获取
 - ![](https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/羊毛/202202211148614.png)这里就可以添加网站获取流量了
 - ![](https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/羊毛/202202211149082.png)这里是获取挂机链接
>例如：`https://www.alexamaster.net/ads/autosurf/175410`

## 脚本配置

 - Debian11系统使用puppeteer来实现自动挂机刷积分
 1. 通过nvm安装Node.js
    ```
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/master/install.sh | bash
    ```
    如无错误，请重启服务器，要确保正确安装nvm，请键入：
    ```
    nvm --version
    ```
    既然您已在Debian机器上安装了nvm，要安装最新的Node.js版本，请键入：
    ```
    nvm install node
    ```
    键入以下命令验证Node.js版本：
    ```
    node --version
    ```
 2. 安装Chrome
    下载安装包
    32位：
    ```
    wget https://dl.google.com/linux/direct/google-chrome-stable_current_i386.deb
    ```
    64位：
    ```
    wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
    ```
    键入安装命令
    ```
    #二选一即可
    dpkg -i ./google-chrome-stable_current_i386.deb
    dpkg -i ./google-chrome-stable_current_amd64.deb
    ```
    解决依赖
    ```
    apt-get -f install
    ```
    对于puppeteer，要安装以下依赖
    ```
    apt install libnss3-dev
    apt-get install libxss1
    apt-get install libasound2
    ```
    一定要确保Chrome的安装目录为/opt/google/chrome，这样才能正常运行！
    ```
    #查看Chrome版本信息：
    /opt/google/chrome/chrome --version
    ```
 3. 安装forever
    ```
    npm install forever -g
    ```
 4. fork仓库
    `https://github.com/dxxzst/alexamaster-autosurf.git`修改`/lib/pub.js`文件中的`surURL`为你的`URL`
    
    ![](https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/羊毛/202202211225445.png)

 5. 拉取文件
    ```
    #注意是自己的仓库
    git clone https://github.com/miranda0111/alexamaster-autosurf.git
    cd alexamaster-autosurf
    #安装资源
    npm install
    ```
 6. 启动程序
    ```
    node index.js
    ```
 7. 使用forever命令让它在后台运行（在程序的目录下执行）
    ```
    #启动
    forever start index.js
    #重启
    forever restart index.js
    #关闭
    forever stop index.js
    ```
## 注意事项
 - 一天能用15G的流量
![](https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/羊毛/202202211232816.png)
 - 网站访问量可以设置一天15次
![](https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/羊毛/202202211234438.png)
 - 千万不要超过30000points，不要让网站发现你有能力提现，不要会被block
![](https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/羊毛/202202211239239.png)
 - 注册Alexamaster时挂了美国的代理，直接注册登录后，下次登录不能换其他国家代理，不然会给你这个
![](https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/羊毛/202202211243049.png)

## 参考文章
>https://yangwenqing.com/archives/749/
https://linux265.com/news/3373.html
https://www.jianshu.com/p/6d7323bfaa0c
https://last2win.com/2020/02/07/linux-chrome-bug/