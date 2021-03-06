# turbo-octo-log
## A log for everyday programming challenges


### Storybook viewport cofigurations ###
`storybook` `viewport`

[https://github.com/storybookjs/storybook/blob/master/addons/viewport/src/defaults.ts#L135](https://github.com/storybookjs/storybook/blob/master/addons/viewport/src/defaults.ts#L135)

[https://storybook.js.org/docs/react/essentials/viewport](https://storybook.js.org/docs/react/essentials/viewport)

---

### Remove storybook body padding or margin ###
`storybook`

[https://github.com/storybookjs/storybook/pull/9229](https://github.com/storybookjs/storybook/pull/9229)

---

### Material Design Easing curve ###

`animation` `easing`
[https://material.io/design/motion/speed.html#easing](https://material.io/design/motion/speed.html#easing)

---
### Collection of Animation easing functions ###

[https://easings.net](https://easings.net/)

---

### Animations using angular directives ###

[Animation using angular directives](https://nativescripting.com/posts/animations-using-angular-directives)

---

### Angular Animation ###
`Angular Animation`

[https://medium.com/web-factory-llc/getting-started-with-programmatic-animations-using-the-angular-animations-api-3389ccc2184d](https://medium.com/web-factory-llc/getting-started-with-programmatic-animations-using-the-angular-animations-api-3389ccc2184d)

[https://medium.com/angular-in-depth/total-guide-to-dynamic-angular-animations-that-can-be-toggled-at-runtime-be5bb6778a0a](https://medium.com/angular-in-depth/total-guide-to-dynamic-angular-animations-that-can-be-toggled-at-runtime-be5bb6778a0a)

--- 

### How to use the calenar component alone without the DatePicker
`Angular` `Material Design `
[Angular Material Calendar Component](https://onthecode.co.uk/angular-material-calendar-component/)


---

### When using !important is the right choice?

[When using !important is the right choice?](https://www.notion.so/scotteau/Daily-Log-0ab8f27db4c64207a5ca8a58ae4826ed#5fb119eb639d435197a7df115998b112)

---

### disable eslint

[link](http://www.justthink.it/articles/turn-off-eslint-rule-via-config-file-via-javascript/)

---

### what is LF and CRLF and how to solve issues of this

[use a command line tool](https://www.ilovefreesoftware.com/28/programming/how-to-convert-lf-line-endings-to-crlf-line-endings.html)

[stack overflow](https://stackoverflow.com/questions/1552749/difference-between-cr-lf-lf-and-cr-line-break-types)

---

### Use git emoji

[resource](https://github.com/carloscuesta/gitmoji)
[explanation](https://opensource.com/article/19/2/emoji-log-git-commit-messages)

---

### What is CI/CD

[What is CI/CD? Continuous integration and continuous delivery explained](https://www.infoworld.com/article/3271126/what-is-cicd-continuous-integration-and-continuous-delivery-explained.html)

---

### Note taken from the beginner's guide to React

[className and style overide](https://egghead.io/lessons/react-style-react-components-with-classname-and-inline-styles)

[use tailwind css with React](https://www.smashingmagazine.com/2020/02/tailwindcss-react-project/)

1. when use the production mode, the prop-type will not work. prop-type is for other developers who use your components
2. it is actually very productive use React with tailwind rather than Bootstrap/AntD in case you will do a lot customization.
3. in use effect we use a function for only once initialization

---

### Drag drop file uploader vanilla js

[Drag drop file uploader vanilla js - Smashing Magazine](https://www.smashingmagazine.com/2018/01/drag-drop-file-uploader-vanilla-js/)

---

### Simple drag and drop file upload in react

[Simple drag and drop file upload in react](https://medium.com/@650egor/simple-drag-and-drop-file-upload-in-react-2cb409d88929)

---

### Dealing with overflow and position: sticky;

[Dealing with overflow and position: sticky](https://css-tricks.com/dealing-with-overflow-and-position-sticky/)

想要 overflow 起作用, 必须设置一个对应方向上的 width 或 height.

---

### How to use React Beautiful DnD?

`drag n drop` `library`
[Beautiful and accessible drag and drop with react beautiful dnd - Egghead.io video course](https://egghead.io/courses/beautiful-and-accessible-drag-and-drop-with-react-beautiful-dnd)

---

### How to use color functions in Sass?

`SASS` `Color function`
[Controlling color with sass color function](https://thoughtbot.com/blog/controlling-color-with-sass-color-functions)

```scss
border: 1px solid darken($base-color, 20%);
text-shadow: 0 -1px 0 darken($base-color, 10%);
@include box-shadow(inset 0 1px 0 lighten($base-color, 20%));
```

---

### How to setup Typescript with Node?

`package.json` `typescript` `node`

#### Project Setup

```
cd desired-folder
mkdir node-project-with-ts
npm init -y
```

```
node-project-with-ts
│   package.json
│   tsconfig.json
│
└───src
│   │   index.ts
│   │
|
└───node_modules
```

#### Installing Dependencies

```
npm i typescript nodemon concurrently -D
```

Initiate Typescript with options

```
npx tsc --init --rootDir src --outDir dist \
--esModuleInterop --resolveJsonModule --lib es6 \
--module commonjs --allowJs true --noImplicitAny true
```

tscnfig.json, 设置源文件和导出文件夹的位置

```
{
  "compilerOptions" :{
    ...
    "rootDir": "src",
    "outDir": "dist",
    "sourceMap": true,
  }
}
```

在 package.json, 用 concurrently 和 nodemon 配合来自动把 ts 编译成 js, 再应用到 node 里.

```javascript
"scripts": {
  "dev": "concurrently \"tsc -w\" \"nodemon dist/index.js\""
},
```

#### Installing Koa & node-fetch

安装 koa 和 node-fetch, 以及@types 文件供 ts 来用.
接下来就可以开始写业务代码了.

```
npm i koa node-fetch
npm i @types/koa @types/node-fetch -D
```

#### 当需要运行时, 请运行一下命令.

```
npm run dev
```

[How to Setup a TypeScript + Node.js Project](https://khalilstemmler.com/blogs/typescript/node-starter-project/)
[Tips for setting up a TypeScript nodejs project](https://codeburst.io/tips-for-setting-up-a-typescript-nodejs-project-5d1c48dc1a2d)
[Setting Up A Node Typescript Project in Under 4 minutes - 另外一种方式](https://dev.to/theghostyced/setting-up-a-node-typescript-project-in-under-4-minutes-4gk2)
[Typescript with Node: Should I use ts-node or tsc & node?](https://www.reddit.com/r/typescript/comments/8vkvzy/typescript_with_node_should_i_use_tsnode_or_tsc/)

## Week 7

---

### 3 ways to autofocus an element

`:focus` `ref`

**总结一下, 当你在 React 里需要 autofocus 一个 input 时, 应该来看这篇文章**

[3 ways to autofocus an input in React that ALMOST always work!](https://blog.danieljohnson.io/react-ref-autofocus/)

---

### 如何在程序里管理你的各种 api 的 access key

`secret` `hide your api keys`

最近 api 用的比较多, 希望大家可以意识到, 不想暴露自己的 api key, 这个 key 是不要直接写在程序里的.

##### 下面是解决方案

1. 在 project root 下创建一个`.env`文件
2. 在.gitignore 里加入.env, 这样这个文件不会被 git 记录.
3. 在`.env`中写入你的 api keys, 务必添加 REACT*APP*在 key 名字前. 比如

```
REACT_APP_GOOGLE_API_KEY=lkdfalkjdfbl1123sdkfjlsdjfls;
```

3. 在需要使用的地方用`process.env.REACT_APP_GOOGLE_API_KEY`来引用你的 key
4. 一般部署的地方可以设置 environment variables, 按照同样的名字设置你的 key.

---

### CORS (Cross-Origin-Resource-Sharing)的前世今生 & 如何解决 Cors 的问题

## `CORS` `网络协议`

[Ollie 找到的解决方案 👍 - 解决 Cors 问题的几个方式 - StackOverflow](https://stackoverflow.com/questions/43871637/no-access-control-allow-origin-header-is-present-on-the-requested-resource-whe)

[文章链接 - 所有人都应该知道的跨域及 COR - 知乎](https://zhuanlan.zhihu.com/p/53996160)
[深入了解 - 你应该了解的 CORS - 知乎](https://juejin.im/post/5d336c95f265da1b5f2690f5)
[强化阅读 - 科普一下 CORS 以及如何节省一次 OPTIONS 请求 - 知乎](https://zhuanlan.zhihu.com/p/70032617)

--

#### 我来试着总结一下, CORS, 跨域访问控制, 又称 HTTP 访问控制.

##### 先要理解, 什么是 `同源策略(Same-origin policy)`?

- 他的存在主要是针对, 1996 年 Netscape 提出的一种在浏览器端执行的安全规则 - **同源策略(Same-origin policy)**.
- 同源策略的目的是, 为了限制 webapp 运行时去运行非当前 origin 下的资源, 比如说连接到另外一个 origin 下的恶意文本.
- 什么才算是 same origin?(同域) 协议(protocol), 域名(domain), 端口(port) 全部相同才算是同域. 否则都算为 cross-origin.
- 本质上来说, meat.daydayup.com 和 vegie.daydayup.com 算是**Cross-origin**, 因为三级域名并不一致. (meat vs vegie). 因此, 这样的访问会被浏览器限制. 对的, 这其实很不合理. 这算是这个规则的设计缺陷.

##### 为了解决这种缺陷, 勤劳勇敢的劳动人民们发明了 JSONP 和同域代理.

- **同域代理(目前已弃用)**

  > 同域代理就是使用 Ajax 向同域下的后台发送请求，同时携带真实请求的地址及参数，后台接受请求后直接根据地址及参数转发请求，因为后台是可以直接模拟 HTTP 客户端发送请求的，所以没有跨域问题，而后台接受到响应数据后再原样返回给前端浏览器，从而实现跨域数据交互.

- **JSONP(目前已弃用)**

  > JSONP 是利用了 script 标签的 src 属性来实现跨域数据交互的，因为浏览器解析 HTML 代码时，原生具有 src 属性的标签，浏览器都赋予其 HTTP 请求的能力，而且不受跨域限制，使用 src 发送 HTTP 请求，服务器直接返回一段 JS 代码的函数调用，将服务器数据放在函数实参中，前端提前写好响应的函数准备回调，接收数据，实现跨域数据交互；

但是这两个方法, 只是绕开了跨域的问题, 并没有真正解决它, 算是临时的解决方案.

##### 主角出现, CORS, 为了彻底解决 跨域资源 访问而退出的一种新的协议, 它依旧住在浏览器里.

#### 简单地来讲, CORS 协议是通过一系列的 HEAD 来实现他的功能的. 这些 head 的作用如下

1. **阻止** 或者 **允许**, 浏览器向其他域名发起请求;
2. **接受** 或者 **拒绝**, 其他域名返回的响应数据.

这里需要注意的是,
跨域是浏览器正确做出请求, 服务器也正确做出响应, 双方沟通过之后, **浏览器礼貌地拒绝**接收 cross-origin 服务器返回的数据.

所以本质上来说, 是浏览器在主导这套规则.

##### 其他的一些细节

- 浏览器发出**异域请求**时, 会添加 Request Head > **Origin: https://www.daydayup.com**, 标明自己的 origin 是什么.
- 如果服务器返回本次响应的数据, 并在返回的会添加一个 Response Head > **Access-Control-Allow-Origin: www.daydayup.com**
- 这样, 浏览器前面发出的**请求 HEAD**和**响应 HEAD**里面 origin 和 Access-Control-Allow-Orign 的信息可以对上, 浏览器就会接收, 反之拒绝.

个人觉得是考虑到响应传输的效率, 简单的请求会直接被允许, 比如说纯文本. 而成本比较高或者的请求, 即复杂请求(图片,脚本等等), 在发出前, 浏览器会发出一个 preflight 请求和服务器进行信息的对接, 如果 ok, 再发出正式请求. 如果对接失败, 就不会正式发出请求.

![](https://user-images.githubusercontent.com/1281209/80579192-2fa16a80-8a3c-11ea-8290-4ff5c11dc6e0.png)

![](https://user-images.githubusercontent.com/1281209/80579024-f7019100-8a3b-11ea-8621-7ffac84af5c9.png)

---

### 关于 React 里的 key 的官方说明和推荐阅读

![](https://user-images.githubusercontent.com/1281209/80592801-9df12780-8a52-11ea-8cdd-3dfaddd0d4f5.png)

> Using index as key may break your application and display wrong data!

- 如果你不设置 key, React 会帮你用 index 来作为 key, 因为它想不到更好的解决方案. 如果你自己用 index, react 假设你知道自己在做什么.
- 每个 item 的 key 应该是**unique** & **permanent**的.
- 最后文章 **强烈推荐**[ShortId](https://www.npmjs.com/package/shortid)来创建 unique id. (e.g. 46Juzcyx)

#### 后面作者还补充, 有些情况用 index 来做 key 也无妨, 当以下几种情况全部全部全部符合

- list or items 是静态的, 不会做任何变化的.
- 列表中的 items 没有自己的 id
- 这个列表不会被重新排序(reordered)或筛选(filtered)

---

### Missing dependency warning related to `useEffect`

`hook` `react` `dependency`

#### 总结, 简单来说就是, 把 missing 的 dependency 从外面搬进 useEffect 里.

![StackOverflow](https://user-images.githubusercontent.com/1281209/80595999-3c33bc00-8a58-11ea-91ad-587dda93aba9.png)

---

### Git 空运行 - `git mergo`

`git`

![](https://user-images.githubusercontent.com/1281209/80596519-14912380-8a59-11ea-9a0a-bd92bc16e78f.png)

---

## Week 6

### React Hook

Link: [official intro](https://reactjs.org/docs/hooks-overview.html)

Summary:

1. react hook 本质上是一种官方推荐的 best practice。react 的生命周期函数明确地分割了 react 框架的行为，而 react hook 则是方便用户的 api，可以减少代码冗余，使代码可读性增强。
2. 使用 hook 的时候接触到 Eslint 的坑，Eslint 是一个规定语法和格式的控制器，如果安装之后 config 不善就会导致各种报错。

---

### context, bind, arrow function, this

Link：[js 教程](https://zh.javascript.info/object-methods)
[my blog](https://blog.csdn.net/Rance_King/article/details/105704085)

---

### Button type

Link:

[W3C button](https://www.w3school.com.cn/tags/att_button_type.asp)

[input types](https://www.cnblogs.com/xiaohuochai/p/5179909.html)

Summary:

1. button 是 HTML5 新特性, 规定上 button 必须设置 type, 默认的 button type 在大多数浏览器上是 submit，在 ie 上是 button
2. 只有三种 button type，即"submit", "reset", "button". "submit" and "reset"用于表单的发送和清空, "button"用于其他情况
3. `<input type='button'>` 是传统的制作 button 的方法
4. 选用 button 种类时，应关注的是 button 如何被使用，而非其外观，这可能也是 HTML5 如此设定的原因，区别于 input 中 20 多种外观的输入方式

---

### 不同的子组件如何同时共享 state 内的数据？

`react`

https://zh-hans.reactjs.org/docs/lifting-state-up.html

---

### 父组件如何获取子组件内 state 的值？

`react`

https://segmentfault.com/q/1010000007295553

---

### context, bind, arrow function, this

Link：[js 教程](https://zh.javascript.info/object-methods)
[my blog](https://blog.csdn.net/Rance_King/article/details/105704085)

---

### Button type

Link:

[W3C button](https://www.w3school.com.cn/tags/att_button_type.asp)

[input types](https://www.cnblogs.com/xiaohuochai/p/5179909.html)

Summary:

1. button 是 HTML5 新特性, 规定上 button 必须设置 type, 默认的 button type 在大多数浏览器上是 submit，在 ie 上是 button
2. 只有三种 button type，即"submit", "reset", "button". "submit" and "reset"用于表单的发送和清空, "button"用于其他情况
3. `<input type='button'>` 是传统的制作 button 的方法
4. 选用 button 种类时，应关注的是 button 如何被使用，而非其外观，这可能也是 HTML5 如此设定的原因，区别于 input 中 20 多种外观的输入方式

---

### Css Grid completed guide

https://css-tricks.com/snippets/css/complete-guide-grid/

### A Smooth scrolling implementation in React

https://codepen.io/brian-baum/pen/mJZxJX

### How to Re-render a react component on Window Resize

https://www.pluralsight.com/guides/re-render-react-component-on-window-resize

### Responsive background images using react hooks

https://itnext.io/responsive-background-images-using-react-hooks-941af365ea1f

### How to add custom utilities in tailwindcss

https://web-crunch.com/posts/how-to-extend-tailwind-css

### Understanding this.setState({ [name]: value})

Link: [a blog](https://medium.com/@bretdoucette/understanding-this-setstate-name-value-a5ef7b4ea2b4)

Summary:

1. 这种对 key 的动态赋值可以用在所有 object 的 key 上，不仅仅是 this.setState 中，与 object key 动态赋值的语法无关，object key 动态赋值是 js 的一个特性
2. 用[]动态指定一个变量, 这个变量的值必须事先已经注册在 this.state 中，这归根结底在于 this.state 是一个特殊的 object，如果不是在 constructor 中事先初始化，事后追加的 this.setState 里面的值是不能出现在 this.state 里面的(与生命周期函数有关)
3. [xxx]中的内容 xxx 其来源是动态的，在 this.setState 的用法中往往是根据函数传进来的参数进行动态赋值
4. 为什么会有这样的 js 设定？可以猜象，因为 object 的 value 是可以用外部的变量进行赋值的，而且 value 并不唯一；但对于 object 的 key 来说，从外部用变量赋值显然是有限制的，因为 key 必须是唯一值，万一两个不同的外部变量给了一个相同的 key 值，那就会造成问题。所以通过动态赋值的写法，就保证了 key 值的唯一，因为无论什么变量传入，都必须以变量的值为准，这个值指向唯一的 key

---

### use git more efficiently

Summary: 对于使用 git add 和 commit 以及提交分支的时机，如果控制得当，可以减少产生 conflict 的状况，并将操作简化。

1. 不随意进行 commit。进行 commit 的时机是阶段性完成之后，简而言之，commit 是为了明确说明自己在这一段里面做了什么。一般写完一些没事用 add 去添加。
2. 在提交之前切换到 develop 进行 pull，切换回本分支进行 commit 以及 merge 操作，这里如果不 commit，merge 操作执行的结果就是 already up to date，并无法提交，这样保证了操作的正确性。把 commit 留到 develop pull 之后再做可以极大减少问题的发生。

---

### axios simple tutorial

Link: [极简 axios 入门和源码分析](https://github.com/zxfjd3g/191121_axios)

---

### How To Use Bootstrap With React

`React` `Bootstrap`

https://www.bootstrapdash.com/use-bootstrap-4-with-reactjs/

### git readme conflict

`git`

今天做完作业，按照往常 add 建立连接，然后 push，结果报错了。发现是 git 远程 repo 与本地 repo 的 readme 共存，所以冲突了。那就 pull 一下咯？
首先 git pull origin master,但是！报错：fatal: refusing to merge unrelated histories
解决方案：git pull origin master --allow-unrelated-histories
然后解决冲突。就可以正常 push 了。

### js 模糊搜索

`js`

在做 timezone 的作业时，碰到一个问题。时区的参数格式是'Australia/Sydney',所有类似的时区格式以数组的形式保存，例如：

```javascript
const cities = ["Australia/Sydney", "Australia/Melbourne", "Australia/Perth"];
```

但是用户的输入可能只是'Sydney'，并不完整，这时候就可以用模糊搜索来搜索片段并定位，链接中有封装好的方法：
https://www.jianshu.com/p/4cd4f74a0b20
https://juejin.im/post/5e859abb6fb9a03c714b4201

### Important concepts:

`this` `arrow function` `scope` `hoist`

summary: 一些容易混淆的基础概念总结。

1. "this" in JavaScript
   https://zhuanlan.zhihu.com/p/31812336 (比较全面的 this 用法和特性介绍以及各个情况下的使用)

2. Difference between Arrow Function and other Functions:
   https://blog.csdn.net/github_38851471/article/details/79446722

3. 老师上节课的 scope 和 hoist 的总结：
   scope:

var is functional scope
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var

let and const are block scope
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const

hoist:

- var
- function

NOTE: only declaration will be hoisted

---

### React Principle

`react` `study summary`

Summary: React 有两个原则--其一是使用不可变的数据结构，其二是使用单向数据流。

1. 单向数据流指的是数据流的流向是单一的，在 constructor 当中用 this.state 来定义某些需要操作的属性。当其他方法中对 this.state 的操作完成之后，不得用 this.state.xx=xxx 去修改 this.state 中的项目，而必须要使用 this.setState 方法将数据流重新导回 this.state，这个规定给 react component 的使用指定了一个方向性。

2. React 拥护不可变的数据结构。这意味着，每一个数据在 react 中都不建议去直接操作并改变它。有一个统一的思路，就是把所有修改数据的操作，统统变成搜集资源->新建数据的操作。如此，es6 中的 spread 运算符几乎就是为这个需求所生的。通过`...`的运算符来利用旧资源创建新资源，这是一个通用思路。

   ***

### React ES6 Tips & Tricks

`react` `es6` `study summary`

Summary: Learn how es6 syntax helps you to write React efficiently

Link:

[React 学习之道](https://leanpub.com/the-road-to-learn-react-chinese/read_full)

[my personal blog](https://blog.csdn.net/Rance_King/article/details/105621030)

---

### Conditional Rendering

`react` `js`

Summary:

most common conditional rendering methods:

1. if(!result) return null
2. result && <myComponent />
3. result ? <myComponent />: null

---

### Modern JS tutorial recommended by React

Link:

[js tutorial](https://zh.javascript.info/)

## Week 5

### How to setup wok css with react typescript?

`react` `tailwind`
https://medium.com/quick-code/tailwind-react-typescript-a0317155e5ee

### How to delete a whole line in zsh?

`cli` `shortcut`

> Ctrl + U

---

### How to pass data from child back to parent?

`react`

从课上到现在为止, 我们都是从 parent 通过 props 的形式向 child 传递数据.

例如: **Card** <- title, description, **Clock** <- city

那如何从 child 向 parent 传递数据呢?

主要的 usecase 是, 如果 child component 的 state 有变化, 你想要 parent component 知道.

比如说, _有个 switch 可以切换 Dark/Light mode_, 或者是 _朋友圈里被点赞, 这个信息想要同步到数据库这个动作_.

```javascript
// 通过从parent向child通过props传入一个()=>{}, a callback function

// App.js

<Switch onToggleMode={this.toggleMode}>  //Child, 只是传入reference并没有执行

---------------------------------------------------------------------------
// Switch component里
...

<button onClick={(data) => this.props.onToggleMode(data)}>

// 这里的data, 可以是event, 可以是state, 是所有你想要传回parent里的数据.

```

---

### Remember to stop page refresh when form submit

`react` `form` `preventDefault`

```javascript
const onHandleSubmit(e) => {
    e.preventDefault();
    ...
}

```

---

### How to calculate the current season by location?

`date` `season` `crazy`
https://stackoverflow.com/questions/5670678/javascript-coding-input-a-specific-date-output-the-season/5671172#5671172

### How to use typescript with react?

`typescript` `react`

```
npx create-react-app my-app --template typescript

```

[Typescript Cheetsheet - React Typescript Cheetsheet](https://github.com/typescript-cheatsheets/react-typescript-cheatsheet)

---

### How to set default launching browser in react project?

`npm`

```
"start": "BROWSER=\"Firefox Developer Edition\" react-scripts start"
```

---

### How to format localeDateString and localeTimeString?

`string manipulation`

[LocalTimeString MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleTimeString)

[localDateString MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleDateString)

---

### How to find a string contains another string?

`string manipulation`

```
string.includes(targetString)
```

---

### How to split string with multiple seperators?

`string manipulation` `regex`

https://stackoverflow.com/questions/5993779/use-string-split-with-multiple-delimiters
https://regex101.com/

---

### 5 ways to style a react component

`css` `react`

https://blog.bitsrc.io/5-ways-to-style-react-components-in-2019-30f1ccc2b5b

---

### How to concat JSX fragments?

`jsx` `react`

https://stackoverflow.com/questions/36912179/how-to-concatenate-two-jsx-fragment-or-variables-or-string-and-component-in-rea/49176188

---

### setting 'src' attribute of img in React

`Ollie` `React` `img tag`
in react, the 'src' attribute of <img> tag lose its original effect, which should be replaced as

```html
<img className="card-img" src={require(`${props.img}`)} alt="gift description"></img>
```

(react)
OR

```html
<img id="sku-quit" src={require('../../../images/quit_button.png')}/>
```

(relative location)

### Ensure you have **import** React and **export** the component

`React` `import` `export`

```
import React from 'react';
```

```
export default yourComponent

```

### The React component lifecycle

`Lawrence` `component lifecycle` `codepen`

[The React component lifecycle](https://codepen.io/lawrence415610/pen/abojvRq)

![images](https://user-images.githubusercontent.com/34848993/79633236-935ba600-81a7-11ea-9f89-ba811ee2b1b6.png)

A slideshow for React component lifecycle

- componentDidMount is only load once after the render() function, and we use ajax to load apis in this function

- componentDidUpdate(preProps, prevState) called immediately after the render(), it's a chance for more ajax request

---

### Fetching data in React

`Lawrence` `es6` `api`

Summary:

A brief introduction to fetch data in React

Links:

[promiss usage&details](https://juejin.im/post/5b2a422bf265da59810b677c)

[fetch API MDN](https://developer.mozilla.org/zh-CN/docs/Web/API/Fetch_API)

[fetch data in React Tutorial](https://www.robinwieruch.de/react-fetching-data)

[fetch data using React Hooks](https://www.robinwieruch.de/react-hooks-fetch-data)

[axios](https://github.com/axios/axios)

Example:

`fetch(url).then(/*function*/).then()....catch(e => e)`

---

### js hoisting & closure

`Lawrence` `js` `closure`

Summary: a short and simple explanation about closure and js hoisting

Link: [my personal blog](https://blog.csdn.net/Rance_King/article/details/105621030)
