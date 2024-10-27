---
title: "文章与博客推荐"
subtitle: ""
date: 2024-10-27T15:09:26+08:00
draft: false
author: "cxz888"
authorLink: "https://cxz888.xyz"
authorEmail: "idlercloud@gmail.com"
description: ""
keywords: ""
license: '<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="知识共享许可协议" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a>'
# comment: false
weight: 0

tags:
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
  auto: false
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

平时上班~~摸鱼~~和业余会看一些博客和技术文章，其中有一些我觉得不错的，记录在这里。

<!--more-->

## 业界新闻/趣闻

- [Why Safety Profiles Failed](https://www.circle-lang.org/draft-profiles.html)
  - 2024 年 10 月
  - safe cpp 提案作者、Circle C++ 编译器作者写的文章
  - 他前段时间提出了 [safe cpp 提案](https://safecpp.org/draft.html)，在社区中引起了巨大争议
  - 这篇文章则是狠狠批评了 C++ 之父 BS 和现在的 C++ 委员会主席 Herb Sutter 主张的另一种叫作 safety profile 的方案
- [What's new in Windows 11, version 24H2](https://learn.microsoft.com/en-us/windows/whats-new/whats-new-windows-11-version-24h2#rust-in-the-windows-kernel)
  - 2024 年 10 月
  - Windows 内核中的 Rust 首次进入正式发布
  - 先前 Windows 自家也有宣传，也有人在内核组件中发现了 Rust 符号
  - 不过这还是第一次正式进入大众视野，略有些纪念意义吧
- [维护者 Serge Semin 的告别信](https://telegra.ph/%E7%BB%B4%E6%8A%A4%E8%80%85-Serge-Semin-%E7%9A%84%E5%91%8A%E5%88%AB%E4%BF%A1-10-24-3)
  - 2024 年 10 月
  - Linux 移除俄罗斯维护者名单事件的其中一位被移除者写的告别信
  - 真情流露，颇有一种托孤之悲壮，令人难以平静
- [Eliminating Memory Safety Vulnerabilities at the Source](https://security.googleblog.com/2024/09/eliminating-memory-safety-vulnerabilities-Android.html)
  - 2024 年 9 月
  - 安卓将关键组件（蓝牙、WiFi 等）从 C/C++ 迁移到内存安全语言（如 Rust）
  - 观察到的内存安全漏洞显著减少
- [The secret inside One Million Checkboxes](https://eieio.games/essays/the-secret-in-one-million-checkboxes/)
  - 2024 年 8 月
  - 有趣的互联网小故事
  - 作者在 2024 年 6 月发布了一个名为「百万复选框」的网站，它上面有一百万个全局复选框，选中（或取消选中）一个框会立即为网站上的每个人更改它
  - 在网站在线期间，它的受欢迎程度远超作者想象：两周内有五十万名玩家勾选了超过六亿五千万次复选框。
  - 在这期间发生了一些充斥着技术浪漫的故事
- [CSS finally adds vertical centering in 2024](https://build-your-own.org/blog/20240813_css_vertical_center/)
  - 2024 年 8 月
  - 2024 年，css 终于添加了一个（直白的）垂直居中的方式
- [JavaScript Bloat in 2024](https://tonsky.me/blog/js-bloat/)
  - 2024 年 2 月
  - 作者用特定的方法查看了一些著名网站的 JavaScript 大小（我不太清楚 ta 的方法是否准确）
  - 然后发现这些号称使用现代前端技术的网站动辄十几乃至几十 MB
  - 有趣的是，真正关心性能的是 Pornhub，只有 1.4 MB
  - Reddit 上有人说这些大小其实主要来自于广告跟踪器、第三方营销工具、Datadog、Rollbar 等。用广告拦截器之类的东西可以显著降低
- [In Loving Memory of Square Checkbox](https://tonsky.me/blog/checkbox/)
  - 2024 年 1 月
  - 有点意思的文章，讲单选框 (radio box) 和复选框 (check box) 的历史
  - 操作系统 UI 有一个长达 40 年的不成文的传统：单选框一定是圆形的，复选框一定是方形的，这样人们可以轻易辨别出到底是单选还是多选
  - 但是今年 (2024)，苹果终于放弃了这个传统，它的新 visionOS 将有圆形复选框
- [Digg's v4 launch: an optimism born of necessity.](https://lethain.com/digg-v4/)
  - 2018 年？
  - 一个用 python 的创业公司，因为函数参数给了默认值，而倒闭（可能略有夸张）
  - 参数写错然后导致程序一直 OOM，在业务最高峰的时候停摆，等修好之后已经寄了
  - python 函数的默认参数是定义时求值而非调用时求值，所以多次调用时，默认参数的实例是同一个，还挺反直觉的

## 精品文章

- [Semantic Versioning Will Not Save You](https://hynek.me/articles/semver-will-not-save-you/)
  - 作者认为：依赖于 SemVer 会伤害用户
  - 有一定道理。读一读可以更多思考项目、依赖、开源库之间的复杂关系
- [Windows NT vs. Unix: A design comparison](https://blogsystem5.substack.com/p/windows-nt-vs-unix-design)
  - 如题，比较 Windows NT 和 Unix 系的设计不同
  - 看了这篇文章真有点感觉 Windows NT 比 unix 系好多了（毕竟它是后来者，有足够的经验可以吸收）
- [Why LSP](https://matklad.github.io/2022/04/25/why-lsp.html)，[LSP could have been better](https://matklad.github.io/2023/10/12/lsp-could-have-been-better.html)
  - 对 lsp 的一些思考。作者 matklad 是 rust-analyzer（rust 的语言服务器）的主要开发者，可能是世界上对 LSP 理解最深刻的人之一了
  - 提到 lsp 是如何做抽象的（很有意思，不是以共性为中心，而是以表现为中心），为什么可以成功
- [How to ask good questions](https://jvns.ca/blog/good-questions/)
  - 开发者社区中很多人可能都听说过[提问的智慧](http://www.catb.org/~esr/faqs/smart-questions.html)
  - 作者认为它是「很受欢迎且充满敌意的文档」，比如它开头就写「我们称这样的人为“失败者”」
  - 他提出了一些略微温和的准则。至于到底如何更好，见仁见智吧
- [Recursive (Re-entrant) Locks](https://blog.stephencleary.com/2013/04/recursive-re-entrant-locks.html)
  - 主要是对可重入锁的批判
- [Beyond Ctrl-C: The dark corners of Unix signal handling](https://sunshowers.io/posts/beyond-ctrl-c-signals)
  - 关于 unix 信号的一篇不错的科普文章，有一段是关于 async rust 的，其他的部分适合所有人
- [Driving Compilers](https://fabiensanglard.net/dc/index.php)
  - 一个不错的系列，讲 c 如何从源文件编译链接最后加载的整个过程，总体比较简洁，熟手拿来查漏补缺也不错
- [沅有芷兮：类型系统的数学之美](https://mp.weixin.qq.com/s/ieEewizkN7H-11z-PexkGw)
  - 其他发布链接：<https://zhuanlan.zhihu.com/p/69223872（有一些格式问题）>、<https://cloud.tencent.com/developer/article/1447498>
  - 科普 primitive type、sum type、product type、generics 在数学上的含义，言简意赅
- [What a good debugger can do](https://werat.dev/blog/what-a-good-debugger-can-do/)
  - 主要讨论了一个优秀的调试器应该具备的功能和特性，不只是断点调试，大开眼界。
  - 剧透：列断点、tracing 断点、数据断点、多线程调试、热重载、时间旅行、全知 (Omniscient) 调试
- [How to Test](https://matklad.github.io/2021/05/31/how-to-test.html)
  - matklad（rust-analyzer 的主要开发者）的文章，讲述一些测试的理念，引人深思
- [The curse of strong typing](https://fasterthanli.me/articles/the-curse-of-strong-typing)
  - 实际上是一篇 Rust 的教学文章，由浅入深，主要是关于类型系统的。
- [A `fork()` in the road](https://www.microsoft.com/en-us/research/publication/a-fork-in-the-road)
  - 微软发表的论文，反对 UNIX `fork()`，列举了诸多 `fork()` 的坏处，并提出了一些替代方案
- [Tour of Rust's Standard Library Traits](https://github.com/pretzelhammer/rust-blog/blob/master/posts/tour-of-rusts-standard-library-traits.md)
  - 介绍 Rust 标准库的 trait，挺全面的
- [Sizedness in Rust](https://github.com/pretzelhammer/rust-blog/blob/master/posts/sizedness-in-rust.md)
  - 和类型「大小」相关的概念。比如 `Sized` trait，dynamically sized types(DST)，zero sized types(ZST)
  - 对于系统编程语言（主要指 C/C++/Rust 等，一般无 GC）而言，类型的大小是一个非常基本的限制，会影响到语言设计的方方面面，也是这类语言复杂性的一个常见来源
  - 因此这篇文章虽然主要是关于 Rust 的，但是对 C/C++ 的理解也可以有一定启发作用

## 博客/时事通讯/播客推荐

- [Without boats, dreams dry up](https://without.boats)
  - 无舟子（戏称）的博客
  - 他是 Rust 异步系统的主要设计人之一，博客文章的见解相当深刻
- <https://blog.yoshuawuyts.com>
  - 也是 Rust 团队成员之一，博客里会探索一些语言设计，也会有一些和 WebAssembly 相关的
- <https://fasterthanli.me>：Amos 的博客
  - 他有许多由浅入深的 Rust 教学文章，深受社区好评
- [Baby Steps](https://smallcultfollowing.com/babysteps)
  - Niko Matsakis 的博客。Rust 团队成员之一，博客有很多语言设计相关的思考（以及画饼）
- [Faultlore](https://faultlore.com/blah)：Gankra 的博客。
  - 她也是 Rust 团队成员，博客里写了很多 unsafe 相关的底层知识
  - 写了 [too many lists](https://rust-unofficial.github.io/too-many-lists/)、[The Rustonomicon](https://doc.rust-lang.org/nightly/nomicon/) 等教程。文风中二而有趣
- [Ralf's Ramblings](https://www.ralfj.de/blog)
  - RalfJung 的博客。Rust 团队成员
  - 主要工作应该也是关于 unsafe 的，比如 [miri](https://github.com/rust-lang/miri) 和 [stacked borrows](https://github.com/rust-lang/unsafe-code-guidelines/blob/master/wip/stacked-borrows.md)
- <https://matklad.github.io>
  - matklad 的博客。他是 rust-analyzer 的主要开发者
  - 博客主要关于 IDE/编译器、软件开发最佳实践（如测试）、理论知识等
- <https://www.redox-os.org/zh/news>
  - redox OS 的新闻，包括每月通讯
- [This Month in Rust OSDev](https://rust-osdev.com/)
  - Rust OS 开发生态的每月通信
- [This Week in Rust](https://this-week-in-rust.org/)
  - Rust 生态系统的每周通讯
- [This Week in Bevy](https://thisweekinbevy.com/)
  - bevy engine 的每周通讯
  - 主要信息来源包括 github、Discord 等
- [Self-Directed Research Podcast](https://sdr-podcast.com/episodes/)
  - Amos 和 James 的播客，各种开发技术都可能讨论

> 版权声明：本文采用 [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/) 进行许可，转载请注明出处。
>
> 本文链接：[{{< permalink >}}]({{< permalink >}})