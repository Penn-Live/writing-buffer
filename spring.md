- AOP 的实现方式有哪几种？如何选择？（必考）

  *答：JDK 动态代理实现和 cglib 实现。*

  *选择：*

  1. *如果目标对象实现了接口，默认情况下会采用 JDK 的动态代理实现 AOP，也可以强制使用 cglib 实现 AOP；*
  2. *如果目标对象没有实现接口，必须采用 cglib 库，Spring 会自动在 JDK 动态代理和 cglib 之间转换。*

- JDK 动态代理如何实现？（加分点） 

  *JDK 动态代理，只能对实现了接口的类生成代理，而不是针对类，该目标类型实现的接口都将被代理。原理是通过在运行期间创建一个接口的实现类来完成对目标对象的代理。*

  1. *定义一个实现接口 InvocationHandler 的类；*
  2. *通过构造函数，注入被代理类；*
  3. *实现 invoke（ Object proxy, Method method, Object[] args）方法；*
  4. *在主函数中获得被代理类的类加载器；*
  5. *使用 Proxy.newProxyInstance( ) 产生一个代理对象；*
  6. *通过代理对象调用各种方法。*

- @transactional注解在什么情况下会失效，为什么。

- BeanFactory 和 FactoryBean？

- Spring IOC 的理解，其初始化过程？

- BeanFactory 和 ApplicationContext？

- Spring Bean 的生命周期，如何被管理的？

- Spring Bean 的加载过程是怎样的？

- 如果要你实现Spring AOP，请问怎么实现？

- 如果要你实现Spring IOC，你会注意哪些问题？

- Spring 是如何管理事务的，事务管理机制？

- Spring 的不同事务传播行为有哪些，干什么用的？

- Spring 中用到了那些设计模式？

- Spring MVC 的工作原理？

- Spring 循环注入的原理？

- Spring AOP的理解，各个术语，他们是怎么相互工作的？

- Spring 如何保证 Controller 并发的安全？
