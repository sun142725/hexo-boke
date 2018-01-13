---
title: node-package
date: 2018-01-12 16:56:37
tags: node
author: 孙继红
---
# Awesome Node.js 中文版

> 一份nodejs的超级大礼包 [包(packages)](#包) and [资源(resources)](#资源)。

被老外的[awesome](https://github.com/sindresorhus/awesome) 清单刺激到，觉得有必要翻译一份，为国产的程序员们做点事情，本清单将保持实时更新同步。PS:进都进来了，就顺便看看其他的吧:
- [awesome-gulp-cn](https://github.com/Pines-Cheng/awesome-gulp-cn)
- [awesome-angularjs-cn](https://github.com/Pines-Cheng/awesome-angularjs-cn)
- [awesome-react-cn](https://github.com/Pines-Cheng/awesome-react-cn)
- [awesome-react-native-cn](https://github.com/Pines-Cheng/awesome-react-native-cn)
- [awesome-npm-cn](https://github.com/Pines-Cheng/awesome-npm-cn)

如果想加入，那就加入吧。

## 目录

- [包(Packages)](#包)
	- [神奇的科学(mad science)](#神奇的科学mad-science)
	- [命令行应用](#命令行应用)
	- [实用的程序](#实用的程序)
	- [HTTP](#http)
	- [调试/数据](#调试--数据)
	- [日志](#日志)
	- [命令行工具](#命令行工具)
	- [构建工具](#构建工具)
	- [硬件](#硬件)
	- [模板](#模板)
	- [Web框架](#web框架)
	- [文档](#文档)
	- [文件系统](#文件系统)
	- [流控制](#流控制)
	- [流](#流)
	- [实时](#实时)
	- [图片](#图片)
	- [文本](#文本)
	- [数字](#数字)
	- [数学](#数学)
	- [日期](#日期)
	- [URL](#url)
	- [数据校验](#数据校验)
	- [解析](#解析)
	- [人性](#人性)
	- [压缩](#压缩)
	- [网络](#网络)
	- [数据库](#数据库)
	- [测试](#测试)
	- [基准化分析](#基准化分析)
	- [缩小](#缩小)
	- [验证](#验证)
	- [Email](#email)
	- [工作队列](#工作队列)
	- [Node.js管理](#nodejs管理)
	- [兼容](#兼容)
	- [自然语言处理](#自然语言处理)
	- [进程管理](#进程管理)
	- [自动化](#自动化)
	- [AST](#ast)
	- [静态站点生成器](#静态站点生成器)
	- [CMS](#CMS)
	- [论坛](#论坛)
	- [博客](#博客)
	- [奇奇怪怪的东东](#奇奇怪怪的东东)
	- [其他](#其他)
- [资源](#资源)
	- [入门](#tutorials)
	- [发现](#discovery)
	- [文章](#articles)
	- [新闻](#新闻)
	- [视频](#视频)
	- [直播](#直播)
	- [书籍](#书籍)
	- [博客](#博客)
	- [课程](#课程)
	- [夹带](#夹带)
	- [工具](#工具)
	- [社区](#社区)
	- [其他](#其他)


## 包
### 神奇的科学

- [webtorrent](https://github.com/feross/webtorrent) - WebTorrent 是一个可工作在node.js和浏览器的流BT客户端。它完全采用JavaScript开发，在浏览器中WebTorrent使用WebRTC (data channels) 来进行p2p传输。它可以不使用浏览器插件，扩展或安装。只有JavaScript。
- [GitTorrent](https://github.com/cjb/GitTorrent) - Git仓库的P2P网络，通过比特流分享。
- [peerflix](https://github.com/mafintosh/peerflix) - 流客户端.
- [dat](http://dat-data.com) - Dat 是开源的项目，进行实时复制，数据集版本控制，提供每个文件格式和数据存储后端的流。.
- [ipfs](https://github.com/ipfs/js-ipfs) - IPFS 是分布式文件系统，寻求连接所有计算机设备的相同文件系统。在某些方面，这很类似于原始的 Web 目标，但是 IPFS 最终会更像单个比特流群交换的 git 对象。
- [stackgl](http://stack.gl) - WebGL的开源软件生态系统，基于browserify和npm构建。
- [peerwiki](https://github.com/mafintosh/peerwiki) - 比特流上的所有wiki
- [peercast](https://github.com/mafintosh/peercast) - 推送视频流到Chromecast.
- [BitcoinJS](http://bitcoinjs.org) - BitcoinJS 是一个纯 JavaScript 库，支持 Node.js和浏览器，用于操作各种比特币钱包。代码清晰，可读性强。
- [Bitcore](https://bitcore.io/) - Bitcore 是一个完整原生的比特币网络的 JavaScript 开发库，提供比特币应用开发的核心功能。
- [PDFKit](http://pdfkit.org) - PDF生成器库.
- [turf](https://github.com/Turfjs/turf) - Turf 是一个 JavaScript 的模块化的 GIS 引擎，它执行地理空间与GeoJSON数据处理任务,可以在服务器或在浏览器上运行。
- [webcat](https://github.com/mafintosh/webcat) - 使用您的GitHub的私有/公共密钥认证的p2p管道，可以通过WebRTC跨web使用。
- [js-git](https://github.com/creationix/js-git) - Git的JavaScript实现。
- [NodeOS](http://node-os.com) - 第一个通过npm实现的操作系统，使用Node.js编写。
- [limdu](https://github.com/erelsgl/limdu) - 一个机器学习框架。
- [Cytoscape.js](http://js.cytoscape.org) - Cytoscape.js 是个开源 JavaScript 图形库，用户可以用 Cytoscape.js 来分析和制作可视化图形。它兼容 CommonJS/Node.js, jQuery 1.4+ 和纯 JavaScript。


### 命令行应用
- [pageres](https://github.com/sindresorhus/pageres) - 网站截图工具。
- [trash](https://github.com/sindresorhus/trash) - trash 命令替代linux rm命令实现windows回收站的功能
- [npm-name](https://github.com/sindresorhus/npm-name) - 检查报名在npm上是否可用。
- [XO](https://github.com/sindresorhus/xo) - XO 是 JavaScript 幸福样式，强制执行严格代码风格，pull request 的时候不会再讨论代码风格。没有 .eslintrc，.jshintrc，.jscsrc 管理。
- [speed-test](https://github.com/sindresorhus/speed-test) - 测试网络连接速度和ping。
- [np](https://github.com/sindresorhus/np) - 比`npm publish`更好用。
- [yo](https://github.com/yeoman/yo) - 运行Yeoman生成器。
- [Babel](https://babeljs.io/docs/usage/cli/) - 从现在开始使用下一代JavaScript。
- [ESLint](http://eslint.org) - ESLint 是一个开源的插件化得JavaScript验证工具，相比JSLint，ESLint具有可配置性。
- [JSCS](https://github.com/jscs-dev/node-jscs) - JavaScript代码风格检查。
- [Standard](https://github.com/feross/standard) - JavaScript标准风格，使用一种风格来限制所有。
- [cpy](https://github.com/sindresorhus/cpy) - 复制文件。
- [fkill](https://github.com/sindresorhus/fkill-cli) - 跨平台的，更好的杀死进程的方式。
- [vantage](https://github.com/dthree/vantage) - Vangtage.js 是一个全新的 Node 交互式 CLI。Vangtage 灵感来源于 commander.js，通过 inquirer.js 的交互式 prompt 把在线 Node 应用转换到 CLI。可以本地或者远程访问，Vantage 可以让你构建自己的 API，导入社区扩展等等。
- [vtop](https://github.com/MrRio/vtop) - 更好更漂亮的图表。
- [tmpin](https://github.com/sindresorhus/tmpin) - 给所有能接受文件输入的CLI应用添加标准输入支持。
- [empty-trash](https://github.com/sindresorhus/empty-trash) - 清空回收站。
- [is-up](https://github.com/sindresorhus/is-up) - 检查Web站点是否在线。
- [is-online](https://github.com/sindresorhus/is-online) - 检查是否联网。
- [public-ip](https://github.com/sindresorhus/public-ip) - 获取你的公网IP。
- [dark-mode](https://github.com/sindresorhus/dark-mode) - 触发OS X的夜间模式。
- [ttystudio](https://github.com/chjj/ttystudio) - 记录你的终端并且编译成GIF或者APNG动态图，无需任何依赖，bash脚本或者gif相关的东西。
- [David](https://github.com/alanshaw/david) - 当你的npm依赖过时的时候通知你。
- [http-server](https://github.com/indexzero/http-server) - 简单，零配置的命令行HTTP服务器。
- [Live Server](https://github.com/tapio/live-server) - 一个自带热加载功能的http服务器。
- [bcat](https://github.com/kessler/node-bcat) - 将命令行输出到web浏览器。
- [normit](https://github.com/pawurb/normit) - 在终端运行的包含语音合成Google翻译。
- [slap](https://github.com/slap-editor/slap) - 类似于Sublime的基于命令行的文本编辑器。
- [jsinspect](https://github.com/danielstjules/jsinspect) - 发现复制粘贴的或者结构相似代码。
- [esformatter](https://github.com/millermedeiros/esformatter) - JavaScript代码格式化。
- [pjs](https://github.com/danielstjules/pjs) - 能作为管道使用的JavaScript，从终端快速过滤，映射等。
- [license-checker](https://github.com/davglass/license-checker) - 检查应用的依赖的证书。
- [browser-run](https://github.com/juliangruber/browser-run) - 轻松在浏览器环境中运行代码。
- [modhelp](https://github.com/runvnc/modhelp) -在终端动态高亮README模块。
- [wifi-password](https://github.com/kevva/wifi-password) - 在终端通过命令行获取当前的wifi密码。.
- [wallpaper](https://github.com/sindresorhus/wallpaper) -命令行改变桌面的背景。
- [brightness](https://github.com/kevva/brightness-cli) - 命令行改变屏幕的亮度。
- [torrent](https://github.com/maxogden/torrent) - 下载种子。
- [tfa](https://github.com/jasnell/tfa) - Two-factor验证客户端。
- [rtail](https://github.com/kilianc/rtail) - 使用Unix管道，在终端实时输出浏览器多个流。
- [kill-tabs](https://github.com/sindresorhus/kill-tabs) - 通过关闭Chrome 窗口来提升性能，减少电池消耗，节约内存。
- [alex](https://github.com/wooorm/alex) - Catch insensitive, inconsiderate writing.
- [pen](https://github.com/noraesae/pen) - 浏览器中的你最喜欢的编辑器Markdown实时预览。
- [subdownloader](https://github.com/beatfreaker/subdownloader) - 电影和电视剧的字幕下载。
- [iponmap](https://github.com/nogizhopaboroda/iponmap) - IP地址查找。
- [Jsome](https://github.com/Javascipt/Jsome) - 根据配置的颜色和排版格式化打印JSON。
- [itunes-remote](https://github.com/mischah/itunes-remote) -iTunes交互控制.
- [dev-time](https://github.com/samverschueren/dev-time-cli) - 获取一个用户当前的本地时间.
- [text-meme](https://github.com/beatfreaker/text-meme-cli) - 生成一个text meme.
- [mobicon](https://github.com/samverschueren/mobicon-cli) - 生成手机应用的icon.
- [mobisplash](https://github.com/samverschueren/mobisplash-cli) - 生成手机应用的 splash 屏幕.
- [diff2html-cli](https://github.com/rtfpessoa/diff2html-cli) - 好看的 git diff 的html生成器.
- [Cash](https://github.com/dthree/cash) - 纯js实现的跨平台的Unix shell命令.
- [vaca](https://github.com/sindresorhus/vaca) - 获取一个随机的ASCII 🐮.
- [gh-home](https://github.com/sindresorhus/gh-home) - 在当前的directory打开一个GitHub仓库的页面.
- [npm-home](https://github.com/sindresorhus/npm-home) - 打开一个npm包的home页面.


### 函数式编程
- [lodash](https://lodash.com/) - 一个工具库，相当于一个更好更快的 Underscore.js.
- [immutable](https://github.com/facebook/immutable-js) - 数据持久化.
- [mori](http://swannodette.github.io/mori/) - A library for using使用 ClojureScript的持久化数据结构，且支持 vanilla JavaScript API的库.
- [Ramda](http://ramdajs.com) - 专注于灵活的函数式编程的工具库，能力来自于自动柯里化和函数参数优先于数据，提供了mutating data.
- [Folktale](http://folktalejs.org/) - 一整套通用的JavaScript函数式编程方案，帮助你构建优雅的，组合式的健壮且高度复用的应用。
- [underscore-contrib](http://documentcloud.github.io/underscore-contrib/) - The brass buckles on Underscore's utility belt.
- [Mout](http://moutjs.com) - 和其他工具库最大的不同是，你可以选择只下载你需要的模块或函数，没有额外的负担。
- [RxJS](http://reactivex.io) - 函数式响应式编程库，专注于大量不同数据的转换，构建和查询。
- [Lazy.js](https://github.com/dtao/lazy.js) - Lazy.js是类似Underscore或Lo-Dash的JavaScript工具库，但是它有一个非常独特的特性：惰性求值。很多情况下，惰性求值都将带来巨大的性能提升，特别是当处理巨大的数组和连锁使用多个方法的时候。


### HTTP

- [got](https://github.com/sindresorhus/got) - A nicer interface to the built-in `http` module.
- [gh-got](https://github.com/sindresorhus/gh-got) - Convenience wrapper for `got` to interact with the GitHub API.
- [request](https://github.com/request/request) - Simplified HTTP request client.
- [Nock](https://github.com/pgte/nock) - A HTTP mocking and expectations library.
- [hyperquest](https://github.com/substack/hyperquest) - Streaming HTTP requests.
- [axios](https://github.com/mzabriskie/axios) - Promise based HTTP client (works in the browser too).
- [spdy](https://github.com/indutny/node-spdy) - Creates SPDY servers with the same API as the built-in `https` module.
- [wreck](https://github.com/hapijs/wreck) - HTTP Client Utilities.
- [download](https://github.com/kevva/download) - Download and extract files effortlessly.
- [http-proxy](https://github.com/nodejitsu/node-http-proxy) - A full-featured HTTP proxy.
- [rocky](https://github.com/h2non/rocky) - Featured, middleware-oriented HTTP proxy with traffic replay and intercept.
- [superagent](https://github.com/visionmedia/superagent) - A small progressive HTTP request library.


### Debugging / Profiling

- [ironNode](https://github.com/s-a/iron-node) - Node.js debugger supporting ES2015 out of the box.
- [node-inspector](https://github.com/node-inspector/node-inspector) - Debugger based on Blink Developer Tools.
- [Theseus](https://github.com/adobe-research/theseus) - A new type of JavaScript debugger featuring real-time code coverage, retroactive inspection and asynchronous call tree.
- [longjohn](https://github.com/mattinsler/longjohn) - Long stack traces with configurable call trace length.
- [debug](https://github.com/visionmedia/debug) - Tiny debugging utility.
- [jstrace](https://github.com/jstrace/jstrace) - Dynamic tracing for JavaScript, similar to dtrace, ktap etc.
- [why-is-node-running](https://github.com/mafintosh/why-is-node-running) - Node.js is running but you don't know why?
- [njsTrace](https://github.com/valyouw/njstrace) - Instrument and trace your code, see all function calls, arguments, return values, as well as the time spent in each function.
- [vstream](https://github.com/joyent/node-vstream) - Instrumentable streams mix-ins to inspect a pipeline of streams.
- [stackman](https://github.com/watson/stackman) - Enhance an error stacktrace with code excerpts and other goodies.
- [TraceGL](https://github.com/traceglMPL/tracegl) - Transforms your JavaScript, injecting monitoring code that produces a log of everything that happens.
- [locus](https://github.com/alidavut/locus) - Starts a REPL at runtime that has access to all variables.
- [bugger](https://github.com/buggerjs/bugger) - Provides Chrome Devtools bindings to debug programs in Chrome.
- [0x](https://github.com/davidmarkclements/0x) - Flamegraph profiling.


### Logging

- [winston](https://github.com/winstonjs/winston) - A multi-transport async logging library.
- [Bunyan](https://github.com/trentm/node-bunyan) - A simple and fast JSON logging library.
- [intel](http://seanmonstar.github.io/intel/) - A comprehensive logging library (handlers, filters, formatters, console injection).
- [console-log-level](https://github.com/watson/console-log-level) - The most simple logger imaginable with support for log levels and custom prefixes.


### Command-line utilities

- [chalk](https://github.com/chalk/chalk) - Terminal string styling done right.
- [meow](https://github.com/sindresorhus/meow) - CLI app helper.
- [minimist](https://github.com/substack/minimist) - Parse command-line flags.
- [get-stdin](https://github.com/sindresorhus/get-stdin) - Easier stdin.
- [user-home](https://github.com/sindresorhus/user-home) - Get the path to the user home directory.
- [log-update](https://github.com/sindresorhus/log-update) - Log by overwriting the previous output in the terminal. Useful for rendering progress bars, animations, etc.
- [Inquirer.js](https://github.com/SBoudrias/Inquirer.js) - Interactive command-line prompt.
- [update-notifier](https://github.com/yeoman/update-notifier) - Update notifications for your CLI app.
- [ansi-escapes](https://github.com/sindresorhus/ansi-escapes) - ANSI escape codes for manipulating the terminal.
- [sudo-block](https://github.com/sindresorhus/sudo-block) - Block users from running your app with root permissions.
- [configstore](https://github.com/yeoman/configstore) - Easily load and persist config without having to think about where and how.
- [insight](https://github.com/yeoman/insight) - Helps you understand how your tool is being used by anonymously reporting usage metrics to Google Analytics.
- [log-symbols](https://github.com/sindresorhus/log-symbols) - Colored symbols for various log levels.
- [figures](https://github.com/sindresorhus/figures) - Unicode symbols with Windows CMD fallbacks.
- [boxen](https://github.com/sindresorhus/boxen) - Create boxes in the terminal.
- [string-width](https://github.com/sindresorhus/string-width) - Get the visual width of a string - the number of columns required to display it.
- [first-run](https://github.com/sindresorhus/first-run) - Check if it's the first time the process is run.
- [sparkly](https://github.com/sindresorhus/sparkly) - Generate sparklines ▁▂▃▅▂▇
- [vorpal](https://github.com/dthree/vorpal) - A framework for interactive CLI apps.
- [blessed](https://github.com/chjj/blessed) - A curses-like library.
- [yn](https://github.com/sindresorhus/yn) - Parse yes/no like values.
- [cli-table](https://github.com/Automattic/cli-table) - Pretty unicode tables.
- [drawille](https://github.com/madbence/node-drawille) - Draw on the terminal with unicode braille characters.
- [googleauth](https://github.com/maxogden/googleauth) - Create and load persistent Google authentication tokens for command-line apps.
- [ascii-charts](https://github.com/jstrace/chart) - ASCII bar chart in the terminal.
- [progress](https://github.com/tj/node-progress) - Flexible ascii progress bar.
- [cli-cursor](https://github.com/sindresorhus/cli-cursor) - Toggle the CLI cursor.
- [columnify](https://github.com/timoxley/columnify) - Create text-based columns suitable for console output. Supports cell wrapping.
- [cli-columns](https://github.com/shannonmoeller/cli-columns) - Columnated unicode and ansi-safe text lists.
- [cfonts](https://github.com/dominikwilkowski/cfonts) - Sexy ASCII fonts for the console.
- [multispinner](https://github.com/codekirei/node-multispinner) - Multiple, simultaneous, individually controllable CLI spinners.
- [omelette](https://github.com/f/omelette) - Shell autocompletion helper.
- [cross-env](https://github.com/kentcdodds/cross-env) - Set environment variables cross-platform.
- [shelljs](https://github.com/shelljs/shelljs) - Portable Unix shell commands.
- [loud-rejection](https://github.com/sindresorhus/loud-rejection) - Make unhandled promise rejections fail loudly instead of the default silent fail.
- [ora](https://github.com/sindresorhus/ora) - Elegant terminal spinner.
- [term-img](https://github.com/sindresorhus/term-img) - Display images in your terminal.
- [yargs](https://github.com/yargs/yargs) - Command-line parser that automatically generates an elegant user-interface.


### Build tools

- [gulp](http://gulpjs.com) - Streaming and fast build system that favors code over config.
- [Broccoli](https://github.com/broccolijs/broccoli) - A fast, reliable asset pipeline, supporting constant-time rebuilds and compact build definitions.
- [browserify](https://github.com/substack/node-browserify) - Browser-side require() the Node.js way.
- [webpack](https://github.com/webpack/webpack) - Packs modules and assets for the browser.
- [Brunch](https://github.com/brunch/brunch) - Front-end web app build tool with simple declarative config, fast incremental compilation, and an opinionated workflow.
- [strong-build](https://github.com/strongloop/strong-build) - Build a node app package and prepare to deploy it as a package to production or use git to commit to a deploy branch.
- [grunt](http://gruntjs.com) - Task runner that can perform repetitive tasks like minification, compilation, unit testing, linting, etc.
- [start](https://github.com/start-runner/start) - Simple tasks runner powered by composable functions and promise chaining.
- [ygor](https://github.com/shannonmoeller/ygor) - A promising task runner for when `npm run` isn't enough and everything else is too much.


### Hardware

- [johnny-five](https://github.com/rwaldron/johnny-five) - Firmata based Arduino Framework.
- [serialport](https://github.com/voodootikigod/node-serialport) - Access serial ports for reading and writing.
- [usb](https://github.com/nonolith/node-usb) - USB library.
- [cylon.js](http://cylonjs.com) - Next generation robotics framework with support for 26 different platforms.
- [i2c-bus](https://github.com/fivdi/i2c-bus) - I2C serial bus access.


### Templating

- [marko](https://github.com/marko-js/marko) - A fast and lightweight HTML-based templating engine that compiles templates to CommonJS modules and supports streaming, async rendering and custom tags.
- [nunjucks](https://github.com/mozilla/nunjucks) - A powerful templating engine with inheritance, asynchronous control, and more (jinja2 inspired).
- [handlebars.js](https://github.com/wycats/handlebars.js) - A superset of Mustache templates which adds powerful features like helpers and more advanced blocks.
- [hogan.js](http://twitter.github.io/hogan.js/) - Twitter's small, fast, phase-separated compiler for Mustache templates.
- [EJS](https://github.com/mde/ejs) - Simple unopinionated templating language.
- [Jade](https://github.com/jadejs/jade) - High-performance template engine heavily influenced by Haml.


### Web frameworks

- [Koa](http://koajs.com) - A new web framework designed by the team behind Express, which aims to be a smaller, more expressive, and more robust foundation for web applications and APIs.
- [Express](http://expressjs.com) - A minimal and flexible web application framework, providing a robust set of features for building single and multi-page, and hybrid web applications.
- [Feathers](http://feathersjs.com) - A minimal and flexible microservice framework built in the spirit of Express.
- [Hapi](http://hapijs.com) - A rich framework for building applications and services.
- [LoopBack](http://loopback.io) - Powerful framework for creating REST APIs and easily connecting to backend data sources.
- [Meteor](https://www.meteor.com) - An ultra-simple, database-everywhere, data-on-the-wire, pure-Javascript web framework. *(You might like [awesome-meteor](https://github.com/Urigo/awesome-meteor))*
- [SailsJS](http://sailsjs.org) - An MVC web framework with a modern twist, supporting WebSockets, streams, and a data-driven API.
- [Restify](http://restify.com) - A node framework built specifically to enable you to build correct REST web services.
- [Interfake](https://github.com/basicallydan/interfake) - Rapid prototyping framework for making mock HTTP APIs, with a Node.js, command-line and HTTP interface.
- [Derby](https://github.com/derbyjs/derby) - MVC framework, making it easy to write realtime, collaborative applications that run in both Node.js and browsers.
- [Restberry](http://restberry.com) - Framework for setting up RESTful JSON APIs, applied to your database models without needing to write any code.
- [Catberry](http://catberry.org) - Framework with Flux architecture, isomorphic web-components, and progressive rendering.
- [ThinkJS](https://thinkjs.org) - Framework with ES2015+ support, WebSockets, REST API.


### Documentation

- [Docco](http://jashkenas.github.io/docco/) - A quick-and-dirty documentation generator which produces an HTML document that displays your comments intermingled with your code.
- [JSDoc](http://usejsdoc.org) - API documentation generator similar to JavaDoc or PHPDoc.
- [dox](https://github.com/tj/dox) - JavaScript documentation generator using Markdown and JSDoc.
- [jsdox](https://github.com/sutoiku/jsdox) - JSDoc3 to Markdown documentation generator.
- [apiDoc](https://github.com/apidoc/apidoc) - Inline documentation for RESTful web APIs.
- [documentation.js](http://documentation.js.org) - API documentation generator with support for ES2015+ and flow annotation.
- [YUIDoc](http://yui.github.com/yuidoc/) - Generates API documentation from comments in source.


### Filesystem

- [del](https://github.com/sindresorhus/del) - Delete files/folders using globs.
- [globby](https://github.com/sindresorhus/globby) - Glob files with support for multiple patterns.
- [cpy](https://github.com/sindresorhus/cpy) - Copy files.
- [rimraf](https://github.com/isaacs/rimraf) - Recursively delete files like `rm -rf`.
- [mkdirp](https://github.com/substack/node-mkdirp) - Recursively create directories like `mkdir -p`.
- [graceful-fs](https://github.com/isaacs/node-graceful-fs) - Drop-in replacement for the `fs` module with various improvements.
- [chokidar](https://github.com/paulmillr/chokidar) - Filesystem watcher which stabilizes events from `fs.watch` and `fs.watchFile` as well as using native `fsevents` on OS X.
- [find-up](https://github.com/sindresorhus/find-up) - Find a file by walking up parent directories.
- [load-json-file](https://github.com/sindresorhus/load-json-file) - Read and parse a JSON file.
- [write-json-file](https://github.com/sindresorhus/write-json-file) - Stringify and write JSON to a file atomically.
- [fs-write-stream-atomic](https://github.com/npm/fs-write-stream-atomic) - Like `fs.createWriteStream()`, but atomic.
- [filenamify](https://github.com/sindresorhus/filenamify) - Convert a string to a valid filename.
- [lnfs](https://github.com/kevva/lnfs) - Force create symlinks like `ln -fs`.
- [istextorbinary](https://github.com/bevry/istextorbinary) - Check if a file is text or binary.
- [fs-jetpack](https://github.com/szwacz/fs-jetpack) - Completely redesigned file system API for convenience in everyday use.
- [fs-extra](https://github.com/jprichardson/node-fs-extra) - Extra methods for the `fs` module.
- [pkg-dir](https://github.com/sindresorhus/pkg-dir) - Find the root directory of an npm package.


### Control flow

- Promises
	- [Bluebird](https://github.com/petkaantonov/bluebird) - A fully featured promise library with focus on innovative features and performance.
	- [pinkie-promise](https://github.com/floatdrop/pinkie-promise) - Promise ponyfill.
	- [pify](https://github.com/sindresorhus/pify) - Promisify a callback-style function.
	- [rfpify](https://github.com/samverschueren/rfpify) - Promisify a result-first callback-style function.
	- [delay](https://github.com/sindresorhus/delay) - Delay a promise a specified amount of time.
- Callbacks
	- [each-async](https://github.com/sindresorhus/each-async) - Async concurrent iterator like forEach.
	- [async](https://github.com/caolan/async) - Provides straight-forward, powerful functions for working with asynchronicity.
	- [async-chainable](https://github.com/hash-bang/async-chainable) - Chainable, pluggable async functionality.
	- [after-all-results](https://github.com/watson/after-all-results) - Bundle results of async functions calls into one callback with all the results.
- Generators
	- [co](https://github.com/tj/co) - The ultimate generator based flow-control goodness.
	- [suspend](https://github.com/jmar777/suspend) - Generator-based control flow that plays nice with callbacks, promises, and thunks.
	- [bluebird-co](https://github.com/novacrazy/bluebird-co) - A set of high performance yield handlers for Bluebird coroutines.
- Streams
	- [Highland.js](http://highlandjs.org) - Manages synchronous and asynchronous code easily, using nothing more than standard JavaScript and Node-like Streams.
- Channels
	- [js-csp](https://github.com/jlongster/js-csp) - Communicating sequential processes for JavaScript (like Clojurescript core.async, or Go).
- Other
	- [zone](https://github.com/strongloop/zone) - Provides a way to group and track resources and errors across asynchronous operations.


### Streams

- [through2](https://github.com/rvagg/through2) - Tiny wrapper around streams2 Transform to avoid explicit subclassing noise.
- [from2](https://github.com/hughsk/from2) - Convenience wrapper for ReadableStream, inspired by `through2`.
- [get-stream](https://github.com/sindresorhus/get-stream) - Get a stream as a string or buffer.
- [concat-stream](https://github.com/maxogden/concat-stream) - Concatenates a stream into strings or binary data.
- [into-stream](https://github.com/sindresorhus/into-stream) - Convert a buffer/string/array/object into a stream.
- [duplexify](https://github.com/mafintosh/duplexify) - Turn a writeable and readable stream into a single streams2 duplex stream.
- [pumpify](https://github.com/mafintosh/pumpify) - Combine an array of streams into a single duplex stream.
- [peek-stream](https://github.com/mafintosh/peek-stream) - Transform stream that lets you peek the first line before deciding how to parse it.
- [binary-split](https://github.com/maxogden/binary-split) - A fast newline (or any delimiter) splitter stream.
- [byline](https://github.com/jahewson/node-byline) - Super-simple line-by-line Stream reader.
- [first-chunk-stream](https://github.com/sindresorhus/first-chunk-stream) - Transform the first chunk in a stream.
- [pad-stream](https://github.com/sindresorhus/pad-stream) - Pad each line in a stream.
- [multistream](https://github.com/feross/multistream) - Combine multiple streams into a single stream.
- [stream-combiner2](https://github.com/substack/stream-combiner2) - Turn a pipeline into a single stream.
- [readable-stream](https://github.com/nodejs/readable-stream) - Mirror of Streams2 and Streams3 implementations in core.
- [through2-concurrent](https://github.com/almost/through2-concurrent) - Transform object streams concurrently.
- [graphicsmagick-stream](https://github.com/e-conomic/graphicsmagick-stream) - Fast conversion/scaling of images using a pool of long lived GraphicsMagick processes.


### Real-time

- [Socket.io](http://socket.io) - Enables real-time bidirectional event-based communication.
- [SockJS](https://github.com/sockjs/sockjs-node) - Low latency, full duplex, cross-domain channel browser-server, with WebSockets or without.
- [Faye](http://faye.jcoglan.com) - Real-time client-server message bus, based on Bayeux protocol.
- [SocketCluster](https://github.com/SocketCluster/socketcluster) - Scalable HTTP + WebSocket engine which can run on multiple CPU cores.
- [Primus](https://github.com/primus/primus) - An abstraction layer for real-time frameworks to prevent module lock-in.
- [Straw](https://github.com/simonswain/straw) - Real-time dataflow framework.


### Image

- [sharp](https://github.com/lovell/sharp) - The fastest module for resizing JPEG, PNG, WebP and TIFF images.
- [image-type](https://github.com/sindresorhus/image-type) - Detect the image type of a Buffer/Uint8Array.
- [gm](https://github.com/aheckmann/gm) - GraphicsMagick and ImageMagick wrapper.
- [lwip](https://github.com/EyalAr/lwip) - Lightweight image processor which does not require ImageMagick.
- [pica](https://github.com/nodeca/pica) - High quality & fast resize (lanczos3) in pure JS. Alternative to canvas drawImage(), when no pixelation allowed.
- [jimp](https://github.com/oliver-moran/jimp) - Image processing in pure JavaScript.
- [is-progressive](https://github.com/sindresorhus/is-progressive) - Check if a JPEG image is progressive.
- [probe-image-size](https://github.com/nodeca/probe-image-size) - Get the size of most image formats without a full download.


### Text

- [Underscore.string](https://github.com/epeli/underscore.string) - Collection of string manipulation utilities.
- [iconv-lite](https://github.com/ashtuchkin/iconv-lite) - Convert character encodings.
- [repeating](https://github.com/sindresorhus/repeating) - Repeat a string.
- [string-length](https://github.com/sindresorhus/string-length) - Get the real length of a string - by correctly counting astral symbols and ignoring ansi escape codes.
- [camelcase](https://github.com/sindresorhus/camelcase) - Convert a dash/dot/underscore/space separated string to camelCase: foo-bar → fooBar.
- [escape-string-regexp](https://github.com/sindresorhus/escape-string-regexp) - Escape RegExp special characters.
- [execall](https://github.com/sindresorhus/execall) - Find multiple RegExp matches in a string.
- [splice-string](https://github.com/sindresorhus/splice-string) - Remove or replace part of a string like `Array#splice`.
- [indent-string](https://github.com/sindresorhus/indent-string) - Indent each line in a string.
- [strip-indent](https://github.com/sindresorhus/strip-indent) - Strip leading whitespace from every line in a string.
- [detect-indent](https://github.com/sindresorhus/detect-indent) - Detect the indentation of code.
- [he](https://github.com/mathiasbynens/he) - A robust HTML entity encoder/decoder.
- [i18n-node](https://github.com/mashpie/i18n-node) - Simple translation module with dynamic JSON storage.
- [babelfish](https://github.com/nodeca/babelfish/) - i18n with very easy syntax for plurals.
- [parse-columns](https://github.com/sindresorhus/parse-columns) - Parse text columns, like the output of Unix commands.
- [hanging-indent](https://github.com/codekirei/hanging-indent) - Format a string into a hanging-indented paragraph.
- [matcher](https://github.com/sindresorhus/matcher) - Simple wildcard matching.


## Number

- [random-int](https://github.com/sindresorhus/random-int) - Generate a random integer.
- [random-float](https://github.com/sindresorhus/random-float) - Generate a random float.
- [unique-random](https://github.com/sindresorhus/unique-random) - Generate random numbers that are consecutively unique.
- [round-to](https://github.com/sindresorhus/round-to) - Round a number to a specific number of decimal places: `1.234` → `1.2`.


### Math

- [ndarray](https://github.com/scijs/ndarray) - Multidimensional arrays.
- [mathjs](https://github.com/josdejong/mathjs) - An extensive math library.
- [math-sum](https://github.com/sindresorhus/math-sum) - Sum numbers.
- [math-clamp](https://github.com/sindresorhus/math-clamp) - Clamp a number.


### Date

- [Moment.js](http://momentjs.com) - Parse, validate, manipulate, and display dates.
- [Moment Timezone](http://momentjs.com/timezone/) - IANA Time Zone Database + Moment.js.
- [dateformat](https://github.com/felixge/node-dateformat) - Date formatting.
- [tz-format](https://github.com/samverschueren/tz-format) - Format a date with timezone: `2015-11-30T10:40:35+01:00`.


### URL

- [normalize-url](https://github.com/sindresorhus/normalize-url) - Normalize a URL.
- [humanize-url](https://github.com/sindresorhus/humanize-url) - Humanize a URL: http://sindresorhus.com → sindresorhus.com.
- [url-unshort](https://github.com/nodeca/url-unshort) - Expand shortened URLs.
- [speakingurl](https://github.com/pid/speakingurl) - Generate a slug from a string with transliteration.
- [linkify-it](https://github.com/markdown-it/linkify-it) - Link patterns detector with full unicode support.
- [url-pattern](https://github.com/snd/url-pattern) - Easier than regex string matching patterns for URLs and other strings.
- [embedza](https://github.com/nodeca/embedza) - Create HTML snippets/embeds from URLs using info from oEmbed, Open Graph, meta tags.


### Data validation

- [joi](https://github.com/hapijs/joi) - Object schema description language and validator for JavaScript objects.
- [is-my-json-valid](https://github.com/mafintosh/is-my-json-valid) - JSON Schema validator that uses code generation to be extremely fast.
- [property-validator](https://github.com/nettofarah/property-validator) - Easy property validation for Express.


### Parsing

- [remark](https://github.com/wooorm/remark) - Markdown processor powered by plugins.
- [markdown-it](https://github.com/markdown-it/markdown-it) - A very fast markdown parser with 100% CommonMark support, extensions and syntax plugins.
- [parse5](https://github.com/inikulin/parse5) - Fast full-featured spec compliant HTML parser.
- [strip-json-comments](https://github.com/sindresorhus/strip-json-comments) - Strip comments from JSON.
- [strip-css-comments](https://github.com/sindresorhus/strip-css-comments) - Strip comments from CSS.
- [parse-json](https://github.com/sindresorhus/parse-json) - Parse JSON with more helpful errors.
- [URI.js](https://github.com/medialize/URI.js) - URL mutation.
- [PostCSS](https://github.com/postcss/postcss) - CSS parser / stringifier.
- [JSONStream](https://github.com/dominictarr/JSONStream) - Streaming JSON.parse and stringify.
- [csv-parser](https://github.com/mafintosh/csv-parser) - Streaming CSV parser that aims to be faster than everyone else.
- [neat-csv](https://github.com/sindresorhus/neat-csv) - Fast CSV parser. Callback interface for the above.
- [PEG.js](https://github.com/pegjs/pegjs) - Simple parser generator that produces fast parsers with excellent error reporting.
- [x-ray](https://github.com/lapwinglabs/x-ray) - A web scraping utility to see through the `<html>` noise.
- [nearley](https://github.com/Hardmath123/nearley) - Simple, fast, powerful parsing for JavaScript.
- [binary-extract](https://github.com/juliangruber/binary-extract) - Extract a value from a buffer of JSON without parsing the whole thing.
- [json-mask](https://github.com/nemtsov/json-mask) - Tiny language and engine for selecting parts of an object, hiding/masking the rest.
- [Stylecow](https://github.com/stylecow/stylecow) - Parse, manipulate and convert modern CSS to make it compatible with all browsers. Extensible with plugins.
- [js-yaml](https://github.com/nodeca/js-yaml) - Very fast YAML parser.
- [excel-stream](https://github.com/dominictarr/excel-stream) - Streaming Excel spreadsheet to JSON parser.
- [xml2js](https://github.com/Leonidas-from-XIV/node-xml2js) - XML to JavaScript object converter.
- [Jison](http://zaach.github.io/jison/) - Friendly JavaScript parser generator. It shares genes with Bison, Yacc and family.


### Humanize

- [pretty-bytes](https://github.com/sindresorhus/pretty-bytes) - Convert bytes to a human readable string: `1337` → `1.34 kB`.
- [pretty-ms](https://github.com/sindresorhus/pretty-ms) - Convert milliseconds to a human readable string: `1337000000` → `15d 11h 23m 20s`.
- [ms](https://github.com/rauchg/ms.js) - Tiny millisecond conversion utility.
- [pretty-error](https://github.com/AriaMinaei/pretty-error) - Errors with less clutter.
- [humanize](https://github.com/taijinlee/humanize) - Data formatter for human readability.
- [read-art](https://github.com/Tjatse/node-readability) - Extract readable content from any page.


### Compression

- [Archiver](https://github.com/archiverjs/node-archiver) - Streaming interface for archive generation, supporting ZIP and TAR.
- [decompress-zip](https://github.com/bower/decompress-zip) - Unzip.
- [pako](https://github.com/nodeca/pako) - High speed zlib port to pure js (deflate, inflate, gzip).
- [tar-stream](https://github.com/mafintosh/tar-stream) - Streaming tar parser and generator. Also see [tar-fs](https://github.com/mafintosh/tar-fs).
- [decompress](https://github.com/kevva/decompress) - A pluggable decompression module with support for `tar`, `tar.gz` and `zip` files out of the box.


### Network

- [get-port](https://github.com/sindresorhus/get-port) - Get an available port.
- [ipify](https://github.com/sindresorhus/ipify) - Get your public IP address.
- [getmac](https://github.com/bevry/getmac) - Get the computer MAC address.


### Database

- Drivers
	- [LevelUP](https://github.com/Level/levelup) - LevelDB.
	- [MongoDB](https://github.com/mongodb/node-mongodb-native) - MongoDB driver.
	- [PostgreSQL](https://github.com/brianc/node-postgres) - PostgreSQL client. Pure JavaScript and native libpq bindings.
	- [MySQL](https://github.com/felixge/node-mysql) - MySQL client.
	- [Redis](https://github.com/luin/ioredis) - Redis client.
- ODM / ORM
	- [Bookshelf](http://bookshelfjs.org) - ORM for PostgreSQL, MySQL and SQLite3 in the style of Backbone.js.
	- [Massive](https://github.com/robconery/massive-js) - PostgreSQL data access tool.
	- [Mongoose](http://mongoosejs.com) - Elegant MongoDB object modeling.
	- [Sequelize](https://github.com/sequelize/sequelize) - Multi-dialect ORM. Supports PostgreSQL, SQLite, MySQL.
	- [Waterline](https://github.com/balderdashy/waterline) - Datastore-agnostic tool that dramatically simplifies interaction with one or more databases.
	- [Iridium](https://github.com/SierraSoftworks/Iridium) - A high performance MongoDB ORM with support for promises, distributed caching, preprocessing, validation and plugins.
	- [OpenRecord](https://github.com/PhilWaldmann/openrecord) - ORM for PostgreSQL, MySQL, SQLite3 and RESTful datastores. Similar to ActiveRecord.
	- [orm2](https://github.com/dresende/node-orm2) - ORM for PostgreSQL, MariaDB, MySQL, Amazon Redshift, SQLite, MongoDB.
	- [firenze](https://github.com/fahad19/firenze) - Adapter-based ORM for MySQL, Memory, Redis, localStorage and more.
- Query builder
	- [Knex](http://knexjs.org) - A query builder for PostgreSQL, MySQL and SQLite3, designed to be flexible, portable, and fun to use.
- Other
	- [NeDB](https://github.com/louischatriot/nedb) - Embedded persistent database written in JavaScript.


### Testing

- [AVA](https://ava.li) - Futuristic test runner.
- [tap](https://github.com/isaacs/node-tap) - A TAP test framework.
- [tape](https://github.com/substack/tape) - TAP-producing test harness.
- [Mocha](http://mochajs.org) - A feature-rich test framework making asynchronous testing simple and fun.
- [power-assert](https://github.com/power-assert-js/power-assert) - Provides descriptive assertion messages through the standard assert interface.
- [Mochify](https://github.com/mantoni/mochify.js) - TDD with Browserify, Mocha, PhantomJS and WebDriver.
- [trevor](https://github.com/vdemedes/trevor) - Run tests against multiple versions of Node.js without switching versions manually or pushing to Travis CI.
- [loadtest](https://github.com/alexfernandez/loadtest) - Run load tests for your web application, with an API for automation.
- [istanbul](https://github.com/gotwarlost/istanbul) - A code coverage tool that computes statement, line, function and branch coverage with module loader hooks to transparently add coverage when running tests.
- [nyc](https://github.com/bcoe/nyc) - Code coverage tool built on istanbul that works with subprocesses.
- [Sinon.JS](https://github.com/sinonjs/sinon) - Test spies, stubs and mocks.
- [navit](https://github.com/nodeca/navit) - PhantomJS / SlimerJS wrapper to simplify browser test scripting.
- [nock](https://github.com/pgte/nock) - HTTP mocking and expectations.
- [intern](https://github.com/theintern/intern) - A next-generation code testing stack for JavaScript.
- [toxy](https://github.com/h2non/toxy) - Hackable HTTP proxy to simulate failure scenarios and network conditions.
- [hook-std](https://github.com/sindresorhus/hook-std) - Hook and modify stdout/stderr.
- [testen](https://github.com/egoist/testen) - Run tests for multiple versions of Node.js locally with NVM.


### Benchmarking

- [Benchmark.js](http://benchmarkjs.com) - A robust benchmarking library that works on nearly all JavaScript platforms, supports high-resolution timers, and returns statistically significant results.
- [matcha](https://github.com/logicalparadox/matcha) - A caffeine-driven, simplistic approach to benchmarking.


### Minifiers

- [UglifyJS2](http://lisperator.net/uglifyjs/) - JavaScript minifier.
- [clean-css](https://github.com/jakubpawlowicz/clean-css) - CSS minifier.
- [minimize](https://github.com/Swaagie/minimize) - HTML minifier.
- [imagemin](https://github.com/imagemin/imagemin) - Image minifier.


### Authentication

- [Passport](http://passportjs.org) - Simple, unobtrusive authentication.
- [everyauth](https://github.com/bnoguchi/everyauth) - Authentication and authorization (password, Facebook, etc) for your Connect and Express apps.
- [passwordless](https://passwordless.net) - Token-based authentication middleware for Express allowing authentication without passwords.
- [Lockit](https://github.com/zemirco/lockit) - Full featured authentication solution for Express. Supports a variety of databases, predefined routes, email and two-factor authentication.
- [Grant](https://github.com/simov/grant) - OAuth middleware for Express, Koa, and Hapi.


### Email

- [Nodemailer](https://github.com/andris9/Nodemailer) - The fastest way to handle email.
- [emailjs](https://github.com/eleith/emailjs) - Send text/HTML emails with attachments to any SMTP server.


### Job queues

- [kue](https://github.com/Automattic/kue) - Priority job queue backed by Redis.
- [bull](https://github.com/OptimalBits/bull) - Persistent job and message queue.


### Node.js management

- [n](https://github.com/tj/n) - Node.js version management.
- [nave](https://github.com/isaacs/nave) - Virtual Environments for Node.js.
- [nodeenv](https://github.com/ekalinin/nodeenv) - A Node.js virtual environment compatible to Python's virtualenv.
- [nvm for Windows](https://github.com/coreybutler/nvm-windows) - Version management for Windows.


### Polyfills

- Node.js
	- [set-immediate-shim](https://github.com/sindresorhus/set-immediate-shim) - Simple `setImmediate()` ponyfill.
	- [path-is-absolute](https://github.com/sindresorhus/path-is-absolute) - Node.js 0.12 `path.isAbsolute()` ponyfill.
	- [os-tmpdir](https://github.com/sindresorhus/os-tmpdir) - Node.js `os.tmpdir()` ponyfill.
	- [os-homedir](https://github.com/sindresorhus/os-homedir) - Node.js 4.0 `os.homedir()` ponyfill.
	- [debug-log](https://github.com/sindresorhus/debug-log) - Node.js 0.12 `util.debuglog()` ponyfill.
	- [buffer-equals](https://github.com/sindresorhus/buffer-equals) - Node.js 0.12 `buffer.equals()` ponyfill.
	- [buffer-includes](https://github.com/sindresorhus/buffer-includes) - Node.js 5.3.0 `buffer.includes()` ponyfill.
	- [buf-indexof](https://github.com/sindresorhus/buf-indexof) - Node.js 4.0 `buffer.indexOf()` ponyfill.
	- [buf-compare](https://github.com/sindresorhus/buf-compare) - Node.js 0.12 `Buffer.compare()` ponyfill.
	- [fs-access](https://github.com/sindresorhus/fs-access) - Node.js 0.12 `fs.access()` & `fs.accessSync()` ponyfill.
	- [exec-file-sync](https://github.com/sindresorhus/exec-file-sync) - Node.js 0.12 `childProcess.execFileSync()` ponyfill.
	- [child-process-ctor](https://github.com/sindresorhus/child-process-ctor) - Node.js 4.0 `childProcess.ChildProcess` ponyfill.
	- [node-status-codes](https://github.com/sindresorhus/node-status-codes) - Node.js `http.STATUS_CODES` ponyfill.
	- [exit-code](https://github.com/isaacs/exit-code) - Node.js 0.12 `process.exitCode` polyfill.
	- [core-assert](https://github.com/sindresorhus/core-assert) - Node.js `assert` as a standalone module.
	- [deep-strict-equal](https://github.com/sindresorhus/deep-strict-equal) - Test for deep equality - Node.js `assert.deepStrictEqual()` algorithm as a standalone module.
- JavaScript
	- [object-assign](https://github.com/sindresorhus/object-assign) - ES2015 `Object.assign()` ponyfill.
	- [pinkie-promise](https://github.com/floatdrop/pinkie-promise) - ES2015 `Promise` ponyfill.
	- [harmony-reflect](https://github.com/tvcutsem/harmony-reflect) - ES2015 `Reflect` and `Proxy` polyfill.
	- [es6-shim](https://github.com/paulmillr/es6-shim) - Collection of ES2015 polyfills.
	- More ES2015 polyfills at [es6-tools](https://github.com/addyosmani/es6-tools#polyfills).


### Natural language processing

- [retext](https://github.com/wooorm/retext) - An extensible natural language system.
- [franc](https://github.com/wooorm/franc) - Detect the language of text.
- [leven](https://github.com/sindresorhus/leven) - Measure the difference between two strings using the Levenshtein distance algorithm.
- [natural](https://github.com/NaturalNode/natural) - A general natural language facility.


### Process management

- [PM2](https://github.com/Unitech/pm2) - Advanced Process Manager.
- [node-windows](https://github.com/coreybutler/node-windows) - Run scripts as a native Windows service and log to the Event viewer.
- [node-mac](https://github.com/coreybutler/node-mac) - Run scripts as a native Mac daemon and log to the console app.
- [node-linux](https://github.com/coreybutler/node-linux) - Run scripts as native system service and log to syslog.
- [forever](https://github.com/foreverjs/forever) - A simple CLI tool for ensuring that a given script runs continuously (i.e. forever).
- [nodemon](https://github.com/remy/nodemon) - Monitor for changes in your app and automatically restart the server.
- [supervisor](https://github.com/petruisfan/node-supervisor) - Restart scripts when they crash or restart when a `*.js` file changes.
- [Phusion Passenger](https://www.phusionpassenger.com/node_weekly) - Friendly process manager that integrates directly into Nginx.
- [naught](https://github.com/andrewrk/naught) - Process manager with zero downtime deployment.


### Automation

- [robotjs](https://github.com/octalmage/robotjs) -  Desktop Automation: control the mouse, keyboard and read the screen.


### AST

- [Acorn](https://github.com/ternjs/acorn) - A tiny, fast JavaScript parser.
- [Rocambole](https://github.com/millermedeiros/rocambole) - Recursively walk and transform JavaScript AST.


### Static site generators

- [Metalsmith](http://www.metalsmith.io) - An extremely simple, pluggable static site generator.
- [Wintersmith](http://wintersmith.io) - Flexible, minimalistic, multi-platform static site generator.
- [Assemble](http://assemble.io) - Static site generator for Node.js, Grunt.js, and Yeoman.
- [DocPad](https://github.com/docpad/docpad) - Static site generator with dynamic abilities and huge plugin ecosystem.


### Content management systems

- [KeystoneJS](http://keystonejs.com) - CMS and web application platform built on Express and MongoDB.
- [Calipso](http://calip.so) - A simple content management system, built along similar themes to Drupal and Wordpress, that is designed to be fast, flexible and simple.
- [Apostrophe2](http://apostrophenow.org) - A content management system with an emphasis on intuitive front end content editing and administration built on Express and MongoDB.


### Forum

- [nodeBB](https://nodebb.org) - A better forum platform for the modern web.


### Blogging

- [ghost](https://ghost.org) - Simple, powerful publishing platform that allows you to share your story with the world.
- [Hexo](https://hexo.io/) - Fast, simple and powerful blogging framework.


### Weird

- [superb](https://github.com/sindresorhus/superb) - Get superb like words.
- [cat-names](https://github.com/sindresorhus/cat-names) - Get popular cat names.
- [dog-names](https://github.com/sindresorhus/dog-names) - Get popular dog names.
- [superheroes](https://github.com/sindresorhus/superheroes) - Get superhero names.
- [supervillains](https://github.com/sindresorhus/supervillains) - Get supervillain names.
- [cool-ascii-faces](https://github.com/maxogden/cool-ascii-faces) - Get some cool ascii faces.
- [cat-ascii-faces](https://github.com/melaniecebula/cat-ascii-faces) - ₍˄·͈༝·͈˄₎◞ ̑̑ෆ⃛ (=ↀωↀ=)✧ (^･o･^)ﾉ”
- [cows](https://github.com/sindresorhus/cows) - ASCII cows.


### Miscellaneous

- [execa](https://github.com/sindresorhus/execa) - A better `child_process`.
- [cheerio](https://github.com/cheeriojs/cheerio) - Fast, flexible, and lean implementation of core jQuery designed specifically for the server.
- [Electron](https://github.com/atom/electron) - Build cross platform desktop apps with web technologies. *(You might like [awesome-electron](https://github.com/sindresorhus/awesome-electron))*
- [opn](https://github.com/sindresorhus/opn) - Opens stuff like websites, files, executables.
- [hasha](https://github.com/sindresorhus/hasha) - Hashing made simple. Get the hash of a buffer/string/stream/file.
- [dot-prop](https://github.com/sindresorhus/dot-prop) - Get a property from a nested object using a dot path.
- [onetime](https://github.com/sindresorhus/onetime) - Only run a function once.
- [mem](https://github.com/sindresorhus/mem) - Memoize functions - an optimization technique used to speed up consecutive function calls by caching the result of calls with identical input.
- [require-uncached](https://github.com/sindresorhus/require-uncached) - Require a module bypassing the cache.
- [stringify-object](https://github.com/yeoman/stringify-object) - Stringify an object/array like JSON.stringify just without all the double-quotes.
- [strip-bom](https://github.com/sindresorhus/strip-bom) - Strip UTF-8 byte order mark (BOM) from a string/buffer/stream.
- [deep-assign](https://github.com/sindresorhus/deep-assign) - Recursive `Object.assign()`.
- [os-locale](https://github.com/sindresorhus/os-locale) - Get the system locale.
- [nan](https://github.com/nodejs/nan) - A header file filled with macro and utility goodness for making add-on development for across Node.js versions easier.
- [multiline](https://github.com/sindresorhus/multiline) - Multiline strings in JavaScript.
- [ssh2](https://github.com/mscdex/ssh2) - An SSH2 client and server module.
- [adit](https://github.com/markelog/adit) - SSH tunneling made simple.
- [lazy-req](https://github.com/sindresorhus/lazy-req) - Require modules lazily.
- [file-type](https://github.com/sindresorhus/file-type) - Detect the file type of a Buffer.
- [Bottleneck](https://github.com/SGrondin/bottleneck) - A powerful rate limiter that makes throttling easy.
- [webworker-threads](https://github.com/audreyt/node-webworker-threads) - Lightweight Web Worker API implementation with native threads.
- [node-pre-gyp](https://github.com/mapbox/node-pre-gyp) - Makes it easy to publish and install Node.js C++ addons from binaries.
- [opencv](https://github.com/peterbraden/node-opencv) - Bindings for OpenCV. The defacto computer vision library.
- [common-errors](https://github.com/shutterstock/node-common-errors) - Common error classes and utility functions.
- [agenda](https://github.com/rschmukler/agenda) - Lightweight job scheduling on MongoDB.
- [dotenv](https://github.com/motdotla/dotenv) - Load environment variables from .env file.
- [remote-git-tags](https://github.com/sindresorhus/remote-git-tags) - Get tags from a remote git repo.
- [semver](https://github.com/npm/node-semver) - [semver](http://semver.org) parser.
- [nar](https://github.com/h2non/nar) - Create self-contained executable binaries.
- [node-bell](https://github.com/eleme/bell.js) - Real-time anomalies detection for periodic time series.
- [Faker.js](https://github.com/Marak/Faker.js) - Generate massive amounts of fake data.
- [nodegit](https://github.com/nodegit/nodegit) - Native bindings to Git.
- [json-strictify](https://github.com/pigulla/json-strictify) - Safely serialize a value to JSON without data loss or going into an infinite loop.
- [parent-module](https://github.com/sindresorhus/parent-module) - Get the path of the parent module.
- [resolve-from](https://github.com/sindresorhus/resolve-from) - Resolve the path of a module like `require.resolve()` but from a given path.

