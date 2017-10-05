# pm2 
- 자동 멀티 쓰레드 지원
- 소스 수정시 자동 reload 지원

## 설치
- npm install -g pm2

## 기본 사용법
- pm2 start app.js
    시작 명령
- pm2 list
    현재 동작중인 리스트 출력
- pm2 stop id
    id 값의 어플리케이션을 중단
    list에는 목록이 나옴
    전체 멈추는 것
    pm2 stop all

- pm2 delete id
    id 값의 어플리케이션 삭제
    list 목록에도 나오지 않음
    전체 지우는 것
    pm2 delete all

## 개발 모드
- pm2-dev app.js

## 멀티쓰레드 cluster
- https://keymetrics.io/2015/03/26/pm2-clustering-made-easy/
- pm2 start app.js -i 2
    2개의 싱글 쓰레드를 띄움
- pm2 scale app +2
    2개 더 싱글 쓰레드를 띄움
- pm2 scale app 2
    싱글 쓰레드를 2개로 변경
- 코어 갯수가 몇개인지 모를경우
    pm2 start app -i 0
    코어 갯수 만큼 출력