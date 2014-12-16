---
layout: post
title: Python中常用的相关文件操作
category: python
---

### 获取当前工作目录

    os.getcwd()

### 获取执行脚本所在路径

    sys.path[0]

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

### 格式化输出字符串

    'Test str {key1} {key2}'.format(key1='hello', key2='world')
    "My name is %s and weight is %d kg!" % ('Zara', 21)

### 计算文件的MD5值

        from hashlib import md5
        m = md5()
        file = open(path, 'rb')
        m.update(file.read())
        file.close()
        md5_str = m.hexdigest()

### 按行读取配置文件内容

    fp = open(path, 'r')
    while 1:
        line = fp.readline().strip('\r\n')
        if not line:
            break
        print line
    fp.close()
