# webpack-demo
webpack模板，打包html、css、js。打包静态页面，多页面开发。

魔改于：[https://github.com/reng99/webpack](https://github.com/reng99/webpack)

## 使用方法

```

# 下载代码
$ https://github.com/WishMelz/webpack-demo.git

# 进入根目录
$ cd webpack-demo

# 安装依赖
$ npm install 

# 开发模式 (执行完npm run dev 后，如果浏览器没有弹出新窗口，请手动输入localhost:9000访问)
$ npm run dev

# 检查语法(此步骤可省略，因为在开发的过程中已经检查)
$ npm run lint

# 生产模式
$ npm run build
[注意，在生产模式中，使用到的第三方的资源需要额外在vendor文件夹中按需引用,建议引用相关的CDN(Content Delivery Network 【内容分发网络】)来进行前端优化]
[如果在生产环境中，相关的.js文件只是引入了.less的文件，那么在生产环境中就要去除生产的相关的.js文件，保留相关的.css文件就可以了。比如：about.js文件引入了about.less的代码，但是about.js文件中没有任何的javascript代码，在生产环境中保留相关的about.css(build后的文件名称有所不同)文件，删除多余的about.js(build后的文件名称有所不同)]
```

## 页面创建

```
build/webpack.base.config.js :14
每个页面的入口文件

build/webpack.base.config.js :98
new HtmlWebpackPlugin 就是一个页面

```

## 语法校验

```
build/webpack.base.config.js :30
不需要可注释掉
```

