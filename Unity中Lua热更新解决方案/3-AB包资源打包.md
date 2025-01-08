# 3.AB包资源打包

第一个下载方法：高版本不适用

![14c820301e8d7f6668dc4f6a7d50e1c9.png](image/14c820301e8d7f6668dc4f6a7d50e1c9.png)

第二个下载方法：直接在github上下载代码拖进来

![c213b88e13a214148cf6b3d78d66c42e.png](image/c213b88e13a214148cf6b3d78d66c42e.png)

![4d45db517d6f265f9a3cb78ff988a2cc.png](image/4d45db517d6f265f9a3cb78ff988a2cc.png)

第三个方法：通过github url进行在线下载（注意：必须开全局梯子，不然可能因网络问题失败）

![13bfe9efc51a7ee3c6145ccf4f551f3c.png](image/13bfe9efc51a7ee3c6145ccf4f551f3c.png)

![25539f2ee5150cf0be6d842ea4b3d873.png](image/25539f2ee5150cf0be6d842ea4b3d873.png)

1.如何把资源关联到AB包里？

![08b97a24a58d025bbea4735ac7688a95.png](image/08b97a24a58d025bbea4735ac7688a95.png)

打开AssetBundles就会看到一个模型的AB包

![813d6585c9cee9287742780ef6c09cad.png](image/813d6585c9cee9287742780ef6c09cad.png)

注意：U3D里C#代码不能被打进AB包中，所以才需要Lua语言

C#是一个编译型语言，所以不能被打包

预设体本质上就是文件包，关联了哪些脚本其实就是关联的文件ID

不是把脚本打成了AB包，而是把关联的数据打成了AB包

![99ddd7039d4a5c07da961283cbb37d7f.png](image/99ddd7039d4a5c07da961283cbb37d7f.png)

AB包打包，每次打包都是指定一个平台进行打包，不同平台需要重新打包

![09d9873eb26c27a716fdeda5b59b47f2.png](image/09d9873eb26c27a716fdeda5b59b47f2.png)

打包后的位置

![b28b1932659bb6cf855737d7882141f2.png](image/b28b1932659bb6cf855737d7882141f2.png)

![22b19d6b5980bb681021c2370bf49509.png](image/22b19d6b5980bb681021c2370bf49509.png)

![1a7a3b9ad4d847a6e10c9bc6bf1ff58b.png](image/1a7a3b9ad4d847a6e10c9bc6bf1ff58b.png)
