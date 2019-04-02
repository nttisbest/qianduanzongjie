# promise

>项目逻辑足够复杂 ，后续步骤必须依赖前置步骤的时候 就会碰到 大量回调嵌套的情况

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Document</title>
  </head>
  <body></body>
</html>
<script>
  /*
  // 回调地狱
    $.ajax({
      success:function(){
         $.ajax({
            success:function(){
               $.ajax({
                  success:function(){
                    
                  }
                })
            }
          })
      }
    })

  // 回调地狱->链式调用
  Promise
    1.Promise 需要实例化才可以使用
    2.Promise 内部可以执行异步的操作 操作执行完毕之后 根据逻辑 触发 成功(.then)或者失败(.catch)的回调
  */
  // resolve 成功回调
  // reject 失败回调
  // let p = new Promise((resolve, reject) => {
  //   // 定时器模拟异步操作
  //   setTimeout(() => {
  //     // 执行成功的逻辑
  //     // resolve('成功啦')
  //     reject('失败啦')
  //   }, 1000)
  // })
  // 错误处理01 第二个回调函数
  // 第二个回调函数 会传到 reject
  // p.then(res => {
  //   console.log(res)
  // },err=>{
  //   console.log(err);
  // })

  // 错误处理02  使用catch
  // catch的回调函数 会传到reject
  // p.then(res => {}).catch(err => {
  //   console.log(err)
  // })

  // 为了简化操作 封装Promise的创建
  // function makePro() {
  //   return new Promise((resolve, reject) => {
  //     // 执行异步的操作
  //     setTimeout(() => {
  //       // 全都是正确的逻辑
  //       resolve('恭喜你对啦')
  //     }, 1000)
  //   })
  // }

  // makePro()
  //   .then(res => {
  //     console.log('第一次异步')
  //     console.log(res)
  //     // 返回一个Promise对象
  //     return makePro()
  //   })
  //   .then(res => {
  //     console.log('第二次异步')
  //     console.log(res)
  //     return makePro()
  //   })
  //   .then(res => {
  //     console.log('第三次异步')
  //     console.log(res)
  //   })

  // axios 基于Promise的封装 axios.get().then()
  let hxios = {
    get() {
      return new Promise((resolve, reject) => {
        // 异步操作
        let randomNum = parseInt(Math.random() * 5)
        // 根据结果 执行不同的逻辑
        setTimeout(() => {
          // 如果大于等于1 成功
          if (randomNum >= 1) {
            resolve('成功啦>>' + randomNum)
          } else {
            reject('失败啦>>' + randomNum)
          }
          // 要么失败
        }, randomNum * 1000)
      })
    }
  }
  hxios
    .get()
    .then(res => {
      console.log(res)
      return hxios.get()
    })
    .then(res => {
      console.log(res)
      return hxios.get()
    })
    .then(res => {
      console.log(res)
      return hxios.get()
    })
    .then(res => {
      console.log(res)
      return hxios.get()
    })
    .then(res => {
      console.log(res)
      return hxios.get()
    })
    .then(res => {
      console.log(res)
      return hxios.get()
    })
    .then(res => {
      console.log(res)
    })

    // async await
</script>

```

