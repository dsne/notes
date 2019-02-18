# 날짜 출력

## 오늘 날짜
~~~java
Date date = Calendar.getInstance().getTime();
~~~

## 특정 날짜
~~~java
date.set(2015, 4 - 1, 12, 11, 14); // 직접 지정
date.setTimeInMillis(1428804862000L); // long타입 대입
~~~

## 문자열 출력
~~~java
System.out.println(new SimpleDateFormat("yyyy-MM-dd HH:mm:ss").format(date));
~~~
