## Java8 新特性
1. 函数式接口（Functional）
   @FunctionalInterface

** java内置的四大函数接口 ** 
1[](https://github.com/wangjianxiongwjx/java8/blob/master/docs/1562474988.jpg)

```
消费型接口：Consumer<T>     void accept(T t)
供给型接口：Suppler<T>      T get()
函数型接口：Function<T, R>  R applay(T t)
断定型接口：Predicate<T>    boolean test(T t)
```

2. 方法引用和构造器引用