## 1. 请说明以下程序运行结果

```javascript
var x; 
console.log(x === undefined)
console.log(y === undefined)
```
### Answer A
- A. true, 程序报错Uncaught ReferenceError: y is not defined
- B. true, true
- C. false, false

## 2. 请说明以下程序运行结果

```javascript
var y = 1;
if (function f() {}) {
  y += typeof f;
}
console.log(y);
```
### Answer B
- A. 1
- B. 1undefined
- C. 程序报错