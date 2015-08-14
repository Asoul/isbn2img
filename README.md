# isbn2img
Get image URL from ISBN

*Read this in other languages: [正體中文](README.zh-tw.md)*

## Methods

use ISBN to get the book, then get the image URL.

## via www.books.com.tw

### [STEP 1] Search Book

```
GET http://search.books.com.tw/exep/prod_search.php?key=ISBN
```

### [STEP 2] Parse Response

The input tag with `name=C1` is the id in www.books.com.tw

### [STEP 3] Calculate Image URL

The Image URL is

```
http://www.books.com.tw/img/TOKEN.jpg
```

where `TOKEN` is `id[3]/id[3:6]/id[6:8]/id`

ex. `id = 1234567890` -> `TOKEN = 123/456/78/1234567890`

## LICENSE

See file LICENSE for more info.