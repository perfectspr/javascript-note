# Object

## 属性值简写

```javascript
let name='test', age=10;
let person = {name, age};
```

## 对象方法简写

```javascript
let car = {
    color: 'red',
    showColor() {
        console.log(this.color);
    }
};
// 对象方法简写语法会自动给方法创建name属性
car.showColor.name; // showColor
```

## 可计算的属性名

Vuex中的Action和Mutation的方法名定义可以通过这种方式来写。

```javascript
let suffix = 'name';
let person = {
    ['first' + suffix] : 'san',
    ['last' +  suffix] : 'zhang'
};
// {'first name': 'san', 'last name': 'zhang'}
```

## 对象解构

```javascript
let book = {
    title: 'vue',
    isbn: '123',
    price: 10
};
let {title, isbn, price} = book;
let title, isbn, price;
({title, isbn, price}) = book; // 注意圆括号
{title, isbn, price} = book; // Error!

let {title, isbn, salesVolume=0} = book; // default value
let {title: bookTitle, isbn: bookISBN} = book; // reanme

let {...newBook} = book; // newBook.title='vue'
let {newBook} = book; // newBook==undefined
```

### 嵌套对象解构

```javascript
let book = {
    title: 'vue',
    category: {
        name: 'Web'
    }
};
let {title, category: {name: category}}  = book; //category=='Web'
```

在解构语法中，冒号前面的标识符代表的是对象中的检索位置，其右侧为要被赋值的变量名。如果冒号右侧是花括号，则表示赋予的最终值嵌套在对象内部更深的层次中。
