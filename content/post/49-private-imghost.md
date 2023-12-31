---
title: 使用 GitHub + PicGo + jsDelivr 搭建自己的私人图床
description: 妈妈再也不用担心我上传图片啦！
date: 2021-03-08 20:51:16
lastmod:

author: Wonz
image: https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2021-03-08_21-44-50.png
categories:
- 数字生活
tags:
- 图床
- PicGo
- 工具

comments: true
mathJax: true
ShowsNavLinks: true #上一篇文章 || 下一篇文章
print_background: true
puppeteer:
  timeout: 1000

draft: false
---
### 一、背景

以前写技术博客的时候，都是用的本地图片，一些博客平台比如 **CSDN** 同步更新的时候需要手动上传图片，这很浪费时间和精力。为了减少重复工作，一直有用**图床**的想法，但是又听到 `XXX图床挂了` ，一直很担心这个问题。后来发现了一个非常棒的搭建属于自己的私人图床的方法，现记录下来，希望帮助到有同样需求的朋友们。

### 二、创建 GitHub 图床仓库

首先你需要有个 **GitHub** 账号（搞技术的应该都知道全球最大程序员~~同性~~交友网站吧）然后按照下图提示创建一个图床仓库，名字随便起好了。

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-01-30_20-47-13.png)

**注意:** 因为 **GitHub** 现在支持创建**私人仓库**了，但是图床仓库不能设为私人的，否则会影响后面的图片超链接显示。一开始我 **GitHub** 图床仓库设成 Private，测试之后发现博客里的图片并不能成功显示出来，后来我把图床仓库改为 Public 之后，图片就能成功显示了。

### 三、生成 Access token

然后进入个人账号的 `Settings` ：

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-01-30_20-48-23.png)

然后选择 `Developer settings` ：

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-01-30_20-49-26.png)

再选择 `Personal access tokens` ：

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-01-30_20-50-47.png)

创建新的 `token`：

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-01-30_20-51-50.png)

然后填写 Note，并把 `repo` 全勾上。

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-01-30_20-52-52.png)

然后点击页面底部的 `Generate token` ，就生成了 `token`，记得及时复制并保存下来，页面关闭就看不到了，后面要用到。

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-01-30_20-53-46.png)

### 四、配置 PicGo，使用 jsDelivr 的 CDN

下载 [PicGo](https://github.com/Molunerfinn/picgo/releases) 软件，安装。

选择系统对应的版本下载，我用的是 `Windows` 系统，所以直接下的 `.exe` 文件。

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-01-30_20-56-24.png)

打开 PicGo 的图床设置：

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-01-30_20-57-49.png)

输入自己的 GitHub 仓库名、分支名写 `master` 、Token、存储路径就写 `img/` 就行了。

因为我们需要使用 `jsDelivr` 加速访问，所以将自定义域名设置为 `https://cdn.jsdelivr.net/gh/GitHub用户名/图床仓库名` ，进行配置：

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-01-30_20-58-29.png)

### 五、使用私人图床

点击上传区，选择图床为 **GitHub图床**，链接格式为 `Markdown` ，直接拖动图片到方框里，等待上传完成，会自动复制 Markdown 链接，然后直接粘贴到正在写的博客中就行，非常方便快捷，大大减少了写作中无意义的重复劳动。

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-01-30_21-02-22.png)

### 六、使用提示

图片上传图床还要注意保护个人隐私，因为仓库是 **Public** 的，其他用户其实可以看到你上传了什么图片。

虽然这篇文章是一年前写的，但是大学室友最近按照我之前写的教程亲测有效，所以我决定重新排下版，润色了一下文字，重新发表出来。

### 七、致谢

[GitHub+jsDelivr+PicGo搭建免费图床](https://segmentfault.com/a/1190000020240864)
