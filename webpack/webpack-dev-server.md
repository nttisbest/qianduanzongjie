# webpack-dev-server

```
npm install --save-dev webpack-dev-server
```

**webpack.config.js**

```js
// 导入path模块
const path = require('path');

// 暴露出去
module.exports = {
  // 打包按照哪个文件为准--入口
  entry: './src/main.js',
  // 打包到哪里去--出口
  output: {
    filename: 'bundle.js',
    path: path.resolve(__dirname, 'dist')
  },
  // 开发者服务器
  devServer: {
    // 网站根目录 www有点类似
    contentBase: './dist'
  },
  // 配置loader 解析器
  module: {
    // 规则
    rules: [
      // 文件的解析规则
      {
        // 匹配文件后缀名 .css作为文件结尾
        test: /\.css$/,
        // 使用下列的loader进行解析
        use: [
          'style-loader',
          'css-loader'
        ]
      },
      // 解析less文件的规则
      {
        test: /\.less$/,
        use: [{
            loader: "style-loader" // creates style nodes from JS strings
        }, {
            loader: "css-loader" // translates CSS into CommonJS
        }, {
            loader: "less-loader" // compiles Less to CSS
        }]
    }
    ]
  }
};
```

**package.json**

添加一个 script 脚本

```js
 {
    "name": "development",
    "version": "1.0.0",
    "description": "",
    "main": "webpack.config.js",
    "scripts": {
      "test": "echo \"Error: no test specified\" && exit 1",
      "watch": "webpack --watch",
+     "start": "webpack-dev-server --open",
      "build": "webpack"
    },
    "keywords": [],
    "author": "",
    "license": "ISC",
    "devDependencies": {
      "clean-webpack-plugin": "^0.1.16",
      "css-loader": "^0.28.4",
      "csv-loader": "^2.1.1",
      "file-loader": "^0.11.2",
      "html-webpack-plugin": "^2.29.0",
      "style-loader": "^0.18.2",
      "webpack": "^3.0.0",
      "xml-loader": "^1.2.1"
    }
  }
```

命令行中运行 `npm start`