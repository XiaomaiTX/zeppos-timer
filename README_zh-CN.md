<a name="readme-top"></a>


[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]

<br />
<div align="center">

  <h3 align="center">zeppos_timer.js</h3>

  <p align="center">
    一个适用于ZeppOS的准确的计时器
    <br />
        <a href="https://github.com/XiaomaiTX/zeppos-fx/blob/master/README.md"><strong>English Document »</strong></a>
    <br />
    <p>我在写文档的时候优先用的英语哦~建议优先读完英文版 当然，中文版更方便大部分大陆开发者使用习惯</p>
    <a href="https://github.com/XiaomaiTX/zeppos-timer/releases">下载稳定版</a>
    ·
    <a href="https://github.com/XiaomaiTX/zeppos-timer/issues">反馈Bug</a>
    ·
    <a href="https://github.com/XiaomaiTX/zeppos-timer/issues">提交新建议</a>
  </p>
</div>

<details>
  <summary>目录</summary>
  <ol>
    <li>
      <a href="#about-the-project">关于 zeppos_timer.js</a>
    </li>
    <li>
      <a href="#getting-started">快速开始</a>
      <ul>
        <li><a href="#prerequisites">前期准备</a></li>
        <li><a href="#installation">安装</a></li>
      </ul>
    </li>
    <li><a href="#usage">如何使用</a></li>
    <li><a href="#roadmap">TODO</a></li>
    <li><a href="#contributing">参与项目</a></li>
    <li><a href="#license">开源协议</a></li>
    <li><a href="#contact">联系我们</a></li>
  </ol>
</details>


## 关于 zeppos_timer.js

一个适用于ZeppOS的准确的计时器
ZeppTimer 是一个小巧精致的 JavaScript 类，能为 ZeppOS 系统提供一个准确的计时器


为什么选择zeppos_timer.js呢:

- 在ZeppOS所有版本中，由于系统底层造成的问题，ZeppOS的计时器与实际时间具有相当大的误差（30s后大概有0.5s的误差），为了更精确的计时，我用了一个比较简单但有效的思路来减小计时误差，并封装成ZeppTimer。

- 并且，在ZeppOS 2.x中，官方使用setTimeOut和cleanTimeOut来替代计时器组件，这使得使用到计时器的ZeppOS 1.0应用在迁移到ZeppOS 2.x及以上时需要进行逻辑调整，如果使用ZeppTimer库将会节省开发者迁移的成本

快速开始？看看下面的 <a href="#usage">Usage</a> 吧

<p align="right">(<a href="#readme-top">返回顶部</a>)</p>


## 快速开始

以下内容可以让开发者们快速上手

### 前期准备

在接入zeppos_timer.js库之前，请确保你已经对 ZeppOS 小程序开发有了一定了解，当然，你也可以从头开始，从 [ZeppOS 官方文档](https://docs.zepp.com/docs/intro/)入手，相信你一定可以快速掌握的

emmm，你还需要一个代码编辑器（比如微软的VSCode），以及有关JavaScript的知识

### 安装

1. 使用zeppos_timer.js之前，你需要准备一个 ZeppOS 小程序项目，如果还没有创建，你可以参考这部分的文档 [ZeppOS quick start](https://docs.zepp.com/docs/guides/quick-start/).

2. 请前往 [Releases](https://github.com/XiaomaiTX/zeppos-timer/releases) 下载最新稳定版zeppos_timer.js，然后把fx.js放到项目根目录的 `libs/` 目录中

3. 在项目中添加对zeppos_timer.js的引用

```js
import { ZeppTimer } from "../libs/zeppos_timer"; // Replace with the path to your zeppos_timer.js
```

至此，你可以尽情享受zeppos_timer.js带来的精准效果了，什么？不知道怎么用？那就看看Usage吧

<p align="right">(<a href="#readme-top">返回顶部</a>)</p>

## 食用方法

如果有什么问题可以提交issue或联系XiaomaiTX，但是在发问前请确保自己已经经过思考
当然，你可以先看看我博客的文章[《提问的智慧》](https://blog.uuu4.cn/archives/12/)

创建一个新的实例：

```javascript
const timer = new ZeppTimer(() => {
  console.log("Tick!");
}, 1000);
```

`ZeppTimer` 构造函数的第一个参数是一个回调函数，在每个计时周期中都会被调用。第二个参数是计时周期的时间间隔，以毫秒为单位。

要启动计时器，请调用 `start` 方法：

```javascript
timer.start();
```

要停止计时器，请调用 `stop` 方法：

```javascript
timer.stop();
```

<p align="right">(<a href="#readme-top">返回顶部</a>)</p>


## TODO

- [x] 为README编写多语言适配（感觉中英就够了？）
  - [x] English
  - [x] 中文

请查看[Issue](https://github.com/XiaomaiTX/zeppos-timer/issues)以获取提出的功能（和已知问题）的完整列表。

<p align="right">(<a href="#readme-top">返回顶部</a>)</p>


## 参与项目

贡献使开源社区成为了真正的社区。 无论是报告错误、功能请求还是贡献代码，您的帮助都将受到感激。

1. Fork 这个仓库
2. 创建您的功能分支 (`git checkout -b feature/AmazingFeature`)
3. 提交您的更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 打开一个拉取请求

<p align="right">(<a href="#readme-top">返回顶部</a>)</p>


## 开源许可

本项目使用 MIT 许可证，详情请参阅`LICENSE`

<p align="right">(<a href="#readme-top">返回顶部</a>)</p>


## 联系我们

XiaomaiTX - i@lenrome.cn

项目链接: [https://github.com/XiaomaiTX/zeppos-timer](https://github.com/XiaomaiTX/zeppos-timer)

<p align="right">(<a href="#readme-top">返回顶部</a>)</p>


[contributors-shield]: https://img.shields.io/github/contributors/XiaomaiTX/zeppos-timer.svg?style=for-the-badge
[contributors-url]: https://github.com/XiaomaiTX/zeppos-timer/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/XiaomaiTX/zeppos-timer.svg?style=for-the-badge
[forks-url]: https://github.com/XiaomaiTX/zeppos-timer/network/members
[stars-shield]: https://img.shields.io/github/stars/XiaomaiTX/zeppos-timer.svg?style=for-the-badge
[stars-url]: https://github.com/XiaomaiTX/zeppos-timer/stargazers
[issues-shield]: https://img.shields.io/github/issues/XiaomaiTX/zeppos-timer.svg?style=for-the-badge
[issues-url]: https://github.com/XiaomaiTX/zeppos-timer/issues
[license-shield]: https://img.shields.io/github/license/XiaomaiTX/zeppos-timer.svg?style=for-the-badge
[license-url]: https://github.com/XiaomaiTX/zeppos-timer/blob/master/LICENSE.txt
