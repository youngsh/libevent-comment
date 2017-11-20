# libevent commented

## 头文件
- 主要就是event.h：事件宏定义、接口函数声明，主要结构体event的声明；
## 内部头文件
- xxx-internal.h：内部数据结构和函数，对外不可见，以达到信息隐藏的目的；
## libevent框架
- event.c：event整体框架的代码实现；
## 对系统I/O多路复用机制的封装
- epoll.c：对epoll的封装；
- select.c：对select的封装；
- devpoll.c：对dev/poll的封装;
- kqueue.c：对kqueue的封装；
## 定时事件管理
- min-heap.h：其实就是一个以时间作为key的小根堆结构；
## 信号管理
- signal.c：对信号事件的处理；
## 辅助功能函数
- evutil.h 和evutil.c：一些辅助功能函数，包括创建socket pair和一些时间操作函数：加、减和比较等。
## 日志
- log.h和log.c：log日志函数
## 缓冲区管理
- evbuffer.c和buffer.c：libevent对缓冲区的封装；
## 基本数据结构
- compat/sys下的两个源文件：queue.h是libevent基本数据结构的实现，包括链表，双向链表，队列等；_libevent_time.h：一些用于时间操作的结构体定义、函数和宏定义；
## 实用网络库
- http和evdns：是基于libevent实现的http服务器和异步dns查询库；
