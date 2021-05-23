
![img.png](img.png)

# 生成Stream流的方式
### Collection体系集合
使用默认方法stream()生成流， default Stream stream()
### Map体系集合
把Map转成Set集合，间接的生成流
### 数组
通过Stream接口的静态方法of(T... values)生成流


### ways
方法名 说明  
#### Stream filter(Predicate predicate) 用于对流中的数据进行过滤
#### Stream limit(long maxSize) 返回此流中的元素组成的流，截取前指定参数个数的数据
#### Stream skip(long n) 跳过指定参数个数的数据，返回由该流的剩余元素组成的流
#### static Stream concat(Stream a, Stream b) 合并a和b两个流为一个流
#### Stream distinct() 返回由该流的不同元素（根据Object.equals(Object) ）组成的流
#### Stream sorted() 返回由此流的元素组成的流，根据自然顺序排序
#### Stream sorted(Comparator comparator) 返回由该流的元素组成的流，根据提供的Comparator进行排序
#### Stream map(Function mapper) 返回由给定函数应用于此流的元素的结果组成的流
#### IntStream mapToInt(ToIntFunctionmapper)  返回一个IntStream其中包含将给定函数应用于此流的元素的结果

## Stream流终结操作方法

> 终结操作的意思是，执行完此方法之后，Stream流将不能再执行其他操作。   

- void forEach(Consumer action) 对此流的每个元素执行操作
- long count() 返回此流中的元素数