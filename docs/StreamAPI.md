## Java8 新特性

1. Stream API
集合讲的是数据，Stream讲的是计算
关注的是对数据的运算，与CPU打交道

**创建Stream的方式： 通过集合**

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

**创建方式二，通过数组**

```
public void test2() {
	int [] arr = {1,2,3,4,5,5,6};
	//调用Arrays类的static<T> Stream<T> stream(T[] array) : 返回一个流
	IntStream stream = Arrays.stream(arr);
	
	Employee e1 = new Employee(1, "tome", 12);
	Employee e2 = new Employee(2, "toni", 13);
	Employee[] arr1 = new Employee[]{e1, e2};
    Stream<Employee> stream1 = Arrays.stream(arr1);
}
```

**创建方式三：通過Stream的of()**

```
public void test3() {
	Stream.of(1,2,3,4,5,5,6);
}

```	


**方式四：创建无限流**

```
 //迭代 static<T> Stream<T> iterate(final T seed, final UnaryOperater<T> f)
public void test4() {
	Stream.iterate(0, t -> t +2 ).limit(10).forEach(System.out :: println);
}
```






