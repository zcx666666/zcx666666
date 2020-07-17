---
title: 入门hexo第一步
date: 2020-07-02 21:32:33
tags:
---
# 安装

前期准备工作肯定是必不可少的，作为前端这些都应该有，但是可能有些人没有，不懂。具体安装这些我就不多说了。需要下载一下，下载完直接安装即可。

get:https://git-scm.com/downloads。

node:https://nodejs.org/en。

都下载完成以后就是如何安装hexo，Hexo是一款快速简洁的博客框架，可以将 md 文档渲染为静态 HTML 页面，拥有非常多的主题和插件可以选择。新建一个文件夹来存放项目。然后再新建的文件夹中右键选择Git Bash。![image-20200704093453826](https://zcx666666.oss-cn-beijing.aliyuncs.com/img/image-20200704093453826.png)



```js
npm install -g hexo-cli
```

![image-20200704094125227](https://zcx666666.oss-cn-beijing.aliyuncs.com/img/image-20200704094125227.png)

安装完以后检查一下是否安装成功

![image-20200704094207387](https://zcx666666.oss-cn-beijing.aliyuncs.com/img/image-20200704094207387.png)

这就整明安装成功了。如果在这些步骤中遇到任何问题就只能多查了。

# 创建项目

先初始化，把hexo初始化的项目拉取到本地。在新建项目的时候init可以写成i，项目明不要有任何符号。

```
hexo init 项目名
```

![image-20200704095000788](https://zcx666666.oss-cn-beijing.aliyuncs.com/img/image-20200704095000788.png)

![image-20200704095141579](https://zcx666666.oss-cn-beijing.aliyuncs.com/img/image-20200704095141579.png)

# 安装hexo依赖模块

安装依赖模块等后续操作都一定要在新建的项目目录中执行。进入到项目目录以后还是右键选择Git Bash

```
npm install
```

![](https://zcx666666.oss-cn-beijing.aliyuncs.com/img/image-20200704095742330.png)

安装完依赖以后此时你的项目就算完整的搭建完成了。接下来就是启动项目配置项目等。启动项目以后在地址栏中输入：http://localhost:4000

```
hexo s
```

![image-20200704095923147](https://zcx666666.oss-cn-beijing.aliyuncs.com/img/image-20200704095923147.png)

![image-20200704101004808](https://zcx666666.oss-cn-beijing.aliyuncs.com/img/image-20200704101004808.png)

本地启动的好处就是，你写完了可以在本地看，确定没有问题在推送到git上

关于网站的基本配置需要在目录下找到_config.yml文件用vscode打开。

说下需要遇到的问题，切记配置值前边一定要有空格，否则报错了就。这些配置改成自己的就行。

![image-20200704102341766](https://zcx666666.oss-cn-beijing.aliyuncs.com/img/image-20200704102341766.png)

修改完以后做以下操作：

清除旧的生成页面

```
hexo clean
```

生成新的html

```
hexo g
```

![image-20200704102831779](https://zcx666666.oss-cn-beijing.aliyuncs.com/img/image-20200704102831779.png)

然后重新启动服务即可在本地看到效果





















