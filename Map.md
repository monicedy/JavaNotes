`interface Map<K,V>` K：键的类型；V：值的类型

#### Map集合的特点
- 键值对映射关系 
- 一个键对应一个值 
- 键不能重复，值可以重复 
- 元素存取无序

`Map<String,String> map = new HashMap<String,String>();`

#### 常用方法
- V put(K key,V value) 
- V remove(Object key) 
- void clear() 
- boolean containsKey(Object key) 
- boolean containsValue(Object value) 
- boolean isEmpty()
- int size()

#### 获取功能
- V get(Object key) 
- Set keySet() 
- Collection values() 
- Set<Map.Entry<K,V>> entrySet()  
  获取所有键值对对象的集合

