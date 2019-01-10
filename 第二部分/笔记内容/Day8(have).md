## 流的功能扩展

1 流的功能扩展：（流的设计模式：装饰器模式，灵活组合扩展功能（积木））

​	InputStream / OutpuStream Byte 流（字节流）

​	基本类型的 IO(int long) DataOutputStream / DataInputStream

​	文本类型（编码）IO

​		Write / Reader 字符流，每次处理一个字符

​		InputStreamReader / OutputStreamWriter

​		BufferReader(readLine()) / PrintWriter(println())

​		Scanner(Java 5)

​		Console(Java 6)

​		Scanner s = new Scanner(System.in);

​		Random random = new Random();

​	对象的 IO

​	图片的 IO

2.DataOutpuStream 对基本的输出流功能扩展，提供了基本数据

​	类型的输出方法，也就是基本类型是序列化方法

​	writeInt() writeDouble()

​	是过滤器

​				Dos				Fos

​	应用程序  —  过滤器  ——>输出流  ——>  文件（Byte）

​		   writeInt(i)	   write()		ff  ff  ff  fd

3. DataInputStream 对基本的输入流（InpuStream）功能扩展

   提供基本类型的输入方法，就是基本类型的反序列化

   ​	DataInpuStream 是过滤器，只是功能扩展，不能直接读取文件

   ​	readInt()		readDouble()...

   ​							Fis 		DIS		dis.readInt()

   文件(Byte 序列)—输入流—>过滤器-->	应用程序

   ​	[7f ff ff ff]	read()		readInt()		0x7fffffff

4. BufferdInpuStream  和  BufferedOutputStream



​	一般打开（in/out）文件，都加上缓冲流，提高IO性能

​				DOS		BOS		FOS

​	应用程序  —  过滤器  -- >过滤器  —>输入流  --文件（Byte）

​		writeInt(i)	write()	write(byte[])	ff ff ff fd

​						   byte[]

​	FileInputStream fis = new FileInpuStream(file);

​	BufferedInpuStream bis = new BufferedInputStream(fis);

​	DataInputStream in = new DataInputStream(bis);

​	FileOutputStream fos = new FileOutputStream(file);

​	BufferedOutputStream bos = new BufferedOutputStream(fos);

​	DataOutputStream out = new DataOutputStram(bos);