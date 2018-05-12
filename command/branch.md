# Branch 分支

語法結構

```
usage: git branch [<options>] [-r | -a] [--merged | --no-merged]
   or: git branch [<options>] [-l] [-f] <branch-name> [<start-point>]
   or: git branch [<options>] [-r] (-d | -D) <branch-name>...
   or: git branch [<options>] (-m | -M) [<old-branch>] <new-branch>
   or: git branch [<options>] [-r | -a] [--points-at]
```

### 常用指令範例

| 範例                       | 說明  |
|--------------------------|-----|
| git branch <branch_name> |     |
| git branch               |     |
| git branch -r            |     |
| git branch -a            |     |
| git branch -m <old_branch_name> <new_branch_name> | |
| git branch -d <branch_name> | delete fully merged branch |
| git branch -D <branch_name> | delete branch (even if not merged) |

### 練習題

1. 使用 `git branch develop` 指令來建立 `develop` 分支
1. 使用 `git checkout develop` 指令來切換至 `develop` 分支
1. 新增一個叫 `develop.txt` 檔案 `git add develop.txt`
1. 透過 `git commit -m 'add develp.txt file'` 送交 commit
1. 確認已有新的分支產生 `git log --graph --oneline --decorate --all`

<!-- 
補充
git checkout -b develop
-->