# 4.4 內容 Content

比較重要的是表格\(table\)。

## 範例 1：inline code

{% embed url="https://codepen.io/carlos411/pen/YmqpPL" caption="inline code" %}

## 範例 2：Responsive images

`.img-fluid`：圖片最大寬度設定為 100%。

{% embed url="https://codepen.io/carlos411/pen/jgqVWE" caption="圖片 img-fluid" %}

## 範例 3：圖片加上外圍邊框及圓角

`.img-thumbnail`：為圖片加上外圍邊框的樣式。

`.rounded`：為圖片加上圓角。

{% embed url="https://codepen.io/carlos411/pen/ZgWBJL" caption="圖片 img-thumbnail 及 rounded" %}

## 範例 4：帶有標題的圖片，使用 figure 元素

{% embed url="https://codepen.io/carlos411/pen/OKNbwJ" caption="帶有標題的圖片，使用 figure 元素" %}

## 範例 5：基本表格

`.table`：基本表格樣式。

`.table-dark`：表格 dark 模式。

{% embed url="https://codepen.io/carlos411/pen/xvVRpY" caption="基本表格" %}

## 範例 6：Responsive tables

[Bootstrap 官網](https://getbootstrap.com/)，主導覽：Documentation，次導覽：Content → Tables → Responsive tables，試著套用 Responsive tables。

提供 html ，試著用一個 `div.table-responsive` 包住整個 table，然後觀察看看：

```markup
<table class="table">
  <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">Heading</th>
      <th scope="col">Heading</th>
      <th scope="col">Heading</th>
      <th scope="col">Heading</th>
      <th scope="col">Heading</th>
      <th scope="col">Heading</th>
      <th scope="col">Heading</th>
      <th scope="col">Heading</th>
      <th scope="col">Heading</th>
      <th scope="col">Heading</th>
      <th scope="col">Heading</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
      <td>Cell</td>
    </tr>
  </tbody>
</table>
```

例：

{% embed url="https://codepen.io/carlos411/pen/ZEzNNRE" %}



