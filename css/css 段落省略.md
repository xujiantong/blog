## CSS  段落文字过长时自动省略的方法

#### 单行情况

```css
white-space: nowrap;
overflow: hidden;
text-overflow: ellipsis;
```

#### 多行情况

```css
display: -webkit-box;
-webkit-box-orient: vertical;
-webkit-line-clamp: 2; //显示文字的行数
overflow: hidden;
word-break: break-all;
```



