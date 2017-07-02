---
layout: post
title: "Debian Wheezy安装Fcitx"
excerpt: "在Debian Wheezy上安装Fcitx记录"
date: 2014-06-08 17:54:01 +0800
category:
- software
tags:
- linux
- tutorial
---

### Overview

Linux下五笔输入法也尝试过一些，IBus经常出一些莫名其妙的问题，不得不转投Fcitx，不过Fcitx也确实很好用。

### Environment

```sh

uname -a
Linux debian 3.2.0-4-amd64 #1 SMP Debian 3.2.57-3+deb7u2 x86_64 GNU/Linux

```

### Steps

#### 1.安装fcitx及五笔的码表

```sh

sudo apt-get install fcitx fcitx-table-wbpy im-switch

```

#### 2.设置fcitx为系统默认输入法
```sh

im-switch

```

选择fcitx

#### 3.根据自己的需求简单配置，默认配置已经很好用了，外观配置文件的位置在:`~/.config/fcitx/conf`
