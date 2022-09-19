# jdk hotspot源码中文注释

## JVM启动流程源码分析

jvm的启动流程可以分为下面几步:

1. JVM 启动入口函数`java.base/share/native/launcher/main.c`的`JLI_Launch`函数。
   1. JVM运行环境的设置和检查
   2. 通过`CreateExecuteionEnvironment`函数查找`JAVA_DLL`动态库是否存在，能不能访问。并设置一些变量
   3. 加载动态库，将动态库中的一些函数链接至本地变量。
   4. 解释`options`和`args`参数。
   5. 新建线程初始化虚拟机
   6. 加载并执行主类

2. 具体的设计及推理验证过程。

## JVM的C++解释器工作原理

## JVM的模版解释器工作原理