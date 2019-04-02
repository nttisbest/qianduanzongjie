# v-on

```html
<!-- 希望用Vue的方式管理的内容 必须放在 el选择器命中的 元素内部 -->
<div id="app" class="app">
  <h2>{{ message }}</h2>
  <!-- 直接写表达式 -->
  <input type="button" value="点我呀！" v-on:click="message='可以晒被子'" /
  <!-- 绑定方法 -->
  <input type="button" value="点我呀！" v-on:click="changeMessage" />
  <!--简写 用的最多-->
  <input type="button" value="点我呀！" @click="changeMessagePro" />
  <!-- 键盘事件 修饰符 -->
  <!-- <input type="text" @keydown.enter="down" /> -->
  <input type="text" @keyup.enter="down" />
  <input type="button" @dblclick='click("西兰花")' />
</div>
```

```javascript
// new时候传入的对象 是实参
// 内部会被直接设置到这个Vue对象（Vue实例身上） 直接通过this.即可获取
var app = new Vue({
  // 选择器
  el: '#app',
  // 数据
  data: {
    message: '今天天气棒棒哒！！！！'
  },
  // 方法
  methods: {
    changeMessage() {
      // this就是当前实例化的Vue对象(Vue实例)
      console.log(this)
      this.message = '要多晒晒太阳，补钙'
    },
    changeMessagePro() {
      this.message = '晒太多了太阳，会跟某林一样'
    },
    down(e) {
      console.log('按下')
      // if(e.keycode=)
      console.log(e);
    },
    click(food){
      console.log('双击啦');
      console.log(food);
    }
  }
})
console.log(app)
```

