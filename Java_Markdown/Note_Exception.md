## 异常体系
![img.png](img.png)

如果程序出现了问题，我们没有做任何处理，最终JVM 会做默认的处理，处理方式有如下两个步骤：  
- 把异常的名称，错误原因及异常出现的位置等信息输出在了控制台
- 程序停止执行

# 1. try-catch

```
try {   
    可能出现异常的代码;  
} catch (异常类名 变量名) {  
    异常的处理代码;
}
```


程序从 try 里面的代码开始执行  
出现异常，就会跳转到对应的 catch 里面去执行  
执行完毕之后，程序还可以继续往下执行  

## Throwable成员方法  
- public String getMessage()   
  返回此 throwable 的 *详细* 消息字符串
- public String toString()   
  返回此可抛出的 *简短* 描述
- public void printStackTrace()   
  把异常的错误信息 *输出在控制台*
  

## 错误类型

编译时异常  
- 都是Exception类及其子类
- 必须显示处理，否则程序就会发生错误，无法通过编译  

运行时异常  
- 都是RuntimeException类及其子类 
- 无需显式处理，也可以和编译时异常一样处理

#  2. Throws 
```
public void 方法() throws 异常类名 { 
方法体 ;
}
```
- 这个throws格式是跟在方法的括号后面的
  
## 编译时异常必须要进行处理
- 编译时异常必须要进行处理，  
  两种处理方案：try...catch …或者 throws，  
  如果采用 throws 这种方案，将来谁调用谁处理
  
## 运行时异常可以不处理
- 运行时异常可以不处理  
  出现问题后，需要我们回来修改代码
  


# 自定义异常
[参考代码](C:\Users\yuqiu\IdeaProjects\ItHeima\LearnJava\src\d13_api_and_Excep\Custom\Teacher.java)


# throws & throw
![img_1.png](img_1.png)

