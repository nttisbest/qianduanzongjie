# v-text指令

```html
<div id="app" class="app">
  <!-- 如果使用v-text 会直接替换标签内部的内容 -->
  <h2 v-text="info">你好吗？</h2>
  <!-- 不会解析html结构 -->
  <h2 v-text="a">你好吗？</h2>
  <!-- 如果想要跟原始内容进行拼接 可以使 {{}} v-text的简写方式 也是
  <h2>你好吗?{{ info }}</h2>
  <h2>你好吗?{{ info + '中分还带波浪' }}</h2>
  <h2>你好吗?{{ info.length }}</h2>
</div>
```

```javascript
/*
  1.简写 {{}}
  2.内部可以写表达式
*/ 
var app = new Vue({
  // 选择器
  el: '#app',
  // 数据
  data: {
    info: '感觉自己萌萌哒',
    a: '<a href="#">萌你奶奶个腿</a>'
  }
})
```

