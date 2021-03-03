## 1.import导包

使用不同包下的类时，使用的时候要写类的全路径
```java
java.util.Scanner sc = new Scanner(System.in);
```
写起来太麻烦了,为了简化带包的操作，Java就提供了导包的功能
```java
import java.util.Scanner;
Scanner sc = new Scanner(System.in);
```
---

## 2. package 带包编译&带包运行
> 包就是文件夹，用来管理类文件的

带包编译：javac –d . 类名.java
- 例如：javac -d . com.heima.demo.HelloWorld.java

带包运行：java 包名+类名
- 例如：java com.heima.demo.HelloWorld
---
## 3.public protected default private
#### 3.1.protected属于子类限制修饰符，

> protected修饰符所修饰的类（这句话中指父类）属成员变量和方法，只可以被子类访问，而不管子类是不是和父类位于同一个包中。

#### 3.2.default属于包限制修饰符。

> default修饰符所修饰的类属成员变量和方法，只可被同一个包中的其他类访问，而不管其他类是不是该类的子类。

## 4.final修饰类、方法、变量的效果

- final修饰类：该类不能被继承（不能有子类，但是可以有父类）
- final修饰方法：该方法不能被重写
- final修饰变量：表明该变量是一个常量，不能再次赋值
    - fianl修饰**基本数据类型**变量
        - 基本类型的数据**值不能发生改变**
    - final修饰引用数据类型变量
        - 引用类型的**地址值**不能发生改变，但是地址里面的**内容**是可以发生改变的
          
    ```
    public static void main(String[] args){
    final Student s = new Student(23);
    s = new Student(24); // 错误
    s.setAge(24); // 正确
    }
    ```

## 5.static修饰
- 可以在不创建对象的情况下,调用静态方法. 

- 在代码运行前就写入内存,貌似跟常量是同时编译的.
 
**静态成员方法只能访问静态成员**

~~5.1. 被类的所有对象共享，这也是我们判断是否使用静态关键字的条件~~

~~5.2. 可以通过对象名调用,【推荐使用类名调用】~~