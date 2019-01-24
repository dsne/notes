# .click()
---

## 기본 형태
~~~js
$('#target').click(function() {
  alert('click')
})
~~~

~~~js
$('#other').click(function() {
  $('#target').click();
})
~~~

## 응용 형태
~~~js
$('#target').on('click', function(event) {
  alert('click')
})
~~~

~~~js
$('#target').on('click', '#target', function(event) {
  alert('click')
})
~~~
