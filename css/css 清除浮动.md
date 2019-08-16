# css 清除浮动

## 最优浮动闭合方案

```css
.clearfix:after{
    content:".";
    display:block;
    height:0;
    clear:both;
    visibility:hidden;
} 
```

## 最简单的清除浮动的办法（推荐）：

```css
.clearfix{overflow:auto;zoom:1} /* zoom is only for IE6 */ 
/* 或 */
.clearfix{overflow:hidden;zoom:1} /* zoom is only for IE6 */  
```

## 骨灰级

```css
/* 缺陷就是改变了html结构*/
.clear{
    clear:both;
}  
/* 或 */
.clear{
    clear:both;
    height:0;
    overflow:hidden;
}  
```

