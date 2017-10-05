## nodejs 설치
- window
    1. https://nodejs.org/ko/ 에서 다운
    2. 클릭해서 설치

- linux
    + 다운 받아 설치
        1. cd /usr/local
        2. 다운로드
            wget https://nodejs.org/dist/v8.1.4/node-v8.1.4-linux-x6
        3. 압축해제
            tar xvf node-v8.1.4-linux-x64.tar.xz
        4. 심볼릭 링크 생성
            ln -s
        5. cd node/bin
        6. 현재 위치 출력 및 복사
            pwd
        7. profile 열기
            vi /etc/profile
            ```
            #nodejs
            export NODE_HOME=/usr/local/node
            export PATH=$PATH:$NODE_HOME/bin
            ```
        8. profile 변경 내용 저장
            source /etc/profile
        9. 제대로 됐는지 확인
            node -v

    + nvm 을 이용한 설치
        1. yum install -y git
        2. git clone git://github.com/creationix/nvm.git ~/.nvm
        3. source ~/.nvm/nvm.sh
        4. nvm install 8.3.0
            nodejs 8.3 버전 설치

## nodejs 기본 세팅 명령어
- express 생성기
    npm install express-generator -g
- pm2
    npm install -g pm2
- 디버깅 툴
    npm install -g node-inspector

## express 세팅
- express --view=ejs express
    