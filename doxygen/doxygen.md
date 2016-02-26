title: 开发文档生成与展示
description: 介绍https://gowalker.org/如果生成和展示文档。介绍Doxygen如何展示和自动生成文档。
theme: ../themes/remark-dark.css
name: inverse
layout: true
class: inverse

---
class: center middle

# 开发文档生成与展示
Iceyer

---

class: menu

## 文档类型

### 设计文档：
描述项目整体设计的文档, 托管在github的wiki上。

https://github.com/linuxdeepin/developer-center/wiki

### API文档：

#### Golang项目：

https://gowalker.org/search?q=github.com/linuxdeepin/

#### Qt/C++ 项目

https://docs.deepin.io/api/dtk

---

## Golang 项目文档浏览

https://gowalker.org/search?q=github.com/linuxdeepin/

```
godoc -http ':8081'
```

---

## Doxygen 简单介绍

Offical Website： [Doxygen: Main Page](http://www.doxygen.org)

### 基本特性

1. 跨平台.
2. C++文档生成工具，同时支持其他语言（C, Objective-C, C#, PHP, Java, Python, IDL (Corba, Microsoft, and UNO/OpenOffice flavors), Fortran, VHDL, Tcl, and to some extent D.）
3. 可以输出html，rtf，latex，方便在线展示.
4. 支持输出Markdown文档

---

## Doxygen 基本使用

```
#生成配置文件
doxygen -g

# 修改配置文件...

#输出文档
doxygen
```

---

## Doxygen 配置文件介绍

```
PROJECT_NAME           = "Deepin Tool Kit"
PROJECT_NUMBER         = 1.0.0

OUTPUT_DIRECTORY       = Docs
INPUT                  = ./deepin-tool-kit

ENABLE_PREPROCESSING   = YES
MACRO_EXPANSION        = YES
EXPAND_ONLY_PREDEF     = NO
SEARCH_INCLUDES        = YES
INCLUDE_PATH           = ./deepin-tool-kit/dbase \
                         ./deepin-tool-kit/dutil \
                         ./deepin-tool-kit/dwidget \

```

---

## 文档自动更新

<img src="https://cloud.githubusercontent.com/assets/1117694/13343016/c157c210-dc82-11e5-9658-10b7283b14c4.png" alt="Drawing" />
---

## Doxygen 文档展示

[Deepin Tool Kit 文档](
https://docs.deepin.io/api/dtk/)

---

class: center middle

# Thanks
