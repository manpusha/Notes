---
title: Java开发环境配置(win7-64bit) 
tags: java
grammar_cjkRuby: true
---
# Java开发环境配置(win7-64bit)

[TOC]

## 1.概述
- 搭建Java开发环境一般需要同时安装JDK和JRE。
- JDK:指Java开发工具包Java Development Kit，开发Java程序时必需，JDK里包含一部分公共JRE。 
- JRE：一个Java运行环境Java Runtime Environment，运行已开发的Java程序时所用。
## 2.文本用到的工具
Java SE基础工具包：[官网下载](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
（版本很多，自行选择适用版本，省略安装过程，安装时候下一步下一步即可）
![enter description here][1]
## 3.环境变量配置
- Java环境变量涉及到三个名词：JAVA_HOME、path、classpath。
- JAVA_HOME代表JDK安装主目录，path代表JDK下可执行文件目录，classpath代表运行java程序时需要查找class文件的目录。
- PATH配置JDK命令文件的位置。
1. 我的电脑（右键）→ 属性
![enter description here][2]

2. 高级系统设置 → 环境变量
![enter description here][3]	![enter description here][4]
3. 系统变量自带是没有JAVA_HOME这个变量，需要自己编辑如下：（变量值就是JDK安装的路径）
![enter description here][5]
4. PATH在系统变量中本来就是存在的，选中PATH → 编辑
![enter description here][6]
-->在最前面输入Bin的路径（用分号隔开其他路径）
![enter description here][7]
5. 系统自带的变量是没有CLASSPATH的，需要添加
![enter description here][8]
→ 用”.”代表当前路径
→ 用”;”隔开
→ 输入Bil的路径（如我的路径是：C:\Program Files\Java\jdk1.8.0_60\lib）
![enter description here][9]
配置到这里就结束了，记得要按确定，没确定是不会自己保存的。
## 4.测试
打开运行àcmdà输入java/javac进行验证(验证成功的效果如下)
![enter description here][10]
![enter description here][11]
如果你看到这样的效果，恭喜你配置成功了。
##6.注意事项
`如果使用1.5以上版本的JDK，不用设置CLASSPATH环境变量，也可以正常编译和运行Java程序。`


  [1]: https://www.github.com/manpusha/githubimg/raw/master/images/1499071467454.jpg
  [2]: https://www.github.com/manpusha/githubimg/raw/master/images/1499071562840.jpg
  [3]: https://www.github.com/manpusha/githubimg/raw/master/images/1499071618968.jpg
  [4]: https://www.github.com/manpusha/githubimg/raw/master/images/1499071630175.jpg
  [5]: https://www.github.com/manpusha/githubimg/raw/master/images/1499071888520.jpg
  [6]: https://www.github.com/manpusha/githubimg/raw/master/images/1499071917771.jpg
  [7]: https://www.github.com/manpusha/githubimg/raw/master/images/1499071949009.jpg
  [8]: https://www.github.com/manpusha/githubimg/raw/master/images/1499071967434.jpg
  [9]: https://www.github.com/manpusha/githubimg/raw/master/images/1499071989689.jpg
  [10]: https://www.github.com/manpusha/githubimg/raw/master/images/1499072042026.jpg
  [11]: https://www.github.com/manpusha/githubimg/raw/master/images/1499072055621.jpg