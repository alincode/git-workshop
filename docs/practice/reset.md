# 練習題：reset

### 2. 情境：重新 commit，並讓不該存在的檔案消失

![](../command/assets/git_reset.png)

1. 新增 1 個 commit 紀錄
1. 編輯 m1.md
1. 加入 hello 文字
1. 並 commit 進去
1. 透過 `reset --hard HEAD^` 指令，還原到前一個 commit 狀態，並把上一次的變更清除。

<!-- 
解答

echo "1" >> m1.md && git add . && git commit -m 'm1'
vi m1.md
git commit -m 'update'
git reset --hard HEAD^
 -->
