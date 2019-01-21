# AJAX 다시 불러오기
---

## reload
~~~
$(document).ready(() => {
  let table = $('#example').DataTable()

  $('#button').click( => {
    table.ajax.url('new_data.json').load();
  })
})
~~~
