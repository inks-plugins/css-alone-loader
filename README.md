# css-alone-loader

css-alone-loader是一个[webpack loaders](https://www.webpackjs.com/configuration/module/#rule-loaders)，用于``art-html-loader``文件中引入css或less的文件的剥离输出与路径修改。其可以将直接引入的样式文件单独打包为一个独立的css文件，而不是编译为js或直接注入至html style标签中。

## Install
```
$ npm install css-alone-loader
```

## Usage
- webpack.config.js
```
module.exports = {
  module: {
    rules: [{
    test: /\.less$/,
    exclude: /node_modules/,
    use: ['css-alone-loader','less-loader']
  }]
}
```

## Options
> ``options``的代码源自[file-loader](https://github.com/webpack-contrib/file-loader#options)，可直接参考``options``的配置

```
use: [{
  loader: 'css-alone-loader',
  options: {
    // ...
  }
}]
```
- name
- regExp
- outputPath
- publicPath
- postTransformPublicPath
- emitFile
- esModule
- context
