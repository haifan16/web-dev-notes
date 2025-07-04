前面学习的**程序计数器、虚拟机栈、本地方法栈都是线程私有的**。

## 堆的特点

1. **线程共享**，堆中的对象都需要考虑线程安全问题
2. 有垃圾回收机制

## 堆内存溢出

可以设置参数 ```-Xmx8m``` 设置堆内存小一些就可以看到多久会有堆内存溢出的问题

## 堆内存诊断

1. jps 工具
   查看当前系统中有哪些 Java 进程
2. jmap 工具
   查看堆内存占用情况 ```jmap -heap 进程id```
3. jconsole 工具
   图形界面的，多功能的监测工具，可以连续监测

案例：垃圾回收后，内存占用仍然很高
-> 使用 JVisualVM 来监控 Java 程序

扩展：JConsole 和 JVisualVM 能监控到 JVM 信息和 Java 程序，都是通过 JMX 实现的