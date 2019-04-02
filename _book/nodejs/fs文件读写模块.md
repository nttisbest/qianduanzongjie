# fs文件读写模块

## 读取文件

```javascript
const fs =  require('fs');
/* 异步读取文件
第一个参数：文件路径
第二个参数：可选  文件编码（默认二进制）  中文：'utf-8'
第三个参数: 读取回调  err:错误信息  data:读取到的数据
*/
fs.readFile('./data/aaa.txt','utf-8',(err,data)=>{
    if(err){
        /* 抛出异常:让node程序停止工作，告诉你具体报错原因，用于调试方便 */
        throw err;
        // console.log(err);
    }else{// err = null
        console.log(data);
        
    }
})

```

## 写文件

```javascript
//1.导入模块
const fs = require('fs');
//2.使用模块
/* 
第一个参数：文件路径
第二个参数：文件数据
第三个参数：文件编码 可选  自动识别文件编码
第四个参数：回调函数   err:错误信息
*/
fs.writeFile('./data/bbb.txt','低着头做事，夹着尾巴做人',(err)=>{
    if(err){
        throw err;
    }else{
        console.log('写入成功');
        
    }
});
```

## 异步和同步的区别

```javascript
/* nodejs中很多api都分为同步和异步
    * 1.一般清空下都是异步（推荐）
    * 2.如果想使用同步，只需要在api后面加上Sync即可
*/

/*js编译代码步骤
1.从上往下编译代码
2.如果是同步：立即执行
3.如果是异步，不执行，而是放入事件循环（队列）Event Loop
4.所有代码编译完毕之后，开始执行事件队列中的异步 
 */


/*同步与异步区别
1.同步阻塞线程(效率低)，异步不阻塞
2.同步有序执行，异步无序执行（随机） : 同步先于异步（女士优先）
3.同步没有回调函数，异步有回调函数
 */
```

