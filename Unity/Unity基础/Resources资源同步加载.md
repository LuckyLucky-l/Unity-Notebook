# Resources资源同步加载

![23d2e995fb19dd68ba13834a6f1c65be.png](image/23d2e995fb19dd68ba13834a6f1c65be.png)

```
在 Unity 中，Resources 文件夹中的资源是通过资源路径进行加载的。由于 Resources 文件夹中的资源类型是不确定的，因此在加载时返回的类型通常是 object。
Resources.Load 和 Resources.LoadAsync 方法都返回 object 类型，因为它们可以加载各种类型的资源，如纹理、音频、预制体等。在使用这些方法加载资源后，你需要将返回的 object 强制转换为你想要的实际类型，比如 Texture、AudioClip 或者 GameObject。
这种设计使得 Resources 文件夹非常灵活，因为你可以在其中存储各种类型的资源，并在运行时根据需要加载它们。但是需要注意的是，由于返回类型是 object，因此在强制类型转换时需要确保转换是安全的，否则可能会导致运行时错误。
```

![bf869235791816f9d232d69b7dd16181.png](image/bf869235791816f9d232d69b7dd16181.png)

![98c4f38851aa2c60aa4dff0a856d5767.png](image/98c4f38851aa2c60aa4dff0a856d5767.png)

![5612461bcc0dd711fee323a8b796856a.png](image/5612461bcc0dd711fee323a8b796856a.png)

![195cbd9883ec0684f2bd5c423d5f693f.png](image/195cbd9883ec0684f2bd5c423d5f693f.png)

![7779ff2f9f7574fda5906851853fa4ce.png](image/7779ff2f9f7574fda5906851853fa4ce.png)

![258abb87cf3888deb9c170ec31628834.png](image/258abb87cf3888deb9c170ec31628834.png)

![b87f7be60c66104ce2604d696b25c4cf.png](image/b87f7be60c66104ce2604d696b25c4cf.png)

![007fef86dd7d16429529546cf0b4da1b.png](image/007fef86dd7d16429529546cf0b4da1b.png)

![67996a1d477fea36702fac94a92761ac.png](image/67996a1d477fea36702fac94a92761ac.png)

![1854535f943004dc909549000432fd44.png](image/1854535f943004dc909549000432fd44.png)

![f81af618f45109a8f09d1695149c8c7a.png](image/f81af618f45109a8f09d1695149c8c7a.png)

![bcd70f7e695a5a5810e0c587dafed1cf.png](image/bcd70f7e695a5a5810e0c587dafed1cf.png)

![cc546b54c78542c47c82703ae6a04e60.png](image/cc546b54c78542c47c82703ae6a04e60.png)

![fa4a987e27cc66b90681360134795e38.png](image/fa4a987e27cc66b90681360134795e38.png)

![c31babd7529a851b8cbab69b2f83fc71.png](image/c31babd7529a851b8cbab69b2f83fc71.png)

![3438a658fc2442cf00763fbe483663d6.png](image/3438a658fc2442cf00763fbe483663d6.png)

![dcb01bd0e4269b06a7662d9d21386791.png](image/dcb01bd0e4269b06a7662d9d21386791.png)

如何解决每次要as一次？

![207780c5cc02a0af2283dcf6b02b2946.png](image/207780c5cc02a0af2283dcf6b02b2946.png)

一般都会使用泛型，Load高级版，基于上面的方法

![3901345384c4e9b3a22827bf05c8319b.png](image/3901345384c4e9b3a22827bf05c8319b.png)

![e93c03b964e878d39100ca8221a19041.png](image/e93c03b964e878d39100ca8221a19041.png)

![94cf0bb851aedd1d01667e66c359c208.png](image/94cf0bb851aedd1d01667e66c359c208.png)

如果同时加载多次会浪费资源吗？

不会，只存在性能浪费，不存在性能浪费

![4c1006c5d9a00cdd73e13c8a9b7a36f9.png](image/4c1006c5d9a00cdd73e13c8a9b7a36f9.png)
