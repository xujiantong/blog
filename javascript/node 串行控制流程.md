### 躲开回调嵌套的情况 

#### Nimble这样的流程控制工具执行这些任务 

```javascript
// npm install nimble
let flow = require('nimble');

flow.series([
    function(callback){
        setTimeout(function(){
            console.log("I execute first");
            callback();
        },1000)
    },
    function(callback){
        setTimeout(function(){
            console.log("I execute next");
            callback();
        },500)
    },
    function(callback){
        setTimeout(function(){
            console.log("I execute last");
            callback();
        },100)
    }
])
```

