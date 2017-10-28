---
layout: default
---
# express > cookies 

1. 설치 
    - express cookies 설치 되어 있는지 확인 
        ```
        npm ls | grep cookie-parser
        ```
    - 설치가 안되있다면 설치 
        ```
        npm install cookie-parser
        ```
2. 기본 세팅 
    ```
    var express = require('express');
    var app = express();
    // 쿠키정보 세팅
    var cookieParser = require('cookie-parser');
    app.use(cookieParser());
    ```
    - 위 정보 추가
3. 쿠키 기본 사용법

    1. 쿠키 정보 확인 하기 
        ```
        app.get("/cookies",(req,res)=>{
            console.log(req.cookies)
        });
        ```
    2. 쿠키 데이터 세팅하기 
        1. 쿠키 정보 기본 사용
            ```
            app.get("/cookies",(req,res)=>{
                res.cookie("count",1); 
            });
            ```
        2. 옵션 사용
            
    
