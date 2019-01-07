## StringBuffer 和 StringBuilder

1.StringBuilder 是变长字符序列

2.StringBuilder 方法：append，insert ... 都返回

   当前 StringBuilder 对象本身的引用

3.如果软件需要大量字符串处理时候建议使用 StringBuilder

4.String s = s1+s2; Java实际上才是如下代码运行：

​	String s = new StringBuilder(s1)

​	.append(s2).toString();

String s = s1+s2+s3+s4;被优化为

​						String s = new StringBuilder(s1).append(s2)

​															    .append(s3).append(s4).toString();

s+="a";//会产生两个新对象（StringBuilder,String）

s+="a";//会产生两个新对象

StringBuilder buf = new StringBuilder();

buf.append("a");

buf.append("a");

5.StringBuffer 和 StringBuilder API 几乎一样！

​	StringBuffer 是java早期提供的，速度稍慢，线程安全

​	StringBuffer 是java 5 以后提供的，速度快，非线程安全

