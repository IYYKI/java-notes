#### ·Java运算符

##### 〉Java运算符分类

   ·数学运算符： +  -  *  /  %

   ·关系与逻辑运算符：>,   <,   >=,   <=,   ==,   !=,   &&,   ||,   !,  |,

   ·自增运算：++，--

   ·条件运算：     ？    ：

〉常用运算符的运算规则

#####    》运算规则：

·同类型参与运算（必要时候自动转换）

·返回同类型（可能发生：上溢出和下溢出）

·整数除法是整除

·byte, short,char 按照int运算

·Java中字面量的运算被Javac优化了，优化为固定的常量。

#####   》取于运算：%

·0%5 -> 0, 2%5->2,   5%5->0,   -1%5->-1

·i=0;  y=i++%5 是周期函数

#####   》字符串的连接运算：+

·任何数据与字符串连接（+）都会生成新的字符串

·“,”+2 -> ",2"

·','+2 -> //错误，返回整数

〉关系与逻辑运算符

· 关系运算：>,<,>=,<=,,==,!=

·逻辑运算：&&，||，！，|，&

·& | 是非短路运算

·&& || 是短路的逻辑运算，大多使用 短路运算

〉实例

·int 	age	=12;

·char sex =‘男’；

·boolean isChild = age<16；

·boolean isMan = sex=='男';

·boolean isBoy = isChild && isMan;

·boolean isGirl = isChild && ! isMan;

·boolean isKid = isBoy || isGirl;

​	〉自增运算

·i++,后++，先将i的值作为整个表达的值，然后将i增加1.

·++i，先++，先将i增加1，让后将i的值作为整个表达的值。

   〉如：

·int a =1; int = b =1;

·b = a++;//

1.a++表达式的值是1

2.执行a=a+1

3.执行赋值运算，将表达式的值1赋值给b，即b=1

  〉条件运算

·布尔表达式？（true表达式）：（false表达式）

 〉计算分页数量

·int rows = 23;数据行数

·int size = 10；每页行数

·int pages； //页数

row

·pages = rows%siaz == 0 ? Rows/size:rows/size+1

if(布尔表达式){

​     //...

}else{

//...



##### switch（整数表达式）{//byte , short, char , int}

Case 整数常量1://必须是整数兼容的常量

执行语句序列1；结束当前switch语句块

case 整数常量2:

执行语句序列2；

break；

default；

〉常用运算符的优先级和结合型

#### ·Java运算符使用技巧

### ·选择控制结构

### ·循环

#### ·for（初始化表达式；布尔表达式；递增表达式）{

##### 关键字 break; continue;

·//循环体}

}

案例：

Int sum = 0;

for(int i =1;i<10;i=i+2){

​	sum+=i;//sum=sum+i;i+=2

}

System.out.println(sum);

​                                    							——2018/11/4（待填补）