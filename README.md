# del-webpack-plugin
remove/clean old files after webpack build

![](https://i.imgur.com/t65OjUv.png)

## feature
- [x] only delete after webpack compile
- [x] skip plugin if compile error
- [x] multiple entry / path support
- [x] exclude files support
- [x] verbose / mute info support
- [x] colorful log with chalk
- [x] example with webpack
- [x] support cross platform

## install
```
// use npm
npm install -D del-webpack-plugin

// use yarn
yarn add -D del-webpack-plugin
```

## usage (in your webpack config)
```
const DelWebpackPlugin = require('clean-webpack-plugin')

{
  plugins: [
    new DelWebpackPlugin({
      info: true,
      exclude: ['test.js']
    })
  ]
}
```

## options

### options.info
console.log added files and deleted files
- type: Boolean
- default: true

### options.exclude
a file list you dont wanna delete
- type: [String]
- default: []
- example: ['test.js', 'test/*.js']

