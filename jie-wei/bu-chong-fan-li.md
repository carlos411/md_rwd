# 大量練習

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

結果示意：

{% embed url="https://youtu.be/8Q7obn9a9hU" %}



## 4 基礎三欄式 RWD

## 5 頁面滑動時，上方置頂區域的隱藏與顯示





## 滿版 - 1

區塊滿版，高度250px，裡面一張圖片，如下結構：

```markup
<div class="img_block">
  <img src="https://picsum.photos/id/866/800/400">
</div>
```

結果示意：

## 滿版 - 2

承上，在 575px 以下行動版時，佔滿的區域比例為寬高1:1\(即正方形\)。

結果示意：

## 區塊的隱藏與切換

結果示意：

{% embed url="https://youtu.be/JmcvKsc1r2I" %}

## z-index

## 高度滿版場景

## 10 個項目在行動版上的呈現模式 - 1

## 10 個項目在行動版上的呈現模式 - 2

滑動有點卡卡的，加上某個 css 讓其變得滑順。

## 觀察 background-attachment 在實際手機上的呈現

## 觀察 select 標籤在實際手機上的呈現

## 6 套用 Font Awesome

[官網](https://fontawesome.com/)

[下載範例](http://notes.carlos-studio.com/download/fontawesome_sample.zip)

## 套用 slick 外掛

## 套用 ScrollMagic 外掛

