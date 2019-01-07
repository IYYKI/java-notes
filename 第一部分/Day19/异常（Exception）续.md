### 异常（Exception）

​	4.异常的分类

A 检查异常 异常检测规则：

​    一个方法如果抛出了异常，这个方法就必须声明异常的抛出.

​    	调用抛出异常的方法，必须处理异常。

B 非检查异常

​    Javac 忽略时 RuntimeException 的检查，包括子类型

​	5.异常的处理原则 与忌讳

A 能够底层处理的尽量处理，但是如果不能处理，必须抛出到调用者（方法）。

B 建议在捕获到异常时候使用 e.printStackTrace()，打印到控制台，输出内容

是：出现异常时候的方法调用堆栈。



​	忌讳：

A 不应该简单的抛弃

B 不建议 粗粒度处理异常 如：catch(Exceptione).

处理方式，依赖于具体业务逻辑，很灵活。

​	6.异常的实例：

​		User reg(String pwd,String email)

​			throws UserException;

​		User login(String email,String pwd)

​			throws NameOrPwdException;



​	自定义异常类一般继承与 Exception

​	软件中会大量使用自定义异常，一般从 Exception 继承。

​	异常类命名要有实际意义，一般都手工继承父类的构造器。