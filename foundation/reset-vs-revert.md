# Reset vs Revert

🤔 什麼時候用 `reset`，什麼時候用 `revert`。

### Reset

* 用在還未發佈的 commit
* 直接修改舊的送交歷史紀錄，不會多增加一個新的節點。

### Revert

* 用在還未發佈的 commit
* 回到指定的 commit 節點的前一個節點的狀態，執行完畢後會新增一個 commit 節點。