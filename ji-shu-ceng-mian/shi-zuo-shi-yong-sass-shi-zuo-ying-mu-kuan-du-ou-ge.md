# 8. 補充：使用 SASS 實作螢幕寬度區隔

## 使用 SASS 劃分螢幕區隔

提供使用 [SASS](https://sass-lang.com/) 的 SCSS 語法，劃分好幾個螢幕區域，方便實作 RWD，建立一個 `_grid.scss` 檔案如下：

{% tabs %}
{% tab title="\_grid.scss" %}
```css
/* 指定不同的區間範圍，給定不同的寬度 */
.c{
  @media screen and (max-width: 575px){  /* xs */
    width: 100%;
  }
  @media screen and (min-width: 576px) and (max-width: 767px){  /* sm */
    width: 540px;
  }
  @media screen and (min-width: 768px) and (max-width: 991px){  /* md */
    width: 720px;
  }
  @media screen and (min-width: 992px) and (max-width: 1199px){  /* lg */
    width: 960px;
  }
  @media screen and (min-width: 1200px){  /* xl */
    width: 1140px;
  }
}

@mixin c-grid($type) {
  @if $type == xs {
    @media screen and (max-width: 575px){ /* xs */
      @content;
    }
  }
  @if $type == sm {
    @media screen and (min-width: 576px) and (max-width: 767px){ /* sm */
      @content;
    }
  }
  @if $type == md {
    @media screen and (min-width: 768px) and (max-width: 991px){ /* md */
      @content;
    }
  }
  @if $type == lg {
    @media screen and (min-width: 992px) and (max-width: 1199px){ /* lg */
      @content;
    }
  }
  @if $type == xl {
    @media screen and (min-width: 1200px){ /* xl */
      @content;
    }
  }
}

@mixin c-grid-up($type) {
  @if $type == xs {
    @media screen and (min-width: 320px){ /* xs */
      @content;
    }
  }
  @if $type == sm {
    @media screen and (min-width: 576px){ /* sm */
      @content;
    }
  }
  @if $type == md {
    @media screen and (min-width: 768px){ /* md */
      @content;
    }
  }
  @if $type == lg {
    @media screen and (min-width: 992px){ /* lg */
      @content;
    }
  }
  @if $type == xl {
    @media screen and (min-width: 1200px){ /* xl */
      @content;
    }
  }
}

@mixin c-grid-down($type) {
  @if $type == xs {
    @media screen and (max-width: 575px){ /* xs */
      @content;
    }
  }
  @if $type == sm {
    @media screen and (max-width: 767px){ /* sm */
      @content;
    }
  }
  @if $type == md {
    @media screen and (max-width: 991px){ /* md */
      @content;
    }
  }
  @if $type == lg {
    @media screen and (max-width: 1199px){ /* lg */
      @content;
    }
  }
  @if $type == xl {
    @content; /* xl */
  }
}
```
{% endtab %}

{% tab title="index.scss" %}
```css
@import '../_grid'; /* 匯入檔案 */

div.test_block{
  @include c-grid-down(md){
    /* 這裡的 CSS 會套用在 md 範圍以下：即 991px 以下，會取代 @mixin 裡的 @content */
  }
  @include c-grid-up(md){
    /* 這裡的 CSS 會套用在 md 範圍以上：即 768px 以上，會取代 @mixin 裡的 @content */
  }
  @include c-grid(md){
    /* 這裡的 CSS 會套用在 md 範圍之中：即 768px ~ 991px，會取代 @mixin 裡的 @content */
  }
}
```
{% endtab %}
{% endtabs %}

範例：

{% embed url="https://codepen.io/carlos411/pen/poojxoz" %}



