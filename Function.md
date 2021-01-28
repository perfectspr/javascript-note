# Function

## 默认参数

Java，C++，Python等语言要求默认参数只能在参数列表的最右侧。而在ES6中，默认参数可以在任意位置。

```javascript
function redirect(url='/home', timeout=2000, callback) {
    // ...
}
redirect(); // url 和 timeout使用默认值
redirect(undefined, undefined, ()=>{}); // url和timeout用默认值
redirect('/login'); // timeout用默认值
redirect('login', null, ()=>{}); // timeout === null
```

## Rest参数

在Javascript中，无论在函数定义中声明了多少形参，都可以传入任意数量的实参，在函数内部可以通过arguments对象来接收传入的参数。

```javascript
function caculate(op) {
    if(op === '+') {
        let result = 0;
        for(let i=0; i<arguments.length; i++) {
            result += arguments[i]
        }
        return result;
    } else if (op === '*') {
        let result = 0;
        for(let i=0; i<arguments.length; i++) {
            result *= arguments[i]
        }
        return result;
    }
}
```

不足之处:

* 调用者无法知道该函数是不是可以接受任意数量的参数

* 第一个参数是命名参数，所以遍历arguments时要从1开始

ES6引入了rest参数解决这个问题.

每个函数最多只能声明一个rest参数，而且它只能是最后一个参数。

```javascript
function caculate(op, ...data) {
    if(op === '+') {
        let result = 0;
        for(let i=0; i<data.length; i++) {
            result += data[i]
        }
        return result;
    } else if (op === '*') {
        let result = 0;
        for(let i=0; i<data.length; i++) {
            result *= data[i]
        }
        return result;
    }
}
```
