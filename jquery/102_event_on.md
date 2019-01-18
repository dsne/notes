# .on()
---

## 클릭 이벤트
~~~
$('#target').on('click', function(event) {
  alert('click')
})
~~~

~~~
$('#other').on('click', '#target', function(event) {
  alert('click')
})
~~~
