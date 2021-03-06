# 6. 大量練習

以下有些會用到一點點 jQuery，直接提供 jQuery 載入的 CDN：\(請放在 body 結束標籤之前\)

```markup
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
```

## 練習

### 1 介面 hamburger icon

指定檔名：`hamburger_icon.html`

用 button 標籤做一個 hamburger icon：

切換 class \(使用 jQuery\)：

```javascript
// jQuery 版本：DOM 載入完成之後執行
$(function(){
  /* 按鈕狀態的切換 */
  $("button.hamburger_icon").on("click", function(){
    $(this).toggleClass("-on");
  });
});
```

切換 class \(使用 JavaScript\)：

```javascript
// JavaScript 版本：DOM 載入完成之後執行
document.addEventListener('DOMContentLoaded', function(){
  
  var hamburger_icon = document.getElementsByClassName("hamburger_icon")[0];
  hamburger_icon.addEventListener("click", function(){
    if( hamburger_icon.classList.contains("-on") ){
      hamburger_icon.classList.remove("-on");
    }else{
      hamburger_icon.classList.add("-on");
    }
  });
  
});
```

結果示意：

{% embed url="https://youtu.be/6rJP4TZF4SU" %}



提供 html：

```markup
<button type="button" class="hamburger_icon">
  <span class="-hr -top"></span>
  <span class="-hr -middle"></span>
  <span class="-hr -bottom"></span>
</button>
```



參考作法：

{% embed url="https://codepen.io/carlos411/pen/rNBErJy" %}





### 2 套用 hamburger icon 的外掛

指定檔名：`hamburger_icon_with_plugin.html`

