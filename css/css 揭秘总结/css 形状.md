#### border-radius 单独指定水平和垂直半径

```css
/** 它可以单独指定水平和垂直半径， 只要用一个斜杠（ /） 分隔这两个值即可。 **/
border-radius: 100px(水平半径) / 75px (垂直半径);
```

#### 平行四边形

```css
.box {
    position: relative;
    width: 100px;
    height: 30px;
    float:left;
	/* 其他的文字颜色、内边距等样式…… */
}
.box::before {
    content: ''; /* 用伪元素来生成一个矩形 */
    position: absolute;
    top: 0; right: 0; bottom: 0; left: 0;
    z-index: -1;
    background: #58a;
    transform: skew(-45deg);
}
```

#### 菱形

```css
/** 方案2: 元素裁剪 炒鸡好看!!!**/
clip-path: polygon(50% 0, 100% 50%, 50% 100%, 0 50%); 

/** 方案1: 基于变形的方案 不建议使用**/
.picture {
    width: 100px;
    height:100px;;
    transform: rotate(45deg);
    overflow: hidden;
    background: #ddd;
    margin: 80px;
}
.picture > img {
	background: #000;
	max-width: 100%;
	height:100px;
	transform: rotate(-45deg) scale(1.42);
}

 
```

#### 切角效果

```css
background: #58a;
background:
linear-gradient(135deg, transparent 15px, #58a 0)
top left,
linear-gradient(-135deg, transparent 15px, #58a 0)
top right,
linear-gradient(-45deg, transparent 15px, #58a 0)
bottom right,
linear-gradient(45deg, transparent 15px, #58a 0)
bottom left;
background-size: 50% 50%;
background-repeat: no-repeat;
------------------------------------------------------
/** 弧形切角 **/
background: #58a;
background:
radial-gradient(circle at top left,
transparent 15px, #58a 0) top left,
radial-gradient(circle at top right,
transparent 15px, #58a 0) top right,
radial-gradient(circle at bottom right,
transparent 15px, #58a 0) bottom right,
radial-gradient(circle at bottom left,
transparent 15px, #58a 0) bottom left;
background-size: 50% 50%;
background-repeat: no-repeat;
```

#### 梯形

```css
transform: perspective(.5em) rotateX(5deg);
```

