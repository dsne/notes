# .click()
---

## 기본 형태
~~~
$('#target').click(function() {
  alert('click')
})
~~~

~~~
$('#other').click(function() {
  $('#target').click();
})
~~~

## 응용 형태
~~~
$('#target').on('click', function(event) {
  alert('click')
})
~~~

~~~
$('#target').on('click', '#target', function(event) {
  alert('click')
})
~~~
