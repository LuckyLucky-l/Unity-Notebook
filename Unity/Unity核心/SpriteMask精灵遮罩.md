# SpriteMask精灵遮罩

![5e12df294e19a4ad8d77b236714437f5.png](image/5e12df294e19a4ad8d77b236714437f5.png)

![0e5b9aa3c75602bd510335d56ff86700.png](image/0e5b9aa3c75602bd510335d56ff86700.png)

怎么创建遮罩

![4c0bf5d2e421fb7683f9835f1e94a72c.png](image/4c0bf5d2e421fb7683f9835f1e94a72c.png)

![720903f8d05ab7e9ce11d9f3fbdb5aad.png](image/720903f8d05ab7e9ce11d9f3fbdb5aad.png)

![a4cecdf941d2b47ff1c4af73814c91ce.png](image/a4cecdf941d2b47ff1c4af73814c91ce.png)

效果

![8901b49a749b3d6889da561285f8627b.png](image/8901b49a749b3d6889da561285f8627b.png)

参数设置

![a7959e5ff0b0e938bd9e3aa62c2beecf.png](image/a7959e5ff0b0e938bd9e3aa62c2beecf.png)

Alpha Cutoff：透明度如果是渐变的可以设置具体的一个分界点0~1

Custom Range：只有大于等于Back小于Front的层级范围才能被影响

当游戏有多个遮罩，每个层级的遮罩需要不同设置时，可以投选自定义遮罩Custom Range

排序层新加的层都会比上一级高，所以无论图片层级填多少，只要是default就会比new layer层级低

![dd10aabd189d7f626b03ca42f502fa74.png](image/dd10aabd189d7f626b03ca42f502fa74.png)

![7459ed8a6eacb78e0bc1525ee278c0fb.png](image/7459ed8a6eacb78e0bc1525ee278c0fb.png)

作业：

![fc382907501259463f15a89187a11441.png](image/fc382907501259463f15a89187a11441.png)

先创建一个小图不需要产生遮罩，层级0层

再创建一个大图设置遮罩显示，层级1层

放大镜遮罩的显示应该是最上层，层级0或1层

![动画.gif](image/动画.gif)
