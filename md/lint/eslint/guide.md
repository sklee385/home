---
layout: default
---
## eslint 
- [참조사이트](https://github.com/eslint/eslint)
- 로컬 설치 및 사용
    - 설치
        - npm i -S eslint 
    - .eslintrc.js
        - ./node_modules/.bin/eslint --init
    - 실행 
        - ./node_modules/.bin/eslint yourfile.js
- 전역 설치 및 사용
    - 설치 
        - npm i -g eslint
    - .eslintrc.js
        - eslint --init
    - 실행 
        - eslint yourfile.js
    

- .eslintrc.js

    - init 으로 만들면 다음과 같은 코드가 만들어 진다.

    ```
    module.exports = {
        "env": {
            "browser": true
        },
        "extends": "eslint:recommended",
        "rules": {
            // 탭에는 공백 설정 
            "indent": [
                "error",
                "tab"
            ],
            // 
            "linebreak-style": [
                "error",
                "unix"
            ],
            // 문자열에 쌍따움표 사용
            "quotes": [
                "error",
                "double"
            ],
            // 마지막에 세미콜론 필요
            "semi": [
                "error",
                "always"
            ]
        }
    };
    ```
    - env
    - extends
    - rules
        - "quotes", "semi" 등은 룰 규칙이다. 
        - 첫번째 값은 3가지중 하나의 값이 들어간다 
            1. "off" 또는 0 : 규칙을 해제
            2. "warn" 또는 1 : 경고로 사용
            3. "error" 또는 2 : 오류로 사용
        - [가이드 - 영어](https://eslint.org/docs/user-guide/configuring) 
        - [가이드 - 한글](https://firejune.com/1794)
            - 대신 이것은 rules 로 검색해서 옵션을 넣는 방식으로 써야 할 듯

