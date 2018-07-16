## 1. 请说明以下程序运行结果

```javascript
var x; 
console.log(x === undefined)
console.log(y === undefined)
```

- A. true, 程序报错Uncaught ReferenceError: y is not defined
- B. true, true
- C. false, false

- Answer A

## 2. 请说明以下程序运行结果

```javascript
var y = 1;
if (function f() {}) {
  y += typeof f;
}
console.log(y);
```
- A. 1
- B. 1undefined
- C. 程序报错

- Answer B

## 3. 以下哪种方式能够清空一个数组

```javascript
var arrayList =  ['a', 'b', 'c', 'd', 'e', 'f'];
```
- A. arrayList = [];
- B. arrayList.length = 0;
- C. arrayList.splice(0, arrayList.length);
- D. 以上全部都对

- Answer D

## 4. 请说明以下程序运行结果

```javascript
var output = (function(x) {
  delete x;
  return x;
})(0);
console.log(output);
```
- A. 0
- B. 1
- C. undefined

- Answer A

## 5. 请说明以下程序运行结果

```javascript
var x = 1;
var output = (function() {
  delete x;
  return x;
})();

console.log(output);
```
- A. 0
- B. 1
- C. undefined

- Answer B

## 6. 请说明以下程序运行结果

```javascript
var x = { foo : 1};
var output = (function() {
  delete x.foo;
  return x.foo;
})();

console.log(output);
```
- A. 0
- B. 1
- C. undefined

- Answer C


## 7. 请说明以下程序运行结果

```javascript
var Employee = {
  company: 'xyz'
}
var emp1 = Object.create(Employee);
delete emp1.company
console.log(emp1.company);
```
- A. xyz
- B. ''
- C. undefined

- Answer A

## 8. 请说明以下程序运行结果

```javascript
var trees = ["xyz", "xxxx", "test", "ryan", "apple"];
delete trees[3];
console.log(trees.length);
```
- A. 3
- B. 4
- C. 5

- Answer C


## 9. 请说明以下程序运行结果

```javascript
var bar = true;
console.log(bar + 0);   
console.log(bar + "xyz");  
console.log(bar + true);  
console.log(bar + false);
```
- A. 1, truexyz, 2, 1
- B. 0, truexyz, truetrue, truefalse
- C. true0, truexyz, truetrue, truefalse

- Answer A

## 10. 下面符合一个有效的javascript变量定义规则的是？

- A. _$a1$_
- B. with
- C. a bc
- D. 2a

- Answer A

## 11. 下面有关javascript系统方法的描述，错误的是？

- A. parseFloat方法：该方法将一个字符串转换成对应的小数
- B. isNaN方法：该方法用于检测参数是否为数值型，如果是，返回true，否则，返回false。
- C. escape方法： 该方法返回对一个字符串编码后的结果字符串
- D. eval方法：该方法将某个参数字符串作为一个JavaScript执行

- Answer C

## 12. 下面有关JavaScript中 call和apply的描述，错误的是？

- A. call与apply都属于Function.prototype的一个方法，所以每个function实例都有call、apply属性
- B. 两者传递的参数不同，call函数第一个参数都是要传入给当前对象的对象，apply不是
- C. apply传入的是一个参数数组，也就是将多个参数组合成为一个数组传入
- D. call传入的则是直接的参数列表。call 方法可将一个函数的对象上下文从初始的上下文改变为由 thisObj 指定的新对象。

- Answer 

## 13. 请说明以下程序运行结果

```javascript
console.log(0.1 + 0.2 == 0.3)
```
- A. false
- B. true

- Answer A


## 14. 请说明以下程序运行结果

```javascript
console.log(false == '0')
console.log(false === '0')
```
- A. true, false
- B. true, true
- C. false, false

- Answer A

## 15. 请说明以下程序运行结果

```javascript
var a={},
    b={key:'b'},
    c={key:'c'};

a[b]=123;
a[c]=456;

console.log(a[b]);
```
- A. 123
- B. 456
- C. 123456

- Answer B

## 16. 请说明以下程序运行结果

```javascript
var length = 10;
function fn() {
	console.log(this.length);
}

var obj = {
  length: 5,
  method: function(fn) {
    fn();
    arguments[0]();
  }
};

obj.method(fn, 1);
```
- A. 10, 5
- B. 10, 1
- C. 10, 2

- Answer C

## 17. 请说明以下程序运行结果

```javascript
(function () {
    try {
        throw new Error();
    } catch (x) {
        var x = 1, y = 2;
        console.log(x);
    }
    console.log(x);
    console.log(y);
})();
```
- A. 1, 2
- B. 1, undefined, 2
- C. 程序报错

- Answer B

## 18. 请说明以下程序运行结果

```javascript
for (let i = 0; i < 5; i++) {
  setTimeout(function() { console.log(i); }, i * 1000 );
}
```
- A. 0, 1, 2, 3, 4
- B. 5, 5, 5, 5, 5
- C. 程序报错

- Answer A

## 19. 请说明以下程序运行结果

```javascript
for (var i = 0; i < 5; i++) {
  setTimeout(function() { console.log(i); }, i * 1000 );
}
```
- A. 0, 1, 2, 3, 4
- B. 5, 5, 5, 5, 5
- C. 程序报错

- Answer B

## 20. 请说明以下程序运行结果

```javascript
console.log(1 < 2 < 3);
console.log(3 > 2 > 1);
```
- A. true, false
- B. true, true
- C. false, true
- D. false, false

- Answer A


## 21. 请说明以下程序运行结果

```javascript

var start = new Date(); 
var end = 0; 
setTimeout(function() { 
	console.log(new Date() - start); 
}, 500); 
while (new Date() - start <= 1000) {}
```
- A. 500
- B. 1004
- C. 1000
- D. 以上都不正确

- Answer DD

## 22. 请说明以下程序运行结果

```javascript
setTimeout(() => console.log(1));
setImmediate(() => console.log(2));
process.nextTick(() => console.log(3));
Promise.resolve().then(() => console.log(4));
(() => console.log(5))();
```
- A. 5, 4, 3, 1, 2
- B. 3, 4, 5, 2, 1
- C. 5, 3, 4, 1, 2
- D. 3, 5, 1, 4, 2

- Answer C

## 23. 关于javascript 基本类型正确的是

- A. string, number, undefined, null, boolean
- B. string, number, null, boolean, array
- C. string, number, undefined, boolean, object
- D. string, number, NaN, null, boolean

- Answer A

## 24. 关于javascript 方法调用以下说法正确的是

- A. javascript是传引用调用
- B. javascript 方法都有 arguments 参数
- C. 关于javascript传参，如果参数是数组类型则是传引用调用，否则为传值调用
- D. 关于javascript传参，如果参数是Object类型则是传引用调用，否则为传值调用

- Answer A


## 25. 以下哪些不是ES6 stage-1的新特性

- A. const, let 定义常量及变量
- B. Promise
- C. 箭头函数
- D. async/await处理异步

- Answer A