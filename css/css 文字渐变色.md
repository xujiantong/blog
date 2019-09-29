#### css 文字渐变色

```css
background-image: -webkit-gradient(linear, left 0, right 0, from(rgb(16, 158, 255)), to(rgb(191, 15, 255)));
/*必需加前缀 -webkit- 才支持这个text值 */
-webkit-background-clip: text;
/*text-fill-color会覆盖color所定义的字体颜色： */
-webkit-text-fill-color: transparent;
```

#### css边框渐变色

```css
.content { 
	width: 100px; 
   	height: 100px; 
    box-sizing: border-box; 
    padding: 5px; 
    border-radius: 50%; 
    background-image: -webkit-linear-gradient(top, red 0%, blue 30%, yellow 60%, green 90%);  
    background-image: -moz-linear-gradient(top, red 0%, blue 30%, yellow 60%, green 90%); 
    background-image: linear-gradient(top, red 0%, blue 30%, yellow 60%, green 90%);  
}
.box { 
	width:100%; 
    height:100%; 
    border-radius:50%; 
    background:#fff; 
}
```

