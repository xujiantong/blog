#### SASS的安装与使用

```
1.安装Ruby
2.使用gem系列命令安装Ruby的插件和扩展
3.在终端输入 gem install sass 进行安装

```

#### 使用变量

```scss
$blue: #1875e7;
div{
    color: $blue;
}
/** sass还支持变量内嵌在字符串中 **/
$side : left;
.rounded{
    border-#{$side}-radius: 5px; 编译后===> border-left-radius: 5px;
}
```

#### 计算

```scss
$width: 100px;
body{
    margin:(14px/2);
    right: $width * 10%;
}
```

#### 使用@import导入

```scss
/** 可以用来插入外部文件 **/
@import 'path/finame.scss';
```

#### 使用@Extend继承

```scss
.class1{border: 1px solid #ddd}
.class2{
    @extend class1;
}
```

#### 使用@Mixin混入

```scss
/** 使用@Mixin 可以定义一个代码块 **/
@mixin float_left{
    float: left;
    margin-left: 10px;
}
div {
    @include float_left;
}
```

#### 使用 @function 定义函数

```scss
@function double($n){
    @return $n * 2;
}
#sidebar{
    width: double(5px);
}
```

#### 控制语句

```scss
@if可以用来判断
@if 1 + 1 ==2 {border: 1px solid;}
@if 5 < 3 {border: 2px dotted;}

@if lightness($color) > 30% {
    background-color: #000;
} @eles {
    background-color: #fff;
}

@for循环
@for $i from 1 to 10{
    .border-#{$i} {
        border: #{$i}px solid blue;
    }  
}
$i: 6;
@while $i > 0 {
    .item-#{$i}{width: 2em * $i;}
    $i: $i-2;
}

@each $member in a,b,c,d {
    .#{$member} {
        background-image: url("/images/#{$memeber}.png")
    }
}
```

