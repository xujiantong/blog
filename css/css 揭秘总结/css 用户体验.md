#### 自定义复选框

```css
<input type="checkbox" id="awesome" />
<label for="awesome">Awesome!</label>

input[type="checkbox"] + label::before {
content: '\a0'; /* 不换行空格 */
display: inline-block;
vertical-align: .2em;
width: .8em;
height: .8em;
margin-right: .2em;
border-radius: .2em;
background: silver;
text-indent: .15em;
line-height: .65;
}
input[type="checkbox"]:checked + label::before {
content: '\2713';
background: yellowgreen;
}
input[type="checkbox"] {
position: absolute;
clip: rect(0,0,0,0);
}

input[type="checkbox"]:focus + label::before {
box-shadow: 0 0 .1em .1em #58a;
}
input[type="checkbox"]:disabled + label::before {
background: gray;
box-shadow: none;
color: #555;
}
```

