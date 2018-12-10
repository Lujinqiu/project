# 三阶段的server

```
//原生模块：nodejs自带的模块，不需要安装，直接使用

//端口

const http = require('http');

//服务器

//请求request

//响应response

//端口  app.listen('端口号',function(){console.log(('服务器连接成功，端口号为3005')})

let app = http.createServer(function(

    request,response){

    //设置响应头，不然服务器不识别

    response.writeHead(200,{'content-type':'text/html;charset=utf-8'});

    //写内容

    response.write('hello word');

    response.write('<h1>你好啊，球球</h1>');

    //标志显示结束，这句必须写的

    response.end('<h2>你好啊，各位<h2>');

    //有修改就必须重启服务器，就是黑窗户重启一下

});

// 配置监听端口

//listen()

app.listen(3005,function(){

console.log('服务器连接成功，端口号为3005');

});

```

## 响应头里面的响应类型

1. text/html   纯文本
2. text/pkain
3. application/json