# log

語法結構

```
usage: git log [<options>] [<revision-range>] [[--] <path>...]
   or: git show [<options>] <object>...

    -q, --quiet           suppress diff output
    --source              show source
    --use-mailmap         Use mail map file
    --decorate[=...]      decorate options
    -L <n,m:file>         Process line range n,m in file, counting from 1
```

### 常用指令範例

| 範例                                                                 | 說明             |
|--------------------------------------------------------------------|----------------|
| git log [HEAD]                                                     |                |
| git log master                                                     |                |
| git log --oneline                                                  |                |
| git log --author="alincode"                                        |                |
| git log -p hello.js                                                |                |
| git log --follow README.md                                         |                |
| git log --graph --oneline --all --decorate                         | 顯示所有分之並圖形化     |
| git log --oneline --abbrev-commit --all --graph --decorate --color |                |
