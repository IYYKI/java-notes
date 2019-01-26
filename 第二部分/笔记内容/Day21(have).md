## 两种方式创建线程

​	1.继承	Thread 类

​	a 继承	Thread 类，覆盖run()方法，提供并发运程的过程

​	b		创建这个类的实例

​	c		使用start()   方法启动线程

​	2.实现 Runnable 接口

​	a 实现Runnable 接口，实现run()方法，提供并发运程的过程

​	b 创建这个类的实例，用这个实例作为Thread 构造器参数创建 Thread类

​	c 使用start () 方法启动线程

​	

​		class Foo implements Runnable{

​			public void  run (){

​				//..

​	}

}

​		Thread  t = new Thread (new Foo());

​		t.start

​	3.使用 内部类/匿名类	创建线程



## Sleep的打断唤醒

​	1.Thread.sleep(times) 是当前线程从 Running 放弃处理器进入Block 状态，休眠times 毫秒，

​	再返回到Runnable

​	2.一个线程可以提前唤醒另一个sleep Block 的线程 interrupt() 打断/中断

​	3.被唤醒线程出现异常 中断异常