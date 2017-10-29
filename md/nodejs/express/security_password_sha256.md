---
layout: default 
---
## security sha256 
- md5를 개선 해서 나온 방식
- 단방향 암호화 방식 (복호화 불가)

1. 설치 
    - 설치 확인 
        ```
        npm ls | grep sha256
        ```
    - 설치 
        ```
        npm install sha256 --save
        ```
2. 사용법
    ```
    var sha256 = require('sha256')
    console.log(sha256('javascript'))
    ```
3. 유의 사항    
    sha256 같은 경우는 문자가 들어가면 항상 같은 문자가 나온다         
    그래서 일반적으로 쓰는 문자들을 저장 시켜 놓고 하는 복호화하는 경우가 있어서     
    그대로 쓰기 어렵다 
    ```
    var sha256 = require('sha256')
    var salt = "^%$^#$@113244fkjsdfi";
    var password = 'javascript';
    console.log(sha256(password + salt))_
    ```

    이런식으로 일반적으로 쓰는 문자가 아니게 만들어야 한다

    이래도 문제가 하나 생긴다      
    만약 비밀번호가 똑같은 사람이 한명 더 있다면   
    두사람의 값은 같게 된다       
    한사람이 뚫리게 된다면 비밀번호가 같은 사람은 다 뚤리게 되는 것이다.     
    이를 방지 하기 위해서는 salt 값을 회원 마다 다르게 적용 하는 방도가 있다 
