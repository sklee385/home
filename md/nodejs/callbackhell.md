## 콜백헬
- 비동기 코딩을 하다보면 콜백들이 어마어마하게 늘어나게 된다      
- 예를 들어 sql 데이터를 가공해서 다시 sql 처리 하는 데에만 해도 어마어마 하게 늘어나게 된다.
- 이를 콜백헬이라고 한다
- 콜백헬을 보완하기 하기 위해 나온 것을 async 라고 한다.

## async
- https://www.npmjs.com/package/async
- [공식 설명서](https://caolan.github.io/async/)
- [잘 정리 된거](http://proinlab.com/archives/1811)

## 설치
- npm install --save async

## 사용법
1. waterfall 사용     
    ```js
    var async = require('async');
    var fs = require('fs');
    var mysql = require('mysql');

    var tasks = [
        function (callback) {
            console.log(1)
            var result = 'a';
            callback(null, result);
            
        },
        function (data, callback) {
            console.log(2)
            console.log(data)       //  a
            var result = 'b';
            callback(null, result);
            
        },
        function (data, callback) {
            console.log(3)
            console.log(data);      // b
            callback(null)
        }
    ];

    async.waterfall(tasks, function (err) {
        if (err)
            console.log('err');
        else
            console.log('done');
    });
    ```