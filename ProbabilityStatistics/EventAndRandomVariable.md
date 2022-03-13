---
title_: Event and Random Variable
trans: 事件和随机变量
catagories: Probability and Statistics
date: 2022-3-13
---

# Event and Random Variable

事件和随机变量的概念属于一学就懂, 一用就懵.

在 [Quora](https://www.quora.com/What-is-the-difference-between-an-event-and-a-random-variable) 中有一篇介绍事件和随机变量区别的帖子, 写的还算中肯, 在此记录下来以备未来查阅.

- 事件: 是实验的结果或多个结果的的联合, 这些结果是可以分配概率(或度量)
- 随机变量: 是变量, 它的域是基本事件的集合, 它的范围(结果)可以是数值的也可以是分类的

即使随机变量是事件元素和数值或分类结果的映射, 但通常我们分析随机变量是使用概率. 换句话说, 我们通常倾向于将产生相同随机变量值的事件聚合起来, 接着我们通过分析变量可以取得值及其相应的概率来分析变量.

假设我们投掷两个公平的骰子.

- 事件的类型可以是:
  - 得到 2 个 6 (这种情况下的概率是 1/36)
  - 得到 2 个奇数, 比如: (1,1), (3,3), (5,5), (1,3), (3, 1)... (这种情况下的概率是 9/36=1/4)
- 随机变量的类型可以是:
  - 将两个骰子的数值合计, 比如: (1,1) 作为事件或结果, 那么随机变量设置为 2; (3,4) 作为事件或结果, 那么随机变量设置为 7.
  - 通过将随机变量相同值聚合到到一起, 我们就可以分析这个随机变量的值在 2 到 12 之间, 每个值的概率.

以下就是在两个骰子的情况下的随机变量和概率

2 1/36 (1, 1)
3 2/36 (1, 2) (2, 1)
4 3/36 (1, 3) (2, 2) (3, 1)
5 4/36 (1, 4) (2, 3) (3, 2) (4, 1)
6 5/36 (1, 5) (2, 4) (3, 3) (4, 2) (5, 1)
7 6/36 (1, 6) (2, 5) (3, 4) (4, 3) (5, 2) (6, 1)
8 5/36 (2, 6) (3, 5) (4, 4) (5, 3) (6, 2)
9 4/36 (3, 6) (4, 5) (5, 4) (6, 3)
10 3/36 (4, 6) (5, 5) (6, 4)
11 2/36 (5, 6) (6, 5)
12 1/36 (6, 6)

上面情况的期望值是 $(2*1/36 + 3*2/36 + ... + 12 * 1/36) = 7$