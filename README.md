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

## 5. 请说明以下程序运行结果

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