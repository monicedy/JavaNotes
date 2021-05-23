#### 删除集合内仅存的元素时,会报错
```
Exception in thread "main" java.util.ConcurrentModificationException
	at java.base/java.util.ArrayList$Itr.checkForComodification(ArrayList.java:1013)
	at java.base/java.util.ArrayList$Itr.next(ArrayList.java:967)
	at d9_Arraylist.StuManner.delStu(StuManner.java:35)
	at d9_Arraylist.StuManner.main(StuManner.java:62)
```

方法名  | 说明  
public boolean remove(Object o) | 删除指定的元素，返回删除是否成功  
public E remove(int index) |  删除指定索引处的元素，返回被删除的元素  
public E set(int index,E element) | 修改指定索引处的元素，返回被修改的元素  
public E get(int index) | 返回指定索引处的元素  
public int size() |  返回集合中的元素的个数  
public boolean add(E e) | 将指定的元素追加到此集合的末尾  
public void add(int index,E element) | 在此集合中的指定位置插入指定的元素  

## 方法一：普通for循环遍历
```java
//仅做代码的格式说明，不涉及具体问题
for(int i = 0 ; i < list.size() ; i++){
system.out.println(list.get(i));
}
```
## 方法二：Iterator迭代器遍历
```java
import java.util.Iterator;

Iterator it = list.iterator();
while(it.hasNext()) {
System.out.println(it.next());
}
```
## 方法三：增强for循环遍历（增强for循环的底层也是Iterator实现的，只是对它包装了一下）
```java
for(String string:list){
system.out.println(string);
}
```