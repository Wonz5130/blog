---
title: 互联网写作规范指北
description: 
date: 2020-11-21 21:09:46
lastmod:

author: Wonz
image: 
categories:
- 数字生活
tags:
- Markdown
- 写作

comments: true
mathJax: true
ShowsNavLinks: true #上一篇文章 || 下一篇文章
print_background: true
puppeteer:
  timeout: 1000

draft: false
---
## 一、写在前面

我从 2018 年开始接触 **Markdown**，自从习惯了 **Markdown** 写作之后，再也不想用 **Word** 写东西了。

按照**维基百科**的说法，**Markdown** 是一种[轻量级的标记语言](https://en.wikipedia.org/wiki/Lightweight_markup_language)，[采用纯文本](https://en.wikipedia.org/wiki/Plain_text)格式语法。你不需要掌握多少语法就可以很轻松地写出非常好看的排版。

## 二、Markdown 基础语法

### 标题

使用 `#` 可以给文章加上标题。

```markdown
# 一级标题：文章的标题
## 二级标题：正文的大标题
### 三级标题：正文的小标题
```

Markdown 最大可支持六级标题，但是过于复杂的章节反而会影响阅读体验。因此我一般只使用二级标题和三级标题。二级标题用来做章节标题，三级标题用来做正文小标题。

### 列表

使用 `‐` 或 `*` 或 `+` 并跟随 1 个空格来表示无序列表。建议使用 `‐`，因为 `*` 会和加粗以及斜体产生混淆，而 `+` 不常见。

```markdown
- 这是1
- 这是2
- 这是3
```

展示效果：

- 这是1
- 这是2
- 这是3

### 有序列表

使用数字 1、2、3 并跟随 1 个 `.` 来表示有序列表。

```markdown
1. 这是第一条
2. 这是第二条
3. 这是第三条
```

### 引用

使用 `>` 并跟随 1 个空格来表示引用。

```markdown
> 这是引用
```

展示效果：

> 这是引用

### 粗体

使用 2 个 * 分别包裹。

```markdown
这是**加粗**
```

展示效果：

这是**加粗**

### 斜体

使用 1 个 * 分别包裹。

```markdown
这是*斜体*
```

展示效果：

这是*斜体*

### 删除线

使用 2 个 ~ 分别包裹。

```markdown
这是~~删除线~~
```

展示效果：

这是~~删除线~~

### 链接

**普通链接**

语法：

```markdown
[这是维基百科首页](https://zh.wikipedia.org/zh-cn/)
```

展示效果：

[这是维基百科首页](https://zh.wikipedia.org/zh-cn/)

**图片链接**

语法：

```markdown
![这是图片](https://upload.wikimedia.org/wikipedia/zh/6/6a/Viva_La_Vida_Coldplay_Album.jpg)
```

展示效果：

![这是图片](https://upload.wikimedia.org/wikipedia/zh/6/6a/Viva_La_Vida_Coldplay_Album.jpg)

图片链接这里最好使用的是图床链接，而不是本地链接，因为如果你需要发布到网上的话，使用图床可以一键识别图片，而不需要手动再单独添加图片。最推荐的当然还是尽量减少图片的使用，因为图床难免会挂掉。

我自己用的是 `GitHub + PicGo + jsDelivr` 搭的图床，相关配置可以参考我写的这篇文章 [GitHub+PicGo+jsDelivr 搭建自己的私人图床](https://blog.csdn.net/Wonz5130/article/details/104119008?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522160586131019724838526745%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fblog.%2522%257D&request_id=160586131019724838526745&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~blog~first_rank_v1~rank_blog_v1-1-104119008.pc_v1_rank_blog_v1&utm_term=picgo)。

我一般写文章主要用到的就是以上这些基础语法，其实三分钟就能学会。

## 三 、Markdown 进阶语法

### 代码

有时我写技术文章的时候，难免会涉及到代码，此时就需要使用代码展示的语法了。

**行内代码**

使用两个重音符 ` 包裹。

```markdown
这是行内 `代码`
```

展示效果：

这是行内 `代码`

**代码块**

使用三个重音符 ` 置于代码块的首行和末行，首行的三个重音符后面可以加代码语言名称。

```markdown
```python
print("hello, python!")
```

```

展示效果：

```python
print("hello, python!")
```

### 任务列表

有时无序列表只能展示一些内容，但是并不能达到可勾选的目的，此时任务列表就出现了。

```markdown
- [ ] 这是任务一
- [x] 这是任务二（已完成）
- [ ] 这是任务三
```

展示效果：

- [ ] 这是任务一
- [X] 这是任务二（已完成）
- [ ] 这是任务三

### 字间距

Markdown 写作有个非常重要的原则就是注意空格。比如：

- 全角中文字符与半角英文字符之间，应有一个半角空格。

  ```markdown
  错误：这是错误的example。
  正确：这是正确的 example。
  ```
- 全角中文字符与半角阿拉伯数字之间，有没有半角空格都可，但必须保证风格统一，不能两种风格混杂。

  ```markdown
  正确：今天是2020年11月21日。
  正确：今天是 2020 年 11 月 21 日。
  ```
- 专有名词请使用正确的大小写。

  ```markdown
  错误：apple 发布了新款 iphone12 手机。
  正确：Apple 发布了新款 iPhone12 手机。
  ```
- 数字与单位之间需要加空格，但是度的标志、百分号不加空格。

  ```markdown
  正确：我身高没有 180 cm，今天空气湿度大概 50%。
  ```
- 全角标点与其他字符之间不加空格。

  ```markdown
  正确：大家好，我是 Wonz。
  ```
- 推荐使用直角引号代替双引号。

  ```markdown
  正确：你知道「Wonz」吗？
  ```

### 表格

有时觉得大段的文字不如一个表格清晰：

```markdown
|    左对齐   |       居中对齐     |       右对齐      |
| :--------- | :--------------: | ---------------: |
|   选项A     |                  |                  |
|   选项B     |                  |                  |
```

展示效果：

| 左对齐 | 居中对齐 | 右对齐 |
| :----- | :------: | -----: |
| 选项A  |          |        |
| 选项B  |          |        |

当然，表格这里我更建议直接使用 **Markdown** 编辑器来实现，而不是写这么多代码来实现格式的规范（后面会提到，先卖个关子）。

当然，以上的这些语法完全是可以嵌套组合使用的，比如无序列表与加粗组合：

```markdown
- 这是**1**
	- 这是**1.1**
- 这是**2**
- 这是**3**
```

展示效果：

- 这是**1**
  - 这是**1.1**
- 这是**2**
- 这是**3**

这完全靠自己写作时候的发挥。

## 四、Markdown 编辑器推荐

我基本只在 **Windows** 平台上进行文章的写作，因此只了解 **Windows** 平台的 **Markdown** 编辑器，强烈推荐 [Typora](https://typora.io/)。

**Typora** 讲究的是**所见即所得**，你使用 **Markdown** 语法写的东西能够马上展示效果，而且它可以将你写的文档导出成 **PDF/HTML/Word** 等多种格式，完全不用担心分享给没有安装 **Markdown** 编辑器的人看。

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/Snipaste_2020-11-20_16-39-43.png)

## 五、写在后面

真的非常建议每个人都学一下 **Markdown** 语法来进行写作。

并不一定是搞技术的才使用 **Markdown** 来写作。其实平时的**朋友圈/微博等社交平台**的内容输出，也可以参考以上的规范与标准，比如如何空格。学会以后，真的很大程度上能够提升阅读体验。

## 六、参考

[Markdown 教程](https://commonmark.org/help/tutorial/)

[中文技术文档的写作规范——by 阮一峰](https://github.com/ruanyf/document-style-guide)

[Markdown 入门教程及书写风格指南](https://tingtalk.me/markdown/)
