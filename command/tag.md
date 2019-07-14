# git tag 指令

標籤

### 使用情境

* 發佈里程碑
* 準備發佈一個穩定版本，給予容易識別的版本命名

### 命名

```
[主版本號].[次版本號].[修訂版本號]
```

```
v0.0.1
// or
v0.0.1
```

### 常用範例

| 範例                                           | 說明           |
|-----------------------------------------------|----------------|
| git tag                                       |               |
| git tag v0.0.1 sha1234                        | 新增輕量 tag    |
| git tag v0.0.1 sha1234 -a -m "feature 123"    | 新增有附註的 tag |
| git tag -d v0.0.1                             | 刪除 tag        |
| git rev-parse v0.0.1                          |                |
| git push origin :refs/tags/v0.0.1             | 刪除遠端 tag    |

### 練習題：建立 tag (如果時間不夠，可以跳過)

1. 透過 `git tag v0.01` 指令，建立標籤
1. 透過 `git tag` 指令，列出所有標籤
1. 透過 `git tag -d v0.01` 指令，刪除標籤
1. 透過 `git tag v0.0.1 -m '新增了一個偉大的功能'` 指令，建立標籤
1. 透過 `git show v0.0.1` 指令，查看標籤詳細
1. 透過 `git tag v0.0.1` 指令，建立標籤

### 練習題：發佈 tag (如果時間不夠，可以跳過)

1. 透過 `git push origin v0.0.1` 指令，發佈標籤

---
### 語法結構

```
usage: git tag [-a | -s | -u <key-id>] [-f] [-m <msg> | -F <file>] <tagname> [<head>]
   or: git tag -d <tagname>...
   or: git tag -l [-n[<num>]] [--contains <commit>] [--points-at <object>]
                [--format=<format>] [--[no-]merged [<commit>]] [<pattern>...]
   or: git tag -v <tagname>...

    -l, --list            list tag names
    -n[<n>]               print <n> lines of each tag message
    -d, --delete          delete tags
    -v, --verify          verify tags

Tag creation options
    -a, --annotate        annotated tag, needs a message
    -m, --message <message>
                          tag message
    -F, --file <file>     read message from file
    -s, --sign            annotated and GPG-signed tag
    --cleanup <mode>      how to strip spaces and #comments from message
    -u, --local-user <key-id>
                          use another key to sign the tag
    -f, --force           replace the tag if exists
    --create-reflog       create a reflog

Tag listing options
    --column[=<style>]    show tag list in columns
    --contains <commit>   print only tags that contain the commit
    --merged <commit>     print only tags that are merged
    --no-merged <commit>  print only tags that are not merged
    --sort <key>          field name to sort on
    --points-at <object>  print only tags of the object
    --format <format>     format to use for the output
```

---


```
$ git rev-parse v0.0.1
d93a61550216134ea18ff5db907f066fd8beb866
```

```
$ git cat-file -p d93a61550216134ea18ff5db907f066fd8beb866

tree cbfd7a8e6c7bd0eec9f524b42bdce9ff31bac2e3
parent 59da3738f9ccf00e1246098a65259b713e848926
author alincode <alincode@gmail.com> 1526267514 +0000
committer alincode <alincode@gmail.com> 1526267514 +0000

add hello2 file
```
