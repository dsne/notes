# 날짜 출력
---

## 오늘 날짜
~~~sql
new Date()
~~~

## 특정 날짜
~~~sql
new Date('1994-10-04')
~~~

## YYYY-MM-DD
~~~sql
new Date().toISOString().slice(0,10)
~~~

## YYYYMMDD
~~~sql
new Date().toISOString().slice(0,10),replace(/-/g,'')
~~~
