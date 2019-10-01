# 媒體類型 Media Type

## 包含哪幾種

* all：所有類型都包含。
* screen：這是最常用的，螢幕裝置。
* print：用於列印時。

## 範例一：Media Type 是 print

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

## 媒體類型\(Media Type\) 的套用方式

一般來說，沒有特別指定的話，Media Type 預設都是 all，也就是不管任何情況，都會套用。

如果要指定 Media Type 的話，可按照以下方式來指定：

### 方式一：設定 media 屬性

在 HTML 中：\(主要是加上 `media` 屬性\)

```markup
<link type="text/css" href="abc.css" media="print">

<!-- 或 -->

<style type="text/css" media="print">
  /* 其它 CSS */
</style>
```

如果要指定複數個媒體類型\(Media Type\)，以半形逗號做區隔即可：

```markup
<link type="text/css" href="abc.css" media="screen, print">

<!-- 或 -->

<style type="text/css" media="screen, print">
  /* 其它 CSS */
</style>
```

### 方式二：寫在 CSS 中

在 CSS 中：\(設定 `@import` 或 `@media` 語法都可\)

```css
/* 只有在列印時，才會套用 */
@import url("abc.css") print;

/* 或以下這個寫法 */

@media print {
  /* 其它 CSS */
}
```

如果是複數個 Media Type：

```css
/* 指定在螢幕或列印時，才會套用 */
@import url("abc.css") screen, print;

/* 或以下這個寫法 */

@media screen, print {
  /* 其它 CSS */
}
```

