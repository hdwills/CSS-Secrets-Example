# Mulitple borders (chapter2 - 2)

* box-shadow 方案
    1. box-shadow 支持逗号分隔，可创建任意数量的投影，层层叠加。
    2. 投影不影响布局，而且也不会受到 box-sizing 属性的影响，为了保证投影能完整显示，需要给元素加内或外边距。
    3. “假”边框不会响应鼠标事件（悬停、点击）

* outline 方案  
    与方案 1 相比  
    优势：可使用虚线边框；可边框与元素的距离 outline-offset  
    劣势：只能加到双层；边框不贴合元素的圆角

```html
<div class="mybox"></div>
<div class="mybox1"></div>
```

```css
.mybox {
  margin: 40px 0 40px 40px;
  width: 100px;
  height: 100px;
  background: yellowgreen;
  border-radius: 5px;
  box-shadow: 0 0 0 10px #655, 0 0 0 20px deeppink;
}

.mybox1 {
  width: 100px;
  height: 100px;
  background: yellowgreen;
  border: 10px solid #655;
  outline: 5px dashed deeppink;
  outline-offset: -12px;
}
```

<style>
* {
  box-sizing: content-box;
}

.mybox {
  margin: 40px 0 40px 40px;
  width: 100px;
  height: 100px;
  background: yellowgreen;
  border-radius: 5px;
  box-shadow: 0 0 0 10px #655, 0 0 0 20px deeppink;
}

.mybox1 {
  width: 100px;
  height: 100px;
  background: yellowgreen;
  border: 10px solid #655;
  outline: 5px dashed deeppink;
  outline-offset: -12px;
} 
</style>

<div class="mybox"></div>
<div class="mybox1"></div>

<div style="margin-top:2em;text-align:right;"><a href="http://hdwills.com/CSS-Secrets-Example/">Back to CSS-Secrets-Example</a></div>