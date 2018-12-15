## 异常（Exception）

#### 	1.异常的引出

A 行为（方法，过程）的意外结果

B Java 的异常是方法的意外结束

​	如：nextLine（）	nextlnt（）

#### 	2.Error	和	Exception的分类层次

Throwable 可抛出的，是错误的跟，包含异常类的实现代码

​	|--Error 是系统不可恢复的错误，由JVM 发生

​	|   |--OutOfMemoryError 堆内存溢出

​	|   |--StackOverflowError  栈内存溢出

​	|--Exception 程序可以检查处理的异常，常见的异常继承根

​		|--java.text.ParseException format 解析对象时候发生

​		|  如： Date d = dateformat.parse("2010-5-5");

​		|--RuntimeException 非检查异常，javac 忽略时

​			|	这类异常的语法检查，如：异常抛出，异常处理等。

​			|--IllegalArgumentException

​			|--NullPointerException *

​			|--ArraylndexOutOfBoundsException *

​			|--ClassCastException *

​			|--NumberFormatException *Interger.parselnt(S)

#### 	3.异常的处理

A 使用 try catch finally 捕获

B 声明抛出异常

​	try catch finally

try 是尝试运程代码块，如果有异常会被随后的 catch 捕获异常发生以后代码不执行



catch 代码块是异常处理代码。需要提供合理的处理，  异常的处理是

具体业务逻辑有关。可以写多个 catch 处理一系列异常，但是要注意：

异常的大小关系，大类型的方法哦后面处理。



finally 代码块，不管是否出现异常，总会执行的代码块。

经常用来处理现场的清理，比如：可靠的数据库连接关闭

