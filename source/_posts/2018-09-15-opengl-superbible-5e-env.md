---
title: OpenGL超级宝典macOS High Sierra环境搭建
date: 2018-09-15 15:39:20
tags:
- opengl
---

### Overview

本文主要是针对[《OpenGL超级宝典（第5版）》](https://book.douban.com/subject/10774590/)在macOS High Sierra中开发环境的搭建并将Ch02中Triangle的示例代码放到Xcode中成功运行。

### Environment

```sh
macOS High Sierra 10.13.6 Xcode 9.4.1
```

### Deps

OpenGL超级宝典主要依赖的库有*opengl*, *glut*, *glew*, *gltools*几个库，其中*opengl*和*glut*是系统自带的库，不需要再安装，在接下来的步骤中我们会通过[brew](https://brew.sh/)去安装*glew*及*cmake*，通过*cmake*编译*gltoos*源码。

### Steps

#### 1. 安装glew及cmake

```sh
brew install cmake glew
```

#### 2. 下载gltools源码
```sh
git clone https://github.com/HazimGazov/GLTools.git
```

#### 3. 编译并安装gltools
```
cd GLTool/build
cmake ..
make
sudo make install
```
gltools默认安装在*/usr/local/lib*下

#### 4. 下载OpenGL超级宝典中的代码

```sh
git clone https://github.com/kimziv/oglsuperbible5.git
```

#### 5. 创建一个Xcode cli项目

![create-cli-project](/assets/opengl-superbible-5e-env/creat-cli-project.png)

#### 6. 创建Triangle工程

![create-triangle-project](/assets/opengl-superbible-5e-env/create-triangle-project.png)

#### 7. 选择deployment target

![choose-deploy-target](/assets/opengl-superbible-5e-env/choose-deploy-target.png)

#### 8. 添加frameworks依赖

![linked-frameworks](/assets/opengl-superbible-5e-env/linked-frameworks.png)

#### 9. 添加OpenGL framework

![linked-frameworks](/assets/opengl-superbible-5e-env/link-opengl.png)

#### 10. 添加glut framework

![linked-frameworks](/assets/opengl-superbible-5e-env/link-glut.png)

#### 11. 添加头文件搜索路径

![header-search-paths](/assets/opengl-superbible-5e-env/header-search-paths.png)

#### 12. 添加库文件搜索路径

![header-search-paths](/assets/opengl-superbible-5e-env/library-search-paths.png)

#### 13. 添加链接选项

```sh
-lGLEW -lgltools
```

![header-search-paths](/assets/opengl-superbible-5e-env/linker-flags.png)

#### 14. 使用 *oglsuperbible5/Src/Chapter02/Triangle/Triangle.cpp*替换*main.cpp*

#### 15. 编译并运行

![run](/assets/opengl-superbible-5e-env/run.png)

### 源码下载

```sh
git clone https://github.com/opengl-superbible5e-learning/Triangle
```
