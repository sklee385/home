---
layout: default 
---
- file에 세션 저장
- express 용으로 만들어짐 

1. 설치 
    - 설치 확인 
        ```
        npm ls | grep session-file-store
        ```
    - 설치 
        npm install session-file-store --save
2. 기본 세팅
    ```
    var session = require('express-session');
    var FileStore = require('session-file-store')(session);
    
    app.use(session({
        secret: 'keyboard cat',
        resave: false,
        saveUninitialized: true,
        store: new FileStore()
    }));
    ```
    - store 에 옵션을 주고 싶을 경우는 new FileStore(option) 으로 해서     
    option을 json 형식으로 주면 된다. 
3. 사용법
    - 세션 사용방법과 동일
4. 주의 사항
    - session 이라는 파일이 생성