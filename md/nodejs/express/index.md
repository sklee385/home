---
layout: default 
---
## express
- [post값 받기](bodyParser.html)
- [request](request.html)
- [response](response.html)
- [cookies](cookies.html)
- session 
    - [session 메모리에 저장하는 방법](session.html) :실제로 사용 안함 
    - [session cookie 저장하는 방법](session_cookie.html) : 가장 많이 사용 하는 방법
    - [session 파일에 저장하는 방법](session_file.html) 
    - session DB에 저장하기
        - [mysql](session_mysql.html)
- security 
    - 단방향 암호화(복호화 불가)
        - [md5](security_password_md5.html) : 이 방식을 쓰지 말 것 
        - [sha256](security_password_sha256.html) : salt 를 랜덤하게 주기 힘듬
        - [pdkdf2](security_pdkdf2.html)    : 이 방식을 추천
    - 양방향 암호화(복호화 가능)

-[passport](passport.html)