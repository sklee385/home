---
layout: default
---
## date issu    
```js
var test = function (month){
    var date = new Date();
    date.setFullYear('1999');
    date.setMonth(parseInt(month)-1);
    date.setDate(1)
    return date.getMonth()+1;
}
console.log("1월” ",test(1));       // 1
console.log("2월” ",test(2));       // 3
console.log("3월” ",test(3));       // 3
```

2월 일 경우 문제가 생긴다     
그 이유는 날짜를 설정을 안하면 디폴트 값이 30인데   
2월은 30일이 없다     

이럴때는 일을 먼저 설정하고 월을 설정 하면 된다.        
```js
var test = function (month){
    var date = new Date();
    date.setFullYear('1999');
    date.setDate(1)
    date.setMonth(parseInt(month)-1);
    return date.getMonth()+1;
}
console.log("1월” ",test(1));       // 1
console.log("2월” ",test(2));       // 2
console.log("3월” ",test(3));       // 3
```
