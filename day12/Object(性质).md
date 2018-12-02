#### 自反性：对于任何非空引用值x，x.equals(x)都应返回 true



#### 对称性：对于任何非空引用值 x 和 y，当且仅当 y.equals(x)返回true时，

#### x.equals(y)才应返回true。



#### 传递性：对于任何非空引用值x、y和z，如果x.equals(y)返回true，并且

#### y.equals(z)返回true，那么x.equals(z)应返回trus



#### 一致性：对于任何非空引用值 x 和 y，多次调用 x.equals(y)始终返回true

#### huo始终返回false，前提是对象上 equals比较中所用的信息没有被修改



#### 对于任何非空引用值 x，x.equals(null)都应返回 false