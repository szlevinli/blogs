# Sampling Distribution, Confidence Interval

这篇文章主要谈及的是 推论统计学 (Inferential Statistics).

推论统计学的关键目标是, 从局部看整体.

样本分布 (Sampling Distribution) 是推论统计学的关键内容. 它可会回答这样的问题: "需要多大的样本容量才能对总体进行特定推断?" 或者 "沿着这条河随机抽取的 100 份水样显示, 这种毒素的平均浓度为 50ppm (百万分之一), 标准差为 4.5 -- 这条河的平均污染程度为 95% 置信区间"

## Central Limit theorem

The samples statistic sample mean $\bar{X}$ exhibits a unique behavior - regardless of the population distribution (uniform, exponential, other), in the limit $n \to \infty$ ($n$ tends to infinity, where $n$ is the sample size), the sampling distribution of $\bar{X}$ tends to nomarl distribution. The _rate_ at which the sampling distribution approaches normal distribution depends on the population distribution. Now, if the population itself is normally distributed, the $\bar{X}$ is normally distributed for _any_ sample size. This is the essence of what is called Central Limit theorem.

> _在统计样本均值 $\bar{X}$ 时会呈现一种独特的行为 - 无论全量分布呈什么形式 (正态分布, 幂分布, 等), 在样本数量 $n$ 趋向于无穷大时 (注: 这个 $n$ 不是指一个样本中的数据量, 应该指的是从全量中提取样本的次数.), $\bar{X}$ 的样本分布趋向于正态分布. 样本分布趋向于正态分布的速度依赖于全量分布形式. 现在, 如果说全量呈正态分布, 那么 $\bar{X}$ 在任何样本数量的情况下都呈正态分布形式. 这就是中心极限理论的基础或本质._

## Degrees of Freedom (DF)

## Confidence Interval
