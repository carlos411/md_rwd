# Retina 螢幕

## 圖片在 Retina 螢幕上的模糊測試

* 一個點佔了4個普通像素。\(示範：截取 Retina 螢幕上的區域看解析度\)

{% embed url="https://codepen.io/carlos411/pen/OJLqKxO" %}

* 視情況，針對某圖準備寬高2倍大或3倍大的圖。\(例如：logo 圖\)。
* 各設針對 logo，我要顯示的範圍是 100 x 50，那就準備200 x 100的圖檔。\(或者是 svg 圖檔\)。
* 視情況，不需要針對網頁上的每張圖片都刻意去準備，畢竟耗資源。而且網站目前尚不支援自動依照 retina 螢幕換圖的機制。[未來請關注 picture 標籤的支援](https://www.w3schools.com/tags/tag_picture.asp)。

參考：

```markup
<picture>
   <source srcset="foo@2x.jpg 2x, foo.jpg 1x">
   <img src="foo.jpg" alt="Bar">
</picture>
```

