# C++是如何工作的

**![de2ebc93f84baf28f68620ddf6d1d3a8.png](image/de2ebc93f84baf28f68620ddf6d1d3a8.png)**

#include <iostream>：搜索iostream连接起来，预处理程序，还没运行就处理好的程序

会复制iostream里所有的文件，然后粘贴进main.cpp

因为cout等函数都是iostream里写好的，所以要先引用iostream才能使用cout

int main函数：程序开始的函数，程序进入main函数，开始一句一句执行整个代码，会默认返回0，因为是main函数很特殊所以不用主动返回值

<<:重载运算符，将它视为函数

![70f56a8fea6f31497fd5934a4d634438.png](image/70f56a8fea6f31497fd5934a4d634438.png) 

1.发送字符串”Hello World“到cout函数，该函数将行打印到控制台上

2.传递endl，它将光标移动到新行

3.cin.get（）函数是等待按下回车移动到程序的下一行，所以程序会停在第6行等待我们按下回车键

4.返回0，然后程序结束

c++是如何把代码编译成实际的机器代码的？

两个重要的参数

![566cb4149b49b6483d76bd99c278613d.png](image/566cb4149b49b6483d76bd99c278613d.png) 

![b21f2755f179ef4d54432e6951eb3679.png](image/b21f2755f179ef4d54432e6951eb3679.png) 

项目配置和平台配置

（配置：构建项目时应用的一组规则）

（平台：编译所针对的平台的设置）

eg：x86-意味着将为windows生成32位应用程序

定义平台的编译我们可以更改的一些规则：

![2b7601aa973dc93c0ed908335940f5e2.png](image/2b7601aa973dc93c0ed908335940f5e2.png)

打开visual studio规则界面

![c5037af01c6d7231f029424db8004674.png](image/c5037af01c6d7231f029424db8004674.png)

1.选择正确的配置和平台

![185ca2b89ad42ee7fa0a1e58809d09ab.png](image/185ca2b89ad42ee7fa0a1e58809d09ab.png)

![ef82ff6440a3a9cf7060c9d599f2496f.png](image/ef82ff6440a3a9cf7060c9d599f2496f.png)

![5f2430014c68ae0f31818f771bd69b05.png](image/5f2430014c68ae0f31818f771bd69b05.png)

我们需要.exe文件，所以将安装保留在Application(.exe)上

**![0a450dafc3e16e6bfa35d73c19af92fb.png](image/0a450dafc3e16e6bfa35d73c19af92fb.png)

编译器设置位于c/c++部分，我们不需要做任何设置**

**但是就是因为这些文件决定我们的文件如何编译**

**![ef46a47beadc08afb418ebf6f501f2f1.png](image/ef46a47beadc08afb418ebf6f501f2f1.png)**

**![579f3249eaab88dfb1ad105d413af560.png](image/579f3249eaab88dfb1ad105d413af560.png)**

**![5390c11b3753bd57832da0b745bbfb79.png](image/5390c11b3753bd57832da0b745bbfb79.png)**

**![7a8869b0c55fa0f4ad95e032a6e89301.png](image/7a8869b0c55fa0f4ad95e032a6e89301.png)**

**![b84e49d5ab49823cdbd69129f512284c.png](image/b84e49d5ab49823cdbd69129f512284c.png)**

**我们项目的每个.ssr文件都会被编译，标头不会被编译，只有.ssr文件�**�

**记住：标头包含在前处理阶段，#include,直接进入.ssr文件并在那儿编译**

**几个.ssr文件，都是单独编译的，每个.ssr文件都被编译成一个目标文件**

**visual studio将目标文件使用.obj命名**

**编译各种.ssr文件，得到一些.obj文件，然后就会将它们组合成一个.exe文件（用linker）**

**linker的任务就是收集所有的.obj文件，然后组合成一个.exe文件夹中**

**![c27d5ae34780fce2efa8becae6bc9570.png](image/c27d5ae34780fce2efa8becae6bc9570.png)**

**如何单独编译一个.ssr**

**在外面右键**

**![9979240baac0f4d2fcb09529ffe7951e.png](image/9979240baac0f4d2fcb09529ffe7951e.png)**

**或�**�

**![155754f8555be00f7d41c98f01f16b5b.png](image/155754f8555be00f7d41c98f01f16b5b.png)**

**![ffc4185c35e3c9cfcc5ed23c0611b556.png](image/ffc4185c35e3c9cfcc5ed23c0611b556.png)**

**![07acc5b048b583989b6ae17ab0f5bab3.png](image/07acc5b048b583989b6ae17ab0f5bab3.png)**

**然后会出现这个图标，直接点就可以了**

**![e1ace4b99fbcf256b2ae55dbb8c3e341.png](image/e1ace4b99fbcf256b2ae55dbb8c3e341.png)**

**打开这个，我们的构建文件就会在里面**

**![95d7e85a1a2f4b6217ccbc285639661c.png](image/95d7e85a1a2f4b6217ccbc285639661c.png)**

**![571ab424cbcfa753c2b486b4b53aeab0.png](image/571ab424cbcfa753c2b486b4b53aeab0.png)**

**用一个函数做这个输出方法，主函数只要调用就可以了**

**![ceee561dce0873907a717d0fa23f2795.png](image/ceee561dce0873907a717d0fa23f2795.png)**

**但是这样写会把所有函数都挤在这个界面，代码会越来越多，越来越乱，怎么办？**

**1.新构建一个项目****![3d63469f67af2f3ea905660c7afc8d65.png](image/3d63469f67af2f3ea905660c7afc8d65.png)**

**2.****![87e1e49054a723663ab33c6cd2f47ef7.png](image/87e1e49054a723663ab33c6cd2f47ef7.png)**

**![5648439879c0037b5f43e533c3d5e5dc.png](image/5648439879c0037b5f43e533c3d5e5dc.png)**

**![4725d2dfeeaaee57f8a923750c4d0ac9.png](image/4725d2dfeeaaee57f8a923750c4d0ac9.png)**

**built编译，然后就会对.ssr进行编译，为每个CBP(.cpp)文件形成obj文件**

**获取他们然后组成一个exe文件**

**![16340fed61a18706a424b37483f6ce40.png](image/16340fed61a18706a424b37483f6ce40.png)**
