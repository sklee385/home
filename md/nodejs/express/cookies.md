---
layout: default
---
## express > cookies 

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
        2. 암호 시간 설정
            ```
            res.cookie("td",1,{
                maxAge : 60*60*1000,    // 한시간 유지
            });
            ```
            - 밀리 세컨드 가 기준
4. 쿠키 암호화
    ```
    app.use(cookieParser('암호화키 입력'));

    // 쿠키 암호화
    app.get('/signedCookies',(req,res)=>{
        // 쿠키 정보 암호화 세팅
        res.cookie("count","1",{
            signed : true
        });
        // 암호화 된 쿠키 확인
        console.log(req.signedCookies)
        res.send("쿠키 암호화");
    });

    ``` 
    1. 쿠키 정보 확인하기
        ```
        console.log(req.signedCookies)
        ```
        - signedCookies 값을 사용해서 확인 가능하다
    2. 쿠키 정보 세팅하기 
        ```
        res.cookie("count","1",{
            signed : true
        });
        ```
        - 옵션 값에 signed : true 를 넣어주면 된다.
        - maxAge 설정을 넣어서 시간 설정 가능
    
