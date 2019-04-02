# 箭头函数的this指向

```
函数上谁点出来的this 就是谁
箭头函数中的this
会跟创建箭头函数 的上下文中的this 相同 并且进行绑定 无法修改
    1.上下文中的this 就是创建箭头函数 所处作用域中的this
    2.this绑定，箭头函数无法使用 call apply bind
语法糖
  程序员可以用很少的编码 实现功能
  箭头函数就是一个语法糖
  语法糖的本质 是把简洁的代码 通过编译器（把代码翻译为计算机可以识别的
  babel的可以把简介的代码翻译会去
```

```javascript
// 箭头函数
setTimeout(() => {
   console.log(this)
    setTimeout(() => {
      console.log(this)
      setTimeout(() => {
        console.log(this)
        setTimeout(() => {
          console.log(this)
        }, 1000)
      }, 1000)
    }, 1000)
  }, 1000)
  // let that = this;
  //  定时器
  // setTimeout(function() {
  //   console.log(this)
  //   setTimeout(function() {
  //     console.log(this)
  //     setTimeout(function() {
  //       console.log(this)
  //       setTimeout(function() {
  //         console.log(this)
  //       }, 1000)
  //     }, 1000)
  //   }, 1000)
  // }, 1000)
}
```

> 在vue中,一般是指vue创建的对象.