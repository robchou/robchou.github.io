---
layout: post
title:  "Git简明教程"
excerpt: "Git 5分钟教程"
date: 2016-07-25 17:54:01 +0800
categories: software
tags:
- git
---
### Overview
Git是一个分散式版本控制软件，最初由林纳斯·托瓦兹（Linus Torvalds）創作，於2005年以GPL釋出。最初目的是为更
好地管理Linux内核开发而设计。(参考[维基百科](http://zh.wikipedia.org/wiki/Git))。
我们当前使用的版本管理系统是SVN，方便起见，我们直接将SVN与Git进行类比，通过类比更快的掌握Git的使用。

CVS/SVN与Git最大的区别就是：CVS及SVN都是集中式的版本控制系统，而Git是分布式版本控制系统。Git相对CVS/SVN灵活很多。

![SVN VS Git](/assets/images/2016-07-25-git-tutorial/collaboration_git_vs_svn.jpg)


#### SVN与Git类比

| SVN      | Git    | 功能               |
|----------|--------|--------------------|
| checkout | clone  | 下载代码到本地     |
| update   | pull   | 更新代码           |
| add      | add    | 添加需要跟踪的代码 |
| N/A      | commit | 提交代码到本地     |
| commit   | push   | 提交代码到服务器   |

### Git简明教程

[这里](http://rogerdudler.github.io/git-guide/index.zh.html)有一份感觉不错的简明教程，可以快速上手。我就不再重复造轮子了。

### Git图形界面工具
如果只是做Android App的开发，android studio自带git插件，如果需要单独管理git仓库，感觉Source Tree还不错，推荐使用。


### Git应用场景

#### 1. Android源码管理
这里可参考我以前写的一篇[教程](https://robchou.github.io/software/2014/07/24/use-repo-to-manage-project.html)。

#### 2. Git服务器搭建
这里可参考我以前写的一篇[教程](https://robchou.github.io/software/2014/05/05/git-server-on-debian-wheezy.html)。

#### 3. 基于Git的在线代码托管网站
目前有很多基于Git的代码托管服务，国外有 [Github](https://www.github.com)， [Bitbucket](https://bitbucket.org/)
国内的有[oschina](http://git.oschina.net/), [CSDN](https://code.csdn.net)，这几个网站项目设置都大同小异，除了
Github都提供免费私有项目的创建。

#### 如果想更深入的学习Git，可以参考官方推荐的书籍:

- [Git官方参考书籍中文版](https://git-scm.com/book/zh/v2)
- [Git官方参考书籍英文版](https://git-scm.com/book/en/v2)
