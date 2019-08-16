#### background-size

```css
background-size: 80px 60px; /* 直接使用长度单位或百分比来指定背景的尺寸 */
background-size: cover; /* 宽度等于元素宽度, 高度设为auto */
background-size: contain; /* 高度等于元素高度, 宽度设为 auto */
```

#### 利用图层叠加,实现多背景

```css
/*css3 允许设置多个背景图片,每个背景图片占一层,层的上下按照css中书写的顺序来定\*/
background: url('./1.png') 0 0  no-repeat,
            url('./2.png') 200px 0  no-repeat,
            url('./2.png') 400px 201px  no-repeat
```

#### 改变图片显示范围, 只在内容部分显示背景

```css
/*指定了图片的起始位置*/
background-origin: border-box / padding-box/ content-box;
background-clip: border-box / padding-box/ content-box;
```

#### 线性渐变

```css
linear-gradient 纵向渐变
radial-gradient 横向渐变
repeating-linear-gradient 重复的纵向渐变
repeating-radial-gradient 重复的横向渐变

background: linear-gradient(red, blue); /*从上到下颜色渐变*/
/*指定方向*/
background: linear-gradient(to right, red, blue);
/*使用角度*/
background: linear-gradient(45deg, red, blue);
/*彩虹色*/
background: linear-gradient(to right, red, orange, yellow, green, blue, indigo, violet)
```

放射渐变

```css
.test{
    width: 200px;
    height: 200px;
    border-radius: 50%;
    background: radial-gradient(red, green, blue);
    background: radial-gradient(red 5%, green 15%, blue 50%);
    background: radial-gradient(buttom left, red 5%, green 15%, blue 50%);
}
```