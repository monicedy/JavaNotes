## LinkedList
addFist,addLast,getFirst,getLast,removeFirst,removeLast

public void addFirst(E e)   
public void addLast(E e)   
public E getFirst()   
public E getLast()   
public E removeFirst()   
public E removeLast()

## Set集合的特点
- 元素存取无序  
- **没有索引、只能通过迭代器或增强for循环遍历**  
- 不能存储重复元素  

`Set<String> st = new hashSet<String>();`

---
               
## HashSet集合的特点

> Object类中的public int hashCode()：返回对象的哈希码值  
同一个对象多次调用hashCode()方法返回的哈希值是相同的

- 底层数据结构是哈希表  
- 对集合的迭代顺序不作任何保证，也就是说不保证存储和取出的元素顺序一致  
- 没有带索引的方法，所以不能使用普通for循环遍历   
- 由于是Set集合，所以是不包含重复元素的集合

> HashSet集合保证元素唯一性的原理   
> 1. 根据对象的哈希值<计算存储位置> 如果当前位置没有元素则直接存入 如果当前位置有元素存在，则进入第二步   
> 2. 当前元素的元素和已经存在的元素<比较哈希值> 如果哈希值不同，则将当前元素进行存储 如果哈希值相同，则进入第三步  
> 3. 通过equals()方法比较两个元素的<内容> 如果内容不相同，则将当前元素进行存储,如果内容相同，则不存储当前元素

## LinkedHashSet集合特点
哈希表和链表实现的Set接口    
具有可预测的迭代次序   
由链表保证元素有序，也就是说元素的*存储和取出顺序*是一致的  
由哈希表保证元素唯一，也就是说没有重复的元素

## TreeSet集合概述和特点【应用】 TreeSet集合概述
*元素有序*，可以按照一定的规则进行排序，具体排序方式取决于构造方法     
- TreeSet()  根据其元素的自然排序进行排序
- TreeSet(Comparator comparator)根据指定的比较器进行排序   

*没有带索引*的方法，所以不能使用普通for循环遍历  
由于是Set集合，所以不包含重复元素的集合


### 自然排序Comparable
### 比较器排序Comparator