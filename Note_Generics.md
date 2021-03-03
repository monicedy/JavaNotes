## 泛型
> 它的本质是参数化类型，也就是说所操作的数据类型被指定为一个参数。一提到参数，最熟悉的就是定义方 法时有形参，然后调用此方法时传递实参。那么参数化类型怎么理解呢？顾名思义，就是将类型由原来的具 体的类型参数化，然后在使用/调用时传入具体的类型。这种参数类型可以用在类、方法和接口中，分别被称 为泛型类、泛型方法、泛型接口

### 泛型定义格式   
- <类型>：指定一种类型的格式。这里的类型可以看成是形参   
- <类型1,类型2…>：指定多种类型的格式，多种类型之间用逗号隔开。这里的类型可以看成是形参  
- 将来具体调用时候给定的类型可以看成是实参，并且实参的类型只能是引用数据类型

### 泛型的好处
- 把运行时期的问题提前到了编译期间 
- 避免了强制类型转换


### i 泛型类
```
public class Generic<T> { 
    private T t;
    public T getT() { return t; }
}

public class GenericDemo { 
    public static void main(String[] args) { 
        Generic<String> g1 = new Generic<String>(); g1.setT("林青霞"); 
        System.out.println(g1.getT());
        ...

```


#### ii 泛型方法
`修饰符 <类型> 返回值类型 方法名(类型 变量名) { }`

#### iii 泛型接口
`修饰符 interface 接口名<类型> { }`

```
//定义泛型接口
public interface Generic<T> { 
    void show(T t);
}
//实现泛型接口
public class GenericImpl<T> implements Generic<T> { 
    @Override 
    public void show(T t) { 
        System.out.println(t);
    } 
}
//测试类
public class GenericDemo { 
    public static void main(String[] args) { 
        Generic<String> g1 = new GenericImpl<String>(); 
        g1.show("林青霞");    
    } 
}
```
