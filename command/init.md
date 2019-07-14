# git init

初始化本地端儲存庫

### 使用情境

* 一開始要替你的專案加入版本控管的時後

### 常用範例

| 範例             | 說明                                        |
|-----------------|---------------------------------------------|
| git init        | 在目前資料夾，初始化本地端儲存庫。                |
| git init demo   | 建立一個空的 demo 資料夾，並將其初始化為本地端儲存庫。  |
| git init --bare | 建立一個裸容器 (沒有工作目錄)                    |

> 裸容器 (bare)：一個沒有工作目錄的容器，目錄通常會取名為 ooxx.git

### 練習題：建立本地端儲存庫

1. 透過 `mkdir demo` 指令，建立一個名字叫 demo 的空資料夾。
1. 透過 `cd demo` 指令，切換到 demo 目錄位置。
1. 透過 `git init` 指令，將目錄初始化成為一個本地端儲存庫。
1. 查看目錄下的檔案 `ls -al`

```
🤔 那跟直接使用 `git init demo` 指令，差在哪？
```

---

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