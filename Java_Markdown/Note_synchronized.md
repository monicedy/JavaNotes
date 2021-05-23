## synchronize block
synchronized(任意对象) { 多条语句操作共享数据的代码
}

---
## synchronize method

#### 同步方法的格式 
同步方法：就是把synchronized关键字加到方法上

`修饰符 synchronized 返回值类型 方法名(方法参数) { 方法体；}`

同步方法的锁对象是什么呢? 
- this

---
#### 静态同步方法 
同步静态方法：就是把synchronized关键字加到静态方法上

`修饰符 static synchronized 返回值类型 方法名(方法参数) { 方法体 }`

同步静态方法的锁对象是什么呢? 
- 类名.class