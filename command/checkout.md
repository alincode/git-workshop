# git checkout 指令

checkout 可用於將特定版本檔案取出，無論是資料夾或檔案皆可。

### 使用情境

* 切換分支
* 透過 `git checkout -- README.md`，還原尚未 commit 的最新的變動

### 常用指令範例

| 範例                        | 說明                            |
|---------------------------|-------------------------------|
| git checkout README.md    | 取出 README.md 檔案               |
| git checkout docs/        | 取出特 docs 資料夾                  |
| git checkout dev          | 取出 dev 分支                     |
| git checkout -b dev       | 新增 dev 分支，並同時切換到 dev 分之上      |
| git checkout -- README.md | 將 README.md 恢復到上一次 Commit 的狀態 |

### HEAD

```
git checkout HEAD^
// 相同
git reset @^
```

### 練習題：切換到 dev1 分支位置，並送交一個新的紀錄。

1. 透過 `git checkout dev1` 指令，來切換到 `dev1` 分支位置。
1. 透過 `vi a.txt` 指令，來編輯 a.txt 檔案內容
1. 透過 `git add .` 和 `git commit -m 'dev1 d1'` 來新增一筆紀錄。
1. 透過 `git log --oneline --decorate --graph --all` 來查看

```
* 98841bf (HEAD -> dev1) dev1 d1
* 957d1b3 (master, dev2) m3
* a26b247 m2
* 20ab970 m1
```

### 練習題：還原尚未送交的變動

1. 透過 `vi b.txt` 指令，來編輯 b.txt 檔案
1. 透過 `git checkout b.txt` 指令，還原修改的內容

---
### 語法結構

```
usage: git checkout [<options>] <branch>
   or: git checkout [<options>] [<branch>] -- <file>...

    -q, --quiet           suppress progress reporting
    -b <branch>           create and checkout a new branch
    -B <branch>           create/reset and checkout a branch
    -l                    create reflog for new branch
    --detach              detach the HEAD at named commit
    -t, --track           set upstream info for new branch
    --orphan <new-branch>
                          new unparented branch
    -2, --ours            checkout our version for unmerged files
    -3, --theirs          checkout their version for unmerged files
    -f, --force           force checkout (throw away local modifications)
    -m, --merge           perform a 3-way merge with the new branch
    --overwrite-ignore    update ignored files (default)
    --conflict <style>    conflict style (merge or diff3)
    -p, --patch           select hunks interactively
    --ignore-skip-worktree-bits
                          do not limit pathspecs to sparse entries only
    --ignore-other-worktrees
                          do not check if another worktree is holding the given ref
    --progress            force progress reporting
```