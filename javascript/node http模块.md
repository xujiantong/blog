### Node中的http模块提供了HTTP服务器和客户端接口 

```javascript
const http = require('http');
// 创建HTTP服务器要调用http.createServer()函数
http.createServer(function(req, res){
                  
})

//Node不会自动往客户端写任何响应
res.end(); //方法结束响应


```

