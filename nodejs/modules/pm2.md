# pm2

## 개요
- 프로세스 관리자
- 로드 밸런싱 기능 제공

## 설치
- npm i pm2 -g

## 시작
- 기본 형태
  - pm2 start *app.js*
- 이름 지정
  - pm2 start *app.js* -n '*server*'
  - pm2 start *app.js* --name '*server*'
- 코드 변경시 자동 재실행
  - pm2 start *app.js* --watch
- 코드 변경시 자동 재실행 제외
  - pm2 start *app.js* --watch --ignore-watch='*public*'
- 클러스터 모드
  - 실행할 인스턴스 개수 지정, 0 지정시 cpu 개수만큼 실행
  - pm2 start *app.js -i *0*

## 처리
- pm2 stop *server*
- pm2 start *server*
- pm2 restart *server*

## 재실행
- pm2 reload *server*

## 삭제
- pm2 delete *server*
- pm2 kill

## 관리
- 목록 확인
  - pm2 list
- 모니터링
  - pm2 monit
- 로그 확인
  - pm2 log

## 시스템 시작 시 자동 재시작
- linux
  - pm2 start app.js
  - pm2 startup
  - 출력 스크립트 실행
  - pm2 save
- windows
  - npm install pm2-windows-startup -g
  - pm2 start app.js
  - pm2-startup install
  - pm2 save
