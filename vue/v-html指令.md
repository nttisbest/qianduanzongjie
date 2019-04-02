# v-html

```html
<div id="app" class="app">
  <!-- v-html会把原始内容替换 -->
  <p v-html="info">西兰花炒蛋</p>
  <!-- 如果有html结构会解析 -->
  <p v-html="a">花菜炒蛋</p>
  <!-- 没有简写方式 -->
</div>
```

```JavaScript
/*
  1.可以解析html
  2.会直接替换标签内部的内容
  3.没有简写
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

