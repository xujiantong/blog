```css
@media screen{}
@media print{}
```

#### 响应式设计一般遵循四个原则

- 重要内容优先
- 体验的一致性
- 友好的连接
  - 引导要清晰强烈
  - 适合手指操作
  - 区块不宜过小
- 考虑移动操作习惯
  - 左手握
  - 右手点

#### 媒介查询的基本语法

```css
@media screen and (max-width:600px){} /* 小于 600 像素的窗口 */

@media screen and (min-width:600px) and (max-width:1200px) /* 宽度在600~900像素之间的窗口 */
```

```
orientation 判断屏幕翻转
device-aspect-ratio 判断屏幕的纵横比
width 窗体宽度
height 窗体高度
device-width 屏幕宽度
device-height 屏幕高度
orientation 设备手持方向 portrait(横向)/landscape(纵向)
aspect-ratio 设备屏幕长宽比
color 颜色模式
color-index 颜色模式列表整数
monochrome 整数
resolution 解析度
grid 栅格设备 整数返回0/1
```

#### 检测设备翻转

```html	
<link rel="stylesheet" media="scree and(orientation:portrait)" href="portrait.css" />
<link rel="stylesheet" media="scree and(orientation:landscape)" href="landscape.css" />
<script>
    window.addEventListener('orientationchange',function(){
        // 这里编写触发屏幕转换时的函数
    })
</script>
```

#### 几个常用的标签

```html	
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<!-- 使用 viewport meta标签在手机浏览器上控制布局 -->
<meta name="apple-mobile-web-app-capable" content="yes"/>
<!-- 通过快捷方式打开时全屏显示 -->
<meta name="apple-mobile-web-app-status-bar-style" content="blank"/>
<!-- 隐藏状态栏 -->
<meta name="format-detection" content="telephone=no"/>
<!-- iPhone 会将看起来像电话号码的数字添加电话连接, 应当关闭-->
```

#### 开发中会遇到的几个问题

```
如何应用媒介查询
响应式设计的基本规则
如何解决兼容性问题
不同设备的尺寸总结
设备反转的处理方法
```

