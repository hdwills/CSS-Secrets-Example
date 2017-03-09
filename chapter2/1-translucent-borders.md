# Translucent borders (chapter2 - 1)

默认背景会延伸到边框所在的区域下层，即使你用的不透明的实色边框。  
背景并没有从半透明的边框处透上来。  
background-clip: border-box(默认值) / padding-box  
用内边距的外沿来把背景裁掉

```html
<div class="wrap1">
  <div class="mybox1"></div>
</div>

<div class="wrap">
  <div class="mybox"></div>
</div>
```

```css
.wrap {
  width: 60px;
  height: 60px;
  background: blue;
}

.mybox {
  width: 50px;
  height: 50px;
  border: 5px dashed rgba(0,0,0,.5);
  background: #999;
  background-clip: padding-box;
}

.wrap1 {
  width: 60px;
  height: 60px;
  background: red;
  margin-bottom: 20px;
}

.mybox1 {
  width: 50px;
  height: 50px;
  border: 5px dashed rgba(0,0,0,.5);
  background: #999;
}
```

<style>
* {
  box-sizing: content-box;
}

.wrap {
  width: 60px;
  height: 60px;
  background: blue;
}

.mybox {
  width: 50px;
  height: 50px;
  border: 5px dashed rgba(0,0,0,.5);
  background: #999;
  background-clip: padding-box;
}

.wrap1 {
  width: 60px;
  height: 60px;
  background: red;
  margin-bottom: 20px;
}

.mybox1 {
  width: 50px;
  height: 50px;
  border: 5px dashed rgba(0,0,0,.5);
  background: #999;
}
</style>

<div class="wrap1">
  <div class="mybox1"></div>
</div>

<div class="wrap">
  <div class="mybox"></div>
</div>

<div style="margin-top: 2em"><a href="http://hdwills.com/CSS-Secrets-Example/">Back to CSS-Secrets-Example</a></div>