# 認識 Git 物件

* blob 物件
* tree 物件
* commit 物件
* tag 物件

### 物件儲存

* 當 Git 要儲存一個物件時，它使用內容雜湊演算值，而不是檔案名稱。若有兩個存在不同目錄，但內容相同的檔案，兩個檔案的 SHA1 會相同。
* SHA1 的前兩位數，會作為 `git/object/前兩位數` 的放置位置。

#### git ls-files -s

```
100644 aff6388cffe192b412dfca52ddeee7a7ebd8961e 0       hello.txt
```
#### find .git


```
.git/objects/af
.git/objects/af/f6388cffe192b412dfca52ddeee7a7ebd8961e
```

#### git write-tree

```
bb9e55860a20ae3a1c441d5e2d8a5e0261a3f2ff
```

#### git cat-file -p cbfd7a8e6c7bd0eec9f524b42bdce9ff31bac2e3

將內容反組譯

```
100644 blob aff6388cffe192b412dfca52ddeee7a7ebd8961e    hello.txt
100644 blob 14be0d41c639d701e0fe23e835b5fe9524b4459d    hello2.txt
```

### 名稱

* 絕對名稱
* 參照名稱

```
refs/head
refs/remotes
refs/tags
```