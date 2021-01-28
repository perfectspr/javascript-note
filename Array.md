# Array

## 数组解构

```javascript
let arr = [1, 2, 3];
let [a, b, c] = arr;
let [, , c] = arr; // 3
```

默认值

```javascript
let a, b, c;
[a, b, c] = arr; // OK
[a, b, c, d = 0] = arr;
```

嵌套数组解构

```javascript
let categories = ['c', ['vue', 'react'], 'java'];
let [lang1, [, lang2]] = categroies; // lang1=='c' lang2=='react'
```

结合展开运算符

```javascript
let [a, ...others] = arr;
let [...newArr] = arr; // copy array
```
