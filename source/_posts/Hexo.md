---
title: 搭建Hexo博客（Next主题）过程中碰到的问题
date: 2018-09-11 11:07:54
tags: [Hexo]
categories: Hexo
---

github主页：https://github.com/iissnan/hexo-theme-next 

## 侧边菜单修改却无法访问

在next的_config.yml文件中修改menu配置，添加tag和categories选项，但点击会出现404页面。

### 解决办法：

在根目录执行以下命令：
``` bash
hexo new page "tags" 
hexo new page "categories"
```
打开它们并相应添加type: "tags"和type: "categories"，保存

----------------------------
## 安装搜索功能 Local Search

在next的_config.yml文件中修改Local Search的enable: true后，搜索功能仍无效

### 解决办法：
安装 hexo-generator-search和 hexo-generator-searchdb

在根目录下执行以下命令：
``` bash
$ npm install hexo-generator-search --save
$ npm install hexo-generator-searchdb --save
```

在根目录的_config.yml文件中添加
``` bash
search:
  path: search.xml
  field: post
  format: html
  limit: 10000
```
