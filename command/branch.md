# Branch

分支

### 使用情境

* 可以讓你的系統依據不同的需求分別進行開發，又不互相影響。

### 名稱

* 絕對名稱
* 參照名稱

```
refs/head
refs/remotes
refs/tags
```

### 常用範例

| 範例                       | 說明  |
|--------------------------|-----|
| git branch <branch_name> |     |
| git branch               |     |
| git branch -r            |     |
| git branch -a            |     |
| git branch -m <old_branch_name> <new_branch_name> | |
| git branch -d <branch_name> | delete fully merged branch |
| git branch -D <branch_name> | delete branch (even if not merged) |

### 語法結構

```
usage: git branch [<options>] [-r | -a] [--merged | --no-merged]
   or: git branch [<options>] [-l] [-f] <branch-name> [<start-point>]
   or: git branch [<options>] [-r] (-d | -D) <branch-name>...
   or: git branch [<options>] (-m | -M) [<old-branch>] <new-branch>
   or: git branch [<options>] [-r | -a] [--points-at]
```
