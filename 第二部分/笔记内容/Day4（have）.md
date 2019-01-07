### 1.Java.io.File

​	用于表示文件（目录）；只用于表示文件（目录）

​	的信息（名称，大小等）不能对文件的内容进行访问

​	File 代表文件系统中对文件/目录的管理操作（增删改查，CRUD）

### 2.Java.io.File 基本 API

任务    A	检查当前文件夹中是否包含目录	demo

​	    B  如果没有demo，就创建文件夹	demo

​	    C  在demo中创建文件 test.txt

​	    D  显示demo中文件夹的内容

​	    E   显示test.txt的绝对路径名

​	    F   显示test.txt 的文件长度和创建时间

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

