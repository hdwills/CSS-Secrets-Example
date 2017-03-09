# Flexible background positioning (chapter2 - 3)

期望图片(45*32)能和容器的边距有相应的距离
1. CSS 2.1 中对于固定尺寸的容器，可容易实现：
    计算相对于左上角的偏移量，然后精确给值。
  
2. CSS 3 中 background-position 扩展语法，允许我们制定背景图片距离任意角的偏移量，只要我们在偏移量前面制定关键字
    如果不支持此属性，需降级处理。比如舍弃间距直接用固定值贴边显示，优雅降级。
  background: url(https://jsfiddle.net/img/logo.png) no-repeat deeppink right bottom;
  background-position: right 10px bottom 10px;
  
3. background-origin

4. calc()，其中 + - 运算符左右需加空格，不然会解析错误！

```css
.img-box-1 {
  margin-bottom: 10px;
  margin-right: 10px;
  width: 180px;
  height: 128px;
  background: url(https://jsfiddle.net/img/logo.png) no-repeat red;
  background-position: 125px 86px;
}

.img-box-2 {
  margin-bottom: 10px;
  width: 180px;
  height: 128px;
  background: url(https://jsfiddle.net/img/logo.png) no-repeat deeppink;
  background-position: right 10px bottom 10px;
}

.img-box-3 {
  margin-bottom: 10px;
  padding: 10px;
  width: 160px;
  height: 108px;
  background: url(https://jsfiddle.net/img/logo.png) no-repeat green;
  background-position: right bottom;
  background-origin: content-box;
}
.img-box-4 {
  width: 180px;
  height: 128px;
  background: url(https://jsfiddle.net/img/logo.png) no-repeat blue;
  background-position: calc(100% - 10px) calc(100% - 10px);
} 
```

```html
<div class="img-box-1"></div>
<div class="img-box-2"></div>
<div class="img-box-3"></div>
<div class="img-box-4"></div>
```

<style>
* {
  box-sizing: content-box;
}

.img-box-1 {
  margin-bottom: 10px;
  margin-right: 10px;
  width: 180px;
  height: 128px;
  background: url(https://jsfiddle.net/img/logo.png) no-repeat red;
  background-position: 125px 86px;
}

.img-box-2 {
  margin-bottom: 10px;
  width: 180px;
  height: 128px;
  background: url(https://jsfiddle.net/img/logo.png) no-repeat deeppink;
  background-position: right 10px bottom 10px;
}

.img-box-3 {
  margin-bottom: 10px;
  padding: 10px;
  width: 160px;
  height: 108px;
  background: url(https://jsfiddle.net/img/logo.png) no-repeat green;
  background-position: right bottom;
  background-origin: content-box;
}
.img-box-4 {
  width: 180px;
  height: 128px;
  background: url(https://jsfiddle.net/img/logo.png) no-repeat blue;
  background-position: calc(100% - 10px) calc(100% - 10px);
} 
</style>

<div class="img-box-1"></div>
<div class="img-box-2"></div>
<div class="img-box-3"></div>
<div class="img-box-4"></div>

<div style="margin-top:2em;text-align:right;"><a href="http://hdwills.com/CSS-Secrets-Example/">Back to CSS-Secrets-Example</a></div>