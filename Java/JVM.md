# JVM

## 什么是JVM
JVM（Java Virtual Machine）是java程序运行环境，即二进制字节码的运行环境

### 好处
- 一次编写，到处运行
- 自动内存管理，垃圾回收功能
- 数组下标自动越界检查
- 多态，面向对象的基石

### 比较
JVM
JRE = JVM + 基础类库
JDK = JVM + 基础类库 + 编译工具

## 学习JVM的作用
- 面试
- 理解底层的实现原理
- 中高级程序员的必备技能


## 内存结构
![JVM内存结构图](https://github.com/chaofengliu/LovingTheCode/blob/main/Java/jvm.webp)


1. 程序计数器
2. 虚拟机栈
3. 本地方法栈
4. 堆
5. 方法区