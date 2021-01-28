# Operators

## 展开运算符

```javascript
function sum(a, b, c) {
    return a + b + c;
};
let arr = [1, 2, 3];
sum(...ar);

let arr2 = [...arr]; // copy
let arr3 = [...arr, ...arr2]// merge [1, 2, 3, 1, 2, 3]

let book = {
    title: 'vue',
    price: 11
};

let bookDetail = {...book, desc: 'a fine book'};
```
