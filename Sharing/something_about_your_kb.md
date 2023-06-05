#Systemize your kb
耗哥说的对，码农应该系统化自己的知识，日积月累终成人才。所以，从现在开始我要开始整理自己工作当中用到的各种知识，最好化成脑图。
（一）先从c++开始，以面试题的形式展示
1.c10是什么问题？
2.为何epoll性能好?
3.libevent的原理？
The problem that libevent solves is, it provides an easy to use library for notifying when an event happens on the file descriptors which you consider interesting. It also hides the real backend (select, epoll, kqueue) being used, and this helps you avoid writing platform-dependent code (eg., kqueue works only on *BSD) and if there were a new and improved backend in the future, your code would not change. It is like the JVM for asynchronous event notification system.

next week, I should work on the purestorage interview.
https://leetcode.com/discuss/interview-question/834142/pure-storage-interview-test-2020
