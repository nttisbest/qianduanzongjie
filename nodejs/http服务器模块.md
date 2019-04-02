# http服务器模块

## 创建服务器

```javascript
//1.导入模块
const http = require('http');
//2.创建服务器
//类似于安装  phpstudy软件

/*参数：回调函数  只要客户端浏览器访问服务器，就会执行这个函数
第一个参数：request  请求对象：负责获取客户端浏览器请求数据
第二个参数：response 响应对象 :负责服务器响应数据
 */
let server = http.createServer((req,res)=>{
    console.log(req.url);
    
});
```

## 开启服务器

```javascript
//3.开启服务器
/* 
ip：电脑网络唯一身份证
port：每一个应用程序都有一个端口号

第一个参数：端口号
第二个参数：ip地址  默认不写就是本机ip
*/
server.listen(3000,()=>{
    console.log('success');
    
});
```

## 根据不同请求响应不同的数据

```javascript
//1.导入模块
const http = require('http');

//2.创建服务器
let server = http.createServer((req,res)=>{
    //这个方法会执行多次：  客户端每请求一次，这个方法就会调用一次
    console.log(req.url);

    //通过判断请求路径：实现根据不同请求响应不同的数据
    if(req.url == '/'){
        res.end('index');
    }else if(req.url == '/login'){
        //设置响应头解决中文乱码: 服务器告诉浏览器我响应给你的数据是什么格式
        /*第一个参数：状态吗 
         */
        res.writeHead(200,{
            'Content-Type':'text/plain;charset=utf-8'
        });
        res.end('这是登录页');
    }else{
        res.end('404 not found');
    }
    
});

//3.启动服务器
server.listen(3000,()=>{
    console.log('success');
    
});
```

## http响应客户端html文件

```javascript
//1.导入模块
const http = require('http');
//导入文件模块
const fs = require('fs');

//2.创建服务器
let server = http.createServer((req,res)=>{
    //需求：  如果路径是/ 返回index.html  如果路径是/login,返回login.html 否则返回404
    if(req.url == '/'){
        //读取index.html文件响应返回
        //浏览器可以自动识别文件数据格式，从而正确加载
        fs.readFile('./views/index.html',(err,data)=>{
            if(err){
                throw err;//500状态码
            }else{
                console.log(data);
                res.end(data);
            }
        });
    }else if(req.url == '/login'){
        fs.readFile('./views/login.html',(err,data)=>{
            if(err){
                throw err;//500状态吗
            }else{
                console.log(data);
                res.end(data);
            }
        })
    }else{
        res.end('404 not found');
    }
});

//3.启动服务器
server.listen(3000,()=>{
    console.log('sucess');
});
```

