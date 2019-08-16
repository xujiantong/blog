使用 反射 让文字倒映

```css
box-reflect 对于布局没有任何影响
.box-reflect:{<方向><间距><渐变效果>}
方向: above,below,left,right
间距: 表示倒影和元素本身之间的额外距离
渐变效果:none , <url>, <linear-gradient>,<radial-gradient>,<repeating-linear-gradient>,<repeating-radial-gradient>
倒影是不占据空间的
```

```css	
.text-reflect{
    float: left;
    -webkit-box-reflect: below 10px -webkit-linear-gradient(transparent, transparent 50%, rgba(255,255,255,0.5))
}
.text-reflect-base{
    float: left;
    -webkit-box-reflect: below 10px;
}
```

字体阴影 ---光晕 浮雕  投影效果

```css	
color: #fff;
font-size: 60px;
text-shadow: 0 0 5px #FF0000; 字体阴影 偏移量设置为0就可以构建出光晕效果

text-shadow: 2px 2px 4px #000000;垂直偏移量和水平偏移量设置相同的值,就可以构建出凸起的浮雕效果;

基本语法 text-shadow: h-shadow v-shadow blur color;
三个长度参数 第一个表示 水平偏移  第二个表示 垂直偏移  第三个表示模糊程度(可选)
颜色值可以写在最后也可以写在最前

h-shadow  必需,水平阴影的位置,允许负值
v-shadow  必需,垂直阴影的位置,允许负值
blur      可选,模糊的距离
color     可选,阴影的颜色
```

字体描边

```css
-webkit-text-stroke : 1.0px #000;
text-stroke: 1.0px #000;

字体阴影实现字体描边效果
text-shadow: #000 1px 0 0, #000 0 1px 0, #000 -1px 0, #000 0 -1px 0; 
```

字体分栏`类似报纸分栏效果`

```css
column-count: 定义分列的数量
column-gap: 定义每一列中间的宽度
column-rule: 敌营分栏中间的样式

column-rule: 样式宽度 样式类型 样式颜色
eg. column-rule: 2px outset red;
column-rule-style:
	none 没有定义规则
	hidden 定义隐藏规则
	dotted 定义点状规则
	dashed 定义虚线规则
	solid  定义实线规则
    double 定义双线规则
	groove 定义3D
   
	
```

处理字体溢出和破字

```css
{
    display: block;
    white-space: normal; /*文本不换行*/
    text-overflow: ellipsis; /*重点*/
    overflow: hidden; /*不允许出现滚动条*/
    width: 100px;
}

text-overflow: clip 修剪文本
			  ellipsis 显示省略号来来代表修剪的文本
               string 使用给定的字符串来代表被修剪的文本
```



