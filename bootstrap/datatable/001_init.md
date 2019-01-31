# Bootstrap DataTable 시작

## 기본
~~~js
$(document).ready(() => {
  $('#example').DataTable()
})
~~~

## 속성 설정
~~~js
$(document).ready(() => {
  $('#example').DataTable({
    paging: false,
    ordering: false,
    info: false  
  })
})
~~~
