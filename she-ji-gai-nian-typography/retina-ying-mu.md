# 圖片在 Retina 螢幕上的呈現

## 圖片在 Retina 螢幕上的呈現

* 示範：截取 Retina 螢幕上的區域看解析度。\(截取 1440 x 100的範圍，出來的解析度會是 2880 x 200。\)

結論：假設在 400 x 200的區塊範圍中呈現一張圖片，我們需要準備較高解析度的圖片\(寬高各兩倍大\)，然後在網頁上呈現時，再透過 CSS 設定為 400px，那在 retina 螢幕上才不會有糊模的現象。如下例：

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

