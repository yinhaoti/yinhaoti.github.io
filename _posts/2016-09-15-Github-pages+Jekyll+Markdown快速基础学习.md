---
layout:     post
title:      "Github pages+Jekyll+Markdown快速基础学习"
subtitle:   "Github pages+jekyll+markdown Study Notes"
date:       2016-09-15
author:     "Haotian"
header-img: "img/post-bg-2015.jpg"
tags:
    - Github Pages
    - Jekyll
    - Markdown
    - 学习笔记
  
---

### 1 Github Pages的学习

#### 1.1 Pages有两种模式：

* User/Organization Pages
*  Project Pages

通常通过User/Organization Pages建立主站，Project Pages挂载二级应用界面

#### 1.2 常用命令：

```shell
$ git clone git@github.com:username/username.github.com.git //本地如果无远程代码，同步到本地
$ git pull origin master //先同步远程文件，后面的参数会自动连接你远程的文件
$ git status //查看本地自己修改了多少文件
$ git add . //添加远程不存在的git文件
$ git commit -m "leave a message"
$ git push origin master //更新到远程服务器上

```

### 2 Jekyll的搭建

* Jekyll是一种简单的、适用于博客的、静态网站生成引擎
* jekyll与github的关系：GitHub Pages一个由 GitHub 提供的用于托管项目主页或博客的服务，jekyll是后台所运行的引擎

#### 2.1 Jekyll的命令

```shell
$ jekyll --version //检测版本
$ jekyll --server //启动工程 本地预览 http:127.0.0.1:4000
```

#### 2.2 Jekyll目录结构

* __posts： _posts中的数据文档，通过注入_layouts定义的模板，通过jekyll --server最终生成的静态页面在_sites目录。目录是用来存放你的文章的，一般以日期的形式书写标题。

* __layouts：_layouts中的模板一般指向了_includes/themes中的模板。目录是用来存放模板的，在这里你可以定义页面中不同的头部和底部。

* _includes：

  ```
  1) _includes/JB中有一些常用的工具，用于列表显示、评论等；

  2) _includes/themes中可参看主题的相关html文档。

  3) _includes/themes中的主题一般包含default.html、post.html和page.html三个文档。default.html定义了网站的最上层框架（模板），post.html和page.html是其子框架（模板）。

  4) 生成好的html子页面通过default.html的{{ content }}变量调用，生成整个页面。
  ```

* assets 渲染页面的CSS和JS文档在assets/themes中

*  _config.yml 站点生成需要用到_config.yml配置文件，站点的全局变量在_config.yml中定义，用site.访问；页面的变量在YAML Front Matter中定义，用page.访问，更多的模板变量可参考模板数据。

*  index.html是你的页面首页。

### 3 Markdown基本语法

* 使用空行来生成段落
* 使用“#”来做h1-h6的标题
* 使用“>”作为段落前缀来标识引用文字段落，这其实是 email 中标记引用文字的标准方式
* 使用 * + - 表示无序列表；使用数字和 . 表示有序列表
* 使用 ```[test](http://example.net "optional title") ```来标记普通链接
* 使用```![img](http://example.net/img.png "optional title") ``` 来标记图片。
* 使用多个 * 或 _ 包裹文本产生 strong 效果



#### 

### 本文内容参考于:

[通过GitHub Pages建立个人站点（详细步骤）](http://www.cnblogs.com/purediy/archive/2013/03/07/2948892.html"optional title")









