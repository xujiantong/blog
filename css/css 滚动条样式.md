## CSS 滚动条样式

```css
/*滚动条样式*/
::-webkit-scrollbar {
    width: 4px;
    height: 14px;
}

::-webkit-scrollbar-track,
::-webkit-scrollbar-thumb {
    border-radius: 999px;
    /*border: 10px solid transparent;*/
}
/*定义滚动条轨道 内阴影+圆角*/ 
::-webkit-scrollbar-track {
    /*box-shadow: 1px 1px 5px rgba(0, 0, 0, 0.2) inset;*/
    background: #001229;
}
/*定义滑块 内阴影+圆角*/ 
::-webkit-scrollbar-thumb {
    min-height: 20px;
    background-clip: content-box;
    /*box-shadow: 0 0 0 5px rgba(0, 0, 0, 0.2) inset;*/
    background: #323D4B;
}

::-webkit-scrollbar-corner {
    background: transparent;
}

::-webkit-scrollbar-thumb:hover {
    background: #a8a8a8;
}
```

```markdown
::-webkit-scrollbar 滚动条整体部分
::-webkit-scrollbar-thumb  滚动条里面的小方块，能向上向下移动（或往左往右移动，取决于是垂直滚动条还是水平滚动条）
::-webkit-scrollbar-track  滚动条的轨道（里面装有Thumb）
::-webkit-scrollbar-button 滚动条的轨道的两端按钮，允许通过点击微调小方块的位置。
::-webkit-scrollbar-track-piece 内层轨道，滚动条中间部分（除去）
::-webkit-scrollbar-corner 边角，即两个滚动条的交汇处
::-webkit-resizer 两个滚动条的交汇处上用于通过拖动调整元素大小的小控件
```

