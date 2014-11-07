title: Git Flow 开发实践
description: Git Flow及其工具 git flow介绍
theme: ../themes/remark-dark.css
name: inverse
layout: true
class: inverse

---
class: center middle

# Git Flow 开发模型及gitflow使用介绍  
Iceyer 

---

class: menu

# What is Git Flow

 * [A successful Git branching model](http://nvie.com/posts/a-successful-git-branching-model/)

 * 软件组织开发活动模型
 * 管理使用git开发过程分支混乱情况

---

class: center middle

# What is Git Flow

<img src="http://nvie.com/img/git-model@2x.png" alt="Drawing" width="200px" />

---

class: menu

# Main & Supporting Branches

 * master

    production release

 * develop

    nightly builds, integration branch

 * feature
    
    branch off develop, merge back to develop, use to develop new feature

 * release
    
    branch off develop, merge back to develop & master
    deal with pre-release

 * hotfix

    branch off master, merge back to develop & master
    for critical bug fix after release


