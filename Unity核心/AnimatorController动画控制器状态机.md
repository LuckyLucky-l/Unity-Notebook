# AnimatorController动画控制器状态机

![1d49f9114e2591f74929794bc4a6cc93.png](image/1d49f9114e2591f74929794bc4a6cc93.png)

1.为一个对象创建动画时会自动创建状态机文件

2.手动创建状态机文件按

![ac8dbc6cbc253973c8ac1e732cb70288.png](image/ac8dbc6cbc253973c8ac1e732cb70288.png)

![9b265a18f0987a630e813287dfdd6f3c.png](image/9b265a18f0987a630e813287dfdd6f3c.png)

![87c7b55afec6ccb6a3f61a8a6d80645e.png](image/87c7b55afec6ccb6a3f61a8a6d80645e.png)

![391d50cdbc75356a919962c192e4c703.png](image/391d50cdbc75356a919962c192e4c703.png)

补充：

层级覆盖主要看权重的多少

![ba2aba3369572905919c656dc1ad8ae2.png](image/ba2aba3369572905919c656dc1ad8ae2.png)

状态：

![de17eba8210bfcc0fcebebe17b3f5a8b.png](image/de17eba8210bfcc0fcebebe17b3f5a8b.png)

切换状态：

![cd6a86aacd2fe4cab5584db3b83064d3.png](image/cd6a86aacd2fe4cab5584db3b83064d3.png)

设置连线

![54db97e57aab60c0492c5cc0b5004bc7.png](image/54db97e57aab60c0492c5cc0b5004bc7.png)

设置本层默认动画

![05720a53d09c7195349eac5ed6eae260.png](image/05720a53d09c7195349eac5ed6eae260.png)

![5bea4c40dfec7870575587a8d82e896e.png](image/5bea4c40dfec7870575587a8d82e896e.png)

![534d51cf51deb5e94e9fa00c99c54ad9.png](image/534d51cf51deb5e94e9fa00c99c54ad9.png)

![357a8c646bd5b4d979abd6de37142731.png](image/357a8c646bd5b4d979abd6de37142731.png)

![bf343e67f5f556cceadcfb9b42ff2ad7.png](image/bf343e67f5f556cceadcfb9b42ff2ad7.png)

可以添加多个动画，只有所有的条件都满足了才会执行后面的动画

![ce190819a3be25a9e5ebdda925dfe74a.png](image/ce190819a3be25a9e5ebdda925dfe74a.png)

特别注意：

![03db819d5859ecb0f5f0ece3408a4ae6.png](image/03db819d5859ecb0f5f0ece3408a4ae6.png)

eg:

没按一下TriggerValue同意，就会执行一次2，然后再次切换到1，等待下一次Trigger

![d0bcd829a919b4b6bc10a8d47e51d967.png](image/d0bcd829a919b4b6bc10a8d47e51d967.png)

动画状态机的设置

![efacf4bfbea440a85306aed61c182345.png](image/efacf4bfbea440a85306aed61c182345.png)