[官網](https://jonsuh.com/hamburgers/)

[官方所提供的 css 在這](https://raw.githubusercontent.com/jonsuh/hamburgers/master/dist/hamburgers.css)。

自行挑選一個效果，學會套用。只需要看 Usage 的 1 ~ 4 點即可。



切換 class \(使用 jQuery\)：

```javascript
$(function(){
  
  // hamburger icon 的切換
  $("button.hamburger").on("click", function(){
    $(this).toggleClass("is-active");
  });

});
```



參考作法：

{% embed url="https://codepen.io/carlos411/pen/xvVLyR" %}





### 3 導覽列縮合

指定檔名：`nav_switch.html`

提供 html：

```markup
<button type="button" class="btn_switch">導覽列縮合按鈕</button>

<nav class="main_nav">
  <ul class="nav_list">
    <li><a href="#">首頁</a></li>
    <li><a href="#">關於我們</a></li>
    <li><a href="#">分類頁</a></li>
  </ul>
</nav>
```

提供 jQuery 寫法：

```javascript
$(function(){
  
  // 點擊按鈕，選單縮放
  $("button.btn_switch").on("click", function(){
    $("nav.main_nav").slideToggle();
  });
  
});
```

結果示意：

{% embed url="https://youtu.be/8Q7obn9a9hU" %}



參考作法：

{% embed url="https://codepen.io/carlos411/pen/XvGKQz" %}



### 4 三欄式 RWD - 使用 Flexbox

指定檔名：`rwd_with_flexbox.html`

說明：

* 768px 以上為桌機版；767px 以下為行動版。
* 左欄及右欄寬度各 200px，剩餘空間寬度都給中間欄。
* 限定使用 Flexbox 來製作三欄式 RWD 排版。

結果示意：

{% embed url="https://youtu.be/ABX7rKgLeXo" %}

提供 HTML 結果如下：

```markup
<div class="all_container">
  <div>
    左側<br>
    另一行
  </div>
  <div>
    中間
  </div>
  <div>
    右側
  </div>
</div>
```



參考作法：

{% embed url="https://codepen.io/carlos411/pen/MWWJQvQ" %}



### 5 內容圖片佔滿版

指定檔案：`full_width_image.html`

區塊滿版，高度250px，裡面一張圖片，如下結構：

```markup
<div class="img_block">
  <img src="https://picsum.photos/id/866/800/400">
</div>
```

並設定在 575px 以下行動版時，佔滿的區域比例為寬高1:1\(即正方形\)。

結果示意：

{% embed url="https://youtu.be/jQq3ocGodaw" %}



參考作法：

{% embed url="https://codepen.io/carlos411/pen/JjjELmR" %}



### 6 區塊場景的滿版

指定檔名：`full_scene.html`

製作三個區塊，寬高都佔滿版，留意高度。分別任意指定不同的背景色以便觀察。

給定 html 如下：

```markup
<section class="scene scene_1">
  scene1
</section>

<section class="scene scene_2">
  scene2
</section>

<section class="scene scene_3">
  scene3
</section>
```

結果示意：

{% embed url="https://youtu.be/Fwd58Kpvrdc" %}



參考作法：

{% embed url="https://codepen.io/carlos411/pen/XWWLXWL" %}





### 7 有 10 個項目的水平方向排版，及手機上的呈現

指定檔名：`ten_items_scroll.html`

請用實際手機看，觀察：滑動是不是卡卡的，加上某個 css 讓其變得滑順。

較舊版的可能滑動會有卡卡的現象，加上以下即可：

```css
ul.ul_list{
  -webkit-overflow-scrolling: touch;
}
```

提供 html 如下：

```markup
<div class="list_container">
  <ul class="ul_list">
    <li class="item">
      <div class="item_block">
        <h1>標題1</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題2</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題3</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題4</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題5</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題6</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題7</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題8</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題9</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題10</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
  </ul>
</div>
```

結果示意：

{% embed url="https://youtu.be/AUN5E3y7eao" %}



參考作法：

{% embed url="https://codepen.io/carlos411/pen/QWWdrbX" %}



### 8 內容固定在螢幕上，但在其它內容的後方

指定檔名：`content_fixed.html`

觀察廣告區塊的介面效果：

{% embed url="https://youtu.be/abtFFCpcw5U" %}

請做出如上廣告區塊的排版效果。

結果示意：

{% embed url="https://youtu.be/jNe2XwPi3uo" %}



提供 html：

```markup
<div class="top_block"></div>

<div class="middle_block">
  <div class="middle_content">
    <a href="https://tw.yahoo.com" target="_blank">這是連結</a>
    <img src="https://i.picsum.photos/id/645/500/400.jpg" class="the_img">
  </div>
</div>

<div class="bottom_block"></div>
```

註：此種效果建議用在行動版上，且內容不要太多。以免超出整個 100vh 的螢幕高度，以致於看不到內容。

提供部份 CSS：

```css
* {
  box-sizing: border-box;
}
body{
  margin: 0;
}
div.top_block{
  background-color: blue;
  height: 200vh;
  position: relative;
}
div.bottom_block{
  background-color: gray;
  height: 200vh;
  position: relative;
}





/* 中間區域 */
div.middle_block{
  border: 1px solid orange;
  height: 100vh;
}
div.middle_block div.middle_content{
  border: 1px solid red;
  width: 100%;
  padding: 10px;
}
img.the_img{
  width: 100%;
}
```

請試著加上一點 CSS 達成效果。

可從這個 codepen 開始實作：

{% embed url="https://codepen.io/carlos411/pen/gOaPWgZ" %}



參考作法：

{% embed url="https://codepen.io/carlos411/pen/ZEGdXdW" %}





### 9 次選單淡入淡出

指定檔名：`submenu_fadein_fadeout.html`

結果示意：

{% embed url="https://youtu.be/8KetZGnnLjs" %}

提供 html：

```markup
<div class="div_block">
  <p class="para">有次選單</p>
  <div class="inner_block">
    <ul>
      <li>項目一</li>
      <li>項目二</li>
      <li>項目三</li>
    </ul>
  </div>
</div>


<div>
  <p>下方內容</p>
  <img src="https://picsum.photos/seed/picsum/200/300">
</div>
```



參考這個 codepen，沒有淡入淡出的方式：

{% embed url="https://codepen.io/carlos411/pen/JjYGYbx" %}

改成淡入淡出。

參考作法：

{% embed url="https://codepen.io/carlos411/pen/xxwKqWQ" %}







## 參考

### 1 套用 Font Awesome

[官網](https://fontawesome.com/)

[下載範例](http://notes.carlos-studio.com/download/fontawesome_sample.zip)



