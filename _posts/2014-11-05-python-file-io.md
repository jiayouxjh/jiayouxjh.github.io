---
layout: post
title: Python中常用的相关文件操作
category: python
---

### 获取当前工作目录

    os.getcwd()

### 判断目录是否存在

    os.path.exists(path)  返回false表示不存在

### 删除一个非空的目录

    import shutil
    shutil.rmtree(path)

### 创建单个（多个）目录

    os.mkdir(name)
    os.makedirs("dir1/dir2")

### 判断文件是否存在

    os.path.isfile(path)

### 删除一个文件

    os.remove(path)

### 获取文件大小

    os.path.getsize(filename)
