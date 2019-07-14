# git revert 指令

反悔，新增一筆反向的送交紀錄

### 使用情境

* 修正已經發佈的送交紀錄，新增一個反向的 rollback 送交紀錄。

### 常用範例

| 範例                       | 說明                  |
|---------------------------|-----------------------|
| git revert HEAD           | 回到前一次 commit 的狀態 |
| git revert HEAD --no-edit | 不編輯 commit 訊息      |

> 🤔 取消 revert？ 可以直接使用 `git reset HEAD^ --hard`

### 情境題：什麼時候用 reset，什麼時候用 revert？

**Reset**

* 用在還未發佈的 commit
* 直接修改舊的送交歷史紀錄，不會多增加一個新的節點。

**Revert**

* 用在還未發佈的 commit
* 回到指定的 commit 節點的前一個節點的狀態，執行完畢後會新增一個 commit 節點。

### 練習題：反悔一個已經發佈的送交紀錄

```
git revert HEAD
git log --oneline
```

---
### 語法結構

```
usage: git revert [<options>] <commit-ish>...
   or: git revert <subcommand>

    --quit                end revert or cherry-pick sequence
    --continue            resume revert or cherry-pick sequence
    --abort               cancel revert or cherry-pick sequence
    -n, --no-commit       don't automatically commit
    -e, --edit            edit the commit message
    -s, --signoff         add Signed-off-by:
    -m, --mainline <n>    parent number
    --rerere-autoupdate   update the index with reused conflict resolution if possible
    --strategy <strategy>
                          merge strategy
    -X, --strategy-option <option>
                          option for merge strategy
    -S, --gpg-sign[=<key-id>]
                          GPG sign commit
```