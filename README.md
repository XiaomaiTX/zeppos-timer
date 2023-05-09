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
    An accurate timer for ZeppOS. 
    <br />
    <a href="https://github.com/XiaomaiTX/zeppos-timer/blob/master/README_zh-CN.md"><strong>中文文档（在写了别催了） »</strong></a>
    <br />
    <br />
    <a href="https://github.com/XiaomaiTX/zeppos-timer/releases">Download</a>
    ·
    <a href="https://github.com/XiaomaiTX/zeppos-timer/issues">Report Bug</a>
    ·
    <a href="https://github.com/XiaomaiTX/zeppos-timer/issues">Request Feature</a>
  </p>
</div>

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The zeppos_timer.js</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>


## About The zeppos_timer.js

An accurate timer for ZeppOS. 
ZeppTimer is a small and refined JavaScript class that provides an accurate timer for the ZeppOS system.


Here's why:

- In all versions of ZeppOS, there is a significant time discrepancy between the system's timer and the actual time due to underlying issues with the system. To achieve more accurate timing, I implemented a simple but effective approach to reduce timing errors and packaged it into ZeppTimer. 

- Furthermore, in ZeppOS 2.x, the official approach to timer components was replaced with setTimeOut and cleanTimeOut, requiring logic adjustments when migrating ZeppOS 1.0 applications that use timers to ZeppOS 2.x and above. Using the ZeppTimer library can save developers the cost of migration.

Use the <a href="#usage">Usage</a> to easily get started.

<p align="right">(<a href="#readme-top">back to top</a>)</p>


## Getting Started

The content here will help you get familiar with the program quickly.

### Prerequisites

Before using this library, please make sure you already have an understanding of ZeppOS applet development, you can refer to the [ZeppOS official documentation](https://docs.zepp.com/docs/intro/).
Also, you need a `code editor(Like Microsoft VSCode)` and `knowledge of JavaScript`.

### Installation

1. To use this library, you need to create a ZeppOS applet project first.refer to the [ZeppOS quick start](https://docs.zepp.com/docs/guides/quick-start/).

2. Please download the latest `zeppos_timer.js` file in the [Releases](https://github.com/XiaomaiTX/zeppos-timer/releases), and place `zeppos_timer.js` in the `libs/` directory of the root of the applet

3. Add a reference to zeppos_timer.js in the project

```js
import { ZeppTimer } from "../libs/zeppos_timer"; // Replace with the path to your zeppos_timer.js
```

At this point, you're ready to use the `zeppos_timer.js` library

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Usage

Then create a new instance of the class:

```javascript
const timer = new ZeppTimer(() => {
  console.log("Tick!");
}, 1000);
```

The first argument to the `ZeppTimer` constructor is a callback function that will be called on each tick of the timer. The second argument is the time interval between ticks, in milliseconds.

To start the timer, call the `start` method:

```javascript
timer.start();
```

To stop the timer, call the `stop` method:

```javascript
timer.stop();
```

<p align="right">(<a href="#readme-top">back to top</a>)</p>


## Roadmap

- [x] Multi-language Support for README
  - [x] English
  - [x] 中文

See the [open issues](https://github.com/XiaomaiTX/zeppos-timer/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>


## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>


## License

Distributed under the MIT License. See `LICENSE` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>


## Contact

XiaomaiTX - i@lenrome.cn

Project Link: [https://github.com/XiaomaiTX/zeppos-timer](https://github.com/XiaomaiTX/zeppos-timer)

<p align="right">(<a href="#readme-top">back to top</a>)</p>


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
