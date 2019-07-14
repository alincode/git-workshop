# git rm 指令

刪除不需要紀錄的檔案

### 常用範例

| 範例                        | 說明                               |
|----------------------------|-----------------------------------|
| git rm README.txt          | 將檔案從儲存庫和工作目錄中刪除         |
| git rm README.txt --cached | 將檔案從儲存庫中刪除，但保留在工作目錄中 |

### 練習題：移除 log，並確保之後沒有人可以在把 log 送交到儲存庫。

1. 透過 `touch system.log`，新增一筆 log。
1. 透過 `git add .`，將更變建立索引。
1. 透過 `git commit -m 'add log'`，新增 commit 紀錄。
1. 透過 `git rm system.log` 指令，刪除 system.log 檔案
1. 透過 `git commit -m 'remove log'` 指令，將刪除檔案的紀錄送交給 repo。
1. 透過 `touch .gitignore` 指令，新增 .gitignore 檔案。
1. 編輯 .gitignore 檔案，加入 *.log
1. 透過 `git add .`，將更變建立索引。
1. 透過 `git commit -m 'add ignore file'`，新增 commit 紀錄。
1. 透過 `touch system.log`，新增一筆 log。
1. 透過 `git status`，查看狀態

### 語法結構

```
usage: git rm [<options>] [--] <file>...

    -n, --dry-run         dry run
    -q, --quiet           do not list removed files
    --cached              only remove from the index
    -f, --force           override the up-to-date check
    -r                    allow recursive removal
    --ignore-unmatch      exit with a zero status even if nothing matched
```