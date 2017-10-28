---
layout: default
---
## post 값 받기 
- express 는 기본적으로 post 값을 못 받는다.
- 따라서 모듈을 설치해야 한다.
1. 설치 
    - 설치 확인
        ```
        npm ls | grep body-parser
        ```
    - 설치
        ```
        npm install body-parser --save
        ```
2. 세팅 
    ```
    var bodyParser = require('body-parser');
    var app = express()
    // 
    app.use(bodyParser.json());
    app.use(bodyParser.urlencoded({ extended: false }));
    ```