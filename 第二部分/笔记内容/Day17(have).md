## Java IO 总结

##### 1.是一种数据操作模型：把任何数据都作为Byte的有序集合看待逐一处理的方式叫做流。

##### ​	Java 流模型，是byte by byte 是数据集合

##### 		data	: 41 42 00 00 ff ff d6 d0

##### 		index	: 0	1	2	3	4	5	6	7	8

##### 		pointer	:	^

##### 	RandomAccessFile	只能操作文件，只能处理基本类型

##### 	节点流：流开始和结束的地方

##### 	过滤器：每次处理一个byte

##### 	字符流：每次出来一个char

​	

##### 	ObjectInputStream in = new ObjectInputStream(

##### 		new CipherInputStream(

##### 			new FileInputStream(file)));

##### 	Object obj = in.readObject();

##### 	CipherInputStream in = new CipherInputStream(

##### 		new FileInputStram(file));

##### 	img = ImagelO.read(in);

​	

##### ​	装饰器模式：流的 API 是按照装饰器模式设计的



##### ​	InputStram 最基本的输入流操作模型，是抽象类read()是没有实现的

##### ​	|--FileInputStram 实现了在文件上读取的方法	read(),节点流

##### ​	|--ByteArrayInputStream 实现了在数组里读取的方法	read()

##### ​	|--FileInputStream 过滤流，包装在一个基本流外部，提供功能扩展

##### 	|	|--DataInputStream 为基本流扩展流基本数据类型读取

##### ​	|	|	readInt()	readBouble()…方法的底层是 read()

##### ​	|	|--BufferdInputStream 为最基本流提供缓冲处理

##### 	|	|--CipherInputStream	解密流入流

##### 	|	|--ZipInputStream 解压流入流

##### 	|--ObjectInputStream 对象输入流，也是过滤器

​	

##### ​	OutputStream 最基本的输出流操作模型,是抽象类write()是没有实现的

##### ​	|--FileOutputStream 实现了在文件上写出的方法 write(),节点流

##### 	|--ByteArrayOutputStream 在变长数组上实现了 write() 方法

##### 	|--FilterOutputStream

##### 	|	|--DataOutputStream	基本类型输出

##### 	|	|

##### 	|	|--BufferedOutputStream	缓冲输出

##### ​	|	|--CipherOutputStream	加密输出

##### 	|	|--ZipOutputStream 压缩输出

##### 	|--ObjectOutputStream 对象输出流

​	

##### 	字符流，每次处理一个字符



##### 	Reader 抽象类，定义了抽象方法 read(),每次读取一个字符

##### 	|--InputStreamReader 也是过滤器，将byte序列解码为char序列

##### 	|	底层也是依赖基本的byte输入流

##### 	|--BufferedReader(Scanner)是字符流过滤器

##### 	|	有常用的文本读取方法 readLine()

##### 	|--FileReader	底层是	FileInputStream + InputStreamReader

##### 	|	不能只指定读取文件的字符编码



##### 	Writer	抽象类，定义抽象方法 wrtie() 每次写出一个字符

##### 	|--OutputStramWriter	也是过滤器，将char序列编码为byte序列

##### 	|	底层也是依赖基本byte输出流

##### 	|--PrintWriter 是过滤器，提供了常用方法 pirintln()

##### ​	|	非常常见的文本处理方法

##### ​	|--FileWriter = OutputStreamWriter + FileOutputStream

##### ​	|	不能指定文本输出编码，不好用！