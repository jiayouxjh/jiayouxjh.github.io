---
layout: post
title: VIM下使用自定义代码片段
category: code_about
---

### 常见片段定义

#### 片段内置默认文本(占位符可以包含其他UltiSnips元素)

        snippet a
        <a href="$1"${2: class="${3:link}"}>
           $0
        </a>a>
        endsnippet

#### 单词开头自动大写

        snippet title "Titelize in the Transformation"
        ${1:a text}
        ${1/\w+\s*/\u$0/g}
        endsnippet

#### 条件替换

        snippet cond
        ${1:some_text}${1/(o)|(t)|..*/(?1:ne)(?2:wo)/}
        endsnippet

#### 部分单词提示(以触发字结尾即可触发)

        snippet ri "rizer" i
        rizer
        endsnippet

#### 有规律的表达式的触发提示

        snippet "chap?t?e?r?" "Latex chapter" rb
        \section{chapter}
            $0
        \end{chapter}
        endsnippet

#### 特殊字符串触发提示

        snippet " this is a trigger" "Multiword & Whitespace" r
        Hello World
        endsnippet

#### 查看UltiSnips文档

        :help UltiSnips
