# Github学习笔记

## 学习目标

- 了解Git基本概念
- 概述Git工作流程
- 使用Git常用命令
- 熟悉Git代码托管服务
- 使用idea操作Git

## Git工作流程

![屏幕截图 2024-08-24 134221](./image/1.png)

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

查看当前git的状态

```bash
git status
```

查看日志

```bash
git log [option]
```

[option]中可选的参数

- `--all`显示所有分支
- `--pretty==oneline`将提交信息显示为一行
- `--abbrev-commit`使得输出的commitID更简短
- `--graph`以图的形式显示

这条指令我们能够看到输出如下

```bash
commit 13990657169b1f85dcc85717755867139ba2ddad (HEAD -> master)
Author: Johnkey00 <1176023870@qq.com>
Date:   Sun Aug 25 09:57:12 2024 +0800

    20240825-first-commit
```

版本回退

```bash
git reset --hard commitId
```

有一些文件我们不想让Git来管理，这个时候如果输入`git status`指令会显示这些文件untracked，比如我有一系列`.a`格式的文件，我不想让Git管理这些文件，这个时候可以考虑加入一个新的文件名为`.gitignore`，输入指令

```bash
touch .gitignore
```

然后编辑这个文件，将不想被管理的文件名写入该文件即可，我创建了`ignore01.a`和`ignore02.a`这两个文件，接着我在`.gitignore`中输入

```bash
ignore01.a
ignore02.a
```

或者输入

```bash
*.a
```

再次输入`git status`就看不到untracked的`ignore01.a`和`ignore02.a`了

## 分支

查看分支

```bash
git branch
```

创建分支

```bash
git branch XXX
```

切换分支

```bash
git checkout XXX
```

创建并切换分支

```bash
git checkout -b XXX
```

合并分支

```bash
git merge XXX
```

删除/强制删除分支

```bash
git branch -d XXX
git branch -D XXX
```

## 解决冲突

在合并时发现如果两边同时修改了同一个地方，就会发生冲突，需要开发者来解决
