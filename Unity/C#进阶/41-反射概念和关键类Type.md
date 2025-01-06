# 41.反射概念和关键类Type

![b6e7d5d2467b5234bb1f8eacab1bcae2.png](image/b6e7d5d2467b5234bb1f8eacab1bcae2.png)

![bf992ea80b446dd5ac55f08c6c6fa4c9.png](image/bf992ea80b446dd5ac55f08c6c6fa4c9.png)

![5f2e4cc06a6e064192e24b1679f9d871.png](image/5f2e4cc06a6e064192e24b1679f9d871.png)

![51b6646e785496be0875533375e4d911.png](image/51b6646e785496be0875533375e4d911.png)

![3a4f37fc24a930030e2086e4800ce993.png](image/3a4f37fc24a930030e2086e4800ce993.png)

反射最大的作用：

在一个程序集里面去使用另一个程序集里写好的代码

可以利用反射的形式，实例化另一个程序集代码里的一个类，并控制它，实现自己的一些功能

自己不用去写别人写好的一些代码了

                                                        ——预制代码

![4cf51d73682e4c43fa768f80da22feae.png](image/4cf51d73682e4c43fa768f80da22feae.png)

![19283c4d4336a4c91a5e783077387996.png](image/19283c4d4336a4c91a5e783077387996.png)

![6448dc02dc43347185f318280f93d65f.png](image/6448dc02dc43347185f318280f93d65f.png)

三种获得Type的方式都是指向的同一个内存地址

![ba4ae005e83f7c6955b2756001abfa84.png](image/ba4ae005e83f7c6955b2756001abfa84.png)

![160074b76b674f5d96cc2a915ee20563.png](image/160074b76b674f5d96cc2a915ee20563.png)

![f42f2e43af4d58949d607060dfedc964.png](image/f42f2e43af4d58949d607060dfedc964.png)

![60cfff0216b1a7ec130ffd54a08e9609.png](image/60cfff0216b1a7ec130ffd54a08e9609.png)

获取其他程序集需要在前面加命名空间.

![df93c8296d54c8f8b0fab17ee45f3bcd.png](image/df93c8296d54c8f8b0fab17ee45f3bcd.png)

![203be77e61f263fa5028ffa5423c44f9.png](image/203be77e61f263fa5028ffa5423c44f9.png)

![e7b9d60386cf0858ea856f4d5ed0e92a.png](image/e7b9d60386cf0858ea856f4d5ed0e92a.png)

![8cfb63ca8a6fe8772dca533a8f64f09c.png](image/8cfb63ca8a6fe8772dca533a8f64f09c.png)

![02569fc5da208c0362aadc4b5c5bd18d.png](image/02569fc5da208c0362aadc4b5c5bd18d.png)

![13a06c99a1770b7f4017e13152426546.png](image/13a06c99a1770b7f4017e13152426546.png)

![fea333bb8e8403fd57931e14cde04d51.png](image/fea333bb8e8403fd57931e14cde04d51.png)

![b570d9f75411013b279d1813e525f576.png](image/b570d9f75411013b279d1813e525f576.png)

![2e890e74870d58a49c58bec5679bd7fd.png](image/2e890e74870d58a49c58bec5679bd7fd.png)

![e254e6c70555541fac930b59affed409.png](image/e254e6c70555541fac930b59affed409.png)

总结：

1.获取对象的Type

2.利用Type里面的API得到指定的成员变量，构造函数，成员函数等具体信息，装起来

3.调用传参执行
