## 获取当前时间

```
Date m = new Date( );
System.out.println("现在是："+m.toString( ));
```

```
Date t = n.getTime ( );  
System.out.println("现在是："+t);
```

## Date   
代表了一个特定的时间，精确到毫秒  
#### 构造方法  
- public Date()    
  对象并初始化，代表它被分配的时间，精确到毫秒
- public Date(long date)   
  对象并初始化,表示从标准基准时间(1970-01-01-08:00:00)起指定的毫秒数

#### 常用方法
- public long getTime()   
  获取的是日期对象从1970年1月1日 00:00:00到现在(调用对象的时间)的毫秒值
- public void setTime(long time)   
  设置时间，给的是毫秒值，同上述设置方法一样


## SimpleDateFormat类概述  
>  SimpleDateFormat是一个具体的类，用于以区域设置敏感的方式格式化和解析日期。  
>  包的位置 java.text.SimpleDateFormat;

- public SimpleDateFormat()   
  构造一个SimpleDateFormat，使用 默认模式和日期格式
- public SimpleDateFormat(String pattern)  
  构造一个SimpleDateFormat，使用 给定的模式 和 默认的日期格式  

格式化(从Date到String)
- public final String format(Date date)  
  将日期格式化成日期/时间字符串   
  
解析(从String到Date)
- public Date parse(String source)  
  从给定字符串的开始解析文本以生成日期

