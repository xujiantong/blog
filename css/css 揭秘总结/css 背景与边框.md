#### 透明边框

```css
{
    border: 10px solid rgba(255,255,255,0,5);
    background: #fff;
    background-clip: padding-box;
}
```

#### 多重边框

```css
{
    background: yellowgreen;
    box-shadow:0 0 0 10px #655,
        0 0 0 15px deeppink,
        0 2px 5px 15px rgba(0,0,0,0.5);
}
```

#### 缝边效果

```css
{
    background: #6C5A57;
    outline: 2px dashed #fff;
    outline-offset: -10px;
}
```

#### 灵活的背景定位

```css
/** 如果想让背景图片跟右边缘保持 20px 的偏移量， 同时跟底边保持 10px 的偏移量 **/
/* 方法1 */
background: url(code-pirate.svg) no-repeat #58a;
background-position: right 20px bottom 10px;
/* 方法2 */
padding: 10px;
background: url("code-pirate.svg") no-repeat #58a
bottom right; /* 或 100% 100% */
background-origin: content-box;

/* 方法3 */
background: url("code-pirate.svg") no-repeat;
background-position: calc(100% - 20px) calc(100% - 10px);
```

#### 一个容器， 只在内侧有圆角， 而边框或描边的四个角在外部仍然保持直角的形状

```css
background: tan;
border-radius: .8em;
padding: 1em;
box-shadow: 0 0 0 .6em #655;
outline: .7em solid #655;
```

#### 条纹背景

```css
/* 假设我们有一条基本的垂直线性渐变， 颜色从 #fb3 过渡到 #58a */
background: linear-gradient(#fb3, #58a); 
=> background: linear-gradient(#fb3 20%, #58a 80%);
=> background: linear-gradient(#fb3 50%, #58a 50%); /* 已经没有任何渐变效果了， 只有两块实色 */
/* 本质上， 我们已经创建了两条巨大的水平条纹。*/

/** 
如果多个色标具有相同的位置， 它们会产生一个无限小的过渡区域，
过渡的起止色分别是第一个和最后一个指定值。 从效果上看， 颜色会在那
个位置突然变化， 而不是一个平滑的渐变过程。
**/
/** 等宽水平条纹 **/
background: linear-gradient(#333 50%, #666 50% );
background-size: 100% 30px;
/** 不等宽水平条纹 **/
background: linear-gradient(#fb3 30%, #58a 30%);
background-size: 100% 30px;

/** 如果我们把第二个色标的位置值设置为 0， 那它的位置就
总是会被浏览器调整为前一个色标的位置值 **/
background: linear-gradient(#fb3 30%, #58a 0);
background-size: 100% 30px;


/*** 生成三种颜色的条纹 ***/
background: linear-gradient(#fb3 33.3%,
#58a 0, #58a 66.6%, yellowgreen 0);
background-size: 100% 45px;
```

#### 垂直条纹

```css
background: linear-gradient(to right , #f69 50%, #eee 50%);
background-size:  45px 100%;
/** 或 **/
background: linear-gradient(90deg , #f69 50%, #eee 50%);
background-size: 45px 100% ;
```

#### 斜向条纹

```css
/** 错误的 **/
background:linear-gradient(45deg, #f69 50%, #f11 0%);
background-size: 35px 35px;

/** 正确的 **/
background: linear-gradient(45deg, #fb3 25%, #58a 0, #58a 50%, #fb3 0, #fb3 75%, #58a 0);
background-size: 30px 30px;

/** 简洁的 **/
background: repeating-linear-gradient(60deg,#fb3, #fb3 15px, #58a 0, #58a 30px);
background: repeating-linear-gradient(60deg, #fb3 0 15px, #58a 0 30px);
/** 灵活的同色系条纹 **/
background: repeating-linear-gradient(30deg,
#79b, #79b 15px, #58a 0, #58a 30px);


background: #58a;
background-image: repeating-linear-gradient(30deg,
hsla(0,0%,100%,.1),
hsla(0,0%,100%,.1) 15px,
transparent 0, transparent 30px)
```

#### 网格、 波点、 棋盘 

```css
/** 网格背景 **/
background: white;
background-image: linear-gradient(90deg,
rgba(200,0,0,.5) 50%, transparent 0),
linear-gradient(
rgba(200,0,0,.5) 50%, transparent 0);
background-size: 30px 30px;
-------------------------------------------
background: #58a;
background-image:
linear-gradient(white 1px, transparent 0),
linear-gradient(90deg, white 1px, transparent 0);
background-size: 30px 30px;


/** 波点 **/
background: #655;
background-image: radial-gradient(tan 30%, transparent 0),
radial-gradient(tan 30%, transparent 0);
background-size: 30px 30px;
background-position: 0 0, 15px 15px;
```

#### 伪随机背景

```css
background: hsl(20, 40%, 90%);
background-image:
linear-gradient(90deg, #fb3 10px, transparent 0),
linear-gradient(90deg, #ab4 20px, transparent 0),
linear-gradient(90deg, #655 20px, transparent 0);
background-size: 80px 100%, 60px 100%, 40px 100%;
```

#### 老式信封背景

```css
padding: 1em;
border: 1em solid transparent;
background: linear-gradient(white, white) padding-box,
repeating-linear-gradient(-45deg,
red 0, red 12.5%,
transparent 0, transparent 25%,
#58a 0, #58a 37.5%,
transparent 0, transparent 50%)
0 / 5em 5em;
```

