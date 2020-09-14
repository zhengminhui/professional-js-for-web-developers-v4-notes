# 语言基础

var ：函数作用域，变量提升

let： 块作用域，在作用域中不会被提升。

暂时性死区 temporal dead zone： 在 let 声明之前的执行瞬间被称为“暂时性死区”

let 声明的变量不会成为 window 对象的属性，var 会。

var 在退出循环时，迭代变量保存的是导致循环退出的值

let 会为每个迭代循环声明一个新的迭代变量

```js
for (var i = 0; i < 5; ++i) {
  setTimeout(() => console.log(i), 0);
}
// 你可能以为会输出 0、1、2、3、4
// 实际上会输出 5、5、5、5、5

for (let i = 0; i < 5; ++i) {
  setTimeout(() => console.log(i), 0);
}
// 会输出 0、1、2、3、4
```

const: 无法修改变量的引用，但可以修改引用的内部属性

数据类型：
- 6 种原始类型
    * Undefined， 
    * Null ，
    * Number，
    * String，
    * Boolean，
    * Symbol

- 复杂数据类型
    * Object

typeof

typeof null 返回 object， null 被认为是一个对空对象的引用

通过 typeof 来区分函数 和其他对象， ‘function’ 表示值为函数
