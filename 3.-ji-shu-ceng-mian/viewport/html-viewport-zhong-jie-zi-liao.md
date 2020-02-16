# 3.2.2 HTML Viewport 中介資料

## **viewport 語法**

```markup
<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
```

* `width=device-width`：設定 viewport 的寬度等於設備寬度。
* `initial-scale=1.0`：設定初始放大率等於1。\(建議不需更改\)
* `user-scalable=yes`：設定使用者是否可以針對網頁縮放\(zoom-in、zoom-out\)。\(實測結果並非所有瀏覽器支援。\)

## 結論

只要做 RWD 的頁面，只要在 html 的 `<head>` 區段中，加上以下的 meta 標籤即可，完全不用改：

```markup
<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
```

