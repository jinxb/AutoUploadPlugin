# Webpack自动上传插件

这是 webpack 插件，用于在 webpack 构建后将静态资源上传到服务器

## 配置

```
// webpack.config.js
plugins: [
  new AutoUploadPlugin({
    host: 'localhost',
    user: 'xxxxx',
    password: 'xxxxxx',
    remoteDir: '/usr/share/nginx/share/xxxx',
    localDir: '/.../dist',
  })
]
```

## 用法

```
let AutoUploadWebpackPlugin = require("AutoUploadWebpackPlugin");
new AutoUploadWebpackPlugin({
  // follow is required
  host:"127.0.0.1",
  user:"root",
  password:"******",
  localDir:"/admin/local/localDir",
  remoteDir:"/usr/root/remoteDir",
  include:[] //  String or Array, dir or files include, default *
  exclude:[],//  String or Array,dir or files include, default none
});
```

## 财产

- `localDir`, 本地资源目录，绝对路径
- `remoteDir`,上传服务器目录,绝对路径
- `include`, 默认 [.*], Array, RegExp 有效,
- `exclude`, 默认 null, Array, RegExp 有效,