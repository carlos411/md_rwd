# 觀念理解

## 格線系統概念

第一步：桌機版、行動版空白頁面：

![](../../.gitbook/assets/desktop_mobile.png)

第二步：任何結構區塊，都視為列\(row\)：

* row 可以出現在頁面任何位置。
* row 的寬度可以是固定寬、或某百分比。
* row 的高度通常依內容來決定。

![](../../.gitbook/assets/grid_row.png)

第三步：顯示網格\(Grid\)

* 每一個小紅框都是寬高 10px。

![](../../.gitbook/assets/grid_show_grid.png)



第四步：任何的列\(row\)，都有自己的 12 個欄位\(Column\)

* 這 12 個欄位，各欄位之間都有固定的間隔\(Gutter\)。
* 間隔\(Gutter\)是由左右 padding 所創造。
* 假設以使用 Bootstrap 為例，間隔\(Gutter\)是 30px，也就是各欄的 padding-left、padding-right 都各是 15px。

![](../../.gitbook/assets/grid_show_grid%20%281%29.png)

第五步：移除網格，只顯示12個欄位\(Column\)。

![](../../.gitbook/assets/grid_show_layout.png)

第六步：內容是放在欄位\(Column\)裡面

* 設計師說：在這個列\(row\)中，有兩張圖片，在桌機版：各佔 6 欄。
* 設計師說：然後在行動版，改成各佔 12 欄。

![](../../.gitbook/assets/grid_content.png)

第七步：移除12欄的顯示提示\(紅色直欄\)

* 就完成利用 網格系統\(Grid System\) 來做 RWD 的基本觀念。

![](../../.gitbook/assets/grid_hidden_layout.png)

## 重點整理

* 不論行動版、桌機版都保有一致性的格線系統。
* 格線系統可運用在任何的寬度、位置。
* 理解列\(Row\)、欄\(Column\)、間隙\(Gutter\)。

