# turbo-octo-log
A log for every day programming challenges

# Week 5
---
`Ollie` `React` `img tag`
in react, the 'src' attribute of <img> tag lose its original effect, which should be replaced as 
```<img className="card-img" src={require(`${props.img}`)} alt="gift description"></img>``` (in react) 
OR```<img id="sku-quit" src={require('../../../images/quit_button.png')}/>```(relative location)
---
### The React component lifecycle
`Lawrence` `component lifecycle` `codepen`  

[The React component lifecycle](https://codepen.io/lawrence415610/pen/abojvRq)  

![images](https://user-images.githubusercontent.com/34848993/79633236-935ba600-81a7-11ea-9f89-ba811ee2b1b6.png)

A slideshow for React component lifecycle
- componentDidMount is only load once after the render() function, and we use ajax to load apis in this function
- componentDidUpdate(preProps, prevState) called immediately after the render(), it's a chance for more ajax request

### Fetching data in React

`Lawrence` `es6` `api`   

Links:  

[promiss usage&details](https://juejin.im/post/5b2a422bf265da59810b677c)  

[fetch API MDN](https://developer.mozilla.org/zh-CN/docs/Web/API/Fetch_API)  

[fetch data in React Tutorial](https://www.robinwieruch.de/react-fetching-data)  

[fetch data using React Hooks](https://www.robinwieruch.de/react-hooks-fetch-data)  

[axios](https://github.com/axios/axios)  

Summary:  

- Simple usage of fetch API:  

```fetch(url).then(/*function*/).then()....catch(e => e)```

### js hoisting & closure

`Lawrence` `js` `closure`  

Summary:

- rule1（变量提升）: 在es5, 所有变量和函数被**定义**时都会被提升到其所处的函数的同级作用域 (简单理解block scope 就是比 function低一个等级的作用域，block scope是{}里面的作用域, 而function scope是与该函数同等级的作用域，也就是指该函数在哪个作用域，被提升的变量和function也会在此同一个作用域).

- rule2（作用域链）: 未被赋值的变量会沿着作用域链向上寻找，直到找到最下一级被赋值的同名变量

- rule3 （闭包closure) : 闭包描述的是函数b作为函数a的返回值被返回的状态，这个函数返回函数的状态即闭包。

  ```javascript
  function a () {
  	return function b (){ }
  }
  ```
  

- 推论：在闭包的b函数中使用的var变量，可以被a函数中定义的同名变量所控制

  ```javascript
  function makeFuncs (){
      const funcs = [];
      for(var i=0,len=3;i<len;i++){
          funcs[i] = function(){
              console.log(`func ${i}`);
          }
      }
      return funcs
  }
  
  const functions = makeFuncs()
  for(var j=0,len=3;j<len;j++){
      functions[j]();
  }
  ```

  如上图示例，输出的结果是三次“func 3”。

  1. 因为变量i被var定义，所以，其会遵循rule1，作用域在函数执行时会被提升到函数作用域顶端，此时变量i的作用范围是makeFuncs；
  2. 在makeFuncs执行时，循环制造了三个函数，这三个函数中都有一个变量为i，此时被这个循环制造出的函数funcs[0], funcs[1], funcs[2] 尚未被执行，其执行体代码中皆有一个i，这个i因为未被执行所以尚且未被赋值，当其随后被执行时，其将会遵循之前的rule2在作用域链上溯，寻找作用域链上层的同名变量。
  3. 此时，makeFuncs此函数作用域范围内，i已经通过叠加至3（由此可以看出循环执行的逻辑，即便到达终点，i++仍然会再执行一次）,这个i的值成为了funcs[0], funcs[1], funcs[2] 中的变量，为3。

  这个示例展示的是一种误用情况下，闭包状态中，上层函数变量对下层函数变量进行影响的情况。

  闭包可以方便我们在上层函数中设置不可被外界访问的变量，并在下层函数中体现出来。比如：

  ```javascript
  function a(){
      let i = 0;
      return function b(){ console.log(i)};
  }
  a()();
  ```

  如上示例，其他的用户能够打印i，但是i这个变量不能够从函数a外传入，别的用户只能执行函数a返回的函数b。这也意味着，别的用户无法对变量i进行修改。简而言之，只有拿到了整个函数a的函数体的人才能够修改变量i，这样就设计了一种修改权限。可以想象在很多实际状况中，我们希望把一个函数给其他地方调用，但同时保留只有在一个地方才能调整的变量。
