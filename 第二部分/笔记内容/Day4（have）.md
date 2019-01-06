### 1.Java.io.File

​	用于表示文件（目录）；只用于表示文件（目录）

​	的信息（名称，大小等）不能对文件的内容进行访问

### 2.Java.io.File 基本 API

​	File(String)

​	long  length()					long lastModified()

​	String  getName				String  getPath()

​	boolean   exists()				

​	boolean   dir.isFile			boolean   dir.isDirectory()

​	boolean   mkdir()				boolean   mkdirs()

​	boolean   delete();

​	boolean createNewFile()  throw IOException File [] ListFile()

### 3.回调模式的FileFilter

​	File [] ListFile(FileFilter)

### 4.java.io.RandomAccessFile

​	可以访问（读/写）一个文件中任意位置的字节信息

​	//arg0	要访问的文件

​	//arg1	访问的模式 “r” 只读模式，"rw"读写模式

​	RandomAccessFile(File String) shows FileNotFoundException

