# .on()

## 클릭 이벤트
~~~js
$('#target').on('click', function(event) {
  alert('click')
})
~~~

~~~js
$('#other').on('click', '#target', function(event) {
  alert('click')
})
~~~
