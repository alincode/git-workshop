# git status 指令

### 使用情境

* 觀看檔案的狀態

### 狀態

![](assets/status2.png)

* Untracked files：未被追蹤的檔案
* Changes not staged for commit：有被更動但尚未要提交的檔案
* Changes to be committed：將要提交的檔案
* staged

![](assets/status.png)

<!-- 這裡指的是 staged 跟 stash 是不同的歐，不要看錯了 -->

### 檔案狀態分類

* 被追蹤：被加入 index 的檔案
* 不被追蹤：還沒被加入 index 的檔案
* 被忽略：被定義在忽略清單的檔案

### .gitignore

* 想忽略的檔案，如暫存檔、log、編譯後的檔案
* [A collection of .gitignore templates](https://github.com/github/gitignore)

**強制刪除那些已被設為忽略，不存在儲存庫，但還存在工作目錄的那些檔案。**

```sh
git clean -fx
```

### 常用範例

| 範例         | 說明       |
|------------|----------|
| git status | 看目前檔案的狀態 |

### 語法結構

```
usage: git status [<options>] [--] <pathspec>...

    -v, --verbose         be verbose
    -s, --short           show status concisely
    -b, --branch          show branch information
    --porcelain           machine-readable output
    --long                show status in long format (default)
    -z, --null            terminate entries with NUL
    -u, --untracked-files[=<mode>]
                          show untracked files, optional modes: all, normal, no. (Default: all)
    --ignored             show ignored files
    --ignore-submodules[=<when>]
                          ignore changes to submodules, optional when: all, dirty, untracked. (Default: all)
    --column[=<style>]    list untracked files in columns
```