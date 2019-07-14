# 設定檔

### 設定檔的位置

參數      | 寫入的檔案位置   | 說明
-------- | -------------- | -----------------------
--system | /etc/gitconfig | 對系統中所有使用者配置
--global | ~/.gitconfig   | use global config file
--local  | .git/config    | use repository config file

編輯設定檔的方式有兩種

1. 使用 `git config` 指令
1. 直接編輯設定檔，例如：`vi .git/config`


### 常用範例

| 範例                                                  | 說明                  |
|------------------------------------------------------|-----------------------|
| git config --list                                    | 列出所有設定值          |
| git config --global user.name "demo_user"            | 設定全域層級的使用者名稱  |
| git config --global user.email "demo_user@demo.com"  | 設定全域層級的使用者信箱  |
| git config --local user.name "demo_user"             | 設定儲存庫層級的使用者名稱 |
| git config --local user.email "demo_user@demo.com"   | 設定儲存庫層級的使用者信箱 |
| git config alias.st "status"                       | 設定 status 暱稱      |
| git config --global alias.l "log --graph --oneline"  | 在全域，設定 l 暱稱      |
| git config core.editor "vim"                   | 修改預設編輯器                |
| git config push.default matching               | 預設發佈到相同分支名稱的遠端分支 |

> 注意：--global 參數比需要緊接著 git config，移到最後面的話，是沒有作用的

### 推薦設定的 alias

```
git config --global alias.tree "log --oneline --decorate --graph --all"

alias.co=checkout
alias.cm=commit -m
alias.st=status
alias.df=diff
alias.br=branch
alias.aa=add .
alias.tree=log --oneline --decorate --graph --all
alias.ls='log --graph --pretty=format:"%h <%an> %ar %s"'
alias.last=log -1 HEAD
```

<!-- 
```
alias.pl=pull
alias.ps=push

alias.cp=checkout -p
alias.cc=checkout .

alias.ss=stash
alias.spp=stash pop
alias.sdd=stash drop

alias.type=cat-file -t
alias.dump=cat-file -p
alias.lg=log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --
alias.logg=log --all --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative
``` 
-->

### 練習題：設定 commit 時要顯示的名稱跟信箱

1. 透過 `git config user.name "demo_user"` 指令，設定 commit 時顯示的名稱。
1. 透過 `git config user.email "demo_user@demo.com"` 指令，設定 commit 時顯示的名稱。
1. 透過 `git config --list` 指令，確認已設定成功

```
🤔 為什麼我看到了兩個 user.name？
```

### 練習題：設定常用指令暱稱

1. 透過 `git config --global alias.st status` 指令，設定 status 暱稱
1. 透過 `git st` 指令，來確定設定完成了

---
### 語法結構

```
usage: git config [<options>]

Config file location
    --global              use global config file
    --system              use system config file
    --local               use repository config file
    -f, --file <file>     use given config file
    --blob <blob-id>      read config from given blob object

Action
    --get                 get value: name [value-regex]
    --get-all             get all values: key [value-regex]
    --get-regexp          get values for regexp: name-regex [value-regex]
    --get-urlmatch        get value specific for the URL: section[.var] URL
    --replace-all         replace all matching variables: name value [value_regex]
    --add                 add a new variable: name value
    --unset               remove a variable: name [value-regex]
    --unset-all           remove all matches: name [value-regex]
    --rename-section      rename section: old-name new-name
    --remove-section      remove a section: name
    -l, --list            list all
    -e, --edit            open an editor
    --get-color           find the color configured: slot [default]
    --get-colorbool       find the color setting: slot [stdout-is-tty]

Type
    --bool                value is "true" or "false"
    --int                 value is decimal number
    --bool-or-int         value is --bool or --int
    --path                value is a path (file or directory name)

Other
    -z, --null            terminate values with NUL byte
    --name-only           show variable names only
    --includes            respect include directives on lookup
```
