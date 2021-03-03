## Calendar类概述  
- 为 *特定瞬间* 与 *一组日历字段* 之间的转换提供了一些方法，并为 *操作日历字段* 提供了一些方法

日历字段:  
- Calendar.YEAR  
- Calendar.MONTH
- Calendar.DATE

提供了一个类方法 getInstance 用于获取这种类型的一般有用的对象。  
该方法返回一个Calendar 对象。  
其日历字段已使用当前日期和时间初始化
- Calendar rightNow = Calendar.getInstance();

## 常用方法

- public int get(int field)  
  返回给定日历字段的值  
  
- public abstract void add(int field, int amount)  
  根据日历的规则，将指定的时间量添加或减去给定的日历字段
  
- public final void set(int year,int month,int date)  
  设置当前日历的年月日