---
title: 我，转岗了
description: 
date: 2022-04-30 14:10:31
lastmod:

author: Wonz
image: https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/WechatIMG473.jpeg
categories:
- 工作
tags:
- 互联网
- 程序员
- 压力
- 绩效
- 后端
- 前端
- 思维方式

comments: true
mathJax: true
ShowsNavLinks: true #上一篇文章 || 下一篇文章
print_background: true
puppeteer:
  timeout: 1000

draft: false
---
# 写在前面

距离[《我，离职了》](https://wonz.wang/2021/07/21/53-resign/)这篇文章已经过去大半年了，如今在毕业后的第二家公司里待了快一年了，最近又经历了转岗，从全栈转到了后端。最近还在转岗适应期，两个多月的时间也收获了很多，决定记录一下。

# 为什么要转岗

首先要说明的是，公司团队并不是笼统地分为大前端、大后端，而是按照实际业务线进行划分的，一个团队里既有产品、前端、后端，又有测试。然后又有整个技术团队的前端技术栈、后端技术栈。当初公司招我的时候就有把我归到后端技术栈的想法。

在我刚入职的半年里，因为业务需求以及人员变动，我干了半年的全栈，负责三个内部系统的前端和后端。其中主要是前端多一点，以及一些比较轻的后端。

在参加公司转正述职的时候，我也提出了自己想转后端的意愿。以前我觉得全栈很酷，一个人既会写前端，又会写后端，多厉害啊。但实际经历之后，才意识到没有一定的技术水平和底蕴，是驾驭不了全栈的。按照我的认知里，一般从事全栈开发的都是至少五年以上工作经验的程序员。另外一点就是，全栈开发需要懂的技术太多了，我感觉自己学不过来。不利于自己想深入学习某一方向的技术，容易造成「会的多，但没有擅长」的局面。当然，最根本的原因还是发现自己并不喜欢前端，相对于前端繁琐的画页面、切图、改样式，还是更喜欢后端更加纯粹的技术。

因此，才更加坚定自己想转到后端的想法。

# 转岗之后有哪些变化

自己转岗其实是换部门了，从之前所在的 9 人团队换到了一个 20+ 人的团队，直属 leader 也换了。

最近的两个月一直在转岗适应期。

## 技术

转岗之前的技术栈是 Python + Flask + Vue + pREST。转岗之后的技术栈是 Golang + Kratos。虽然自己之前自学过 Golang 的基础语法，但实际开发的时候，发现还是不熟悉，缺少实践，导致经常遇到一些基础的问题都花了很长时间和精力解决。其中印象最深的一次是晚上被同事手把手教怎么写接口，一边教一边问我参数、返回值这些基础语法知识。最后同事还是建议我多补补语法，好在现在已经刷了好几遍语法，开发起来相对没那么生疏了。

至于 B 站开源的 Kratos 这个微服务框架，自己之前看了不下三遍官方文档，看的云里雾里，还是不知道讲的啥。然后自己就上手重构开发项目了。当时心态真的是慌得不行，完全不会啊。好在有同事整理的文档，以及自己厚着脸皮经常请教同事关于这个框架的问题。在连续开发了两三个接口之后，逐渐找到了感觉。

## 一些重构感想

最近一直在做公司的项目重构，前同事几乎把大部分逻辑处理都写在了前端，所以后端选了非常轻的技术。这次重构选择了新的后端技术栈，直接把逻辑处理都迁移到了后端。某天下午重构接口，把前端 Vue 处理逻辑的代码用 Golang 重写。发现自己过去写了半年前端还是有点用的，至少代码看起来不费劲，换门语言写也没什么问题，框架熟悉了无非就是语法换一换。畅通无阻地一下午敲了 200 多行代码，越敲越有感觉，好久没这么享受写代码了。

发现自己还是喜欢敲代码的，接口开发完成的时候还是有点成就感的，虽然大部分是被代码虐。正所谓“我待代码如初恋，代码虐我千百遍”。

## 开发流程与规范

新的团队有一套完整的开发流程，从本地开发 + 自测，到部署在测试环境，与前端进行联调，测试同事进行测试，再到部署在预发布环境，测试同事进行测试，最后再上线，部署到线上环境。总体来说流程还是挺规范的。

另外，对于一些公共组件也有规范要求，比如有公司内部的统一日志包等。

## 博客记录

因为新技术的使用经常会遇到各种各样的问题，有时候是基础问题，有时候却是不限语言的通用技术。比如和前端联调的时候，发现了 Golang 跨域的问题，学习了相关的博客文章做了点笔记记录。平时遇到的 bug 什么的也陆续有博客记录，算是坚持的一个好的工作习惯。

![](https://raw.githubusercontent.com/Wonz5130/My-Private-ImgHost/master/img/image-20220430164957258-20220504004803271.png)

## 工作压力与节奏

新部门工作压力肯定是比之前部门更大了。因为项目和业务更加有直接联系，这就导致了 deadline 一般都是定死的，很少有 delay 的情况被允许。反正我到现在还是很害怕每周一甚至每天的早会，汇报前一天工作进度的时候生怕自己效率不够高，拖延了工作进度。

## 同事相处

转岗之后和新部门的同事聚过一次餐，新部门全是男的，没有一个女同事（太惨了）！聚餐的时候倒是挺随意，撸串 + 啤酒，就熟络开了。

因为我是刚上手开发 Golang 项目，经常问同事们问题，逮一个问一个，但是看同事们每天工作也挺忙，有时候也不好意思。有一次周五晚上麻烦同事帮我解决一个问题一直解决到了 20:30 下班，才总算搞出来，还挺不好意思的，耽误同事早点下班过周末了。

# 写在后面

不管是转岗前所在的团队，还是转岗后所在的团队，我都觉得很不错，庆幸自己人品好，遇到的 leader 和同事们人都不错。在公司见到之前团队的同事也会叫一声“xxx老师好”，问问最近怎么样，总体来说我挺喜欢前团队的同事们和现团队的同事们的。

前段时间和一个朋友吃饭聊到工作。我觉得大多数人不喜欢工作，是因为工作并没有给自己带来成就感。

比如我以前并不喜欢工作，因为工作内容激不起自己的热情。因此更想「玩」。但是真正遇到能激发自己热情的工作的时候，发现做起来成就感会很多，自然而然就会有动力去努力工作，当然这里指的是在工作时间。前提还是工作和生活要分开，追求 work life balance。

最后，期待自己技术变强的那一天早日到来，希望那时候还有头发：）
