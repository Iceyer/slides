title: 深度开发框架构建
description: 深度开发团队发展过程中的遇到的基础开发库的问题与解决思路
theme: ../themes/remark-dark.css
name: inverse
layout: true
class: inverse

---
class: center middle

# 深度开发框架建设

[Iceyer]

---

class: center middle

# 开发中存在的问题?

---

## 开发中存在的问题?

### 设计风格不统一

### 基本框架不稳定

### 技术管理不够

### 文档！文档！文档！

---

class: menu

## 设计风格不统一

* 6个应用，6种风格

<img src="https://cloud.githubusercontent.com/assets/1117694/12353383/cdf42eca-bbc9-11e5-98b4-157d06ba06d3.png" alt="Drawing" width="600px" />

---

class: menu

## 设计风格不统一

* 同一种风格，不同的细节

<img src="https://cloud.githubusercontent.com/assets/1117694/12354022/f7c28270-bbcd-11e5-8209-d2cb36fcd471.png" alt="Drawing" width="600px" />

---

class: menu

## 基础框架不稳定

### 2012/2013: Python

* 对Python系统库进行hack，破坏其他发行版本依赖，后续版本已解决
* 不知道为啥就放弃python了，性能？

### 2014: QML/golang

* QML技术并不成熟，显卡驱动支持不好
* HTML5/Webkit无法维护（小强深受其害）
* golang基本稳定
* 性能，性能，性能！！！

### 2015: Qt/C++/golang

* Qt/C++就是要折腾，重新工作量巨大

---

class: menu

## 基础框架不稳定

#### 生命不息，折腾不止

#### 应用框架每年就要变换一次， 人力资源损耗巨大， 许多基础库处于半完成状态就被废弃。

  * deepin-ui/qml-widget

#### 框架维护较少，没有时间重构，代码copy。

  * 桌面对话框， libdui/dde-desktop/clouprint各有一套类似的代码。

  * gettext中的QueryLang接口在deepin-file-backend中有一份相似又不完全兼容的实现。

---

class: menu

## 技术管理不够

* 开发规范（编码规范、API规范，技术评估）

   配置文件到处都是，日志命名逼死强迫症

* 开发流程

* 过程管理

#### 以上没有或者不完善

---

class: center middle

# 如何改进

---

class: menu

## 应用开发:  统一设计规范并严格实行


* 已有设计规范实施不严格，导致开发人员无法有效重构代码。


#### 这个问题并不严重，并且很多是历史遗留问题

---

class: menu

## 技术选型: 拒绝折腾

* 稳定的使用Qt/C++/Golang进行桌面环境开发

#### 可行性较高

---

class: menu

## 及时重构: 制定规范，及时改进

* 编码规范
* API设计原则，应用API，桌面API，系统API，lib/DBUS接口
* 重复代码去除，开发之间加强沟通，避免冲突和重复工作

#### 耗时耗力，实施困难，需要长期有效的进行监督和推动

---

class: menu

## Tookit构建: Deepin Development Framework， not Deepin Theme

* 借鉴KDE，抽取公共模块。golang已经完成了部分工作，Qt/C++基本没有。支持后续更多应用的开发工作。

#### 耗时耗力，实施困难，需要长期有效的进行监督和推动

---

class: menu

## 开发文档

* 对于稳定的公共库，必须有开发文档， 如libdui/golib。

* 文档生成工具，godoc/doxygen/Qt-Doc

* 方便开发内部交流以及和社区对接

#### 耗时耗力，实施困难，需要长期有效的进行监督和推动

