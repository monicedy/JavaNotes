## Collection集合概述
- 是单例集合的顶层接口，它表示一组对象，这些对象也称为Collection的元素
- JDK 不提供此接口的任何直接实现，它提供更具体的子接口（如Set和List）实现  
 如：`Collection<String> c = new ArrayList<String>()`
  
#### Collection 常用方法
add,remove,clear,contains,isEmpty,size
- 1. boolean add(E e)  
  添加元素
- 2. boolean remove(Object o)  
  从集合中移除指定的元素
- 3. void clear()   
  清空集合中的元素
- 4. boolean contains(Object o)   
  判断集合中是否存在指定的元素
- 5. boolean isEmpty()   
  判断集合是否为空
- 6. int size()   
  集合的长度，也就是集合中元素的个数

## Iterator 迭代器的介绍
- 迭代器，集合的专用遍历方式  
- `Iterator iterator()`返回此集合中元素的迭代器  
迭代器是通过集合的iterator()方法得到的，所以我们说它是依赖于集合而存在的
  
遍历格式
```
while ( it.hasNext() ) {
    String s = it.next();
    System.out.println(s);
}
```


# List集合概述  
- 有序集合(也称为序列)  
  - 用户可以精确控制列表中每个元素的插入位置  
  - 用户可以通过整数索引访问元素，并搜索列表中的元素
  - 与Set集合不同，列表通常允许重复的元素
    

- List集合特点
  - 有索引
  - 可以存储重复元素
  - 元素存取有序
    
#### List 接口 特有方法
get,set,add,remove
- void add(int index,E element)  
  在此集合中的指定位置插入指定的元素
- E remove(int index)   
  删除指定索引处的元素，返回被删除的元素
- E set(int index,E element)   
  修改指定索引处的元素，返回被修改的元素
- E get(int index)   
  返回指定索引处的元素