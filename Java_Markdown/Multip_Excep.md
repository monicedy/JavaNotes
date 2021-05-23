## 同时定义多个
`throws E1,E2`
> throws 可能存在，谁调用谁处理（throw）
> throw 任意位置抛出
> 
## 同时处理多个
- 子类在前，父类在后  
```
try{ ;
}catch Esub{ ;
}catch Esup{ ;
}
```

## 同时抛出

- 把多个异常信息放到list中
