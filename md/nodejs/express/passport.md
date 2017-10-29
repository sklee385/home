---
layout: default 
---
## passport
1. 설치 
    - 설치 확인
        ```
        npm ls | grep passport
        ```
    - 설치 
        ```
        npm i passport --save
        ```
        ```
        npm i passport-local --save
        ```
2. 사용법
    ```
    var passport = require('passport')
    , LocalStrategy = require('passport-local').Strategy;

    // session 설정 밑에 추가 
    app.use(passport.initialize());
    app.use(passport.session());
    ```
