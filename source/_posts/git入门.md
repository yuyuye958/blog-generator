---
title: git入门
date: 2018-09-10 23:57:00
tags: [git]
categories: git
---


### git版本控制中几个重要概念
``` bash
1.git init
    初始化本地仓库 .git
2.git add
    文件路径，用来将变动加到暂存区
3.git commit -v
    提交时显示所有diff信息
```

### 使用git前配置
``` bash
git config --global user.name 你的英文名
git config --global user.email 你的邮箱
git config --global push.default matching
git config --global core.quotepath false
git config --global core.editor "vim"
```

### 常用命令
``` bash
git init //不要在已经初始化好的仓库使用，否则会将已经初始化完成的仓库覆盖
git status //查看状态
git add //提交文件放入暂存区
git commit  //将暂存区的更新提交到本地仓库
git push origin master //把当前本地仓库里的改动推送到远程仓库（origin）的master分支。之后可以直接git push。
git pull //当远程仓库有变动但是本地仓库没有更新，会拒绝git push， 使用git pull将远程仓库拉到本地仓库，合并变动。
git push -f origin master //强制推送，会覆盖别人的代码
git remote add xxx git@xxx.git //再次添加一个远程仓库的标签
git push xxx master //推送到xxx标签的地址
git remote remove xxx //删除xxx标签
git remote set-url origin url //修改origin标签对应的地址
git remote rename xxx coding //把xxx标签名修改为coding
```

### 实例
打开 git bash，进入某目录后输入以下命令：
``` bash
cd blog -- 进入blog文件夹
git init -- 初始化本地仓库，创建.git目录
touch index.html -- 添加index.html文件
git add index.html -- 将文件添加到暂存区 (也可以使用git add . 表示将当前目录内所有改动都加入暂存区)
git commit index.html -m '添加index.html' 告诉 git，这些文件我要加到仓库里(也可以一次性git commit -m "添加所有改动文件")
```