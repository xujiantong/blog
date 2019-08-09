## 用匿名函数保留全局变量的值 

``` javascript
function asyncFunction(callback){
	setTimeout(callback, 200)
}
var color = 'blue';
(function(color){
    asyncFunction(function(){
        console.log('The color is ' + color)
    })
})(color)
color = 'green'
```

