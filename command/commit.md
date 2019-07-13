# git commit 指令

* 送交
* 版本和容器變動的最小單位

### 使用情境

* 新增送交
* 更改送交

### 常用範例

| 範例                                       | 說明                      |
|-------------------------------------------|---------------------------|
| git commit -m "commit message"            | 新增一筆送交紀錄             |
| git commit -a -m "commit message"         | git add . + git commit -m |
| git commit --amend -m "修改成新的 message"  | 改變最後一次提交紀錄         |

<!-- ### 為什麼要分兩段式 commit？ p045 -->

### 情境題

漏了一個更動忘了 commit

```sh
touch a.txt
git add a.txt
git commit --amend --no-edit
```

* --no-edit：不要編輯 commit 訊息

### 練習題：新增兩個送交紀錄

1. 透過 `mkdir commit` 指令，新增一個資料夾叫 `commit`
2. 透過 `git init` 指令，進行專案初始化。
1. 透過 `echo "Hello World" >> README.md` 指令，在資料夾中，新增一個檔案叫 `README.md`
1. 透過 `git add .` 指令，將所有更變加入 index 中
1. 透過 `git commit -m 'init'` 指令，將更變送交給 git
1. 透過 `echo 123 >> README.md` 指令，編輯 `README.md`
1. 透過 `git add .` 指令，將所有更變加入 index 中
1. 透過 `git commit -m 'update readme'` 指令，將更變送交給 git
1. 完成第一個版本控制範例


<!--
答案：

echo "Hello World" >> README.md && git add . && git commit -m 'init'
echo 123 >> README.md && git add . && git commit -m 'update readme'

-->

### 語法結構

```
usage: git commit [<options>] [--] <pathspec>...

    -q, --quiet           suppress summary after successful commit
    -v, --verbose         show diff in commit message template

Commit message options
    -F, --file <file>     read message from file
    --author <author>     override author for commit
    --date <date>         override date for commit
    -m, --message <message>
                          commit message
    -c, --reedit-message <commit>
                          reuse and edit message from specified commit
    -C, --reuse-message <commit>
                          reuse message from specified commit
    --fixup <commit>      use autosquash formatted message to fixup specified commit
    --squash <commit>     use autosquash formatted message to squash specified commit
    --reset-author        the commit is authored by me now (used with -C/-c/--amend)
    -s, --signoff         add Signed-off-by:
    -t, --template <file>
                          use specified template file
    -e, --edit            force edit of commit
    --cleanup <default>   how to strip spaces and #comments from message
    --status              include status in commit message template
    -S, --gpg-sign[=<key-id>]
                          GPG sign commit

Commit contents options
    -a, --all             commit all changed files
    -i, --include         add specified files to index for commit
    --interactive         interactively add files
    -p, --patch           interactively add changes
    -o, --only            commit only specified files
    -n, --no-verify       bypass pre-commit hook
    --dry-run             show what would be committed
    --short               show status concisely
    --branch              show branch information
    --porcelain           machine-readable output
    --long                show status in long format (default)
    -z, --null            terminate entries with NUL
    --amend               amend previous commit
    --no-post-rewrite     bypass post-rewrite hook
    -u, --untracked-files[=<mode>]
                          show untracked files, optional modes: all, normal, no. (Default: all)
```
