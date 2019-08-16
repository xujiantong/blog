### 弹性盒子 Flex-box (待定是否已过时或修订)

#### 基本用法

```css
.father{display: box} /* 父元素声明 , 有了这个声明 才能证明父元素的空间是可以被子元素分配的。 */
/*假设要在这个父元素内部进行一个三栏布局 比例是 1:3:1*/
.son1{box-flex:1}
.son2{box-flex:3}
.son3{box-flex:1}
/* 如果想采用中间固定宽度, 两侧成比例自适应布局,同样非常简单*/
.son1{box-flex:1}
.son2{width: 500px}
.son3{box-flex:1}
```

#### 注意

```
多列模块中的 column-* 属性对弹性子元素无效
float和clear对弹性子元素无效 使用float会导致display属性计算为block
vertical-align 对弹性子元素的对其无效
```

#### 问题

```
需要垂直分配空间
需要页面先加载中间部分
需要控制剩余空间的使用
```

#### 控制子元素方向

```css
/** 
在父元素中定义box-orient属性来确定子元素的排列方向
可选值有horizontal、vertical、inline-axis、block-axis、inherit
其中 inline-axis是默认值,且horizontal 与 inline-axis的效果值一样,让子元素横排
vertical与block-axis的效果也一样,让元素竖排
inherit和用在其他属性中是一样的,表示继承父元素 
**/
.container {
	display:flex-box
    box-orient:block-axis;
}

```

#### 控制元素对齐

```css
/**
box-align与 box-pack都能决定盒子内部剩余空间怎么使用,在效果上类似我们平常说的"对齐"
**/

/**
box-align决定了垂直方向上的对齐表现, 可选参数有 start,end,center,baseline,stretch
其中stretch是默认值,表示拉伸
end为底部对齐
center为居中对齐
baseline表示基线(起始文字的底边位置线)对齐
**/

/**
box-pack决定了父标签水平遗留空间的使用,其可选值有start,end,center,justify
默认值为start,具体的表现类似于 text-align的left,right,center,justify属性
**/
.container{
    display: flex-box
}
```

#### 控制元素显示顺序

