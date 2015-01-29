---
layout: post
title: 无处不在的Markdown
category: code_about
---

### 什么是Markdown

Markdown 是一种轻量级标记语言，创始人为约翰·格鲁伯（John Gruber）。它允许人们“使用易读易写的纯文本格式编写文档，然后转换成有效的XHTML(或者HTML)文档”。这种语言吸收了很多在电子邮件中已有的纯文本标记的特性。Markdown同时还是一个由Gruber编写的Perl脚本：Markdown.pl。它把用markdown语法编写的内容转换成有效的、结构良好的XHTML或HTML内容，并将左尖括号('<')和&号替换成它们各自的字符实体引用。

---

### 语法简介

 + 段落

    > 上下含有一个以上的空行，会被视为一个独立的段落。

 + 换行

    > 使用`<br>`标签，或是结尾处插入两个空格。

 + 标题

        标题1(最高阶)
        =============

        标题2(第二高阶)
        --------------

        # 这是H1

        ## 这是H2

        ###### 这是H6

 + 区块引用

     > 在行首或是段首使用区块`>`来建立引用区块(注意上下要有空行)，引用区块内可以使用其他的Markdown语法。

 + 无序列表

        + One
        + Two

    等同于

        * One
        * Two

    等同于

        - One
        - Two

 + 有序列表

        1. One
        2. Two

 + 代码区块

     > 建立代码区块很简单，只要简单地缩进 4 个空格或是 1 个制表符就可以。

 + 分割线

    > 在一行中使用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。

 + 强调
    > 使用星号（*）和底线（_）作为标记强调字词的符号，被 * 或 _ 包围的字词会被转成用 `<em>` 标签包围，用两个 * 或 _ 包起来的话，则会被转成 `<strong>`。

 + 链接

    + 行内式

            [链接文字](http://jiayouxjh.github.io/ "Title")

    + 参考式

            [id]:  http://jiayouxjh.github.io/ "Title"
            [链接文字][id]

 + 图片

    > 与添加链接的方法类似，只需要在开头加上 \! 即可。Markdown目前不支持指定图片的宽高，可以使用`<img>`来实现。

 + 代码

    > 标记一小段行内代码，可以用反引号把它包起来（\`），要在代码区段内插入反引号，可以用多个反引号来开启和结束代码区段。

---

### 使用Markdown同步印象笔记

 + geeknote

    > geeknote是一款使用python编写的命令行工具，可使用与Linux或是Mac的终端上。通过其提供的命令来实现使用Markdown编写修改指定账户下的相关笔记，包括同步指定目录。针对Evernote和印象笔记，geeknote有两个版本，用于不同服务器的同步工作。

 + Evernote版

    > [https://github.com/VitaliyRodnenko/geeknote](https://github.com/VitaliyRodnenko/geeknote "geeknote Evernote版")

 + 印象笔记版

    > [https://github.com/gmajian/geeknote](https://github.com/gmajian/geeknote "geeknote 印象笔记版")

---

### 转换格式

> 使用强大的pandoc，Github地址 [https://github.com/jgm/pandoc](https://github.com/jgm/pandoc "pandoc")

