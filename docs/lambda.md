## Java8 新特性
1. Lambda 表达式的使用
   -> ：lambda 操作符 或者 箭头操作符
   -> 左边：lambda表达式的形参列表（其实就是接口中的抽象方法的形参列表）
   -> 右边：lambda 体 （其实就是重写的抽象方法的方法体）

```
           语法格式一： 无参，无返回值 
	public void testLambda() {
		Runnable r1 = new Runnable() {
			@Override
			public void run() {
				System.out.println("我爱天安门");
			}
		};
		r1.run();
		
		Runnable r2 = () -> System.out.println("我爱故宫");
		r2.run();
	}
```

```
	语法格式二：lambda表达式需要一个参数，但没有返回值
	public void testLambda1() {
		Consumer<String> con = (String s) -> {
			System.out.println(s);
		};
		con.accept("谎言和誓言的区别是什么？");
	}
```

```
	语法格式三： 数据类型可以省略因为可以由编译器推断得出， 称为 类型推断
	List<String> list = new ArrayList<>();
	
	语法格式四：lambda 若只需要一个参数时参数的小括号可以省略
	Consumer<String> con1 = s -> {
		System.out.println(s);
	};
```

```
	语法格式五： lambda 需要两个或者以上参数，多条执行语句，并且可以由有返回值
	Comparator<Integer> con3 = (o1, o2) -> {
		System.out.println(o1);
		System.out.println(o2);
		return o1.compareTo(o2);
	};
```

```
	语法格式六： 当lambda 体只有一条语句时，return与大括号都可以省略
	Comparator<Integer> con3 = (o1, o2) -> o1.compareTo(o2);
```

















