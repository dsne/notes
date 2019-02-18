# array와 stringlist 변환

## array to stringlist
~~~java
List<String> list = new ArrayList<>();
String[] array = list.toArray(new String[list.size()];
~~~

## stringlist to array
~~~java
String[] array = list.toArray(new String[list.size()];
List<String> list = new ArrayList<>(Arrays.asList(array);
~~~
