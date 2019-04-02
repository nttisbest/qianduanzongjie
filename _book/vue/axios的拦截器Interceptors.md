# axios的拦截器(Interceptors)

<https://github.com/axios/axios>

**放在main.js里作为全局**

```javascript
// 拦截器
// 请求拦截器
// 请求之前统一设置一些内容  比如token
// Add a request interceptor
axios.interceptors.request.use(
  // config是请求体的一些配置
  function(config) {
    // Do something before request is sent
    config.headers.Authorization = window.sessionStorage.getItem("token"
    // 返回请求体
    return config;
  },
  function(error) {
    // Do something with request error
    return Promise.reject(error);
  }
);
//响应拦截器
// 响应拦截  统一做响应处理
// Add a response interceptor
axios.interceptors.response.use(
  function(response) {
    // Do something with response data
    console.log('响应拦截');
    console.log(response)
    //当响应体出现200  201  204的时候弹出饿了吗ui框  提示正确
    if([200,201,204].indexOf(response.data.meta.status) != -1){
      Vue.prototype.$message.success(response.data.meta.msg)
    }else{
      // 其他  为错误
      Vue.prototype.$message.warning(response.data.meta.meg)
    }
    // 返回响应体
    return response;
  },
  function(error) {
    // Do something with response error
    return Promise.reject(error);
  }
);
```

