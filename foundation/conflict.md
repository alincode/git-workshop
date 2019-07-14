# 觀念解說：解決衝突 (conflict)

如果兩個分支，在同一行都發生了修改的情況下，這時會導致 Git 無法自動判斷，那一份才是正確的，於是發出衝突緊訊告知使用者需要手動排解衝突。

遠端儲存庫跟本地端儲存庫的同個名稱的分支，也算是不同分支，也可能會發生衝突。


```
$ git diff

diff --cc a.txt
index 71d0fdc,b24b282..0000000
--- a/a.txt
+++ b/a.txt
@@@ -1,1 -1,1 +1,5 @@@
++<<<<<<< HEAD
 +Hello World, John
++=======
+ Hello World Alex
++>>>>>>> dev2

$ git status

On branch master
You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)

	both modified:   a.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

### 練習題：解決衝突

1. 透過 `git status` 指令，查看哪些檔案衝突。
1. 透過 `git diff` 指令，查看衝突的地方。
1. 透過 `vi a.txt` 指令，編輯 a.txt 檔案內容，透過人工的方式解決衝突。
1. 透過 `git add .` 和 `git commit` 指令來告訴 git 你已經解完了衝突。
1. 透過 `git status` 指令，確認工作目錄狀態
1. 透過 `git show` 指令，查看剛剛手動解衝突修改的內容