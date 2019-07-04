# 為什麼我們需要 Git

很多人已經有使用 SVN 的經驗，為什麼要改使用 Git 呢？因為 Git 解決了 SVN 幾項令人詬病的問題，使得 Git 最終贏得了這場勝利。

### Git VS SVN

我們將 Git 與 SVN 分別描述，並做一些比較。

#### Git

* 支援離線機制，可以在離線狀態 commit
* 非常快速
* 更好的 merge 機制
* 數不清的新功能
* Straight merge 預設的合併模式，會有全部的被合併的 branch commits 記錄加上一個 merge-commit，看線圖會有兩條 Parents 線，並保留所有 commit log。

#### SVN

* 不能在離線狀態 commit
* 只要 commit 多的時候，查看 log 容易 timeout
* 很容易發生衝突，甚至只要檔案重新命名，SVN 就認不出來了。
* Squashed commit 壓縮成只有一個 merge-commit，不會有被合併的 log。

#### 比較

* Git 的「送交」與「發布」步驟是分開的
* Git 沒有唯一的真實歷史紀錄，在分散式開發環境中，大家都是平等的。
* 時間戳不重要，重點是「父子關係」。

#### transport

![Git transport](https://patrickzahnd.ch/uploads/git-transport-v1-1024x723.png)

![SVN transport](https://patrickzahnd.ch/uploads/svn-transport-v1.png)
