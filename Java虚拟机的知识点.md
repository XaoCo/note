# Java虚拟机的知识点

## 1. JVM运行时，数据区的知识点

```
JVM运行时，数据区包含：虚拟机栈，堆，方法区，本地方法栈，程序计数器，
其中，堆和方法区是线程共享的，虚拟机栈和程序计数器是线程私有的。
```



## 2. JDK 和 JRE

```tex
 1. JRE(Java Runtime Environment     Java运行环境)：包括Java虚拟机和Java程序所需要的核心类库，如果想要运行一个开发好的Java程序，计算机中只需要安装jre即可。
 2. JDK(Java Developement Kit   Java开发工具包)：jdk是提供给开发人员使用的，    其中包含了Java的开发工具（编译工具：javac.exe  打包工具：jar.exe）,也包括了jre，所以安装了jdk,就不用单独安装jre了。
简而言之：JRE=JVM+Java类库       JDK=JRE+Java开发工具
jdk下载路径：http://www.oracle.com
```



## 3.JVM参数问题

```tex
-Xmx10240m -Xms10240m -Xmn5120m -XXSurvivorRatio=3
  
-Xmx：最大堆大小
-Xms：初始堆大小
-Xmn:年轻代大小 
-XXSurvivorRatio：年轻代中Eden区与Survivor区的大小比值
年轻代5120m， Eden：Survivor=3，
   Survivor区大小=1024m（Survivor区有两个，即将年轻代分为5份，
   每个Survivor区占一份），总大小为2048m。
-Xms初始堆大小即最小内存值为10240m
```

