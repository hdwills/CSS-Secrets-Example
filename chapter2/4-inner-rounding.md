# Inner rounding (chapter2 - 4)

我们需要一个容器，只在内侧有圆角，而边框的四个角在外部仍然保持直角的形状。

1. 用传统方式实现（两层元素）

```css
.wrap1 {
  background-color: #655;
  padding: .5em;
}
.content1 {
  background-color: tan;
  border-radius: .5em;
  padding: 1em;
}
```

```html
<div class="wrap1">
  <div class="content1">
    Lorem ipsum dolor sit amet, consectetur adipisicing elit.  
  </div>
</div>
```

<div class="wrap1">
  <div class="content1">
    Lorem ipsum dolor sit amet, consectetur adipisicing elit.  
  </div>
</div>

2. 用边框和阴影，边框不跟着元素的圆角走，圆角部位的空隙用阴影补齐

```css
.wrap2 {
  background-color: tan;
  padding: 1em;
  box-shadow: 0 0 0 .2em #655;
  border-radius: .5em;
  outline: .5em solid #655;
}
.wrap3 {
  background-color: tan;
  padding: 1em;
  box-shadow: 0 0 0 .2em red;
  border-radius: .5em;
  outline: .5em solid #655;
}
```

```html
<div class="wrap2">Lorem ipsum dolor sit amet, consectetur adipisicing elit.</div>
<div class="wrap3">Lorem ipsum dolor sit amet, consectetur adipisicing elit.</div>
```
<div class="wrap2">Lorem ipsum dolor sit amet, consectetur adipisicing elit.</div>
<br>
<div class="wrap3">Lorem ipsum dolor sit amet, consectetur adipisicing elit.</div>

<style>
* { box-sizing: border-box; }

.wrap1 {
  background-color: #655;
  padding: .5em;
  
  margin-bottom: 1em;
}
.content1 {
  background-color: tan;
  border-radius: .5em;
  padding: 1em;
}

.wrap2 {
  background-color: tan;
  padding: 1em;
  box-shadow: 0 0 0 .2em #655;
  border-radius: .5em;
  outline: .5em solid #655;
  
  margin: 8px;
  margin-bottom: 1em;
}
.wrap3 {
  background-color: tan;
  padding: 1em;
  box-shadow: 0 0 0 .2em red;
  border-radius: .5em;
  outline: .5em solid #655;
  
  margin: 8px;
}
</style>

<div style="margin-top:2em;text-align:right;"><a href="http://hdwills.com/CSS-Secrets-Example/">Back to CSS-Secrets-Example</a></div>
