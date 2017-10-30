---
layout: default
---
## ajax 뒤로가기 이슈
- [참고사이트](https://blog.outsider.ne.kr/test1)

1. history/state api 사용
    - [참고사이트](http://firejune.com/1743/HTML5+History%252FState+API%EB%A5%BC+%EC%9D%B4%EC%9A%A9%ED%95%9C+Ajax+%ED%9E%88%EC%8A%A4%ED%86%A0%EB%A6%AC+%EA%B5%AC%ED%98%84)
    - ie10 부터 됨

    ```
    history.pushState(data, data.title, data.url);

    history.state
    ```
