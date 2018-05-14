# Branch

分支

在開發軟體時，可能同時會有多人在開發同一功能或修復錯誤，也可能會有多個發佈版本的存在，並且需要針對每個版本進行維護。為了能支援同時進行數個功能的增加或版本控制，Git具備了分支的功能。分支是為了將修改記錄的整體流程分開儲存，讓分開的分支不受其他分支的影響，所以在同一個數據庫裡可以同時進行多個不同的修改。

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

| 範例                     | 說明                        |
|------------------------|---------------------------|
| git branch dev         | 新增 dev 分支                 |
| git branch             | 列出 local 分支               |
| git branch -r          | 列出遠端分支                    |
| git branch -a          | 列出所有分支                    |
| git branch -m dev dev2 | 修改分支名稱                    |
| git branch -d dev2     | 刪除分支                      |
| git branch -D dev2     | 強迫刪除分支 (即使分支，還沒被 merge 過) |

### 相關聯指令

| 範例                  | 說明        |
|---------------------|-----------|
| git push origin dev | 發佈 dev 分支 |

### 語法結構

```
usage: git branch [<options>] [-r | -a] [--merged | --no-merged]
   or: git branch [<options>] [-l] [-f] <branch-name> [<start-point>]
   or: git branch [<options>] [-r] (-d | -D) <branch-name>...
   or: git branch [<options>] (-m | -M) [<old-branch>] <new-branch>
   or: git branch [<options>] [-r | -a] [--points-at]
```
