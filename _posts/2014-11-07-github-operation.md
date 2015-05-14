---
layout: post
title: 常用的Git操作
category: linux
---

### 初始化操作

    git config -global user.name <name>     #设置提交者名字

    git config -global user.email <email>   #设置提交者邮箱

    git config -global core.editor <editor> #设置默认文本编辑器

    git config -global merge.tool <tool>    #设置解决合并冲突时差异分析工具

### 修改和提交

    git add .                       #添加所有改动过的文件

    git add <file>                  #添加指定的文件

    git mv <old> <new>              #文件重命名

    git rm <file>                   #删除文件

    git rm -cached <file>           #停止跟踪文件但不删除

    git commit -m <file>            #提交指定文件

    git commit -m "commit message"  #提交所有更新过的文件

    git commit -amend               #修改最后一次提交

    git commit -C HEAD -a -amend    #增补提交

### 查看提交历史

    git log            #查看提交历史

    git log -p <file>  #查看指定文件的提交历史

    git log HEAD       #查看已经add但还没有commit的文件

    git blame <file>   #以列表方式查看指定文件的提交历史

    git status         #查看当前状态

    git diff           #查看变更内容

### 撤销操作

    git reset --hard HEAD               #撤销工作目录中所有未提交文件的修改内容

    git checkout HEAD <file1> <file2>  #撤消指定的未提交文件的修改内容

    git checkout HEAD .                #撤消所有文件

    git revert <commit>                #撤消指定的提交

### 分支和标签

    git branch                     #显示所有本地分支

    git checkout <branch/tagname>  #切换到指定分支或标签

    git branch <new-branch>        #创建新分支

    git branch -d <branch>         #删除本地分支

    git branch -va                 #查看远程仓库的其他分支

    git checkout -b a origin/a     #切换远程分支

    git tag                        #列出所有本地标签

    git tag <tagname>              #基于最新提交创建标签

    git tag -d <tagname>           #删除标签

    git merge <branch>             #合并指定分支到当前分支

    git rebase <branch>            #衍合指定分支到当前分支

### 远程操作

    git remote -v                           #查看远程版本库信息

    git remote show <remote>                #查看指定远程版本库信息

    git remote add <remote> <url>           #添加远程版本库

    git fetch <remote>                      #从远程库获取代码

    git pull <remote> <branch>              #下载代码及快速合并

    git push <remote> <branch>              #上传代码及快速合并

    git push <remote> : <branch>/<tagname>  #删除远程分支或标签

    git push -tags                          #上传所有标签
