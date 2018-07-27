- SpringMVC 的执行流程

  *springMVC是由dispatchservlet为核心的分层控制框架。首先客户端发出一个请求web服务器解析请求url并去匹配dispatchservlet的映射url，如果匹配上就将这个请求放入到dispatchservlet，dispatchservlet根据mapping映射配置去寻找相对应的handel，然后把处理权交给找到的handel，handel封装了处理业务逻辑的代码，当handel处理完后会返回一个逻辑视图modelandview给dispatchservlet，此时的modelandview是一个逻辑视图不是一个正式视图，所以dispatchservlet会通过viewresource视图资源去解析modelandview，然后将解析后的参数放到view中返回到客户端并展现。* 

- Spring MVC 的核心控制器是什么？消息处理流程有哪些？ 

  核心控制器为 DispatcherServlet。消息流程如下： ![img](https://images2017.cnblogs.com/blog/1246845/201712/1246845-20171226085701197-1809231596.jpg)

