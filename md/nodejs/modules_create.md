## 모듈 만들기
```
// cicle.js
var PI = Math.PI;

exports.area = function (r) {
    return PI * r * r;
};

exports.circumference = function (r) {
    return 2 * PI * r;
};
```
```
// foo.js
var circle = require('./circle.js');
console.log( 'The area of a circle of radius 4 is '   + circle.area(4));
```
