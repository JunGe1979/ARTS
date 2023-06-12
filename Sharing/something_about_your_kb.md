#Systemize your kb
耗哥说的对，码农应该系统化自己的知识，日积月累终成人才。所以，从现在开始我要开始整理自己工作当中用到的各种知识，最好化成脑图。All the knowledge should be orgnized in Interview Question, which can give me more pressure.

A.C++
*1. What's the c10k problem?
The term "C10K problem" refers to a challenge in computer science that emerged in the 1990s. It represents the difficulty of designing a server or network architecture capable of handling a large number (10,000 or more) of simultaneous client connections.
2. 为何epoll性能好?
3. libevent的原理？
The problem that libevent solves is, it provides an easy to use library for notifying when an event happens on the file descriptors which you consider interesting. It also hides the real backend (select, epoll, kqueue) being used, and this helps you avoid writing platform-dependent code (eg., kqueue works only on *BSD) and if there were a new and improved backend in the future, your code would not change. It is like the JVM for asynchronous event notification system.

*4. What's the implementation of c++ macro? what's the discons of macro?
It just expands the macro with code, and it won't make type check, that's the problem it has.

*5. In linux kernal, there's a tear-off tech which can get the address of a struct when you have the address of the member? How does it work?
The technique you're referring to is commonly known as "container_of" or "offset_of." It is a technique used in the Linux kernel (and other C-based systems) to obtain the address of a containing structure given the address of one of its members. This technique allows efficient navigation from a member to its parent structure.
#define container_of(ptr, type, member) \
    ((type *)((char *)(ptr) - offsetof(type, member)))
#define offsetof(type, member) ((size_t)(&((type*)0)->member))

6. The kernal process scheduling algorithm?

7. The high performance programming in C++?

8. Forward in c++11?

9. How does c struct align?

10. How does twitter optimized its framework?

11. Storage knowledge: RAID
