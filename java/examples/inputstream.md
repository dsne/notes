# inputstream

## parsing
~~~java
InputStream input = channel.getInputStream();
ByteArrayOutputStream baos = new ByteArrayOutputStream();
String result;

int length;
byte[] buffer = new byte[1024];
while ((length = input.read(buffer, 0, buffer.length)) != -1)
  baos.write(buffer, 0, length);

result = new String(baos.toByteArray(), "UTF-8");
System.out.println(result);
~~~
