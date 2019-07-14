# git stash 指令

將變更的內容，先移到暫存區 (stash)。

### 使用情境

* 通常用於臨時必須要切換到其他分支，但現在工作做到一半還不能送交時，就先把修改存起來在切到其他分支，等事情做完之後，再回來把紀錄取出來，繼續剛剛未完成的工作。

### 常用範例

| 範例                         | 說明                 |
|-----------------------------|----------------------|
| git stash                   | 暫時儲存當前目錄        |
| git stash pop               | 取出最新的一筆, 並移除  |
| git stash list              | 列出所有暫存區的資料    |
| git stash clear             | 把 stash 都清掉       |
| git stash drop <stash_name> | 清掉單一筆暫存         |

### 練習題：將未完成的更改放入暫存區，並且之後可以重新取出。

1. 透過 `git checkout dev1`，切換到 `dev1` 分支
1. 透過 `vi b.txt` 指令，編輯 b.txt 檔案
1. 因為某種需求臨時要先切換到 `dev2` 分支，進行其他項目的實作。
1. 透過 `git stash` 指令，將檔案暫時放置在暫存區
1. 透過 `git stash list` 指令，確認真的有暫存了
1. 透過 `git checkout dev2`
1. 透過 `vi a.txt` 指令，編輯 a.txt 檔案
1. 透過 `git add .` 指令，新增索引。
1. 透過 `git commit -m 'dev2 d1'` 指令，新增一個送交紀錄
1. 透過 `git checkout dev1` 指令，回到 `dev1` 分支。
1. 透過 `git stash pop` 指令，將存擋取出。
1. 透夠 `git checkout .` 指令，還原修改記錄。

---
### 語法結構

```
usage: git stash list [<options>]
   or: git stash show [<stash>]
   or: git stash drop [-q|--quiet] [<stash>]
   or: git stash ( pop | apply ) [--index] [-q|--quiet] [<stash>]
   or: git stash branch <branchname> [<stash>]
   or: git stash [save [--patch] [-k|--[no-]keep-index] [-q|--quiet]
                       [-u|--include-untracked] [-a|--all] [<message>]]
   or: git stash clear
```