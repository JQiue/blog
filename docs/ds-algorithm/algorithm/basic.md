---
title: 算法的定义与特性
tag: 算法
author: JQiue
article: false
---

算法是对解决特定问题的求解步骤的描述，在计算机中表现为指令的有限序列，每一条指令表示一个或多个操作，没有通用的算法，只有专用的算法

算法有五个特性：

+ 输入：算法执行前，必须具备的先决条件，可以没有输入
+ 输出：算法执行后，得出的结果，必须要有输出，不一定是打印，可以是一个返回值
+ 有穷性：算法在执行有限的步骤后能够自动停止，且每一个步骤都能在可接受的时间内完成
+ 确定性：算法的每一步都有确定的含义，没有二义性，不能够模棱两可
+ 可执行性：算法的每一步必须是可执行的，每一步通过执行有限的次数完成，能偶被转换成计算机程序执行

算法在设计上也有要求：

+ 正确性：没有语法错误，对合法的数据能够产生满足需求的结果，对于不合法的数据有信息反馈
+ 可读性：便于人们理解的算法，否则难以调试和修改
+ 健壮性：对于不合法的数据，也能够做出相关处理不会产生一些莫名其妙的结果
+ 高效性：执行时间短，占用存储空间低，时间和空间是衡量算法性能的重要指标

解决问题的效率，不仅仅跟数据的组织方式有关，也和运行空间有关

数据结构与算法本身解决的是“快”与“省”的问题，因此执行效率是算法的一个非常重要的考量指标，这就是算法的时间和空间复杂度分析

+ 空间复杂度S（n）：根据算法写成的程序在执行时占用的存储单元，占用的大小往往和问题的规模有关，空间复杂度过高的算法可能导致内存爆满，从而导致程序终止
+ 时间复杂度T（n）：根据算法写成的成T恤在执行时耗费的时间，占用的大小也和问题的规模有关，时间复杂度过低的算法会导致在有生之年也看不到结果

## 为什么需要复杂度分析

把代码跑一遍，通过统计、监控就能得到算法的执行时间和占用空间，这是一种非常局限性的算法效率评估，因为测试结果非常依赖测试环境，硬件的不同导致测试结果会有很大的影响，同时也受到问题的规模影响，这个评估算法执行的效率的方法在很多书里面叫做**事后统计法**（事后诸葛亮），所以需要一个不用具体的测试数据来测试，就可以粗略的估计算法的执行效率的方法

## 大 O 表示法

大 O 表示法是一种粗略的度量，在数据项个数发生变化时，算法的效率会发生改变

一般分析算法的效率时，经常关注两种复杂度：

+ 最坏情况复杂度
+ 平均复杂度
