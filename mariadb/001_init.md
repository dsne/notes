# 시작하기

## 실행여부 확인
- netstat -tap | grep mysql

## mysql 시작, 중지, 재시작
- service mysql start
- service mysql stop
- service mysql restart

## 관리자 비밀번호 변경
- mysqladmin -u root -p password '*새로운 비밀번호*'
- Enter password: *초기 비밀번호 없음, 입력 없이 엔터*

## mysql 접속
- mysql -u*아이디* -p
- Enter password: *비밀번호*

## 사용자 확인
- select user, host from mysql.user;

## database 생성
- create database *데이터베이스 이름*;

## 사용자 추가
- grant usage on *데이터베이스 이름*.* to *사용자 이름*@localhost identified by '*비밀번호*';
- grant all on *데이터베이스 이름*.* to *사용자 이름*@localhost;
- flush privileges;

## 비밀번호 변경
- update mysql.user set password=password*'*새로운 비밀번호*'* where user='*사용자 이름*';

## 외부 접속 권한 추가
- grant all privileges on *데이터베이스 이름*.* to *사용자 이름*@'%' identified by '*비밀번호*';
- flush privileges;

## 익명 유저 삭제
- delete from mysql.user where user='';
