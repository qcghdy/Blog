学习spring，在语言转型的过程中，从Cpp转Java，使用spring框架时，用起来感觉挺容易，但又遇到了很多概念，例如IoC、控制反转，DI 依赖注入，这两个词从中文翻译理解，真的是一头雾水。
只有先理解了概念，才能更好的去使用java。

首先理解一个基础，又觉得容易理解，但理解起来又感觉模模糊糊，刚开始说不清的概念，inject，注入。

首先要理解一个oop中的基础概念，类的关系，主要包括继承、组合、聚合、关联。这些关系，除了继承这种强关系外，其余的都可以认为，依赖是两个类，实际上是程序运行时两个类的一种最弱关系，也就意味着耦合最小的关系。

常规流程中，A依赖B，包括组合，聚合，关联，那对象之间，一定要先new或者初始化之后，才能使用。

What is spring injection?
Spring provides a light-weight container, e.g. the Spring core container, for dependency injection (DI). This container lets you inject required objects into other objects. ... The injection in Spring is either done via setter injection of via construction injection.


类加载:Java命令的作用是启动虚拟机，虚拟机通过输入流，从磁盘上将字节码文件(.class文件)中的内容读入虚拟机，并保存起来的过程就是类加载。

 

类加载特性 :
      *在虚拟机的生命周期中一个类只被加载一次。
      *类加载的原则：延迟加载，能少加载就少加载，因为虚拟机的空间是有限的。
      *类加载的时机：
      1）第一次创建对象要加载类.
      2）调用静态方法时要加载类,访问静态属性时会加载类。
      3）加载子类时必定会先加载父类。
      4）创建对象引用不加载类.
      5) 子类调用父类的静态方法时
          (1)当子类没有覆盖父类的静态方法时，只加载父类，不加载子类
          (2)当子类有覆盖父类的静态方法时，既加载父类，又加载子类
      6）访问静态常量，如果编译器可以计算出常量的值，则不会加载类,例如:public static final int a =123;否则会加载类,例如:public static final int a = math.PI。
