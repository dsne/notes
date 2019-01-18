# multer
---

## 설치
~~~
npm i -s multer
~~~

## include
~~~
const multer = require('multer')
~~~

## init
~~~
const upload = multer({
  dest: '/uploads',
  limits: {
    fileSize: 10 * 1024 * 1024   // 10mb
  }  
})
~~~
- dest: 저장경로
- limits: 용량제한

## 적용
~~~
app.post('/', upload.any(), (req, res) => {
  console.log(req.body)
  console.log(req.files)
})
~~~
