# 實作：使用 sass 實作螢幕寬度區隔

提供使用 SASS 的 SCSS 語法，劃分好幾個螢幕區域，方便實作 RWD：

{% code-tabs %}
{% code-tabs-item title="\_grid.scss" %}
```css
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

.c{
  @media screen and (max-width: 575px){  /* xs */
    width: 100%;
  }
  @media screen and (min-width: 576px) and (max-width: 767px){  /* sm */
    width: 576px;
  }
  @media screen and (min-width: 768px) and (max-width: 991px){  /* md */
    width: 768px;
  }
  @media screen and (min-width: 992px) and (max-width: 1199px){  /* lg */
    width: 992px;
  }
  @media screen and (min-width: 1200px){  /* xl */
    width: 1200px;
  }
}

```
{% endcode-tabs-item %}
{% endcode-tabs %}

