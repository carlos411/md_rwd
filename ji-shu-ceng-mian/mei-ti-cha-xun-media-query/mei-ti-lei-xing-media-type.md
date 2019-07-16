# 媒體類型 Media Type

## 包含哪幾種

* all：所有類型都包含。
* screen：這是最常用的，螢幕裝置。
* print：用於列印時。

還有其它像 speech\(螢幕閱讀器時\)、projection\(投影\) 等，較為少用。

## 範例一：media type 是 print

使用 print 這 media type 來指定列印時，要套用的 CSS：

```css
h1{
  border: 1px solid red;
  color: red;
}

/* 使用 print 這 media type 來指定列印時，要套用的 CSS */
@media print {
  h1{
    border: 1px solid blue;
    color: blue;
  }
}
```

{% embed url="https://codepen.io/carlos411/pen/orKXpG" caption="Media Query 使用 Media Type 為 print\(列印時\)" %}



