---
layout: default
---
- 사용자 쿠키에 데이터가 쌓여서 변조 위험이 있다.
- 암호화 되긴 하지만 주의 해야 함

1. 설치
    - 설치 확인 
        ```
        npm ls | grep cookie-session
        ```
    - 설치
        ```
        npm install cookie-session --save
        ```
2. 기본 세팅
    ```
    var cookieParser = require('cookie-parser');
    var cookieSession = require('cookie-session');

    app.use(cookieParser());
    app.use(cookieSession({secret:'암호키asdfasdf'}))    
    ```
3. 사용법 
    - 기존 session 과 동일



