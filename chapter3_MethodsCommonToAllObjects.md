# 对于所有对象都通用的方法

**10.覆盖equals时请遵守通用约定**

- Object类的对象相等是什么概念？
- 哪些情况下不应该覆盖equals方法？
- 哪些情况下应该覆盖equals方法？
- 讲一讲值类？
- 重写equals方法时，应该遵守哪些约定？
- 什么是等价关系？
- 有那些情况是违反equals约定的（举例）？
- 什么是里氏替换原则？
- jdk中有违反equals约定的情况存在吗？
- 讲讲java.sql.TimeStamp、java.net.URL，它们违背了什么约定？
- 在继承体系中，如果需要扩展超类的属性字段，同时又要重写equals方法，要如何保证不违反equals约定？
- 是否需要对equals方法的入参进行判空？为什么？
- 高质量实现equals方法有那些诀窍？
- 在判断相等时，dubbo、float要做什么特殊处理？使用Float.equals、Double.equals方法有什么劣势？
- 对象域的比较，需要遵循哪些原则？会对性能有影响吗？
- public boolean equals(Myclass o)，有问题吗？
-  Google的AutoValue是什么？