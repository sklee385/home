---
layout: default
---
## express request
- 값을 받을 때 사용

1. 자주 쓰는 기능
    - req.body
        - body-parser 설치후 사용 가능
        - post 값 확인 할 때 사용
    - req.query
        - url 뒤 ? 뒤에 들어가는 쿼리값 확인할 떄 사용
    - res.cookie
        - cookie-parser 설치 후 사용 가능
        - cookie 값 확인 시 사용
    - req.signedCookies
        - cookie-parser 설치 후 사용 가능
        - 암호화된 쿠키값 확인 시 사용
    
