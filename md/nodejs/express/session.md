---
layout: default
---
## express > session 
- 서버 메모리에 데이터가 저장된다
- 잘 못 사용할 경우 메모리 누수된다.

1. npm 설치
    - 설치 확인 
        ```
        npm ls | grep express-session
        ```
    - 설치 
        ```
        npm install express-session --save 
        ```

2. 기본 세팅
    ```
    var session = require('express-session');
    app.use(session({
        secret: '암호키값',
        resave: false,
        saveUninitialized: true
    }));
    ```
3. 사용법
    ```
    res.session.a = 1;
    console.log(res.session.a);
    ```


