<h1 align="center">Welcome to tree-shaking 👋</h1>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-1.0.0-blue.svg?cacheSeconds=2592000" />
  <a href="https://shudong.wang/treeshking.html">
    <img alt="Documentation" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg" target="_blank" />
  </a>
  <a href="https://twitter.com/wsd312">
    <img alt="Twitter: wsd312" src="https://img.shields.io/twitter/follow/wsd312.svg?style=social" target="_blank" />
  </a>
</p>

> webpack-cg tree shaking

### 🏠 [Homepage](https://shudong.wang)

## Install

```sh
yarn
```

## Usage

```sh
npm run start
```

## Author

👤 **starkwang**

* Twitter: [@wsd312](https://twitter.com/wsd312)
* Github: [@wsdo](https://github.com/wsdo)

## Show your support

Give a ⭐️ if this project helped you!


#### 概念

你可以将应用程序想象成一棵树。绿色表示实际用到的 source code(源码) 和 library(库)，是树上活的树叶。灰色表示未引用代码，是秋天树上枯萎的树叶。为了除去死去的树叶，你必须摇动这棵树，使它们落下。

#### 注意点

- 使用 ES2015 模块语法（即 `import` 和 `export`）。
- 确保没有 compiler 将 ES2015 模块语法转换为 CommonJS 模块（这也是流行的 Babel preset 中 @babel/preset-env 的默认行为 - 更多详细信息请查看 [文档](https://babel.docschina.org/docs/en/babel-preset-env#modules)）。
- 在项目 `package.json` 文件中，添加一个 "sideEffects" 属性。
- 通过将 `mode` 选项设置为 [`production`](/concepts/mode/#mode-production)，启用 minification(代码压缩) 和 tree shaking。

#### sideEffects 属性
sideEffects 默认false
如果所有代码都不包含 side effect，我们就可以简单地将该属性标记为 false，来告知 webpack，它可以安全地删除未用到的 export
#### 在开发环境中怎么让tree shaking起作用

#### 怎么避免不需要 tree shaking 优化的文件

