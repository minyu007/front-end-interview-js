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

## 26. 以下程序运行结果为

```javascript
var a = 1;
function b(){
  var a;
  console.log(a);
  a = 2;
}
```
- A. 1
- B. 2
- C. undefined
- D. 以上都不对

- Answer C

## 27. 以下程序运行结果为

```javascript
var a = 1;
var obj = {
  a: 2,
  getA: function(){
      console.log(this.a)
  }
}
obj.getA()
var _getA = obj.getA()
_getA()
```
- A. 1, 1
- B. 2, 1
- C. 1, 2
- D. 以上都不对

- Answer C

## 29. 以下哪个方法不是javascript Array 的ES6特性

- A. of()
- B. from()
- C. concat()
- D. fill()

- Answer C

## 30. javascript 异步发展史顺序

- A. callback -> promise -> yied/next -> async/await
- B. callback -> yied/next -> promise -> async/await
- C. callback -> async/await -> yied/next -> promise

- Answer 

## 31. 在代码可读性的角度，以下哪一种是解决javascript多层回调的最好方式

- A. callback嵌套
- B. promise
- C. yied/next
- D. async/await

- Answer D

## 32. 在es6环境下解决javascript多个异步请求并发描述正确的是

- A. 使用callback嵌套
- B. 使用promise.all
- C. 使用多层async/await

- Answer B

## 33. 在浏览器环境下，所有js原型链的根节点是什么

- A. null
- B. Object
- C. window
- D. Document

- Answer A

## 34. 关于javascript以下描述错误的是

- A. function都有一个prototype属性
- B. Object都有一个隐藏的__proto__属性
- C. function都有一个隐藏的arguments参数
- D. Array都有一个prototype属性

- Answer D

## 35. 以下哪一种不是es6中的原始数据类型

- A. Symbol
- B. Object
- C. Array
- D. String

- Answer C


## 36. 以下程序运行结果为

```javascript
let s1 = Symbol();
let s2 = Symbol();
console.log(s1 === s2)
let s1 = Symbol('foo');
let s2 = Symbol('foo');
console.log(s1 === s2)
```
- A. false, false
- B. false, true
- C. true, true
- D. 以上都不对

- Answer A

## 37. javascript是单线程语言还是多线程？

- A. 单线程
- B. 多线程

- Answer A

## 38. 关于js中小数计算精度不准确的问题，请给写一个function给出解决方案。

## 39. es6中为什么要引入Symbol类型

## 40 请简单的描述一下javascript闭包

## 41 请简单描述一下javascript中的事件委托，事件委托是通过什么机制实现的

## 42 javascript中那些事件没有冒泡机制，请举例。

## 43 请描述一下angular1.x 与angular2+ 的本质区别

## 44 请描述vue2， react， angular2+ 三个框架的优缺点

## 45 请使用es6的语法对以下两个数组进行，并集，交集，全集操作

```javascript
let arrA = [{a: 1, b: 2}, {c: 3, d: 4}, {e: 5, f: 6}]
let arrA = [{e: 5, f: 6}, {g: 7, h: 8}, {i: 9, j: 10}]
```

## 46 请使用es5的语法对以下两个数组进行，并集，交集，全集操作

```javascript
let arrA = [{a: 1, b: 2}, {c: 3, d: 4}, {e: 5, f: 6}]
let arrA = [{e: 5, f: 6}, {g: 7, h: 8}, {i: 9, j: 10}]
```

## 47 请使用es6的语法操作以下数组, 将3号位复制到0号位

```javascript
let arr = [1, 2, 3, 4, 5]
```
## 48 请使用es5的语法修改以下程序存在的bug

```javascript
var arr = [10, 32, 65, 2];
for (var i = 0; i < arr.length; i++) {
  setTimeout(function() {
    console.log('The index of this number is: ' + i);
  }, 3000);
}
```

## 49 请简单描述redux框架的作用

## 50. 以下程序运行结果为

```javascript
function mul(x) {
  return function(y) {
    return function(z) {
      return function(w) {
        return function(p) {
          return x * y * z * w * p;
        };
      };
    };
  };
}
console.log(mul(2)(3)(4)(5)(6));
```
- A. 720
- B. undefined
- C. Type Error
- D. Reference Error

- Answer A
