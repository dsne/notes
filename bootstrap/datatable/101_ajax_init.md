# AJAX 시작

## 기본
~~~js
$(document).ready(() => {
  $('#example').DataTable({
    ajax: 'data.json'
  })
})
~~~

## 속성 설정
~~~js
$(document).ready(() => {
  $('#example').DataTable({
    ajax: {
      url: `data.json`,
      type: `post`,
      processData: false,
      contentType: false,
      error: (error) => {
        alert(`error: ${error.message}`)
      },
      success: (result) => {
        alert(`success!`)
      }
    }
  })
})
~~~
