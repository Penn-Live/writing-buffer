- 基于Redis做分布式锁

  Redis做分布式锁，主要是利用redis的三个条命令，setnx, expire,del，以及redis的watch命令和事务。setnx的含义是如果没有值即设置，因此，可以利用设置某个key来作为锁的语义，如果设置成功，就认为它获取了锁，如果这个key已经被别人设置了，那么就认为没有获取锁。expire规定了key的过期时间，这个设置可以防止服务器宕机之后造成死锁。当要释放一个锁的时候，所想watch这个key，如果这个key被的线程释放了，那么后面的del操作不执行。否则使用事务，将这个key删除。

- 基于Zookeeper的分布式锁的代码实现 

  

![图片](http://test-yr-ad-images-pr.oss-cn-beijing.aliyuncs.com/123456.png)