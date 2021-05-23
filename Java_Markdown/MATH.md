

## MATH
public static int abs(int a) 返回参数的绝对值  
public static double ceil(double a) 返回大于或等于参数的最小double值，等于一个整
数  
public static double floor(double a) 返回小于或等于参数的最大double值，等于一个整
数  
public static int round(float a) 按照四舍五入返回最接近参数的int  
public static int max(int a,int b) 返回两个int值中的较大值  
public static int min(int a,int b) 返回两个int值中的较小值  
public static double pow (double a,double b) 返回a的b次幂的值    
public static double random() 返回值为double的正值，[0.0,1.0)  

## SYSTEM
public static void exit(int status) 终止当前运行的 Java 虚拟机，非零表示异常终止  
public static long currentTimeMillis() 返回当前时间(以毫秒为单位)  

## Object超类
>Object 是类层次结构的根，每个类都可以将 Object 作为超类。所有类都直接或者间接的继承自该类，
换句话说，该类所具备的方法，所有类都会有一份
> > 查看方法源码的方式:  `选中方法，按下Ctrl + B`

equals方法的作用  
- 用于对象之间的比较，返回true和false的结果
- 举例：s1.equals(s2); s1和s2是两个对象  

重写equals方法的场景
- 不希望比较对象的地址值，想要结合对象属性进行比较的时候。  

重写equals方法的方式
- 1. alt + insert 选择equals() and hashCode()，IntelliJ Default，一路next，finish即可
- 2. 在类的空白区域，右键 -> Generate -> 选择equals() and hashCode()，后面的同上。

> Arrays类的定义  
    Arrays类位于 java.util 包中，主要包含了操纵数组的各种方法  
    使用时导包:import java.util.Arrays  
二、Arrays常用函数（都是静态的)  
1.void Arrays.sort()  
    void Array.sort(Object[] array)  
    功能：对数组按照升序排序  

## 工具类设计思想  static 

1、构造方法用 private 修饰  
- 用private修饰的构造器，在其他类构造对象时会报错  

2、成员用 public static 修饰