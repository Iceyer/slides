title: 深度开发者线下会议-二月份计划回顾
description:
theme: ../themes/remark-dark.css
name: inverse
layout: true
class: inverse

---
class: center middle

# 深度开发者线下会议
## 二月份计划回顾

Iceyer

---

class: menu

## 二月份预订计划

### Github Wiki规范推行

### 文档工作

### 项目自动检测代码质量CI上线

---

## Github Wiki规范推行

主要试推行Commit书写规范

除了dde-daemon规则比较特殊外，其他提交的commit规范基本能按照github要求进行书写。

<img src="https://github.com/Iceyer/slides/releases/download/DeepinDevelopmentFramework/c.png" width="600px" alt="Drawing" />

---

### Dtk/dde-daemon 文档工作

Dtk/dde-daemon文档主要通过注释完成， 通过注释量初步判断文档完成度

#### dde-daemon项目

```
commit 62ff4f1ce7ea6ac733df128ce3a4ad36585fda90
Author: jouyouyun <jouyouwen717@gmail.com>
Date:   Tue Feb 16 15:34:09 2016 +0800
```
```    
 Language  Files   Code  Comment  Blank  Total
         C     29   2111     1164    643   3890
        Go    385   1858    60890   7383  70126
  Markdown      3    127        0     49    176

```
注释比例 = （markdown_total_lines + all_code_comment_lines） / (all_code_lines + markdown_total_lines)

注释比例： (176+60890+1164) / (70126+3890+176) = 0.838769679

---

### Dtk/dde-daemon 文档工作

```
commit 265ff679ec714a5a62d10dea4ea8c9fa3f9b7365
Author: Xu Fasheng <fasheng.xu@gmail.com>
Date:   Wed Mar 23 16:06:14 2016 +0800
```
```
  Language  Files   Code  Comment  Blank  Total
         C     29   2173     1127    648   3920
        Go    391   1989    61151   7388  70521
  Markdown      3    128        0     49    177
```
注释比例： (177+1127+61151) / (70521+3920+177) = 0.836996435

dde-daemon 的注释率略有下降

ps. sloc统计似乎有问题。注释率太高了。

---

### Dtk/dde-daemon 文档工作

### Dtk项目

```
commit ea7fecebd31d0724a2b21faa48efe0ce3f3412a4
Author: Iceyer <me@iceyer.net>
Date:   Fri Feb 5 16:02:12 2016 +0800
```

```
-------------------------------------------------------------------------------
Language                     files          blank        comment           code
-------------------------------------------------------------------------------
C++                             74           3330           1567          10964
C/C++ Header                   100           1464            895           4333
XML                              1              0              0             44
IDL                              3             13              0             34
Bourne Shell                     1              1              0              2
-------------------------------------------------------------------------------
SUM:                           179           4808           2462          15377
-------------------------------------------------------------------------------
```

注释比例： 2462/15377 = 0.160109254

---

### Dtk/dde-daemon 文档工作

### Dtk项目

```
commit b4c02ecb8a384af31f739a32947904a5c509a7b8
Author: Iceyer <me@iceyer.net>
Date:   Thu Mar 24 00:01:49 2016 +0800
```
```
-------------------------------------------------------------------------------
Language                     files          blank        comment           code
-------------------------------------------------------------------------------
C++                             98           3706           1700          12644
C/C++ Header                   129           1721           1039           4988
IDL                              7             36              0            133
XML                              1              0              0             44
-------------------------------------------------------------------------------
SUM:                           235           5463           2739          17809
-------------------------------------------------------------------------------
```

注释比例： 2739/17809 = 0.153798641

---

### Dtk/dde-daemon 文档工作

dde-daemon: 83.9% --> 83.7%
dtk:        16.0% --> 15.4%

结果比较惨淡，从代码注释率结果来看，文档化在下降

原因：

   1. 开发时没有将文档放在重要地位
   2. 缺乏对应基本知识

建议：

 展开一个小的文档编写培训，提供大家的文档编写意识

---

## 项目自动检测代码质量CI上线

由于人员时间关系，本月未执行。

建议：

列入下个月的执行计划中。

---

## 补充： 仓库推送工作进度

本月已完成工作：

    1. 创建Review等基本功能
    2. 登录接入DeepinID/权限管理
    3. RPA推送机制
    4. 连接Jenkins CI，提供hook供其他项目使用

TODO List:

    1. 收集用户sources.list
    2. changelog展示
    3. 失效测试检测

预计上线时间：4月8日之前

## 4月主要工作计划

    1. 通过内部培训/代码review检查提高文档率
    2. 仓库推送上线
    3. 项目自动检测代码质量CI
    4. 国际化相关规范推行
