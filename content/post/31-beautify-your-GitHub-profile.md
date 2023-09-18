---
title: 使用 Shields.io 数据牌 + GitHub 统计卡片美化你的 GitHub profile
date: 2020-09-07 19:06:07
tags: [GitHub,美化]
categories: 数字生活
---
<!--more-->

### 一、在 GitHub 中发现小彩蛋

首先，在 GitHub 中创建和账号**同名的**一个 repository，就会发现这个小彩蛋。

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-09-04_15-35-38.png)

### 二、编写 README，完善属于自己的 profile

用 [Typora](https://typora.io/) 打开创建完的这个项目下的 README 文件，可以看到如下界面。

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-09-04_19-29-30.png)

你可以根据自己需求填写相关信息，完善属于自己的 profile。当然，也有美化 README 的方法。

### 三、认识 Shields.io

在浏览 GitHub 项目的时候，经常可以发现下图所示的 `数据牌` 展示。我们完全可以使用 `数据牌` 进行美化自己的 profile。

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-09-04_20-01-37.png)

[Shields.io](https://shields.io/) 就可以完成我们的这个需求，它其实就是一个「牌子渲染服务」。里面分为静态展示数据牌和动态展示数据牌。

### 四、静态数据牌展示

静态的比较简单。

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-09-04_20-03-52.png)

* `label` 写要展示的名字，比如：CSDN。
* `message` 可以写展示数据，比如：全国前 4K 名。
* `color` 选择一个颜色（当然，也可以到[这里](https://www.sioe.cn/yingyong/yanse-rgb-16/)找喜欢的颜色，输入对应的十六进制代码）。

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-09-04_20-06-16.png)

然后点右边的 `Make Badage`，就会看到效果展示了：

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-09-04_20-06-49.png)

然后复制地址栏里的地址，直接使用 Markdown 的插入图片语法：`![](这里粘贴地址栏地址)`，就可以展示出来了。但是需要注意的是，这种方法是静态展示，如果数据改变了，需要自己手动更新，不够自动化。

### 五、动态数据牌展示

动态展示相比静态展示，自然就更加自动化，可以实时更新数据。

这里介绍 [SpencerWoo](https://github.com/spencerwooo) 开发的 [Substats](https://github.com/spencerwooo/Substats) 小工具。使用教程可以参考开发人员写的这篇[文章](https://sspai.com/post/59593)，当然也可以自己查看[使用文档](https://substats.spencerwoo.com/)。

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-09-04_20-08-59.png)

* 简单来说，就是先找到自己想展示的 API URL，比如我的 GitHub URL 就是：https://api.spencerwoo.com/substats/?source=github&queryKey=Wonz5130。一般都只需要修改 `source` 后面的目标服务器以及 `queryKey` 后面的请求数据标签，前者一般都是平台名，后者一般都是用户名。
* `data type` 选择 `json` 。
* `label` 选择数据牌左侧你想展示的东西，比如我想展示的是 `GitHub`。
* `query` 填： `$.data.totalSubs`。
* `color` 填写一个十六进制的颜色代码。
* 剩下两个分别是数据牌右侧展示数据的前缀和后缀，我一般会填一个后缀 `关注数`。

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-09-04_20-23-22.png)

然后点击 `Make Badge`，可以看到以下界面：

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-09-04_20-23-44.png)

然后还是复制地址栏里的地址，用 Markdown 的插入图片语法：

```
![](https://img.shields.io/badge/dynamic/json?color=000000&label=GitHub&query=%24.data.totalSubs&suffix=%20followers&url=https%3A%2F%2Fapi.spencerwoo.com%2Fsubstats%2F%3Fsource%3Dgithub%26queryKey%3DWonz5130)
```

就会展示以下标签了：

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-09-04_20-25-37.png)

当然，有些平台的用户名并不是你的用户名而是一串**独特的数字**（比如微博），具体请参考 [API 文档](https://substats.spencerwoo.com/api.html#%E5%8D%B3%E5%88%BB-jike-app)。

目前支持的有这些平台：

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-09-05_11-03-36.png)

当然，你也可以在给标签加个**超链接**指向自己的**主页**，比如我给上面 GitHub 就加了一个自己的主页，代码如下：

```
[![](https://img.shields.io/badge/dynamic/json?color=000000&label=GitHub&query=%24.data.totalSubs&suffix=%20followers&url=https%3A%2F%2Fapi.spencerwoo.com%2Fsubstats%2F%3Fsource%3Dgithub%26queryKey%3DWonz5130)](https://github.com/Wonz5130)
```

这样别人就能通过点击标签跳转到你的其他平台主页了。

### 六、GitHub 统计卡片

当然，还可以再加一个 GitHub 统计卡片。

下面我是在**即刻员工** [Joway](https://github.com/joway/joway) 的 profile 里发现的如下语法：

```
<img align="right" src="https://github-readme-stats.vercel.app/api?username=joway&show_icons=true&icon_color=CE1D2D&text_color=718096&bg_color=ffffff&hide_title=true" />
```

只需要把 username 改成自己的 GitHub 用户名就可以了。

当然也可以查看[这个项目](https://github.com/anuraghazra/github-readme-stats)的[官方文档](https://github.com/anuraghazra/github-readme-stats/blob/master/docs/readme_cn.md)，进行个性化设置，比如选择[主题](https://github.com/anuraghazra/github-readme-stats/blob/master/themes/README.md)，或者自己选择相应板块颜色。

下面就是我的 GitHub 统计卡片：

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-09-05_11-16-10.png)

### 七、最终效果展示

红色方框里的就是最终效果展示：

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-09-04_19-38-18.png)

### 八、致谢

[用 Substats 和 Shields.io 为你的个人主页定制动态数据小牌子](https://sspai.com/post/59593)

[GitHub Readme Stats](https://github.com/anuraghazra/github-readme-stats/blob/master/docs/readme_cn.md)
