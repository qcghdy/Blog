# poll
/pəʊl/
学习发音
查看以下字典中提供的定义：
All
Electoral
Breed
Telecommunications
Computing
Agriculture
verb

2.
TELECOMMUNICATIONS•COMPUTING
**check the status of (a device)**, especially as part of a repeated cycle.
"the network manager can also use the software to poll each Mac on the net"

## epoll的本质
https://my.oschina.net/editorial-story/blog/3052308
网络服务程序中，先从硬件到内核，到应用程序，数据协议、数据收发过程介绍。
1、网卡收到来自自层协议栈的数据时，会产生中断，并由操作系统调用中断程序，接受数据，并写入到socket object的接受接收缓冲区，并通知监听该socket的进程。
那么，从接口层面来看，服务端是需要监听多个连接的，（如listen的连接端口connfd，以及建好连接后的数据传输连接rwfd），而revc、accept都只能监控单独某一个sokcet，因此存在一个**多对一**的关系，也就是诉求，即**操作系统需要提供一种机制，能够帮助应用程序监控多个文件描述符socket**


https://zhuanlan.zhihu.com/p/115220699
1. 什么是IO多路复用
一句话解释：单线程或单进程同时监测若干个文件描述符是否可以执行IO操作的能力

多路是指网络连接，复用指的是同一个线程。多路复用则是指计算机提供一种机制，能够在同一个线程（或者进程）同时监听多个网络连接。当连接有IO事件产生时，就通知程序读写；没有IO事件时，则阻塞，让出CPU
本质上：在单线程/进程中处理多个事件流的方法。
这个和分时处理器相关，处理并发，相对的就是串行。

https://idea.popcount.org/2017-02-20-epoll-is-fundamentally-broken-12/
https://idea.popcount.org/2017-02-20-epoll-is-fundamentally-broken-22/
