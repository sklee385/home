---
layout: default 
---
## nodejs install 

### nvm 설치 후 설치 
- [공식 가이드](http://docs.aws.amazon.com/ko_kr/elasticbeanstalk/latest/dg/nodejs-devenv.html)

1. 설치 
    ```
    curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.6/install.sh | bash
    ```
2. nvm 활성화 
    ```
    . ~/.nvm/nvm.sh
    ```
3. 노드 버전에 맞게 설치
    - 최신 버전
        ```
        nvm install --lts
        ```
    - 특정 버전
        ```
        nvm install 8.9.0
        ```
4. node 버전 확인   
    ```
    node --version
    ```
    - 버전 리스트 확인
        ```
        nvm ls
        ```
    - 버전 변경
        ```
        nvm use 8.9.0
        ```
    