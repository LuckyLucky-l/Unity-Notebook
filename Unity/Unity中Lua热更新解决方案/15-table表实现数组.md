# 15.table表实现数组

![c7d28730bc56c0533032f2ad58bb2d45.png](image/c7d28730bc56c0533032f2ad58bb2d45.png)

![3b725a0c6552a4b96575b94404f99caa.png](image/3b725a0c6552a4b96575b94404f99caa.png)

![1f124d7f7cb8da66b96dd2e393a94ed2.png](image/1f124d7f7cb8da66b96dd2e393a94ed2.png)

![b7a170ced5cebf7c3e696034fae5206d.png](image/b7a170ced5cebf7c3e696034fae5206d.png)

![8ae02a99eba1a718a934b64c35d974d2.png](image/8ae02a99eba1a718a934b64c35d974d2.png)

```
-- 创建一个表
local t = {1, 2, 3}
-- 插入元素
table.insert(t, 2, 10)  -- t 变为 {1, 10, 2, 3}
-- 删除元素
table.remove(t, 2)      -- t 变为 {1, 2, 3}
-- 连接元素
local str = table.concat(t, ", ")  -- str = "1, 2, 3"
-- 排序元素
table.sort(t)  -- t 变为 {1, 2, 3}
-- 解包元素
local a, b, c = table.unpack(t)  -- a = 1, b = 2, c = 3
-- 移动元素
local src = {1, 2, 3, 4, 5}
local dest = {}
table.move(src, 2, 4, 1, dest)  -- dest 变为 {2, 3, 4}
-- 清空表
table.clear(t)  -- t 变为空表
```
