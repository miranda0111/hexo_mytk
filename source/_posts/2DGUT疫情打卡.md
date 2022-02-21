---
title: 东莞理工学院-疫情打卡-脚本及使用方法分享
date: 2022-01-30 20:16:51
updated: 2022-02-01 20:33:00
tags: DGUT疫情打卡
categories: 脚本
description: 使用Github Actions进行自动打卡并提交，如果不会弄可以联系我哦😎
keywords:
top_img: https://github.com/miranda0111/hexo-mytk-pic-go/raw/master/DGUT/20220203213955.png
cover: https://github.com/miranda0111/hexo-mytk-pic-go/raw/master/DGUT/20220203213955.png
sticky: 1
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

## [疫情打卡链接](https://yqfk-daka.dgut.edu.cn/)

## 免责申明
    
- 该教程仅供学习使用，严禁用于商业用途，由此造成的一切后果，本人概不负责。

## 准备材料

- [GitHub帐号](https://github.com) 
- [server酱](https://sct.ftqq.com/)

## 食用方法
1. 打开[GitHub官网](https://github.com) ，注册一个GitHub账号，按照提示完成注册
   ![sign up](https://github.com/miranda0111/hexo-mytk-pic-go/raw/master/DGUT/Ha9b2f3c156bb4a5ba8e2d8b0c14d3226a.png) 

2. 打开[DGUT_Auto_Report脚本仓库](https://github.com/Bertramoon/DGUT_Auto_Report)，点击`Star`&`Fork` ![fork](https://github.com/miranda0111/hexo-mytk-pic-go/raw/master/DGUT/H1fe9df80a4ff4fd09408a3e5f665a711E.png)

3. 打开[server酱官网](https://sct.ftqq.com/)，登入![server酱官网](https://github.com/miranda0111/hexo-mytk-pic-go/raw/master/DGUT/Ha414f9f751a148219aaae424d7b664fcG.png) 记录你的sendkey![记录你的sendkey](https://github.com/miranda0111/hexo-mytk-pic-go/raw/master/DGUT/H87f5f0a1c06942699e5a27b0919baab2v.png) 点击上方`消息通道`可以选择以下这些作为打卡成功的通知渠道，个人推荐使用`方糖服务号（即微信公众号）`![方糖服务号](https://github.com/miranda0111/hexo-mytk-pic-go/raw/master/DGUT/H186ecd73a2854439ad2fba24194eee1a2.png) 

4. 添加环境变量配置：回到仓库点击`Settings`=>`Secrets`=>`Actions`然后点击`New repository secrets`在里面里面添加3个环境变量![环境变量](https://github.com/miranda0111/hexo-mytk-pic-go/raw/master/DGUT/Hbbb7056184d14ad2a84533646830b715O.png)![环境变量](https://github.com/miranda0111/hexo-mytk-pic-go/raw/master/DGUT/Hc0b81c919df34e6fab54161a96b9e472I.png)
   
5. 环境变量示例
   
 |   | Name | Value |
 | - | - | - |
 |1| `USERNAME` | 202041231212|
 |2| `PASSWORD` | 密码 |
 |3| `SERVER_KEY`| -K SCT10*80T2xdNVRuTk*****cMmKQgWaJE |
 |4| `PAT`      | PAT申请的key（用于同步，最后补充） |

- （注意，sendkey前需要加上-K）

>例子

![example](https://github.com/miranda0111/hexo-mytk-pic-go/raw/master/DGUT/H70eafc7e5bc2421c92749915f9878313e.png)

## 手动运行一次

1. 点击`Actions`=>`Enable workflows`=> “莞工防控疫情打卡”，在右边找到`run workflows`即可
![111](https://github.com/miranda0111/hexo-mytk-pic-go/raw/master/DGUT/HVXImoLlkNyu6Mr.png)
2. 然后star ⭐星标本仓库（自己的）即可运行或者修改一下`README.md`文件的内容，然后就能自动运行一次
![111](https://github.com/miranda0111/hexo-mytk-pic-go/raw/master/DGUT/Hde2a1891204c4caf8371ac28a9915dc5E.png)

## 修改打卡时间
>说明

<img src="https://github.com/miranda0111/hexo-mytk-pic-go/raw/master/DGUT/H00868c0ede0b4c49a9da8bcfee8fb8c5g.png"/>
<img src="https://github.com/miranda0111/hexo-mytk-pic-go/raw/master/DGUT/H21f62be667b243bbbacf172c264e5c5em.png"/>
<img src="https://github.com/miranda0111/hexo-mytk-pic-go/raw/master/DGUT/H8e31285f1d804b4692637281efaa257fT.png"/>
<img src="https://github.com/miranda0111/hexo-mytk-pic-go/raw/master/DGUT/H2f31cad22d214467a9d14bfc36ec9186D.png"/>
<img src="https://github.com/miranda0111/hexo-mytk-pic-go/raw/master/DGUT/H7d65f5973d0f44e4a1e30716ac55d38dA.png"/>

## 启用自动同步功能

- 若要使用自动同步功能，请在`Secrets`处添加`PAT`如何申请PAT[点击这里](https://github.com/miranda0111/JDscret/blob/main/backup/reposync.md)此处借用jdsecret的同步进行说明，感谢搬运 大佬的支持！

## 其他

- 不懂得使用请加b站私聊:[398055394](https://space.bilibili.com/398055394?spm_id_from=333.1007.0.0)
- 可以私聊本人代为挂载。