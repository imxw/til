---
title: 使用git show检查指定 commit
date: 2023-03-12 18:22
---
# 使用`git show`检查指定 commit

## 查看指定 commit 的变更总结

```bash
git show <commmit> --stat
```

示例如下

```bash
$ git show f71a3c9c --stat
```
![](./_image/2023-03-12/2023-03-12-18-31-03@2x.png)
`--stat`会展示所有变更文件的变更总结，如增加几行，删除几行

## 查看指定文件的 commit 变更

```bash
git show <commit> -- <filepath>
```

示例如下

```bash
$ git show f71a3c9c -- modules/images.py
```
![](./_image/2023-03-12/2023-03-12-18-28-28@2x.png)
会高亮展示变更内容