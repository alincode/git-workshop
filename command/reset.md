# git reset 指令

reset(重新指向)，具有三種模式：

* --mixed: 預設的模式，變成還沒加入 index 的狀態，但實際上的檔案修改還存在。
* --sort: 變成還沒 commit 的狀態，但已被加入 index。
* --hard: 把暫存區和工作目錄的檔案都丟掉。(注意：檔案會消失)

### 使用情境

* 將新增並已加入索引的檔案，還原到沒加入索引之前。
* 還原到過去某一個狀態，重新 commit。
* 強制清除某一個狀態的修改的內容

### 注意事項

* 只能用在未發佈的送交紀錄

### 常用範例

| 範例                     | 說明        |
|------------------------|-----------|
| git reset HEAD^        |           |
| git reset --sort HEAD^ |           |
| git reset –-hard       | 回復到沒修改的狀態 |

### 語法結構

```
usage: git reset [--mixed | --soft | --hard | --merge | --keep] [-q] [<commit>]
   or: git reset [-q] <tree-ish> [--] <paths>...
   or: git reset --patch [<tree-ish>] [--] [<paths>...]

    -q, --quiet           be quiet, only report errors
    --mixed               reset HEAD and index
    --soft                reset only HEAD
    --hard                reset HEAD, index and working tree
    --merge               reset HEAD, index and working tree
    --keep                reset HEAD but keep local changes
    -p, --patch           select hunks interactively
    -N, --intent-to-add   record only the fact that removed paths will be added later
```