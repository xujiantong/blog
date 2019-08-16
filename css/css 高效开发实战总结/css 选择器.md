相邻元素选择器

```html	
<div class="content">
    <h1>
        测试
    </h1>
    <p>测试内容</p>
</div>
<style>
    h1+p{
        color:red;
    }
</style>
```

属性选择器

```css
[title]{color:red}

a[href][title]{color:red}

a[href="http://baidu.com"][title="百度"]{
    color:red;
}
```

```css
:only-child /*如果一个父元素只有一个子元素,那么选取这个子元素*/

:root 选择文档的根元素 html

:empty 是用来选择没有任何内容的而元素

目标伪类
:target

状态伪类
input:enabled  input:disabled
:checked  == input["check"]
:indeterminate 当前页面打开时,某组中的单选框或复选框元素还没有选取状态时的样式
:default 状态伪类选择器用来指定当前元素处于非选取状态的单选框或复选框的样式

:not(selector) 将selector的元素排除
div :not(.test){
    background: red;
}

```

