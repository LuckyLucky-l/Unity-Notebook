# 结合反射——List数据类型存储

![b8bfca6ae5099db43a6693353678b7b0.png](image/b8bfca6ae5099db43a6693353678b7b0.png)

1.传入数据，拆掉字节段一次一次的调用save()存储

2.判断是否是list对象——>只要都是IList中的子类就是

3.是list对象之后，递归重新拆分类型，存入

<span style="background-color: #ffaaaa"><span style="background-color: #ffaaaa">（int,float（list）），int,float存完了，得把list单独重新拆一遍，变成int,float，这样list中的数据才能都存储</span></span>

![3b4fa1552c16466fe938f62409fcb933.png](image/3b4fa1552c16466fe938f62409fcb933.png)

---
