# Github学习笔记

## 学习目标

- 了解Git基本概念
- 概述Git工作流程
- 使用Git常用命令
- 熟悉Git代码托管服务
- 使用idea操作Git

## Git工作流程

![屏幕截图 2024-08-24 134221](C:\Users\Johnkey\OneDrive - University of Leeds\Pictures\Screenshots\屏幕截图 2024-08-24 134221.png)

## 配置Git

打开`git bash`并配置用户信息

```shell
git config --global user.name "XXX"
git config --global user.email "XXX"
```



## 本地仓库

创建本地仓库，首先在某个指定的文件夹下打开`git bash`，并输入

```shell
git init
```

将会得到如下输出

```shell
Initialized empty Git repository in C:/Users/Johnkey/OneDrive/Desktop/Johnkey/Study/learn-git/.git/
```

## Git常用指令

将文件从工作区（workspace）添加到暂存区（index）

```bash
git add .
```

将文件从暂存区（index）提交到仓库（repository）

```bash
git commit -m "XXX"
```

