# MathF

![0fd5dd8f406df23bfd2a941456dab107.png](image/0fd5dd8f406df23bfd2a941456dab107.png)

Math是静态类，Mathf是结构体，两个都是静态，所以基本上看到静态的内容就是工具类的常量和方法

![694bfe6060e11beae10bb376eeaf13d5.png](image/694bfe6060e11beae10bb376eeaf13d5.png)

Math中的数学方法基本上Mathf里都有，除此以外还有专门为游戏开发所有的数学方法

一般用Mathf开发就可以了

![12f0d0a1d40b96b424893c63a86418a0.png](image/12f0d0a1d40b96b424893c63a86418a0.png)

PI已经在里面写好了直接用就可以:3.14159274

![a2ae9f8b40d6420dab6498c275b4152f.png](image/a2ae9f8b40d6420dab6498c275b4152f.png)

输出：10,20,1

![638329d9aafff55856db2d439df0a657.png](image/638329d9aafff55856db2d439df0a657.png)

输出：1,2,2

因为c#强转默认是向下取整，而向上取整比如1.00001f，只要比1大一点点都会取2

![2f51e0aedf8101e6e2f6a4081e5faa96.png](image/2f51e0aedf8101e6e2f6a4081e5faa96.png)

除了强转，也可以用这个方法向下取整，但是不是根据四舍五入转的，9.6也是转成9

![27ce42bfaaae1b9fb640b7766c5225f7.png](image/27ce42bfaaae1b9fb640b7766c5225f7.png)

输出：11,20,15

(取值,最小,最大)，取值只能在最小和最大中间取，超过范围，取最大值和最小值其中一个

---

![60d90bd40148a7e9716a5f1b390d2e7b.png](image/60d90bd40148a7e9716a5f1b390d2e7b.png)

输出最大值，8,2

![e0e55cd87e84dd402e8d340e6e6e3d72.png](image/e0e55cd87e84dd402e8d340e6e6e3d72.png)

输出最小值，1,0.4

且最大值和最小值可以整数和小数混搭

![ed99ed3819df62f5a97545589a78a833.png](image/ed99ed3819df62f5a97545589a78a833.png)

---

![f78d7868f1d12a4c83273527c4db7554.png](image/f78d7868f1d12a4c83273527c4db7554.png)

输出，16,8

（底数，幂），4的2次方

![2733583779b009c714829c83e1f4098c.png](image/2733583779b009c714829c83e1f4098c.png)

输出：1，2

![95032729a8f18139f8abc10e166c190e.png](image/95032729a8f18139f8abc10e166c190e.png)

输出：2,16,64

就是开根号

![973d35834c980d1dd4f57d73c3f17ad1.png](image/973d35834c980d1dd4f57d73c3f17ad1.png)

输出：true,true,false,true

只要是2的n次方就输出true

![7fc61e994988262c68bad3453ebdb92c.png](image/7fc61e994988262c68bad3453ebdb92c.png)

输出：1,1，-1,1，-1

正数输出1，负数输出-1

---

线性插值：

![a066682450cf4d0d50e59b1dfda61009.png](image/a066682450cf4d0d50e59b1dfda61009.png)

![1648663571738ba8bd131db7364e84c9.png](image/1648663571738ba8bd131db7364e84c9.png)

用法一：先快后慢，无限接近end位置

用法二：匀速到达end位置，匀速直线运动必须每次运动清空，time,result,和start的值

用法：

1.某个对象跟随另一个对象移动的时候

2.某一个值要趋近于一个值的时候

用法一：无限接近目标值，先快后慢

![0255c1e52ca1e7803c7eb58a354eb412.png](image/0255c1e52ca1e7803c7eb58a354eb412.png)

![07f61ff102b2ed405195d98c209d2d85.png](image/07f61ff102b2ed405195d98c209d2d85.png)

用法二：匀速到达目标值

![d2ee0f691126356c48a0f4a60aaab1d4.png](image/d2ee0f691126356c48a0f4a60aaab1d4.png)

---

![e55462a01b70b1f389c8a3457feb9f07.png](image/e55462a01b70b1f389c8a3457feb9f07.png)

![3ebc21b63a01884e7f92e43ea8a82ee9.png](image/3ebc21b63a01884e7f92e43ea8a82ee9.png)

![0744bcf5bfc80ea63533b9cb8c2bfae2.png](image/0744bcf5bfc80ea63533b9cb8c2bfae2.png)
