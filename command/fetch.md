# git fetch 指令

### 常用指令範例

| 範例               | 說明       |
|------------------|----------|
| git fetch        | 更新遠端容器   |
| git fetch origin | 更新指定遠端容器 |

### 語法結構

```
usage: git fetch [<options>] [<repository> [<refspec>...]]
   or: git fetch [<options>] <group>
   or: git fetch --multiple [<options>] [(<repository> | <group>)...]
   or: git fetch --all [<options>]

    -v, --verbose         be more verbose
    -q, --quiet           be more quiet
    --all                 fetch from all remotes
    -a, --append          append to .git/FETCH_HEAD instead of overwriting
    --upload-pack <path>  path to upload pack on remote end
    -f, --force           force overwrite of local branch
    -m, --multiple        fetch from multiple remotes
    -t, --tags            fetch all tags and associated objects
    -n                    do not fetch all tags (--no-tags)
    -p, --prune           prune remote-tracking branches no longer on remote
    --recurse-submodules[=<on-demand>]
                          control recursive fetching of submodules
    --dry-run             dry run
    -k, --keep            keep downloaded pack
    -u, --update-head-ok  allow updating of HEAD ref
    --progress            force progress reporting
    --depth <depth>       deepen history of shallow clone
    --unshallow           convert to a complete repository
    --update-shallow      accept refs that update .git/shallow
    --refmap <refmap>     specify fetch refmap
```