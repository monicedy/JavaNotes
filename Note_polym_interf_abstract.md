## 多态

什么是多态

- 同一个对象，在不同时刻表现出来的不同形态

多态的前提
- 要有继承或实现关系
- 要有方法的重写
- 要有父类引用指向子类对象

多态中的成员访问特点（记忆）
- 成员访问特点
    - 成员 **变量**
      - 编译看父类，运行看父类
    - 成员 **方法**
      - 编译看父类，运行看子类 
        
多态中的转型

向上转型
- 父类引用指向子类对象就是向上转型

向下转型
- 格式：子类型 对象名 = (子类型)父类引用;

```java
//向上转型
Animal a = new Cat();
a.eat();
// a.playGame();
//向下转型
Cat c = (Cat)a;
c.eat();
c.playGame();
```

多态的形式
- 具体类多态，
- 抽象类多态，
- 接口多态

## 抽象类
-  一个*没有方法体的方法*应该定义为抽象方法
-  而*类中如果有抽象方法*，该类必须定义为抽象类 
   
>
成员变量：
   - 既可以是变量
   - 也可以是常量
   
构造方法：
   - 空参构造
   - 有参构造
   
成员方法：
   - 抽象方法
   - 普通方法
>


抽象类不能实例化 
- 但可以通过子类对象实例化，这叫抽象类多态

抽象类的子类: 
- 要么重写抽象类中的所有抽象方法
- 要么是抽象类

## 接口
>是一种公共的规范标准，只要符合规范标准，大家都可以通用  
> 接口更多的体现在对行为的抽象

接口不能实例化
- 但可以通过实现类对象实例化，这叫接口多态。
>
成员变量 - 静态常量
- 只能是静态常量 默认修饰符：public static final  
- 即使写了 public int ，也自动修复成 public static final
- 尽量规范 public static final int a;  

构造方法
- 没有，因为接口主要是扩展功能的，而没有具体存在

成员方法 - 抽象方法
- 只能是抽象方法, 默认修饰符：public abstract
- 所以 void method 可行，自动加上 public abstract
- 尽量规范public abstract void method();
>
待补充：
- 关于接口中的方法，JDK8和JDK9中有一些[新特性](https://blog.csdn.net/qq_40896788/article/details/108037819)

## 抽象类和接口的区别
成员区别  
- 抽象类  
    - 变量,常量；  
    - 有构造方法；  
    - 有抽象方法,也有非抽象方法  
- 接口
    - 常量； 
    - 抽象方法  

关系区别

- 类与类
    - 继承，单继承
- 类与接口
    - 实现，可以单实现，也可以多实现
    - <类> 可以多实现 <接口>  
      `public class Human extends Sub implements run,swim`
- 接口与接口
    - 继承，单继承，多继承
    - <接口> 可以多继承<接口> 
      `public interface sport extends run,swim`
      
- [参考 d10_extends.learn.Demo_ext](C:\Users\yuqiu\IdeaProjects\ItHeima\LearnJava\src\d10_extends\learn\Demo_ext.java)

设计理念区别
- 抽象类
    - 对类抽象，包括属性、行为
- 接口
    - 对行为抽象，主要是行为


