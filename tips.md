# 實用小技巧

### 新增空的資料夾


```
.gitkeeper
```

### 救回誤刪的檔案

```
# 查看已刪除的檔案
git ls-files -d

# 將已刪除的檔案還原
git ls-files -d | xargs git checkout —
```

### 快速尋找臭蟲

* 善用 grep
* 善用 blame 文件逐行追溯
* 善用 bisect 二分查找