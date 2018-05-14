# git stash 指令

暫存
### 常用範例

| 範例                          | 說明           |
|-----------------------------|--------------|
| git stash                   | 放入暫存區        |
| git stash list              | 列出所有暫存區的資料   |
| git stash pop               | 取出最新的一筆, 並移除 |
| git stash clear             | 把 stash 都清掉  |
| git stash drop <stash_name> | 清掉單一筆暫存      |


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