---
title: PicGo+Gitee部署免费图床教程
date: 2022-02-03 22:40:00
updated: 2022-02-03 22:40:00
tags: 图床
categories: hexo
description: 部署个人图床，为自己的博客提供稳定的图片来源
keywords:
top_img: https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/PicGo教程/20220203203008.png
cover: https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/PicGo教程/20220203203008.png
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

>说明：PicGo+Gitee搭建图床不需要任何代码操作，新手不需要头盔直接上路。

### 准备材料

 - [nodejs](http://nodejs.cn/)
 - [PicGo--Github](https://github.com/Molunerfinn/PicGo) or [PicGo官网](https://molunerfinn.com/PicGo/)
 - [Gitee帐号](https://gitee.com/)

### 建立gitee图床仓库

 - 点击右上角的+号，新建仓库，按照图示内容打✔
    ![](https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/PicGo教程/20220203204145.png)

 - 点击右上角的头像，在左侧边栏，找到`私人令牌`
    ![](https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/PicGo教程/20220203204401.png)

 - 新建`私人令牌`，按照下列图示操作即可生成`token`，一定要复制保存好，等下要用
    ![](https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/PicGo教程/20220203204415.png)
    ![](https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/PicGo教程/20220203204422.png)
    ![](https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/PicGo教程/20220203204431.png)

### PicGo软件设置

 - 打开软件，点击`插件设置`，安装`gitee-uploader`
    ![](https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/PicGo教程/20220203204827.png)

 - 点击`图床设置`，点击`gitee`  
   repo：用户名/仓库名称；
   branch：填master
   token：填私人令牌生成的一串密钥
   path：（下图说明）
   customPath：提交消息，默认即可
   customURL： 可不填，这个会影响生成图片的url代码
    ![](https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/PicGo教程/20220203205159.png)

### 部署完毕

 - 截图或复制一张图片在`上传区`，点击`剪贴板图片`即可快速上传图片
    ![](https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/PicGo教程/20220203210100.png)
 - 打开gitee可以见到文件夹生成
    ![](https://gitee.com/miranda0111/hexo-mytk-pic-go/raw/master/PicGo教程/20220203210239.png)
 - 部署成功！！！