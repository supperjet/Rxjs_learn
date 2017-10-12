### 创建Observable -- of
如果想要同步的传递几个值，可以使用of构造器。

```
Rx.Observable.of(something)

```

其中something可以是

1.string 形式可以是下面这两种

```
var string1 = 'he';
var string2 = 'she';
var source = Rx.Observable.of(string1, string2);

```

```

var source = Rx.Observable.of('he', 'she');

```

2.array 

```
var arr1 = [{a: 1}, 'b', function(c){return c;}, 0];
var arr1 = [{a: 1}, 'b', function(c){return c+c;}, 0];
var source1 = Rx.Observable.of(arr1, arr2);

```
会同步的输出arr1， arr2. 数组元素的类型可以string， number, object, arr 。。。
在observer中可以对返回的数组做处理，比如observer

```
var observer = {
    next:function(value){
        //1.输出数组中的值
        console.log(value[1]);
        //2.执行数组中的方法
        value[2](5)
    }
}

```

3. Object
传入Object的行为与array一样，都会同时返回传入的值，可以多对象的属性进行操作。

3.function
返回函数，可执行

总结： of会同步的的传递的值，传递的值包括string, array ,object, function等




