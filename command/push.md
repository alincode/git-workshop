### git push 指令

### 使用情境

* 將本地端新增的送交紀錄，發佈至遠端

### 常用範例

| 範例                        | 說明                                          |
|---------------------------|------------------------------------------------|
| git push origin master    | 發佈 master                                    |
| git push origin v0.0.1    | 發佈標籤至遠端                                   |
| git push origin :dev      | 刪除遠端 dev 分支                                |

**設定 Upstream**

參數 `-u` 等同於 `--set-upstream` (上游)，設定 upstream 可以使分支開始追蹤指定的遠端分支

```sh
git push --set-upstream origin master

// 縮寫
git push -u origin master
```

```
git branch --set-upstream-to=github/master master
git push
```

### 情境：有時候 push 不上去

### 語法結構

```
usage: git push [<options>] [<repository> [<refspec>...]]

    -v, --verbose         be more verbose
    -q, --quiet           be more quiet
    --repo <repository>   repository
    --all                 push all refs
    --mirror              mirror all refs
    --delete              delete refs
    --tags                push tags (can't be used with --all or --mirror)
    -n, --dry-run         dry run
    --porcelain           machine-readable output
    -f, --force           force updates
    --force-with-lease[=<refname>:<expect>]
                          require old value of ref to be at this value
    --recurse-submodules[=<check|on-demand|no>]
                          control recursive pushing of submodules
    --thin                use thin pack
    --receive-pack <receive-pack>
                          receive pack program
    --exec <receive-pack>
                          receive pack program
    -u, --set-upstream    set upstream for git pull/status
    --progress            force progress reporting
    --prune               prune locally removed refs
    --no-verify           bypass pre-push hook
    --follow-tags         push missing but relevant tags
    --signed[=<yes|no|if-asked>]
                          GPG sign the push
    --atomic              request atomic transaction on remote side
```
