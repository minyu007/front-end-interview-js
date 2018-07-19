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

## 12. ES6中的箭头函数与普通function区别描述错误的是

- A. 函数体内的this对象，就是定义时所在的对象，而不是使用时所在的对象。
- B. 不可以当作构造函数，不可以使用new命令，否则会抛出一个错误。
- C. 不可以使用arguments对象，该对象在函数体内不存在。
- D. 可以使用yield命令，用作 Generator 函数。

- Answer D

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

## 22. Node环境下请说明以下程序运行结果

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
- B. javascript 函数都有隐藏的 arguments 参数
- C. 关于javascript传参，如果参数是数组类型则是传引用调用，否则为传值调用
- D. 关于javascript传参，如果参数是Object类型则是传引用调用，否则为传值调用

- Answer A


## 25. 以下哪一项属于ES6 stage-3的特性

- A. const, let 定义常量及变量
- B. Promise
- C. 箭头函数
- D. async/await处理异步

- Answer D

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

- Answer B

## 29. 以下哪个方法不属于ES6 Array 的新加入的。

- A. of()
- B. from()
- C. concat()
- D. fill()

- Answer C

## 30. javascript 异步发展史顺序

- A. callback -> promise -> generator(yied/next) -> async/await
- B. callback -> generator(yied/next) -> promise -> async/await
- C. callback -> async/await -> generator(yied/next) -> promise
- C. callback -> generator(yied/next) -> async/await -> promise
- Answer A

## 31. ES6环境，在代码可读性的角度，以下哪一种是解决javascript多层异步回调的最好方式

- A. callback嵌套
- B. promise
- C. generator(yied/next)
- D. async/await

- Answer D

## 32. 在ES6环境下解决javascript多个异步请求并发描述正确的是

- A. 使用callback嵌套
- B. 使用promise.all
- C. 使用多层async/await

- Answer B

## 33. 在浏览器环境下，javascript原型链的根节点是什么

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
let arrB = [{e: 5, f: 6}, {g: 7, h: 8}, {i: 9, j: 10}]
```

## 46 请使用es5的语法对以下两个数组进行，并集，交集，全集操作

```javascript
var arrA = [{a: 1, b: 2}, {c: 3, d: 4}, {e: 5, f: 6}]
var arrB = [{e: 5, f: 6}, {g: 7, h: 8}, {i: 9, j: 10}]
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

## 51. 以下程序运行结果为

```javascript
(function() {
  console.log(typeof displayFunc);
  var displayFunc = function(){
    console.log("Hi I am inside displayFunc");
  }
}());
```
- A. function
- B. undefined
- C. 'Hi I am inside displayFunc'
- D. ReferenceError: displayFunc is not defined

- Answer B

## 52. 以下程序运行结果为

```javascript
(function() {
  var array = new Array('100');
  console.log(array);
  console.log(array.length);
}());
```
- A. [undefined × 100] 100
- B. undefined undefined
- C. ["100"] 1
- D. ReferenceError: array is not defined

- Answer C

## 53. 以下程序运行结果为

```javascript
(function() {
  var array1 = [];
  var array2 = new Array(100);
  var array3 = new Array(['1',2,'3',4,5.6]);
  console.log(array1);
  console.log(array2);
  console.log(array3);
  console.log(array3.length);
}());
```
- A. [] [] [Array[5]] 1
- B. [] [undefined × 100] Array[5] 5
- C. [] [] ['1',2,'3',4,5.6] 5
- D. [] [] [Array[5]] 5

- Answer A

## 54. 请描述react的组件生命周期钩子方法与作用。
## 55. 请描述Vue2的组件生命周期钩子方法与作用。

## 56. 关于javascript中的setTimeout(function, timer)方法第二个时间参数描述错误的是

- A. timer是可选参数
- B. 如果timer设置为0，这该function会变为同步方法立即执行
- C. timer值在不同浏览器环境下有不同的上限
- D. function不一定会在设置的timer时间结束后执行。

## 57. 为什么在query中可以使用链式调用，比如$( "div" ).css( "width", "300px" ).add( "p" ).css( "background-color", "blue" );

## 58. 以下程序运行结果为:

```javascript
function a(){
  return
  {
    message: 'hello'
  }
}
a()
```
- A. undefined
- B. {message: 'hello'}
- C. Uncaught TypeError
- D. {}

- Answer A

## 59. 以下程序运行结果为:
```javascript
function foo() {
  return () => {
    return () => {
      return () => {
        console.log('id:', this.id);
      };
    };
  };
}
var f = foo.call({id: 1});
var t1 = f.call({id: 2})()(); 
var t2 = f().call({id: 3})(); 
var t3 = f()().call({id: 4}); 
```

- A. id: 1, id: 1, id: 1
- B. id: 2, id: 3, id: 4
- C. id: 1, id: 2, id: 3
- D. 以上都不正确

- Answer A

## 60.请说明下ES6中的双冒号运算符，以及他的作用。

## 61. ES5中相等运算符（==）和严格相等运算符（===）描述错误的是

- A. ==会自动转换数据类型
- B. NaN === NaN 返回false
- C. -0 === +0 返回ture
- D. null === null 返回false

- Answer D

## 62. 请简单描述一下react与vue2中所使用的vDom内部原理。

## 63. 以下关于ES6 声明变量的方式描述正确的是

- A. var命令和function命令
- B. let和const命令
- C. import命令和class命令
- D. 以上都正确

- Answer D

## 64. 关于rxjs你了解多少

- A. 听过
- B. 简单使用过
- C. 精通
- D. 精通并熟悉原理

- Answer D

## 65. 以下关于ES5 顶级对象描述正确的是

- A. 浏览器里面，顶层对象是window，但 Node 和 Web Worker 没有window
- B. 浏览器和 Web Worker 里面，self也指向顶层对象，但是 Node 没有self
- C. Node 里面，顶层对象是global，但其他环境都不支持。
- D. 以上都正确

- Answer D

