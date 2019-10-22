# 大量練習

以下有些會用到一點點 jQuery，直接提供 jQuery 載入的 CDN：\(請放在 body 結束標籤之前\)

```markup
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
```

## 1 介面 hamburger icon

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



## 2 套用 hamburger icon 的外掛

指定檔名：hamburger\_icon\_with\_plugin.html

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

## 3 導覽列縮合

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



## 4 三欄式 RWD - 使用 Flexbox

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

## 5 頁面滑動時，上方置頂區域的隱藏與顯示

指定檔名：`fixed_top_nav.html`

結果示意：

{% embed url="https://www.youtube.com/watch?v=o\_OxCWQH21c" %}

提供最上方置頂的那塊 html：

```markup
<div class="fixed_top">這是置頂的區域</div>
```

提供 jQuery ：

```javascript
var header_active = function(){
  
  // 取得使用者滑了多少 px
  var scroll_top = $(window).scrollTop();
  
  // 將 scroll_top 數值放到 p.-pos 內容
  $("p.-pos").html(scroll_top);
  
  
  if(scroll_top >= 100){
    $("div.fixed_top").addClass("-on");
  }else{
    $("div.fixed_top").removeClass("-on");
  }
  
};


$(function(){
  
  // 第三步：偵測頁面滑動時會觸發
  $(window).scroll(function(){
    header_active();
  });
  
});
```

## 6 內容圖片佔滿版

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

## 7 區塊場景的滿版

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



## 10 個項目在行動版上的呈現模式 - 1

## 10 個項目在行動版上的呈現模式 - 2

滑動有點卡卡的，加上某個 css 讓其變得滑順。

## 觀察 background-attachment 在實際手機上的呈現

## 觀察 select 標籤在實際手機上的呈現

## 觀察 z-index 造成的覆蓋情況

## 6 套用 Font Awesome

[官網](https://fontawesome.com/)

[下載範例](http://notes.carlos-studio.com/download/fontawesome_sample.zip)

## 套用 slick 外掛

## 套用 ScrollMagic 外掛

