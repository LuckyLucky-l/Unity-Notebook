# MonoBehavior中的重要内容

学习MonoBehavior最好的方法是直接选中，然后f12

![830b661f98f3c352ba6d283f7528bbdd.png](image/830b661f98f3c352ba6d283f7528bbdd.png)

![4f36ff94d8d41756ea75f022e6bb172d.png](image/4f36ff94d8d41756ea75f022e6bb172d.png)

![1929fca5b9552ed3d6029e9872e63aee.png](image/1929fca5b9552ed3d6029e9872e63aee.png)

![e0fe18ed6f2b40d8f1fd72506c179ed6.png](image/e0fe18ed6f2b40d8f1fd72506c179ed6.png)

![d2faa29425b3310cb43971e0934b8eb6.png](image/d2faa29425b3310cb43971e0934b8eb6.png)

![ce20556753eb71e8f7809ac95de778b5.png](image/ce20556753eb71e8f7809ac95de778b5.png)

![574dd12600602bd916172d8cfd6d0dca.png](image/574dd12600602bd916172d8cfd6d0dca.png)

要拖过来的脚本对象，必须挂载了这里指定类型的脚本，比如这里的是获取otherLesson3的脚本对象的物体信息和姓名

而otherLesson3是一个lesson1类型的变量，所以另一个物体必须挂载lesson1脚本

![6cf4d0eafc5e73e720cf361590e35f8e.png](image/6cf4d0eafc5e73e720cf361590e35f8e.png)

![56ce619a7182885e87d1f4aa5d47543a.png](image/56ce619a7182885e87d1f4aa5d47543a.png)

![3567d33c7836ac16d175acfdb4e65252.png](image/3567d33c7836ac16d175acfdb4e65252.png)

typeof(Lesson3_Test)=获取一个Lesson3_Test的type(类型)

![3bd1ef24ee5dff7f25e5a3d1d3e44ebe.png](image/3bd1ef24ee5dff7f25e5a3d1d3e44ebe.png)

编译器可以根据 **as** 关键字右边的类型 **Lesson3_Test** 推断出变量 **t** 的类型应该是 **Lesson3_Test**

**![8057c2a8b42d7bfc2b170a068e7f0718.png](image/8057c2a8b42d7bfc2b170a068e7f0718.png)**

**![51462ea7bf97e58efd81be9b294ea0cc.png](image/51462ea7bf97e58efd81be9b294ea0cc.png)**

**![18bf6d5fe268426296779c8a23f70d29.png](image/18bf6d5fe268426296779c8a23f70d29.png)**

**![c210dadcc95e6e30650f6b220a4c26ad.png](image/c210dadcc95e6e30650f6b220a4c26ad.png)**

![e14ae6d76ee241a76cac2f538651bbdb.png](image/e14ae6d76ee241a76cac2f538651bbdb.png)

<span style="background-color: #ffaaaa"><span style="background-color: #ffaaaa">总结：可以打印出来自己的脚本依附的对象挂载的其他脚本</span></span>

![1d28ecbfb007b11b520655bb296b7cb3.png](image/1d28ecbfb007b11b520655bb296b7cb3.png)

<span style="background-color: #ffaaaa">总结：可以得出挂载了这个脚本的数量</span>

![257560b4c49def1a3b2890df3e3dcc3b.png](image/257560b4c49def1a3b2890df3e3dcc3b.png)

![eed89ee2c92a4ed6198ce05d0d6034a1.png](image/eed89ee2c92a4ed6198ce05d0d6034a1.png)

![f258eb48b4bddc2243a9dda9359fc473.png](image/f258eb48b4bddc2243a9dda9359fc473.png)

<span style="background-color: #ffaaaa">总结:</span>

<span style="background-color: #ffaaaa">获取单个脚本就是获得脚本名字依附在那个对象上</span>

<span style="background-color: #ffaaaa">多个脚本就是获得对象依附了多少个这个脚本</span>

![56dea735455f6883dfa48d89fc1d3fc6.png](image/56dea735455f6883dfa48d89fc1d3fc6.png)

![04ba98288430c16151a038ccf553d905.png](image/04ba98288430c16151a038ccf553d905.png)

总结：以上两种方法都可以获取单个脚本时为空时，不执行里面的内容

![4b6608a66c1c55fc907dc71f77d3326e.png](image/4b6608a66c1c55fc907dc71f77d3326e.png)

![add14e1d1a741fb7ba9efed3e3222733.png](image/add14e1d1a741fb7ba9efed3e3222733.png)

![5233bacdc3dd09781d184d8256996678.png](image/5233bacdc3dd09781d184d8256996678.png)

同一对象直接获取就可以了

![2e3fefec77c002e7bf82b444e7a3ccd1.png](image/2e3fefec77c002e7bf82b444e7a3ccd1.png)

![4743f73cd01af61334884444bb8a3f78.png](image/4743f73cd01af61334884444bb8a3f78.png)

总结：

![2f59d42c15cee72fd54176976216c72a.png](image/2f59d42c15cee72fd54176976216c72a.png)

脚本之间都可以用Public B b;（创建一个B类型的b变量）进行关联，只要关联了，把对应脚本拖拽到对象上，再关联就可以实现不同对象间（或者同一对象）的调用
