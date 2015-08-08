# isbn2img
Get image URL from ISBN

## 原理

用 ISBN 搜尋找到對應的書，然後得到圖片 URL。

## via 博客來原理

### [STEP 1] 找尋該書

```
GET http://search.books.com.tw/exep/prod_search.php?key=ISBN
```

### [STEP 2] 解析 Response

其中 `name=C1` 的 input tag 的 value 就是該書在博客來的 id

### [STEP 3] 算出 Image URL

博客來的圖片網址如下

```
http://www.books.com.tw/img/TOKEN.jpg
```

其中 `TOKEN` 是剛剛 `id[3]/id[3:6]/id[6:8]/id` 組成

ex. `id = 1234567890` -> `TOKEN = 123/456/78/1234567890`

## LICENSE

See file LICENSE for more info.