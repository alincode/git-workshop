# git log 指令

查看送交紀錄，例如 sha 碼、作者、送交日期、送交訊息

```
$ git log
commit 72fac4600e934ca28968adb29371ef1a0d4dc16f (HEAD -> master)
Author: ALin <alin.code@gmail.com>
Date:   Sun Jul 14 18:02:37 2019 +0800

    add c.txt

commit d8d4aecd03766569fccf4a7e2c442593747740c4
Author: ALin <alin.code@gmail.com>
Date:   Sun Jul 14 17:58:27 2019 +0800

    init
```

### 使用情境

* 查看送交紀錄
* 查看送交歷史訊息

> 補充：SHA-1 是一種雜湊演算法，計算之後的結果為 40 個 16 進位的數字呈現，只要有相同的輸入值，就會有相同的輸出值。Git 的編號就是以此演算法算出。

### 常用指令範例

| 範例                                          | 說明                           |
|----------------------------------------------|--------------------------------|
| git log                                      | 查看送交歷史紀錄             |
| git log --oneline                         | 查看送交歷史紀錄，用一行的方式呈現 |
| git log -10                                  | 查看最後 10 筆送交歷史紀錄     |
| git log --oneline --grep="fixed"        | 查看送交訊息裡面包含有 fixed 的紀錄 |
| git log --oneline -S "hello world"           | 查看內容有包含 hello world 的紀錄  |
| git log -p hello.js                        | 查看這個檔案每次的送交做了什麼修改 |
| git log master                               |                                |
| git log --author="alincode"                  | 只查看特定人的送交紀錄             |
| git log --follow README.md                   | 列出包含該檔案變動的提交(包含改名前) |
| git log --graph --oneline --all --decorate   | 顯示所有分之並圖形化               |
| git log --since="1 weeks ago"                | 一週內的 log                     |

* –graph：排列出送交紀錄節點的演進圖
* –oneline：最精簡的方式顯示．
* –all：顯示所有分支的commit紀錄。
* –decorate：表示要標示分支的名稱。

<!-- git log \^[commitA] # A 之後的提交(不列出 A 之前的提交，不含 A) -->

```
🤔 `git log --oneline --grep="hello world"` 和 `git log --oneline -S "hello world"` 差在哪？
```

<!-- 
```
$ git log --oneline --grep="hello world"
62ee82b (HEAD -> master) add hello world
```

```
$ git log --oneline -S "hello world"
cac2448 (HEAD -> master) update c.txt
``` 
-->

### 練習題：新增第一個 commit

1. 透過 `touch a.txt b.txt` 指令，建立兩個檔案
1. 透過 `git add a.txt` 指令，將更變加入 index 中
1. 透過 `git status` 指令，查看狀態
1. 透過 `git add b.txt` 指令，將更變加入 index 中
1. 透過 `git commit -m 'init'` 指令，建立 commit 紀錄
1. 透過 `git log` 指令，來查看

### 練習題：修改最後的一個送交紀錄

1. 透過 `git commit --amend` 指令來修改送交紀錄

### 練習題：快速補送交

```sh
vi a.txt
git commit --amend --no-edit
```

> --no-edit 的意思是，不要編輯送交訊息 (沿用原本的)

---
### 語法結構

```
usage: git log [<options>] [<revision-range>] [[--] <path>...]
   or: git show [<options>] <object>...

    -q, --quiet           suppress diff output
    --source              show source
    --use-mailmap         Use mail map file
    --decorate-refs <pattern>
                          only decorate refs that match <pattern>
    --decorate-refs-exclude <pattern>
                          do not decorate refs that match <pattern>
    --decorate[=...]      decorate options
    -L <n,m:file>         Process line range n,m in file, counting from 1
```