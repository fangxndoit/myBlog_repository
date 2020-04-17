---
title: css loading
date: 2020-04-17 15:26:59
tags: css
---

#### HTML

```html
<div class="donut">
</div>
```

#### CSS

``` css
.donut{
  display: inline-block;
  border: 4px solid rgba(0, 0, 0, 0.1);
  border-left-color: #7983ff;
  border-radius: 50%;
  width: 30px;
  height: 30px;
  animation: donut-spin 1.2s linear infinite;
}
@keyframes donut-spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
```

[在线运行](https://jsfiddle.net/fire_flower/0vnfL4eo/)

