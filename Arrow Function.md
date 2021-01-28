# Arrow Function

```javascript
let w = msg=>msg;
let w = (user, msg)=>`${user}, ${msg}`
let w = ()=>'welcome'
let add = (a, b)=> {
    let c = a + b;
    return c;
}
let e = ()=>{}
let newCar = (color, doors) =>({color, doors})
let person = ({name, age})=>`${name}'s age is ${age}`
```

## Arrow function 和 this

[this - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)

Javascript中的this并不是指对象本身，其指向是根据当前执行上下文的变化而变化的。

- In a method, `this` refers to the **owner object**.
- Alone, `this` refers to the **global object**.
- In a function, `this` refers to the **global object**.
- In a function, in strict mode, `this` is `undefined`.
- In an event, `this` refers to the **element** that received the event.
- Methods like `call()`, and `apply()` can refer `this` to **any object**.
- bind() method

箭头函数和this:

* 箭头函数的this值取决于该函数外部非箭头函数的this值，而且不能通过calls(), apply() and bind()方法来改变this值

* 不能通过new关键字调用

* 没有原型，没有prototype属性

* 不可以改变this的绑定，在函数生命周期内始终保持一致

* 不支持arguments对象。

```javascript

```
