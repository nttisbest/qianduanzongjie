# v-bind

```html
<div id="app">
  <!-- 完整写法 -->
  <!-- <h2 v-bind:style="'color:'+setColor" @click="changeColor">你好
  <!-- 简写 -->
  <h2 style="color:hotpink" >你好吗</h2>
  <h2 :style="'color:'+setColor" @click="changeColor">你好吗</h2>
  <img :src="imgUrl" @click="imgUrl='./img/girl.png'" alt="" />
</div>
```

```javascript
let app = new Vue({
  // 不可以使用body和html
  // el:"body"
  el: '#app',
  data: {
    setColor: 'yellowgreen',
    imgUrl: './img/cat.gif'
  },
  methods: {
    changeColor() {
      this.setColor = 'hotpink'
    }
  }
})
```

