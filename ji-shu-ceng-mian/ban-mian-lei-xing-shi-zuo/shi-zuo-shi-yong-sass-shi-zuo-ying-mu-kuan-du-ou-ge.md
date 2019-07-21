# 範例：使用 sass 實作螢幕寬度區隔

## 使用 SASS 劃分螢幕區隔

提供使用 SASS 的 SCSS 語法，劃分好幾個螢幕區域，方便實作 RWD，建立一個 `_grid.scss` 檔案如下：  
\(註：SASS 編譯不在此課程範圍內。\)

{% code-tabs %}
{% code-tabs-item title="\_grid.scss" %}
```css
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
{% endcode-tabs-item %}
{% endcode-tabs %}

那麼該如何使用呢？假設有一個 index.scss 需要用到，使用方式如下：

{% code-tabs %}
{% code-tabs-item title="index.scss" %}
```css
@import '../_grid'; /* 匯入檔案 */

div.test_block{
  @include c-grid-down(sm){
    /* 這裡的 CSS 會套用在 sm 範圍以下：即 767px 以下 */
  }
  @include c-grid-down(sm){
    /* 這裡的 CSS 會套用在 sm 範圍以上：即 576px 以上 */
  }
  @include c-grid(sm){
    /* 這裡的 CSS 會套用在 sm 範圍之中：即 576px ~ 767px */
  }
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}

