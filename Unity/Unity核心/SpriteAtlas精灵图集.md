# SpriteAtlas精灵图集

![36925dd08ccacd08e8804108f56d4f2d.png](image/36925dd08ccacd08e8804108f56d4f2d.png)

![840b80a10a227668c79ade991a358df0.png](image/840b80a10a227668c79ade991a358df0.png)

图集就是把很多小图片拼成一个大图片，一次渲染一个大的图片，这样可以减少渲染次数，提高游戏运行速度和内存利用率。

打图集=制作图集，把一个个小图制作成一张大的图集

构建时，就是只在打包成exe时才会生成图集，目前一般选择Always Enable

![7283586283927c8f0b076c05ac08edbf.png](image/7283586283927c8f0b076c05ac08edbf.png)

![8c65d566320858628bc5042e8735a634.png](image/8c65d566320858628bc5042e8735a634.png)

怎么创建一个图集？

![228d26bc4ce88b38bb2645ad7b18bb4c.png](image/228d26bc4ce88b38bb2645ad7b18bb4c.png)

参数设置：

![f374e71a37ae3840c25458a0ff4de9d4.png](image/f374e71a37ae3840c25458a0ff4de9d4.png)

UI不要选Allow Rotation,勾选上会自动将图片以最大密度方式放置图片

![9022ba77b49d6346df97e9bdf3e7b7a5.png](image/9022ba77b49d6346df97e9bdf3e7b7a5.png)

Tight Packing:不以矩形打包，而是图片像素点，透明区域不打包

![8b16bcce47d4c1fcccb007ffd9a3cc20.png](image/8b16bcce47d4c1fcccb007ffd9a3cc20.png)

一般2D游戏不勾选Mip Map

![28d74e003fed92a14b8f8ab9d9f5fb20.png](image/28d74e003fed92a14b8f8ab9d9f5fb20.png)

![355b7f7e124dbd14df1d2ecd827e3f7f.png](image/355b7f7e124dbd14df1d2ecd827e3f7f.png)

![6b5267ec2c6f409f58d3ffe2d766c68c.png](image/6b5267ec2c6f409f58d3ffe2d766c68c.png)

![f5326e1ad850fcc154a8cdb882d6864e.png](image/f5326e1ad850fcc154a8cdb882d6864e.png)

往图集添加需要打包的图片，也可以拖图片和文件夹添加

![bbbdff1c1a1dd561b055c71754f09182.png](image/bbbdff1c1a1dd561b055c71754f09182.png)

如何使用：

直接将图片拖到场景中使用

怎么看有没有打包成功？

看运行后和运行前draw call有没有变化

![c22fb5f369e43288cb6b438e887e7ecb.png](image/c22fb5f369e43288cb6b438e887e7ecb.png)

![d7cbee80722539eda8b1a9cc9ef8d249.png](image/d7cbee80722539eda8b1a9cc9ef8d249.png)

如何通过代码直接将图集中的一个图片加载到场景中

![d32dca17037072a97279d1a84aad957a.png](image/d32dca17037072a97279d1a84aad957a.png)

![140be7e7f03fb1df3db5c7669fe16a8f.png](image/140be7e7f03fb1df3db5c7669fe16a8f.png)

![67d8e1252c266e20545ea3a79d656e77.png](image/67d8e1252c266e20545ea3a79d656e77.png)

1.

![4da0da81dd64f6ac71c66976f34d0378.png](image/4da0da81dd64f6ac71c66976f34d0378.png)

2.DrawCall数量是3，因为最上层和最下层虽然在一个图集，但是两个层之间夹杂了其他层，所有的就会分开渲染

![997472980fdac62a30323fa8d006e28f.png](image/997472980fdac62a30323fa8d006e28f.png)
