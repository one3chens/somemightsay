---

layout: post
title: Git Flow 分支模型
date: 2014-01-14 21:16
tags: [translate,git]

---

在这篇文章中我将介绍一种在过去一年中我一直在项目（工作项目和私有项目）中实践的Git开发模型，这种Git开发模型被证明是很成功的。我已经想写这篇文章有一段时间了，但是一直没有找到时间，直到现在。在这篇文章中我不会去谈及项目的细节，仅仅是讨论分支策略及发布管理。

![git-flow](https://dl.dropboxusercontent.com/u/24683331/blog_img/2014-01-14-a-successful-Git-branching-model-cn/git-flow.png) 

这种模型是基于[Git][ref_Git](版本控制工具)的。

## 为什么是Git

如果你想深入的讨论Git和中心化代码版本控制系统的优缺点，请[看][ref_see]这[里][ref_web]，那里还在火热的讨论当中。做为一个开发者，在当今所有的其他版本控制系统中我跟倾向于Git。Git完全改变了开发者对合并与分支的认识。在古老的CVS/SVN时代，合并和分支一直被认为是很可怕的事（“当心合并冲突把你弄崩溃”）而且每隔一段时间你只能做一件事情。

但是对于Git，那些操作都是极其简单和廉价的，他们绝对是你工作流中核心的一部分。例如，在CVS/SVN的[教程][ref_books]中，分支与合并操作首次被提及是在书中的后几个章节（给进阶用户看的），而在每本Git[教程][ref_every_Git_book]中，你早在第三章（基础知识）就发现他们。

考虑到分支与合并的简单和重复的特性，

由于简单和高重复的特性，分支与合并不应该再是惧怕的东西。版本控制工具应该更好的支持分支及合并操作。

讨论了完了工具，让我们开始讨论开发模型吧，我将呈现的本质仅仅是一些每个团队成员为了管理软件开发流程所遵循的procedures

## 分布式但是中心化

{To be continued}

[ref_see]: http://whygitisbetterthanx.com/ 
[ref_web]: http://git.or.cz/gitwiki/GitSvnComparsion
[ref_Git]: http://git-scm.com/	
[ref_books]: http://svnbook.red-bean.com/
[ref_every_Git_book]: http://pragprog.com/book/tsgit/pragmatic-version-control-using-git