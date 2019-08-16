## Less 其实更多

扩展了 `变量 继承 函数 计算` 等

#### 使用变量和操作符

```less
/* 在LESS中使用@对变量进行定义*/
@color : #f69;
#header{
    color: @color;
}
```

#### 使用Mixin混入

```less
/* Mixin 在这里具体的作用就是把一些通用的定义抽取出来,以后就无需编写重复代码了 */
.rounded-corners(@radius: 5px){
    -webkit-border-radius: @radius;
    -moz-border-radius: @radius;
    -ms-border-radius: @radius;
    -o-border-radius: @radius;
    border-radius: @radius;
}
#header{
    .rounded-corners;
}
#footer{
    .rounded-corners(10px);
}
/* Mixin的语法关键词是一个 . 符号*/
```

#### 内嵌规则

```less
/* less 可以用嵌套的方式编写层叠样式 */ 
/* Before */
#main{...} #main div{...} #main div p{...}
/* Now */
#main{
    background: #ccc;
    div{
        color: red;
        li{
            font-size: 12px;
        }
    }
}
```

#### 运算

```less
/* 任何数字、变量或者颜色都可以参加运算 */
@base: 5%;
@filler: base * 2;
@other: @base + @filler;
@color: #888 / 4;
background: @base-color + #111;
height: 100%/2 + @filler;

/* less 的运算能分辨出颜色和单位 */
@length: 1px + 7; => 8px

/* 可以使用括号来改变 运算 的优先级 */
@width: (@var + 5) * 2;

/* 可以在符合属性中进行运算 */
border: (@width * 2) solid black;    
```