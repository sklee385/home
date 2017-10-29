---
layout: default
---
## express response 
- 데이터를 넘겨줄 떄 사용

1. 자주 사용 하는 기능들
    - res.redirect
        - url 이동시 사용
    - res.send('')
        - 화면에 값을 출력 할 때 사용
    - res.cookie('key','value',{})
        - cookie-parser 설치 후 사용 가능
        - 쿠키 값을 세팅 할 때 사용
        - 3번 째 파라미터는 옵션 값(생략 가능)
            ```
            {
                signed : true,          // 암호화 해서 넘김
                maxAge : 1000*60        // 쿠키 유지 시간 기본 단위는 밀리 세컨드
            }
            ```
