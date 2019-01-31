# 스케쥴러

## 환경변수 조회
- show variables like 'event%';

## 환경변수 활성화
- SET GLOBAL event_scheduler = ON;
- SET @@global.event_scheduler = ON;
- SET GLOBAL event_scheduler = 1;
- SET @@global.event_scheduler = 1;

## 목록조회
~~~sql
select event_schema
     , event_name
     , interval_field
  from information_schema.event;
~~~
