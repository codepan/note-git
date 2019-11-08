git学习笔记
```js
// bundler.config.js
module.exports = {
  entry: './src',
  output: './git',
  deploy: {
    rootPath: 'xxx',
    connectOptions: {
      host: 'xxx',
      user: 'xxx',
      password: 'xxx'
    }
  }
}
```