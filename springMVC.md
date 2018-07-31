- SpringMVC 的执行流程

  *1.用户发送请求到DispatchServlet*

  *2.DispatchServlet根据请求路径查询具体的Handler*

  *3.HandlerMapping返回一个HandlerExcutionChain给DispatchServlet*

  　*HandlerExcutionChain：Handler和Interceptor集合*

  *4.DispatchServlet调用HandlerAdapter适配器*

  *5.HandlerAdapter调用具体的Handler处理业务*

  *6.Handler处理结束返回一个具体的ModelAndView给适配器*

     *ModelAndView:model-->数据模型，view-->视图名称*

  *7.适配器将ModelAndView给DispatchServlet*

  *8.DispatchServlet把视图名称给ViewResolver视图解析器*

  *9.ViewResolver返回一个具体的视图给DispatchServlet*

  *10.渲染视图*

  *11.展示给用户*

   

- Spring MVC 的核心控制器是什么？消息处理流程有哪些？ 

  核心控制器为 DispatcherServlet。消息流程如下： ![img](https://images2017.cnblogs.com/blog/1246845/201712/1246845-20171226085701197-1809231596.jpg)

