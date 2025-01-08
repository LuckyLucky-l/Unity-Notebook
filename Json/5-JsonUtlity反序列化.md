# 5.JsonUtlity反序列化

![3a74edb222e1918b7fa7b648e7c94f0b.png](image/3a74edb222e1918b7fa7b648e7c94f0b.png)

![dd818983619320c7b010cd8d16db8925.png](image/dd818983619320c7b010cd8d16db8925.png)

1.数据集合就是这种list类型的，直接由Excel转换而来的数据

![702ea9b098c0f687d30f6dbe290fef08.png](image/702ea9b098c0f687d30f6dbe290fef08.png)

![7f59de10963b61018d62b1fb8aa19667.png](image/7f59de10963b61018d62b1fb8aa19667.png)

直接读取会报错

![0f5ba5035966bfe73629f98fd246543d.png](image/0f5ba5035966bfe73629f98fd246543d.png)

![24016301fe0119c2ddc539cb94cf2a4c.png](image/24016301fe0119c2ddc539cb94cf2a4c.png)

那如何解决呢？

把这个数据类，再包裹一层List类型的类，且将.Json文件修改成由对象包裹的形式

![a81827174087ecb5dc9ebb0c414378ee.png](image/a81827174087ecb5dc9ebb0c414378ee.png)

![2bedce54efbe85c4cce36fa8573fd47d.png](image/2bedce54efbe85c4cce36fa8573fd47d.png)

![e859c1a3fc8f965a0364f0179f5f9e6f.png](image/e859c1a3fc8f965a0364f0179f5f9e6f.png)

2.除UTF-8以外，其他类型读取都会报错

![bc382d979c57a025a0d43ebdde0cfbe8.png](image/bc382d979c57a025a0d43ebdde0cfbe8.png)

![4ab7aab4c9a7de34e59d586a9954277e.png](image/4ab7aab4c9a7de34e59d586a9954277e.png)

![289c515017f86c9504aedc765f9eb237.png](image/289c515017f86c9504aedc765f9eb237.png)

![0dd30dce9a9a4cb39280e08c33df0a7d.png](image/0dd30dce9a9a4cb39280e08c33df0a7d.png)

![87ede91863a235e9a4d8923cccaf6a21.png](image/87ede91863a235e9a4d8923cccaf6a21.png)

![d978cae2ee1d707869ad0ad7529c3df4.png](image/d978cae2ee1d707869ad0ad7529c3df4.png)

![3bdb8dc66886a51addf09c2fa0214d90.png](image/3bdb8dc66886a51addf09c2fa0214d90.png)

总结：

1. **读取文件**：使用 **File.ReadAllText** 方法将JSON文件的内容读取为字符串。
2. **反序列化**：使用 **JsonUtility.FromJson** 方法将读取到的JSON字符串转换为相应的对象或对象列表。
3. **使用类装载数据**：将反序列化得到的数据存储在相应的类实例中，以便后续操作。
