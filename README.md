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
