# find command
---

## 전체 조회
~~~
db.getCollection('collection_name').find({})
~~~

## 조건 조회
~~~
db.getCollection('collection_name').find({
  'field_name1': 'value1', 'field_name2': 'value2', ...
})
~~~
~~~
db.getCollection('collection_name').find({
  'field_name1': {
    '$operator': 'value1', ...
  }, ...
})
~~~

## 연산자
- eq, ne: equal, not equal
- in, nin: in, not in
- gt, glt: greater than, grater then or equal
- lt, lte: less then, less then or equal
