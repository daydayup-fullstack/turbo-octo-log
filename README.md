# turbo-octo-log
A log for everyday programming challenges

  # Week 6

### use git more efficiently

Summary: 对于使用git add和commit以及提交分支的时机，如果控制得当，可以减少产生conflict的状况，并将操作简化。

1. 不随意进行commit。进行commit的时机是阶段性完成之后，简而言之，commit是为了明确说明自己在这一段里面做了什么。一般写完一些没事用add去添加。
2. 在提交之前切换到develop进行pull，切换回本分支进行commit以及merge操作，这里如果不commit，merge操作执行的结果就是already up to date，并无法提交，这样保证了操作的正确性。把commit留到develop pull之后再做可以极大减少问题的发生。

---

### axios simple tutorial

Link: [极简axios入门和源码分析](https://github.com/zxfjd3g/191121_axios)

---

### Important concepts:

`this ` `arrow function` `scope` `hoist`

summary: 一些容易混淆的基础概念总结。

1. "this" in JavaScript 
 https://zhuanlan.zhihu.com/p/31812336  (比较全面的this用法和特性介绍以及各个情况下的使用)

2. Difference between Arrow Function and other Functions:
 https://blog.csdn.net/github_38851471/article/details/79446722

3. 老师上节课的scope和hoist的总结：
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

1. 单向数据流指的是数据流的流向是单一的，在constructor当中用this.state来定义某些需要操作的属性。当其他方法中对this.state的操作完成之后，不得用this.state.xx=xxx去修改this.state中的项目，而必须要使用this.setState方法将数据流重新导回this.state，这个规定给react component的使用指定了一个方向性。

2. React拥护不可变的数据结构。这意味着，每一个数据在react中都不建议去直接操作并改变它。有一个统一的思路，就是把所有修改数据的操作，统统变成搜集资源->新建数据的操作。如此，es6中的spread运算符几乎就是为这个需求所生的。通过```...```的运算符来利用旧资源创建新资源，这是一个通用思路。

   ---

### React ES6 Tips & Tricks

`react` `es6` `study summary`

Summary: Learn how es6 syntax helps you to write React efficiently

Link:  

[React学习之道](https://leanpub.com/the-road-to-learn-react-chinese/read_full)

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

# Week 5

### How to setup tailwind css with react typescript?
`react` `tailwind`
https://medium.com/quick-code/tailwind-react-typescript-a0317155e5ee

### How to delete a whole line in zsh?
`cli` `shortcut`

> Ctrl + U

---

### How to pass data from child back to parent?
`react`

从课上到现在为止, 我们都是从parent通过props的形式向child传递数据.

例如: **Card** <- title, description, **Clock** <- city

那如何从child向parent传递数据呢?

主要的usecase是, 如果child component的state有变化, 你想要parent component知道. 

比如说, *有个switch可以切换Dark/Light mode*, 或者是 *朋友圈里被点赞, 这个信息想要同步到数据库这个动作*.

``` javascript
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

```fetch(url).then(/*function*/).then()....catch(e => e)```

---

### js hoisting & closure

`Lawrence` `js` `closure`  

Summary: a short and simple explanation about closure and js hoisting  

Link: [my personal blog](https://blog.csdn.net/Rance_King/article/details/105621030)

