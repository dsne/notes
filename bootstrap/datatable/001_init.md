# Bootstrap DataTable 시작
---

## 기본
~~~
$(document).ready(() => {
  $('#example').DataTable()
})
~~~

## 속성 설정
~~~
$(document).ready(() => {
  $('#example').DataTable({
    paging: false,
    ordering: false,
    info: false  
  })
})
~~~
