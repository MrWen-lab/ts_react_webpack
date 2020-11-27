## TS + React + Webpack 从零开始尝试搭建项目

### package.json 文件

<!-- {
  "name": "wxf",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "webpack-dev-server --hot --inline",
    "dev": "webpack-dev-server --devtool eval-source-map --progress --colors --hot --inline --content-base",
    "build": "webpack --progress --colors"
  },
    "author": "",
    "license": "ISC",
    "devDependencies": {
    "echarts": "^3.7.2",
    "open-browser-webpack-plugin": "0.0.5",
    "webpack": "^3.8.1",
    "webpack-dev-server": "^2.9.3"
  },
  "dependencies": {
    "babel-loader": "^7.1.2",
    "react-hot-loader": "^3.0.0"
  }
} -->

### webpack.config.js 文件

<!-- var path = require('path');
var webpack = require('webpack');
var OpenBrowserPlugin = require('open-browser-webpack-plugin');
var WebpackDevServer = require('webpack-dev-server');

module.exports = {
  entry: './index.js',
  output: {
    path: path.resolve(__dirname, './dist'),
    publicPath: '/dist/',
    filename: 'bundle.js'
  },
  //设置开发者工具的端口号,不设置则默认为8080端口
  /*devServer: {
    inline: false,
    port: 8181
  },*/
  plugins: [
    // 开启全局的模块热替换(HMR)
    new webpack.HotModuleReplacementPlugin(),
    new OpenBrowserPlugin(
      {
        url: 'http://localhost:8080/echart_demo.html'
      }
    )
  ],
  module: {
    loaders: [
      {
        test: /\.css$/,
        loader: "style!css"
      }
    ]
  }
} -->
