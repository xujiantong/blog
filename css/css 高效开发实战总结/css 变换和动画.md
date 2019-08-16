#### 变换 Transform

```css
旋转 扭曲 位移 缩放
rotate 旋转变换 transform: rotate(7deg); rotateX /*沿X轴旋转*/ rotateY /*沿Y轴旋转*/
skew 扭曲变换 skew(30deg, 120deg)
scale 比例缩放
translate 位移变换

```

#### 渐变 Transition (过渡)

```css
transition: all .5s ease 1s  ; 属性 / 过渡时间/ 过渡函数/ 延迟时间

/*过渡函数*/
ease 逐渐变慢
linear 匀速
ease-in 加速
ease-out 减速
ease-in-out 加速然后减速
cubic-bezier 允许开发者自定义一个开发曲线

```

#### 关键帧 @keyframes

```css
@keyframe spin {
    from{
        transform: scale(1);
    }
    to{
        transform: scale(2);
    }
}
@keyframe spin {
    0% {
        transform:rotateY(0)
    }
    50% {
        transform: rotateY(-180deg)
    }
    100% {
        transform: rotateY(-360deg)
    }
}
animation: spin 8s infinite linear; 动画名称/第一次执行动画的时间/动画循环次数/动画的速度函数
animation-play-state:paused(暂停动画)/running(开始动画)
```

#### 动画参考 css 样式库

```
hover.css
ihover.css
move.js
```

