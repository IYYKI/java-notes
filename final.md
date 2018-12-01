### final（最终的）

​	〉1 final 修饰的类，不能再被继承

··Java的String就是final类，不能被继承！Math也是final类

··在实际项目开发中，原则上不允许使用final类！如：spring，

Hibernate，Struts 2，这些框架经常动态代理（动态继承）技术。

使用finale的类可能造成这些框架的工作问题

​	〉2 final 修饰的方法，不能再被覆盖

··在实际项目中，原则上不允许使用final方法

​	〉3 final 修饰的变量，初始化以后不允许再修改了

··a final 局部变量

··b final 方法参数

··c final 成员变量

​	〉4 final static——Java使用final  static修饰的变量作为常量

一般要求常量名都有大写字母

 Public static void main (Sting [] args){

}

java(jvm)->day01.HelloWorld.main(strs)