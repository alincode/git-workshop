# git branch 指令

### 為什麼我們需要分支 (branch)

* 快速試錯
* 切換不同情境的分支


```
$ git branch --all
  dev1
  dev2
* master
```

<!-- 
### 名稱

* 絕對名稱
* 參照名稱

```
refs/head
refs/remotes
refs/tags
``` 
-->

### 常用範例

| 範例                          | 說明                                |
|------------------------------|-------------------------------------|
| git branch                   | 列出 local 分支                      |
| git branch dev               | 新增目前位置的 dev 分支                |
| git branch dev sha1234       | 新增指定位置的 dev 分支                |
| git branch -a                | 列出所有分支                          |
| git branch -r                | 列出遠端分支                          |
| git branch -m dev dev2       | 更改分支名稱                          |
| git branch -d dev2           | 刪除分支                             |
| git branch -D dev2           | 強迫刪除分支 (即使分支，還沒被 merge 過) |
| git push origin dev          | 發佈 dev 分支                        |
| git push origin --delete dev | 刪除遠端分支                          |
| git remote prune origin      | 刪除 remote 底下所有過時的分支         |

### 練習題：新增三個分支，並刪除 `dev3` 分支。

```
echo "Hello World" >> a.txt && git add . && git commit -m 'm1'
echo "2" >> b.txt && git add . && git commit -m 'm2'
echo "3" >> c.txt && git add . && git commit -m 'm3'
```

1. 透過 `git branch dev1` 指令，建立 `dev1` 分支
1. 透過 `git branch dev2` 指令，建立 `dev2` 分支
1. 透過 `git branch dev3` 指令，建立 `dev3` 分支
1. 透過 `git branch` 指令，查看所有分支
1. 透過 `git branch -d dev3` 指令，刪除 `dev3` 分支
1. 透過 `git branch` 指令，查看所有分支

---
### 語法結構

```
usage: git branch [<options>] [-r | -a] [--merged | --no-merged]
   or: git branch [<options>] [-l] [-f] <branch-name> [<start-point>]
   or: git branch [<options>] [-r] (-d | -D) <branch-name>...
   or: git branch [<options>] (-m | -M) [<old-branch>] <new-branch>
   or: git branch [<options>] [-r | -a] [--points-at]
```
