# vue-components的data是一个函数

**每创建一个新的组件实例，都会调用data函数，data函数会新开辟一个新的data对象，这样才不会不会相互影响**

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Document</title>
  </head>
  <body>
    <div id="app">
        <addnum></addnum>
        <addnum></addnum>
        <addnum></addnum>
        <addnum></addnum>
    </div>
  </body>
</html>
<script src="./lib/vue.js"></script>
<!-- 模板单独抽取出来
   type只要不是 text/javascript即可
    type="text/x-template"
    type="text/html"
    组件的模板必须有根节点
    组件时可复用的Vue实例
      为了让每一个组件的数据都唯一
      data必须是一个函数 
      返回一个对象
-->
<script id="addNumTem" type="text/x-template">
  <div>
    <span>{{ num }}</span><input  @click="add" type="button" value="+">
  </div>
</script>
```



```javascript

<script>
  // 写组件 ->可以复用的Vue实例
  // 组件命名时 用大写字母 也会被转化为小写
  // 建议用小写
  Vue.component('addnum', {
    // id选择器
    template: '#addNumTem',
    // 组件的data必须是函数
    data() {
      return {
        num: 0,
        step:2
      }
    },
    methods: {
      add() {
        console.log('家啦！！！')
        // this.num++
        this.num+=this.step
      }
    }
  })

  let app = new Vue({
    el: '#app'
  })
</script>

```

