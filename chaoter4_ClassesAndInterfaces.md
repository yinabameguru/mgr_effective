# 类和接口

**15.使类和成员的可访问性最小化**

- 什么叫封装？好的封装应该表现出什么样的效果？
- 封装有哪些好处？

- 讲一讲访问级别？

- final常量数组要怎么实现？

- java9对访问级别做出了什么样的调整？

**16.要在公有类而非公有域中使用访问方法**

- 使用访问方法有什么好处？
- 什么情况下可以直接暴露类的数据域？
- jdk中有哪些地方违反了“共有类不应该直接暴露数据域”的建议？

**17.使可变性最小化**

- 什么是不可变类？jdk中有哪些？

- 为什么会有不可变类？

- 建立不可变类要遵循哪些规则？
- 讲一讲函数式和命令式？
- 讲一讲jdk里同样是数值增加，为什么有时使用plus，有时使用add？
- 不可变对象有那些优点？
- 既然不可变对象可以被自由的共享，那么如何充分发挥这种优势呢？
- 讲一讲不可变类与静态工厂？jdk中有哪些例子？选一例详细讲讲？
- 讲一讲不可变对象内部组件的复用？有那些巧妙的用法？
- 不可变对象有什么缺点？
- 用过BitSet嘛？

- 当使用不可变对象遇到频繁创先对象产生的性能问题时，有哪些解决方法？

- 为了达到”不允许类被子类化“的目的，出了将类声明为final还有什么好的实现方法嘛？

- 执行方法aa对象的属性a的值时多少？

  ```java
  public void aa() {
      Pa pa = new Ch(2);
  }
  
  class Pa {
  
      private int a;
      private Pa(int a) {
          a = 1;
      }
  }
  
  class Ch extends Pa {
  
      public Ch(int a) {
          super(a);
      }
  }
  ```

- 不可变类就是指对象的所有域都必须是final，这个说法对吗？不可变类可以延迟初始化嘛？

**18.组合优先于继承**

- 如何实现一个set，可以查看它被创建依赖一共添加了多少个元素？

- 如何实现一个集合，所有被插入集合的元素都满足某一先决条件？使用继承会有什么问题?
- 重写会又潜在的安全问题，那么只对超类进行扩展，是不是就完全没有风险了呢？
- 讲一讲组合、转发、转发方法？
- 讲一讲decorator？
- 什么是is-a关系？jdk中有哪些违反is-a原则的地方？

**19.要么设计继承并提供文档说明，要么禁止继承**

- 在设计继承体系时，为什么要对publish、protect方法提供文档说明？需要说明哪些内容？
- 讲一讲java8的新注解@apiNote、@implSpec、@inplNote？

-  执行方法aa输出的结果是什么？

  ```java
  class Super {
  
      public Super() {
          overrideMe();
      }
  
      public void overrideMe() {
  
      }
  
  }
  
  final class Sub extends Super {
      private final Instant instant;
  
      Sub() {
          instant = Instant.now();
      }
  
      public void overrideMe() {
          System.out.println(instant);
      }
  }
  
  public void aa() {
      new Sub().overrideMe();
  }
  ```

- 为继承而设计的类在序列化或者克隆时要注意什么？

**20.接口优于抽象类**

- 对比一下接口和抽象类？讲讲优缺点？

- 什么是模板方法模式？
- 讲一讲SkeletalCollection？
- 什么是适配器模式？

- 什么是模拟多重继承？

- 什么是简单实现？

**21.为后代设计接口**