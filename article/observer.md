### 1. 什么是观察者
因为Observable可以被订阅，即
```
observable.subscribe(observer);

```
被订阅的事件———observer，被称为观察者

observer有3个methods:
next: 每当observable发送新值，next方法就会被调用
complete:  在observable没有其他的资料可以取得时，complete方法就会调用，next方法不会再起作用
error: 当observable发生错误时调用

创建形式参考：observer.html

[30 天精通 RxJS (05)： 建立 Observable(一)](https://juejin.im/post/59c9b6d3f265da065815358a)