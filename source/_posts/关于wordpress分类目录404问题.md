---
title: 关于WordPress分类目录404问题
tags: []
id: '471'
categories:
  - - uncategorized
date: 2020-06-18 10:56:33
---

## 概述

前两天把博客给玩脱了和，也没有备份，重新搞了之后我其实想隐藏博文中链接地址里面的index.php无意间隐藏了index.php还神奇的把分类目录的404解决了。

## 我遇到的问题，本人萌新，如果有什么不对的地方希望大佬手下留情ヾ(≧へ≦)〃

我的博客的问题是就算使用word press的 月份和名称型类型地址也会报错。 以及我的分类目录404，但是文章标签就可以正常打开，这对于我来说已经非常玄学了。

## 开始解决：

我是用的nginx。我抄的是nginx修改的代码是这个[博主写的](https://blog.csdn.net/weixin_41846803/article/details/80488726 "博主写的")

```
location / {
       if (!-e $request_filename) {
            #一级目录
            rewrite ^/(.*)$ /index.php/$1 last;
        } 
    }
```

然后进入你的宝塔面板，网站——选择你需要改的网站——设置——更改配置——拆入代码。我插入的是第50行 ![](http://c-dreamer.top/wp-content/uploads/2020/06/word-press的404.png)