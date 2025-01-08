# 3.Canvas渲染模式的控制

![6f94b997b41bee7a6781f87ca5b663ef.png](image/6f94b997b41bee7a6781f87ca5b663ef.png)

![929fdd08978df73a7c98d586bf19b23f.png](image/929fdd08978df73a7c98d586bf19b23f.png)

![00153ad1808bf7c79698d1639a33eb3c.png](image/00153ad1808bf7c79698d1639a33eb3c.png)

![b58eaa87b08dbc6d71828017e2a66e55.png](image/b58eaa87b08dbc6d71828017e2a66e55.png)

![34b94aa357400ee41a80c87b87eef6c4.png](image/34b94aa357400ee41a80c87b87eef6c4.png)

![8a0e9dfbf5206c16f567b8f1bbe431c7.png](image/8a0e9dfbf5206c16f567b8f1bbe431c7.png)

数字越大，越后渲染，越后渲染，越显示在前方

![49026c0eca669822824349f998654994.png](image/49026c0eca669822824349f998654994.png)

![68bd9d6e278ceb8a4e1e0f94e1526308.png](image/68bd9d6e278ceb8a4e1e0f94e1526308.png)

小技巧：

1.创建一个摄像机专门用来渲染UI层，摄像机渲染模式选择只渲染自己层相关的东西

![98af9830cf8843c7fe321b9655f4047c.png](image/98af9830cf8843c7fe321b9655f4047c.png)

2.选择渲染模式

3.如果某一些3D对象想渲染在UI界面之前，单独创建在UI界面上

4.排序层越大，越后渲染，显示越前面

![c1921d323f7b5444556d56e912360bd5.png](image/c1921d323f7b5444556d56e912360bd5.png)

![52800c9ab0fdbada8852168fdda21394.png](image/52800c9ab0fdbada8852168fdda21394.png)

注意：

一般3D模式关联的就是主摄像机，因为要监听所有的事件

这种模式其实就是把UI图片当成3D物体来处理了 ，缩放大小和尺寸都是和世界坐标一样的 

![8b73aa4d699d22c6bf92e4b5b2f52e6e.png](image/8b73aa4d699d22c6bf92e4b5b2f52e6e.png)

![e250843939cb77f539e44134f8da31f3.png](image/e250843939cb77f539e44134f8da31f3.png)

 
