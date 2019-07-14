# git add 指令

當執行了 add 指令，檔案放到預備「物件儲存」中，具有物件獨特的 sha 碼，Git 替這些更動建立了索引 (index)，隨時可以被 commit 進儲存庫中。

### 常用範例

| 範例                | 說明                       |
|--------------------|---------------------------|
| git add README.txt | 將指定的檔案建立 index       |
| git add .          | 將目前目錄現在更變建立 index  |
| git add --all       | 將所有變動的檔案建立 index  |

```
🤔 `git add .` 跟 `git add --all` 有什麼不同？
```

---
### 語法結構

```
usage: git add [<options>] [--] <pathspec>...

    -n, --dry-run         dry run
    -v, --verbose         be verbose

    -i, --interactive     interactive picking
    -p, --patch           select hunks interactively
    -e, --edit            edit current diff and apply
    -f, --force           allow adding otherwise ignored files
    -u, --update          update tracked files
    -N, --intent-to-add   record only the fact that the path will be added later
    -A, --all             add changes from all tracked and untracked files
    --ignore-removal      ignore paths removed in the working tree (same as --no-all)
    --refresh             don't add, only refresh the index
    --ignore-errors       just skip files which cannot be added because of errors
    --ignore-missing      check if - even missing - files are ignored in dry run
```