# 날짜 출력
---

## 오늘 날짜
~~~
new Date()
~~~

## 특정 날짜
~~~
new Date('1994-10-04')
~~~

## YYYY-MM-DD
~~~
new Date().toISOString().slice(0,10)
~~~

## YYYYMMDD
~~~
new Date().toISOString().slice(0,10),replace(/-/g,'')
~~~
