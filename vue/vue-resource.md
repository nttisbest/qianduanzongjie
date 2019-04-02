# vue-resource

> vue-resource 是vue的一个ajax插件
>
> [https://github.com/pagekit/vue-resource](https://github.com/pagekit/vue-resource)

+ 可以发ajax请求
+ JSONP

```javascript
<!-- 开发环境版本，包含了有帮助的命令行警告 jquery.js -->
<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
<!-- vue-resource 其实 为Vue增加了一个$http的属性 把所有的请求方法都设置在这个属性上 -->
<script src="https://cdn.jsdelivr.net/npm/vue-resource@1.5.1"></script>
<script>
  let app = new Vue({
    el: '#app',
    data: {
      city: '',
      weatherList: []
    },
    methods: {
      searchWeather() {
        console.log(this.$http)
this.$http.get('url string').then(response => {
// 成功触发的函数
// console.log(response)
},errResponse => {
// 错误时触发
console.log(errResponse)
}
)
}
}
})
</script>
```

