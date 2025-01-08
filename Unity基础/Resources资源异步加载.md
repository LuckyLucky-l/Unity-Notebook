# Resources资源异步加载

![3bbf556fcb2a7bdc9bfa3c7bcb14e468.png](image/3bbf556fcb2a7bdc9bfa3c7bcb14e468.png)

![5201b5602b7505e0edbc739e40a9efa6.png](image/5201b5602b7505e0edbc739e40a9efa6.png)

![4acae66d5aa3be4fde632b2dd9d83050.png](image/4acae66d5aa3be4fde632b2dd9d83050.png)

---

---

同步加载会将全部资源加载到内存中，如果文件过大，可能会造成每16.66ms加载不玩所有文件

这样就会造成卡顿

![b77287a2b4be757de6e42a3274c51d07.png](image/b77287a2b4be757de6e42a3274c51d07.png)

异步加载是新开一条线程然后用来加载资源，加载完了主线程再使用

![4fce5fc31d125022d50724d8d707813d.png](image/4fce5fc31d125022d50724d8d707813d.png)

![f2128d8dfeb9d141604e93dead461a44.png](image/f2128d8dfeb9d141604e93dead461a44.png)

![a74f9ab1fb3eb59e0d270fada6f48b8f.png](image/a74f9ab1fb3eb59e0d270fada6f48b8f.png)

![5e18c259553582cc69bc1258905bce62.png](image/5e18c259553582cc69bc1258905bce62.png)

![8027a140fd85641ae9cf7c8ae52d6a7c.png](image/8027a140fd85641ae9cf7c8ae52d6a7c.png)

LoadAsync会新开一个线程进行资源处理

completed事件监听，监听资源加载结束

Load函数写具体的资源加载逻辑

![2a5978fc16af792a8e1f6e9e8271dcf0.png](image/2a5978fc16af792a8e1f6e9e8271dcf0.png)

![84747cbc734584bc92e9bd8524aac528.png](image/84747cbc734584bc92e9bd8524aac528.png)

![865beaffa71425728d6b90f04ff415c6.png](image/865beaffa71425728d6b90f04ff415c6.png)

![c2326ad98118e2e91833240163224721.png](image/c2326ad98118e2e91833240163224721.png)

![a1ff8b51696d54cdc0911015b2f4521d.png](image/a1ff8b51696d54cdc0911015b2f4521d.png)

![61f44530fc388d8d0c4475d0f52b1169.png](image/61f44530fc388d8d0c4475d0f52b1169.png)

![3f4307b8e9e0e1d60234f9f90221bdee.png](image/3f4307b8e9e0e1d60234f9f90221bdee.png)

![eadc4c7f4462665f385282ed14914083.png](image/eadc4c7f4462665f385282ed14914083.png)

总结：

加载一个资源用监听函数加载函数

加载多个资源拼接，用协程加载函数

![48fbf1d4accbc59e2e9913c876866c0a.png](image/48fbf1d4accbc59e2e9913c876866c0a.png)

测试类：

![f84e0c010c0d39069ff1bfede3dbde54.png](image/f84e0c010c0d39069ff1bfede3dbde54.png)

资源管理类：

![936344b2cc1e1e5d1aa2eb1dbf743e81.png](image/936344b2cc1e1e5d1aa2eb1dbf743e81.png)

如果不封装是怎么样的？

![2338d21d616ff45eaa12c074afdf9189.png](image/2338d21d616ff45eaa12c074afdf9189.png)

用协程的方法写：

![ec3ebef5cf6c19ef76ffe9a676f714d3.png](image/ec3ebef5cf6c19ef76ffe9a676f714d3.png)

![0db28bbe65c2f96b28c2fab3cab13913.png](image/0db28bbe65c2f96b28c2fab3cab13913.png)

---

---

![6501d9d15d4adff73266b74c572c0505.png](image/6501d9d15d4adff73266b74c572c0505.png)

![2d7572a80552686e9c41c194957c28b6.png](image/2d7572a80552686e9c41c194957c28b6.png)
