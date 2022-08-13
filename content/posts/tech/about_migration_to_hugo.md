---
title: "迁移说明"
subtitle: ""
date: 2022-08-12T22:40:19+08:00
draft: false
author: "cxz888"
authorLink: "https://cxz888.xyz"
authorEmail: "idlercloud@gmail.com"
description: ""
keywords: ""
license: '<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="知识共享许可协议" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a>'
comment: false
weight: 0

tags:
    - 思考
categories:
    - tech

hiddenFromHomePage: false
hiddenFromSearch: false

summary: ""
resources:
    - name: featured-image
      src: featured-image.jpg
    - name: featured-image-preview
      src: featured-image-preview.jpg

toc:
    enable: true
math:
    enable: false
lightgallery: false
seo:
    images: []

repost:
    enable: false
    url: ""
# See details front matter: /theme-documentation-content/#front-matter
---

最近花了一些时间把博客从 WordPress 迁移到了 Hugo 上。

来简单谈谈我的选择吧，夹杂一些胡思乱想，和技术上的关系不是很大。

<!--more-->

大概是今年 2 月多吧，在大佬的指引下建立了自己的博客。

当时就是有些创作欲，又觉得知乎、CSDN、博客园之类的平台不够满意，于是做了这个有些草率的决定。

说草率主要是因为服务器蛮贵的。。。然后我发现自己目前的水平还不够高，只能写一些使用教程啥的。

就是肚里墨水不太足呗。

![hifumi 啊哈哈](/memes/hifumi-ahaha.jpg "啊哈哈")

总之最初选择的是开箱即用、傻瓜操作的 WordPress。

它足够强大，资料也足够丰富，想要什么一查就有。

但是对我而言缺点也很快暴露出来。

## 1. 自定义需要一定的 PHP、CSS 功底

CSS 还好，只到够用的程度的话看看就懂。

何况基本上未来必学，早点熟悉也不是坏事。

但我对 PHP 并没有太多的兴趣（无贬义），可要是基本语法不懂基本上很难自定义，只能抄抄别人的代码，然后不断（痛苦）试错。

## 2. 编辑体验割裂

我喜欢用 markdown 写作。WordPress 则有自己的编辑器。

虽然也有很好的插件支持 markdown，然而在网站中写文章还是很割裂。

有一次我在写文章时服务器忽然崩了，重启后草稿丢失，失去灵感索然无味。

我其实最想要的是本地写作，然后某个命令一键发布。

## 3. 后台界面有点丑

指的是登录之后那个丑丑的页眉工具栏。

我试了不少方法自定义，都以失败告终。

而后台的设置界面反应不够快，还经常要在主题文件编辑器和主页之间来回窜。

## 4. 功能太多太复杂

WordPress 并非一个纯粹的面向个人博客的网站系统，它是广义上的 CMS。

面对诸多商业网站的需求，因而必须要很多复杂的功能。包括在主题和插件中能搜索到的，很多都是面向电子商务网站的。

因为功能太多，所以 API 复杂，很难从中找到自己需要的。

## 简单纯粹就是好

其实这些原因都不算太大吧，只是一个个积累起来有点不顺手。

这种不顺手有点妨碍了我最初的目的——写作。我花了大量的时间去自定义页面主题，去寻找插件，反垃圾评论，SEO 等等。

可我最初只是想写点东西，释放释放创作欲。

现在我开始觉得简单纯粹的东西最好。

分析一下，我理想的博客系统只有如下需求：

1. 方便的写作和发布
2. 简易的评论系统
3. 分类、标签功能

我是比较爱折腾的那种人，曾经花了两天捣鼓终端美化。这次也花了不少时间捣鼓了 Hugo。

它的主要优点是易于理解。不像 WordPress 那庞大的系统，难以知晓它在幕后究竟做了什么。Hugo 这样的静态网站生成器的大致行为很容易猜测。这使得自定义很方便。

它可以轻松满足我的三个需求。

静态页面还有个好处是硬件需求不高，而且迁移方便。搭建自己的博客只需 Github Pages 即可，没必要租服务器。而且 Github Pages 的集成更好使，推荐。

## 最小可工作的 Hugo

刚下载的 Hugo 需要找到一个合适的主题。幸好这方面资源很多，除了官方列表中的，在知乎等地搜索可以找到很多开源的主题。

我目前使用的 FixIt 就很让人满意。它所参考的 LoveIt 也很不错。

Hugo 不太方便的一点是，本地写作之后生成站点，需要手动同步到服务器中。

最开始我是用 WinSCP 的同步功能。但是它太慢了，而且还是需要不少操作。

后来是上传压缩包、解压、覆盖。虽然快了不少，但是操作更多。

现在的方案是在服务器维护远程非裸仓库，本地构建好直接 push 到远端即可，十分方便。

主题自带的分类和标签功能基本满足需求。而尽管现在尚未开启，评论系统也是支持的。

一切问题解决了。

现在的工作流程就是：本地写作 -> hugo 构建 -> push。

几乎是最小工作量了。

唯一可能改进的地方就是写作时用到的图片，目前我是手动将其放到 static 目录下，使用 pinga 压缩，然后在 md 中引用。

不过反正是在本地，未来完全可以写个简易程序将其自动化。

最理想的效果就是写作完，敲一个命令，然后自动将用到的图片处理好，并且构建和 push。

## 思考

这篇博客的标题，本来想叫做迁移说明和极简主义。

不过其实称不上极简啦。也就是偏好简单而已。

软件工程中著名的 KISS 原则，感觉同样可以应用到生活中。

越简单的人生，具有越强大的免疫力以抵挡外界。

希望能一直简单下去，提高自我，有朝一日写出对得起服务器价格的文章吧。

（不过刚好服务器快过期了，也许我会试着迁移到 Github Pages 上试试。)

![喝茶看报猫猫](/memes/tea-newspaper-cat.jpg)