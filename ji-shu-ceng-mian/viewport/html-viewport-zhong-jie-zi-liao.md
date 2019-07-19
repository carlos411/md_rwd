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

沒有指定 viewport 時的狀況，顯示了桌機版的網頁版本，瀏覽器試圖將整個網頁縮小，讓整個瀏覽器都看得到，導致缺代使用者體驗：

![&#x5716;&#x4E00;&#xFF1A;&#x684C;&#x6A5F;&#x7248;&#x7DB2;&#x9801;](../../.gitbook/assets/viewport_no.png)

有指定 viewport 再搭配正確的 CSS Media Query，顯示了行動版的網頁：

![&#x5716;&#x4E8C;&#xFF1A;&#x884C;&#x52D5;&#x7248;&#x7DB2;&#x9801;](../../.gitbook/assets/viewport_yes.png)

