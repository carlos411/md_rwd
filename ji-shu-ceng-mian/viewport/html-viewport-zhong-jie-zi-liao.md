# HTML Viewport 中介資料

## **viewport 語法**

```markup
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
</head>
```

* `width=device-width`：設定 viewport 的寬度等於設備寬度。
* `initial-scale=1.0`：設定初始放大率等於1。\(建議不需更改\)
* `user-scalable=yes`：設定使用者是否可以針對網頁縮放\(zoom-in、zoom-out\)。\(實測結果並非所有瀏覽器支援。\)

## **範例**

**沒有指定 viewport 時的狀況，顯示了桌機版的網頁版本\(下圖出自於博客來官網\)：**

**有指定 viewport 的正確情況，顯示了行動版的網頁：**

