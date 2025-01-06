# 结合反射——读取List数据类型

1.传入对象数据

2.循环对像的各个字段

3.如果是List字段，则循环List列表

4.对List中的每一个属性用GetGenericArguments()方法获取List是什么泛型

递归调用Load方法，传入泛型类型和key值，添加到list列表中![3a76070ca5cd94813b817e9472ebc0e9.png](image/3a76070ca5cd94813b817e9472ebc0e9.png)
