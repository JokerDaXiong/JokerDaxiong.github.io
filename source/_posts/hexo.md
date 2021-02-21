---
title: hexo+Github搭建静态个人博客搭建
author: JokerDaxiong
avatar: https://cdn.jsdelivr.net/gh/JokerDaxiong/JokerDaxiong.github.io@main/images/avatar.png
authorLink: jokerdig.com
authorAbout: 一个代码小白
authorDesc: 
categories: 干货
date: 2021-2-21 1:07:01
comments: true
tags: 
 - hexo
 - github
 - 博客搭建
keywords: 静态博客搭建
description: hexo博客搭建
photos: https://jokerdig.com
---

## hexo+Github搭建静态个人博客搭建


1. 下载nodeJS：<https://nodejs.org/en/>

2. 安装 一键式

3.  cmd >查询node和npm的版本，确认安装成功

   ```yml
   node-v  //查询node版本
   npm-v  //查询npm版本
   ```

4. 使用npm安装cnpm（国内使用淘宝镜像加速下载）

   ```yml
   npm install -g cnpm --registry=https://registry.npm.taobao.org
   cnpm -v    //确认版本号（安装结束后）
   ```

5. 全局安装hexo

   ```yml
   cnpm install -g hexo-cli  //全局安装hexo
   hexo -v //确认hexo版本号（安装结束后）
   ```

6. 在c或d 盘建立一个空文件夹（下方以d:/blog为例）

7. cmd进入该文件夹后，用hexo生成博客

   ```yml
   hexo init  //初始化hexo  （此建议处用git窗口）
   ```

8. 本地预览生成的默认博客

   ```yml
   hexo s //本地预览
   localhost://4000 --本地地址复制到浏览器即可 （ctrl+c关闭）
   ```


9. 发布到github
   1. 创建github账号
   2. 并创建一个仓库，命名为：**你的github昵称.github.io**

10. 在本地blog文件安装一个git部署插件

    ```yml
    npm install hexo-deployer-git --save  //在git或cmd到blog目录下输入
    ```

11. 设置blog目录下_config.yml文件_最后的deploy如下

    ```yml
    deploy:
      type: git
      repo: 你新建的仓库地址
      branch: main  //注意，main是现在github的默认分支，**每个冒号后有一个空格** 
    ```

    

12. 将博客部署到GitHub仓库

    在blog下打开cmd或git 输入：

    ```yml
     hexo clean --清除
     hexo g --生成
     hexo d --部署
    ```

13. 最后，输入你的仓库名称到浏览器即可访问

    
    



  这只是搭建完成，还可以更改主题，美化博客！

  网上有相当多美化博客教程可以参考

  暂时挖个坑，有时间在填 。~~绝对不是因为我懒~~

---



> 作者：JokerDaxiong 
>
> 博客：[Jokerdig.com]("Hey,Joker")
>
> 时间：2021-2-18
