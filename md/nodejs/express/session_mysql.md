---
layout: default
---
## express session mysql

1. 설치 
    - 설치 확인 
        ```
        npm ls | grep express-mysql-session
        ```
    - 설치 
        ```
        npm install express-mysql-session --save
        ```
2. 기본 세팅 
    ```
    var express = require('express');
    var app = module.exports = express();
    var session = require('express-session');
    var MySQLStore = require('express-mysql-session')(session);
    
    var options = {
        host: 'localhost',
        port: 3306,
        user: 'session_test',
        password: 'password',
        database: 'session_test'
    };
    
    var sessionStore = new MySQLStore(options);
    
    app.use(session({
        key: 'session_cookie_name',
        secret: 'session_cookie_secret',
        store: sessionStore,
        resave: false,
        saveUninitialized: false
    }));
    ```
    - file 과는 틀리게 반드시 option 정보를 넣어줘야 한다.
    - sessions 라는 테이블에 정보가 쌓인다.
3. 사용법
    - 기존 session 과 사용법이 동일 
4. 주의 사항 
    - DB 서버를 이용 하는 것이 때문에 저장하는데 시간이 걸려서 redirect 할 경우 문제가 될 소지가 있다 
        ```
        // 저장이 완료 된 후 실행
        // DB를 사용 할 경우 문제가 소지가 있기 때문에(저장 시간 등...) 저장이 완료 된 후 리다이렉트
        req.session.save(()=>{
            res.redirect("/welcome");
        })
        ```
        