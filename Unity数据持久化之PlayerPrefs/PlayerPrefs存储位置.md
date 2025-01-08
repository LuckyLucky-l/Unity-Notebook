# PlayerPrefs存储位置

![d1124abb8994f397b1a865c6ca84e08b.png](image/d1124abb8994f397b1a865c6ca84e08b.png)

![bfdc02fc776b06a5f3d4730d3918e451.png](image/bfdc02fc776b06a5f3d4730d3918e451.png)

![9a23c7db1dc344ee4e71852b88120e17.png](image/9a23c7db1dc344ee4e71852b88120e17.png)

![8f2874c8811c9f3511a0224ecdd3ea5c.png](image/8f2874c8811c9f3511a0224ecdd3ea5c.png)

![5aa4aec34f8ba0989babca2ad16e950f.png](image/5aa4aec34f8ba0989babca2ad16e950f.png)

---

---

![939d47ada04ecb28d9d1bef49da516bb.png](image/939d47ada04ecb28d9d1bef49da516bb.png)

1.如何避免不同的玩家之间的数据覆盖？

答：不同玩家传不同的string与键名拼接，组成玩家独特的键值对（传参）

![4eb2b16d8e3c65294d57a24d8c9ec941.png](image/4eb2b16d8e3c65294d57a24d8c9ec941.png)

![3034beff19af3e2d024a965d19c45891.png](image/3034beff19af3e2d024a965d19c45891.png)

![a52734f6ee54ff2970097c062d57aae7.png](image/a52734f6ee54ff2970097c062d57aae7.png)

![5ec916686e9e1591eb2ec8616cee5d21.png](image/5ec916686e9e1591eb2ec8616cee5d21.png)

2.怎么用呢？

![72f7f3b436ec0984e2edf5a3665faac5.png](image/72f7f3b436ec0984e2edf5a3665faac5.png)

3.为什么列表不用避免重复？

![e17f3ff75b3bf1f9cbd50ae6965d232a.png](image/e17f3ff75b3bf1f9cbd50ae6965d232a.png)

答：因为不同的玩家会创建不同的player类，不同的player类实例化的列表不一样

![39522f86e103755e8b4aae53da74b01e.png](image/39522f86e103755e8b4aae53da74b01e.png)

---

---

![d79682760b137efe01085ccb25ad3b8a.png](image/d79682760b137efe01085ccb25ad3b8a.png)

**Phb 类：**

- **构造函数 (****Phb()****)：�**�
    - 输出日志，表示正在创建 **Phb** 对象。
    - 调用 **Load()** 方法加载排行榜数据。
    - 输出日志，表示已经从 PlayerPrefs 中加载了一定数量的排行榜数据。
- **phbxxes** **列表：**
    - **List<Phbxx>** 类型的列表，用于存储排行榜中的每个条目。
- **add** **方法：**
    - 接收玩家的名称、得分和时间作为参数，创建一个新的 **Phbxx** 对象，并将其添加到 **phbxxes** 列表中。
- **Save** **方法：**
    - 保存排行榜数据到 PlayerPrefs 中。
    - 使用 **PlayerPrefs.SetInt** 存储排行榜条目的数量。
    - 使用循环遍历 **phbxxes** 列表，并使用 **PlayerPrefs** 分别存储每个 **Phbxx** 对象的名称、得分和时间。
- **Load** **方法：**
    - 从 PlayerPrefs 中加载排行榜数据。
    - 获取排行榜条目的数量，如果没有存储则默认为 0。
    - 使用循环遍历 PlayerPrefs，根据存储的键名获取每个排行榜条目的名称、得分和时间，并创建相应的 **Phbxx** 对象，然后添加到 **phbxxes** 列表中。

**Phbxx 类：**

- **Phbxx** 类表示排行榜中的一个条目，包含名称、得分和时间。

![5196066ad40d2f2c34db83651a580ee2.png](image/5196066ad40d2f2c34db83651a580ee2.png)

![92a115e5b613cea99ce104a62552b883.png](image/92a115e5b613cea99ce104a62552b883.png)
