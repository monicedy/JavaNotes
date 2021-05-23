* synchronized 修饰方法时锁定的是调用该方法的对象。
* 它并不能使调用该方法的多个对象在执行顺序上互斥
* 顺序上互斥，用static
*
*
*  while 放在 同步 之外
*
*  synchronized (new Object) 方案无效



1，相对于ReentrantLock而言，synchronized锁是重量级锁，重量级体现在活跃性差一点。synchronized锁是内置锁，意味着JVM能基于synchronized锁做一些优化：比如增加锁的粒度(锁粗化)、锁消除。

2，在synchronized锁上阻塞的线程是不可中断的：线程A获得了synchronized锁，当线程B也去获取synchronized锁时会被阻塞。而且，线程B无法被其他线程中断(不可中断的阻塞)，而ReentrantLock锁能实现可中断的阻塞。

3，synchronized锁释放是自动的，当线程执行退出synchronized锁保护的同步代码块时，会自动释放synchronized锁。而ReentrantLock需要显示地释放：即在try-finally块中释放锁。

4，线程在竞争synchronized锁时是非公平的：假设synchronized锁目前被线程A占有，线程B请求锁未果，被放入队列中，线程C请求锁未果，也被 放入队列中，线程D也来请求锁，恰好此时线程A将锁释放了，那么线程D将跳过队列中所有的等待线程(即：线程B和线程C)并获得这个锁。

而ReentrantLock能够实现锁的公平性。

5，synchronized锁是读写互斥并且 读读也互斥，ReentrantReadWriteLock 分为读锁和写锁，而读锁可以同时被多个线程持有，适合于读多写少场景的并发