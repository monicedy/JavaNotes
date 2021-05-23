
## 创建Integer对象
- Integer instance = new Integer(1)
- Integer a = Integer.valueOf(1);  
  两个都是得到一个Integer对象，但是Integer.valueOf的效率高。  
  为什么呢？因为Integer.valueOf用到了缓存
  
> new Integer.valueof()  ---返回的是Integer的对象。   
 Integer.parseInt()  --- 返回的是一个int的值。  
 new Integer.valueof().intValue()  ---返回的也是一个int的值  
> 
## int转换为String
- 1 直接在数字后加一个空字符串
- 2 通过String类静态方法valueOf()
## String转换为int
- 1 先将字符串数字转成Integer，再调用valueOf()方法  
- 2 通过Integer静态方法parseInt()进行转换  

## String.split(" ")