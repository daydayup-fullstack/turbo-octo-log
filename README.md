# turbo-octo-log
A log for every day programming challenges

# Week 5
---
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

  # Week 6
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

---

