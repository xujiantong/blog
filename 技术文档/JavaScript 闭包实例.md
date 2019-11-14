#### 常见闭包实例

```js
var cnt = (function(){
    var a = 0;
    return function(){
        console.log(a);
        a++;
    }
})()
cnt(); //=>0
cnt(); //=>1
cnt(); //=>2
```

```js
var arr = [1,2,3,4,5];
for(var i = 0; i < 5; i++){
    (function(j){
        setTimeout(function(){
            console.log(arr[j]);
        },0)
    })(i)

}
```

```js
// 问题代码
function box(){
  var arr=[];
  for(i=0;i<5;i++){
      arr=function(){return i;}
    }
return arr;  
}
var a=box();
alert(a);//包含五个函数体的数组
alert(a[0]());
alert(a[1]());

// 解决方案1
function box(){
  var arr=[];
  for(i=0;i<5;i++){
      arr=(function(num){return i;})(i);
    }
return arr;  
}
var a=box();
for(var i=0;i<a.length;i++){
  alert(a);
}


// 解决方案2
function box(){
var arr=[];
    for(var i=0;i<5;i++){


        arr=(function(num){
            return function(){return num;}
        })(i);

    }
return arr;        
}
 
var arr=box();
 
for(var i=0;i<5;i++){
    alert(arr());//0,1,2,3,4
}


// 关键代码
arr=(function(num){
         return function(){return num;}
})(i);
// i=0 时
arr[0]=(function(num){return function(){return num;}})(0);
// 1时
arr[1]=(function(num){return function(){return num;}})(1);
```

```
当函数可以记住并访问所在的词法作用域时， 就产生了闭包， 即使函数是在当前词法作用域之外执行。
无论通过何种手段将内部函数传递到所在的词法作用域以外， 它都会持有对原始定义作用域的引用， 无论在何处执行这个函数都会使用闭包。
```

```
本质上无论何时何地， 如果将函数（访问它们各自的词法作用域） 当作第一
级的值类型并到处传递， 你就会看到闭包在这些函数中的应用。 在定时器、 事件监听器、Ajax 请求、 跨窗口通信、 Web Workers 或者任何其他的异步（或者同步） 任务中， 只要使用了回调函数， 实际上就是在使用闭包！
```

