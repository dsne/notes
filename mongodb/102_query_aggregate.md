# aggregate command
---

## 집계 조회
~~~
db.getCollection('collection_name').aggregate([ ... ])
~~~

## 집계 전체 조회
~~~
db.getCollection('collection_name').aggregation([ {
  $group: {
    _id: '$field_name1', aggregation_field_name: {
      $sum: '$field'
    }
  }
} ])
~~~

## 집계 조건 조회
- count는 $sum: 1로 대체
~~~
db.getCollection('collection_name').aggregation([ {
  $match: {
    $or: [ field_name1: <value> ... ] }
  }, {
    $group: {
      _id: '$field_name2', aggregation_field_name: {
        $sum: '$field'
      }
    }
  }
} ])
~~~
