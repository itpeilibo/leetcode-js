---
nav:
  title: 数据结构
  order: 1
group:
  title: 介绍
  order: -1
---

# 数据结构

本系列文章是作者在 B 站学习完 [《数据结构与算法》](https://www.bilibili.com/video/BV1x7411L7Q7)后，为了进行总结和复习而整理的学习笔记，视频讲解的特别好，给大家安利一波～

## 一、什么是数据结构？

> 数据结构（data structure）是计算机中存储、组织数据的方式。通常情况下，精心选择的数据结构可以带来最优效率的算法。---中文维基百科

一句话总结：数据结构就是在计算机中，**存储和组织数据的方式**。

例如：图书馆中存放了很多书籍，怎样摆放图书既能放很多书，还方便取？

其实我们主要思考两个问题

- 新书怎么插入？
- 怎么快速对找到指定的书？

1. 如果新书随便摆放，那么在找指定的书时，图书馆那么大，肯定会累死
2. 按照书名的拼音字母顺序排放
   1. 新书的插入， 按照字母顺序找到位置，然后插入。
   2. 书籍的查找：根据字母顺序进行查找
3. 现实生活中，图书馆会先划分类别，然后在对应类别中，根据字母顺序插入，这样查找效率会更高

### 结论

- 解决问题方法的效率，根据数据的组织方式有关
- 计算机中存储的数据量相对于图书馆的书籍来说数据量更大，更多
- 以什么样的方式，来存储和组织我们的数据才能在使用数据时更加方便呢?
- 这就是数据结构需要考虑的问题。

### 常见的数据结构

- [数组（Array）](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array)
- [栈（Stack）](/data-structure/01_stack)
- [队列（Queue）](/data-structure/02_queue)
- [链表（Linked List）](/data-structure/03_linked_list)
- [哈希表（Hash）](/data-structure/07_hash_table)
- [树（Tree）](/data-structure/08_tree&binary_tree)
- [图（Graph）](/data-structure/11_graph)
- [堆（Heap）](https://zh.wikipedia.org/wiki/%E5%A0%86%E7%A9%8D)

> 注意：数据结构与算法与语言无关，常见的编程语言都有**直接或间接**的使用上述常见的数据结构。

## 二、什么是算法（Algorithm）？

### 算法的定义

- 一个有限指令集，每条指令的描述不依赖于语言
- 接收一些输入（有些情况下不需要输入）
- 产生输入
- 一定在有限步骤之后终止

算法通俗理解：解决问题的办法/步骤逻辑。数据结构的实现，离不开算法。

## 案例

假如杭州和上海之间有一条高架线，高架线长度是 1,000,000 米，有一天高架线中有一米出现了故障，请你想出一种算法，可以快速定位到处问题的地方。

- 线性查找
  - 从上海的起点开始一米一米的排查，最终一定能找到出问题的线段。
  - 但是如果线段在另一头，我们需要排查 1,000,000 次，这是最坏的情况，平均需要 500,000 次。
- 二分查找
  - 从中间位置开始排查，看一下问题出在杭州到中间位置，还是中间到上海的位置。
  - 查找对应的问题后，再从中间位置分开，重新锁定一般的路程。
  - 最坏的情况，需要多少次可以排查完呢? 最坏的情况是 20 次就可以找到出问题的地方。
  - 怎么计算出来的呢? log(1000000, 2)，以 2 位底，1000000 的对数 ≈ 20。

结论：你会发现，解决问题的办法有很多，但是好的算法对比于差的算法，效率天壤之别。
