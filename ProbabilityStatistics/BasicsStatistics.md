---
title_: Basic Statistics
trans: 统计学基础
catagories: Probability and Statistics
date: 2022-3-12
---

# Basic Statistics

## What is a hypothesis test?

A hypothesis test is rule that specifies whether to accept or reject a claim about a population depending on the evidence provided by a sample of data.

> 假设检验是一种规则, 它根据数据样本提供的证据来指定是否接受或拒绝一个关于总体的主张.

[假设检验]检查关于总体的两个相反假设: 原假设和备择假设. 原假设是正在测试的陈述. 通常, 原假设(null hypothesis)是"没有影响"或"没有差异"的陈述. 备择假设(alternative hypothesis)是你希望能够根据样本提供的证据得出的结论是正确的陈述.

检验根据样本数据决定是否决绝原假设. 用 p 值来确定. 如果 p 值小于显著性水平(significance level, 记做 $\alpha$ 或 alpha), 那么你可以拒绝原假设.

一个常见的错误是, 统计假设检验的目的是选择两个假设中更有可能的那个. 然而, 在设计假设检验时, 我们将原假设设为我们想要否定的东西. 因为我们在分析之前将显著性水平定的很小(通常, 值为 0.05 就可以了), 所以当我们拒绝原假设时, 我们就有了统计证据来证明备择假设是正确的. 相反, 如果我们不能拒绝原假设, 我们是没有统计证明零假设是正确的. (也就是说假设检验只能证明备择假设是正确的, 而不能证明原假设是正确的.)

可以用假设检验来回答的问题包括:

- 本科女性的平均身高是否与 66 英寸不同?
- 她们身高的标准差是否等于或小于 5 英寸?
- 男女大学生的平均身高有不同吗?
- 本科男生的比例是否显著高于本科女生的比例?

## Example of performing a basic hypothesis test

可以遵循 6 个基本步骤来正确的设置和执行假设检验.

例如, 管道制造厂的经理想要确定他们的管道的平均直径是否与 5 厘米不同.

> 在收集数据前, 应该确定测试的标准和所需的样本量.

1. Specify the hypothesis.

   首先, 管理者制定假设. 原假设: 所有管道的整体均值等于 5 厘米. 写作: $H_0:\mu = 5$

   接着, 管理者从下面的备择假设中进行选择:

   | 测试条件           | 备择假设               |
   | ------------------ | ---------------------- |
   | 整体均值小于目标   | one sided: $\mu \lt 5$ |
   | 整体均值大于目标   | one sided: $\mu \gt 5$ |
   | 整体均值不等于目标 | two sided: $\mu \ne 5$ |

   因为他们需要确保管道不大于或小于 5 厘米, 这个管理者选择双面备择假设, 即所有管道的整体均值不等于 5 厘米. 写作: $H_1 : \mu \ne 5$

2. Choose a significance level (also called alpha or $\alpha$).

   管理者选择显著性水平 0.05, 这是常用的显著性水平.

3. Determine the power and sample size for the test.

   管理着使用功效和样本大小计算来确定需要测量多少根管道, 才能很好地检测到距离目标直径 0.1 厘米或更多的差异.

4. Collect the data.

   收集管道样本并测量他们的直径.

5. Compare the p-value from the test to the significance level.

   执行假设检验后, 管理者得到 p-value 为 0.004. 这个 p-value 小于显著性水平 0.005.

6. Decide whether to reject or fail to reject the null hypothesis.

   管理者拒绝了原假设, 并得出结论, 所有管道的平均直径不等于 5 厘米.

## About the null and alternative Hypothesis

原假设和备择假设是关于总体的两个互斥的表述. [假设检验]检查使用样本数据确定是否要拒绝原假设.

- **原假设 ($H_0$)**

  原假设表示总体参数(如均值, 标准差等)等于假设值. 原假设通常是基于以前的分析或专业知识的最初主张.

- **备择假设 ($H_1$)**

  备择假设表示总体参数小于, 大于或不同于原假设中的假设值. 备择假设是你认为是真的或者希望被证明是真的.

## One-sided and two-sided hypothesis

备择假设可以是单侧的的或双侧的.

- **Two-sided**

  使用双侧备择假设(也称为非定向假设)可以确定总体参数是大于还是小于假设值. 双侧检验可以检测到总体参数在任一方向的不同, 但其功效小于单侧检验.

- **One-sided**

  使用单侧备择假设(也称为定向假设)可以确定总体参数在某个特定方向与假设是否不同. 你可以将方向指定为大于假设值或小于假设值. 单侧检验的功效大于双侧检验, 但是单侧检验无法检测总体参数在相反方向是否不同.

## Examples of two-sided and one-sided hypothesis

- **Tow-sided**

  研究员拥有某高中参加了全国高考的考生样本. 他想要知道该学校的分数是否不同于全国平均分 850. 双侧备择假设比较合适, 因为研究员侧重于确定分数是小于还是大于全国平均分. ($H_0 : \mu = 850, H_1 : \mu \ne 850$)

- **One-sided**

  研究员拥有参加全国考试培训课程的学生样本. 他想知道经过培训的学生的分数是否高于全国平均分 850. 可以使用单侧备择假设, 因为研究员特别假设经过培训的学生的分数大于全国平均分. ($H_0 : \mu = 850, H_1 : \mu \gt 850$)

## References

-[Basic Statistics](https://support.minitab.com/en-us/minitab/18/help-and-how-to/statistics/basic-statistics/supporting-topics/basics/what-is-a-hypothesis-test/)
