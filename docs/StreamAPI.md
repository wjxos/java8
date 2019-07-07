## Java8 新特性

1. Stream API
集合讲的是数据，Stream讲的是计算
关注的是对数据的运算，与CPU打交道

创建Stream的方式： 通过集合
```
default Stream(E) Stream() : 返回一个顺序流
default Stream(E) parallelStream() ：返回一个并行流

public void test1() {
	List<Employee> employee = new ArrayList<>();
	//default Stream(E) Stream() : 返回一个顺序流
	Stream<Employee> stream = employee.stream();
	
	//default Stream(E) parallelStream() ：返回一个并行流
	Stream<Employee> parallelStream = employee.parallelStream();
}
```

```
default Stream(E) Stream() : 返回一个顺序流
default Stream(E) parallelStream() ：返回一个并行流

public void test1() {
	List<Employee> employee = new ArrayList<>();
	//default Stream(E) Stream() : 返回一个顺序流
	Stream<Employee> stream = employee.stream();
	
	//default Stream(E) parallelStream() ：返回一个并行流
	Stream<Employee> parallelStream = employee.parallelStream();
}
```
