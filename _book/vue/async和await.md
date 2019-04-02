# async和await

> es7的异步解决方案 目前的终极解决方案 async  await

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
    Promise
      回调地狱->链式编程
      1.实例化Promise对象
      2.传入的参数是一个函数，函数内部执行的是异步的逻辑 
      3.通过Promise对象的then方法可以在异步执行完毕之后触发
      4.resolve,reject 分别是正确和错误的回调，到底执行那个 看我们封装的代码逻辑
  */

  // let p = new Promise((resolve, reject) => {
  //   let randomNum = parseInt(Math.random() * 10)
  //   // 异步的逻辑
  //   setTimeout(() => {
  //     // 根据结果 执行正确 或者错误的回调
  //     if (randomNum > 8) {
  //       resolve('正确' + randomNum)
  //     } else {
  //       reject('错误' + randomNum)
  //     }
  //   }, 2000)
  // })
  // p.then(res => {
  //   console.log(res)
  // }).catch(res=>{
  //   console.log(res);
  // })
  // axios
  // axios.get().then(res=>{})

  let hxios = {
    get(url) {
      return new Promise((resolve, reject) => {
        // 使用Promise封装ajax
        //1.创建对象
        let xhr = new XMLHttpRequest()
        //2.设置请求行(get请求数据写在url后面)
        xhr.open('get', url)
        //3.设置请求头(get请求可以省略,post不发送数据也可以省略)
        //3.5注册回调函数 onload
        xhr.onreadystatechange = function() {
          if (xhr.status == 200 && xhr.readyState == 4) {
            // callback(xhr.responseText)
            resolve(xhr.responseText)
          }
        }
        //4.请求主体发送(get请求为空，或者写null，post请求数据写在这里，如果没有数据，直接为空或者写null)
        xhr.send(null)
      })
    },
    getOld(url, callback) {
      // 使用Promise封装ajax
      //1.创建对象
      let xhr = new XMLHttpRequest()
      //2.设置请求行(get请求数据写在url后面)
      xhr.open('get', url)
      //3.设置请求头(get请求可以省略,post不发送数据也可以省略)
      //3.5注册回调函数 onload
      xhr.onreadystatechange = function() {
        if (xhr.status == 200 && xhr.readyState == 4) {
          callback(xhr.responseText)
        }
      }
      //4.请求主体发送(get请求为空，或者写null，post请求数据写在这里，如果没有数据，直接为空或者写null)
      xhr.send(null)
    }
  }
  // 测试数据获取
  // hxios
  //   .get('http://wthrcdn.etouch.cn/weather_mini?city=深圳')
  //   .then(res => {
  //     console.log(res)
  //     return hxios.get('http://wthrcdn.etouch.cn/weather_mini?city=武汉')
  //   })
  //   .then(res => {
  //     console.log(res)
  //     return hxios.get('http://wthrcdn.etouch.cn/weather_mini?city=北京')
  //   })

  // es7的异步解决方案 目前的终极解决方案 async  await
  // async 必须放在函数声明的左边
  // await 必须 放在 async修改的函数内部
  // 这样的函数 称之为 异步函数 写的时候跟同步一样，但是 内部的逻辑是异步的
  // async await 可以把链式调用-> 看起来是同步执行
  // async 内部的异步操作 是依次执行的 函数外部的操作 不会受到异步的影响
  async function searchWeather() {
    let res1 = await hxios.get(
      'http://wthrcdn.etouch.cn/weather_mini?city=武汉'
    )
    console.log(res1)
    let res2 = await hxios.get(
      'http://wthrcdn.etouch.cn/weather_mini?city=深圳'
    )
    console.log(res2)
    let res3 = await hxios.get(
      'http://wthrcdn.etouch.cn/weather_mini?city=东莞'
    )
    console.log(res3)
    let res4 = await hxios.get(
      'http://wthrcdn.etouch.cn/weather_mini?city=潮州'
    )
    console.log(res4)
  }
  // 异步函数
  searchWeather()
  console.log('我是底部的代码')

  // axios 一般是在某些方法中获取数据 点击事件  生命周期函数
  let app = {
    el: 'xx',
    async created() {
      let res = await axios.get('xxx')
    },
    methods: {
      async click() {
        let res = await axios.get('xxx')
      }
    }
  }
</script>

```

