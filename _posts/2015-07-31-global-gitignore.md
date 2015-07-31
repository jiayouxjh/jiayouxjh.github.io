---
layout: post
title: 设置全局的.gitignore
category: linux
---

### 设置指定全局.gitignore

    git config --global excludesfile 用户目录

    或者用户目录下的.gitconfig文件中的core标签下加上
        excludesfile = /Users/xujh/.gitignore_global

### 建立.gitignore_global

    在用户目录下（如/Users/xujh/)建立.gitignore_global文件，并添加自己的缺省设置

### .gitignore语法

    # 以'#' 开始的行，被视为注释.

    # 忽略掉所有文件名是 foo.txt 的文件.
    foo.txt

    # 忽略所有生成的 html 文件,
    *.html

    # foo.html是手工维护的，所以例外.
    !foo.html

    #  忽略所有.o 和 .a文件.
    *.[oa]
