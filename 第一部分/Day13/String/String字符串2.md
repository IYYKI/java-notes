### String 字符串----

##### 				--------------一串字符就是字符串：char[] ， String ， StringBuilder

1. ##### 字符串“字面量”都是String类型实例	String 内部就是一个char[].

2. ##### String API 有一个实现原则：对象内容永远不变 也就是说：String对象永远不变

3. ##### String 字面量（直接量），如果相同，会替换为同一个String对象的引用，常量

#####        连接的结果也会被优化为一个字符串

##### ​	String s =new String("abc");

#####   4.String 的比较，equals ， hashCode（）

#####   5.String API（字符串的常用方法）

#####      这些方法如果返回String 一定是一个新String对象 toString（）除外

#####   字符串中的字符有序号，从0开始

##### API  方法：详细请看：/Users/yaoyukai/Documents/java/java基础/Day13/String/String API.md