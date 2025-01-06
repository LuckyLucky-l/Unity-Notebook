# SpriteRender精灵渲染器

![9418149661241e246ecea98ad4a30a53.png](image/9418149661241e246ecea98ad4a30a53.png)

![e8800e60fedbf6567b56c2bc98b83924.png](image/e8800e60fedbf6567b56c2bc98b83924.png)

![cd5c3d0708f81c779eafcd0fcde779ec.png](image/cd5c3d0708f81c779eafcd0fcde779ec.png)

1.直接拖入

![feb9c2ed82d37926b99397f76eeaebbb.png](image/feb9c2ed82d37926b99397f76eeaebbb.png)

![b5cbf94da9d37c2fe6f641e8ef8258ef.png](image/b5cbf94da9d37c2fe6f641e8ef8258ef.png)

2.右键创建

![254b16b44d4aeac58961bab1f2870b07.png](image/254b16b44d4aeac58961bab1f2870b07.png)

关联

![91858cb8704bedd89685379bcb762d03.png](image/91858cb8704bedd89685379bcb762d03.png)

3.空物体添加脚本，重复步骤2

![49257c9ce99dbfac0bf543d51b5a0829.png](image/49257c9ce99dbfac0bf543d51b5a0829.png)

![3424ff1706ce28d7a8c07f7fa3823e76.png](image/3424ff1706ce28d7a8c07f7fa3823e76.png)

![14d910561c5ace2b1746c2b639bb7766.png](image/14d910561c5ace2b1746c2b639bb7766.png)

                                                  ![70efd4a432a2e974e66e57db7e8cb997.png](image/70efd4a432a2e974e66e57db7e8cb997.png)

---

![df46e0af863ae0f968176da398ea00e5.png](image/df46e0af863ae0f968176da398ea00e5.png)

切片模式的原理，只有中间十字区域缩放，原图片必须是full rect类型

![2315132ab0d2a9588c41faa8495880b9.png](image/2315132ab0d2a9588c41faa8495880b9.png)

![46ce7ebc265d493023156ef343fb3294.png](image/46ce7ebc265d493023156ef343fb3294.png)

![68b962d797f70bcc2b381fe55dde351c.png](image/68b962d797f70bcc2b381fe55dde351c.png)

![5b6600b8b6aebb5d9cbcd8616387d1a5.png](image/5b6600b8b6aebb5d9cbcd8616387d1a5.png)

![5efda214c68a0feab2e9b97166272097.png](image/5efda214c68a0feab2e9b97166272097.png)

轴心点是自己设置的，那个圆圈，center就是图片中心

![88c095e58fd25d6919a1561c15f624de.png](image/88c095e58fd25d6919a1561c15f624de.png)

选择2D游戏是否需要光照影响之类的

![90cdd605c20b0c004f2801bb2d095d82.png](image/90cdd605c20b0c004f2801bb2d095d82.png)

新建的层会显示在前面

![dc05f9f9f2817998d9019f2c8b13bf10.png](image/dc05f9f9f2817998d9019f2c8b13bf10.png)

![ca9896316d0a732bb82531830bf64fb4.png](image/ca9896316d0a732bb82531830bf64fb4.png)

![f37890c29923965fda9a6670c561f0ae.png](image/f37890c29923965fda9a6670c561f0ae.png)

自己写的

![72d3942ae6e457e51494e2e444ca029c.png](image/72d3942ae6e457e51494e2e444ca029c.png)

![32ecd444efc66b53281a131be5e42f7c.png](image/32ecd444efc66b53281a131be5e42f7c.png)

![ba25de280e378fc7de165e51a26fe053.png](image/ba25de280e378fc7de165e51a26fe053.png)

思路，将整个图集存入到字典中，然后再循环将具体的图片存入到字典中

![d13a7b8cd26dba3b9fd3dcd3ac2f3d60.png](image/d13a7b8cd26dba3b9fd3dcd3ac2f3d60.png)

![1dd2ebe32b2e7db6b5419f0017aa7e68.png](image/1dd2ebe32b2e7db6b5419f0017aa7e68.png)

![7248cddc71e0abcdbdcb19cf2743ed2e.png](image/7248cddc71e0abcdbdcb19cf2743ed2e.png)

传一个大图和小图名字

如果有大图则直接传回去小图

如果没有大图就动态加载并且存入到字典中，如果有小图则传回去，没有则返回null

![240f3fbd5174cb4f73a4774c21b8ffec.png](image/240f3fbd5174cb4f73a4774c21b8ffec.png)

![7e4f449c63371b7d2b883d89cfe9db01.png](image/7e4f449c63371b7d2b883d89cfe9db01.png)

删除图集就是清空字典和卸载资源

![ee72db962d40fba1ee7dbf49583ec155.png](image/ee72db962d40fba1ee7dbf49583ec155.png)

![2aadac0f9e7a33d8c35f8d7aac1cfa79.png](image/2aadac0f9e7a33d8c35f8d7aac1cfa79.png)

自己重写

![e55f055c874374526811e9ba35b3726d.png](image/e55f055c874374526811e9ba35b3726d.png)

![9172ea5a20749cc6f5fa6944ef4a185d.png](image/9172ea5a20749cc6f5fa6944ef4a185d.png)

![f62b0aee2008b1f20da3271e385cd443.png](image/f62b0aee2008b1f20da3271e385cd443.png)

注意：1.图片的轴心点最好在脚下，buttom

![aecdff9d9458ea7b9a42caac52f2efe5.png](image/aecdff9d9458ea7b9a42caac52f2efe5.png)

![2a2a4370660586e2550b50e29e5856c0.png](image/2a2a4370660586e2550b50e29e5856c0.png)
