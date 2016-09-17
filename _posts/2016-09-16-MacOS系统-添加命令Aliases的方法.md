---
layout:     post
title:      "MacOS系统 添加命令Aliases的方法"
subtitle:   "MacOS System: How to add Aliases"
date:       2016-09-16
author:     "Haotian"
header-img: "img/post-bg-2015.jpg"
tags:
    - MacOS
    - Terminal
    - Bash
    - Zsh
  
---

### 创建临时Alias

创建一个临时的Alias只会在当前terminal有效，关闭后则失效

```
$ alias new_name='command to be performed'
## Example 
$ alias github="cd /Users/haotianyin/Documents/GitHub"
```

### 永久存储Alias

我们可以添加环境变量来永久保存alias，这里我们使用VIM

```html
## 添加到bash
vim ~/.bash_profile 
## 添加到zsh
vim ~/.zshrc
```

最后关闭当前terminal，重新打开就好啦



