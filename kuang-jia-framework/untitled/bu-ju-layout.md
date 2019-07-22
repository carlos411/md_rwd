# 佈局 Layout

## 格線系統

![&#x5716;&#x4E00;&#xFF1A;Bootstrap &#x7684;&#x683C;&#x7DDA;&#x7CFB;&#x7D71;](../../.gitbook/assets/bootstrap_grid_options.png)

## 瞭解樣式 container 和 container-fluid

### container

div 元素加上 container 樣式：

```markup
<div class="container">
</div>
```

這時的 `div.container`，寬度就會如圖一的 `Max container width` 來做變化。  
例：螢幕寬度 &gt;= 1200px 時，`div.container` 的寬度就是 1140px。以此類推。

### container-fluid

div 元素加上 container-fluid 樣式：

```markup
<div class="container-fluid">
</div>
```

這時的 `div.container`，寬度就是 100%。

## 範例1：sm 範圍以上三欄均分

{% embed url="https://codepen.io/carlos411/pen/XvmmPJ" caption="sm 範圍以上三欄均分" %}

## 範例2：各欄寬度自動均分

{% embed url="https://codepen.io/carlos411/pen/wVKJMR" caption="各欄寬度自動均分" %}



