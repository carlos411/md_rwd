# 圖片在 Retina 螢幕上的呈現

## 圖片在 Retina 螢幕上的呈現

* 示範：截取 Retina 螢幕上的區域看解析度。\(截取 1440 x 100的範圍，出來的解析度會是 2880 x 200。\)

### 範例

假設在 400 x 200 的區塊範圍中呈現一張圖片，我們需要準備較高解析度的圖片\(寬高各兩倍大\)，然後在網頁上呈現時，再透過 CSS 設定為 400px，那在 retina 螢幕上才不會有糊模的現象：

{% embed url="https://codepen.io/carlos411/pen/OJLqKxO" %}



## 結論

Q1: 需要針對網頁上的每張圖片去做寬高各兩倍大的圖片嗎？

A: 不需要針對網頁上的每張圖片都刻意去準備，這樣會導致網站下載時間變長。而且網站目前還沒有良好的自動依照 retina 螢幕換圖的機制。

Q2: 那有什麼特別重要的圖需要針對 Retina 螢幕來優化嗎？

A: 有的，主要是 Logo，假設要顯示的範圍是 100 x 50，那就準備 200 x 100 的圖片，除了 png 、jpg 等選擇之外。或者也可以使用 svg 格式的圖片\(例：[ukik](https://uknowiknow.com/)\)，那就可以確定不論該圖無論大小，都不會有模糊現象。

Q3: Retina 好像還有更好的\(Higher Retina\)，需要準備到寬高各三倍大的圖？

A: 同 Q1，不需要特別去準備，如果需要較好的解析度，那再一開始的時候，就準備好寬高各兩倍大、或三倍大的圖，然後去縮放。只是這類圖數量不宜過多，畢竟檔案相對較大。

Q4: 什麼時候可以支援自動換圖呢？

A. [未來請關注 picture 標籤的支援](https://www.w3schools.com/tags/tag_picture.asp)。

參考：

```markup
<picture>
   <source srcset="foo@2x.jpg 2x, foo.jpg 1x">
   <img src="foo.jpg" alt="Bar">
</picture>
```



