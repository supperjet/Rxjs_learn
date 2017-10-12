### 创建Observable -- from
[30 天精通 RxJS (06)： 建立 Observable(二)](https://juejin.im/post/59c9b738f265da0648446334)


from 可用来接收任何可列举的参数！之前的of对传入的数组会直接原封不动的返回，而from则可以将数组中的内容
遍历输出.

记得任何可列举的参数都可以用喔，也就是说像 Set, WeakSet, Iterator 等都可以当作参数！

>因为 ES6 出现后可列举(iterable)的型别变多了，所以 fromArray 就被移除囉。

另外 from 还能接收字串(string),会依次输出字符串的每个字符

demo: [](../examples/from.html)




