# 媒體描述 Media Features

## 範例一：min-width

當螢幕寬度大於等於 768px 時，連結`<a>` 的文字顏色會變成紅色。

沒有寫 `Media Type` 的話，預設都是 `all`：

```css
@media (min-width: 768px){
  a{
    color: red;
  }
}
```

以上的原始碼，如果加上 Media Type 的會，等同於以下：

```css
@media all and (min-width: 768px){
  a{
    color: red;
  }
}
```

## 範例二：max-width

當螢幕寬度小於等於 767px 時，連結`<a>` 的文字顏色會變成綠色。

```css
@media (max-width: 767px){
  a{
    color: green;
  }
}
```

## 範例三：結合 min-width 與 max-width

當螢幕寬度大於等於 768px 且小於等於 992px 時，連結`<a>` 的文字顏色會變成橘色。

```css
@media (min-width: 768px) and (max-width: 992px){
  a{
    color: orange;
  }
}
```

## 範例四：結合 Media Type

當是螢幕時，螢幕寬度大於等於 768px 且小於等於 992px 時，連結`<a>` 的文字顏色會變成紅色。

```css
@media screen and (min-width: 768px) and (max-width: 992px){
  a{
    color: red;
  }
}
```



## orientation



