# 初始化專案

裸容器 (bare)：一個沒有工作目錄的容器

### 常用範例

| 範例              | 說明  |
|-----------------|-----|
| git init        |     |
| git init --bare |     |

### 語法結構

```
usage: git init [-q | --quiet] [--bare] [--template=<template-directory>] [--shared[=<permissions>]] [<directory>]

    --template <template-directory>
                          directory from which templates will be used
    --bare                create a bare repository
    --shared[=<permissions>]
                          specify that the git repository is to be shared amongst several users
    -q, --quiet           be quiet
    --separate-git-dir <gitdir>
                          separate git dir from working tree
```