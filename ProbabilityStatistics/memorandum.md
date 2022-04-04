---
title_: Probability And Statistics Memo
trans: 概率和统计备忘录
catagories: Probability and Statistics
date: 2022-3-12
---

# Probability Statistics

## Normal Distribution

> Source: [maths is fun - Normal Distribution](https://www.mathsisfun.com/data/standard-normal-distribution.html)

The **Normal Distribution** has:

- mean = median = mode
- symmetry about the center
- 50% of values less than the mean and 50% greater than the mean

### Standard Deviations

> Source: [maths is fun - Standard Deviation and Variance](https://www.mathsisfun.com/data/standard-deviation.html)

- **68%** of values are within **1 standard deviation** of the mean
- **95%** of values are within **2 standard deviations** of the mean
- **99.7%** of values are within **3 standard deviations** of the mean

The Standard Deviation is a measure of how spread out numbers are.

Its symbol is $\sigma$ (the greek letter sigma)

The formula is easy: it is the **square root** of the **Variance**.

#### Variance

To calculate the variance follow these steps:

- Work out the Mean
- Then for each number: substract the Mean and square the result (the _squared difference_)
- The work out the average of those squared differences.

$$
\begin{aligned}
  Mean &= \frac {600+470+170+430+300}{5} \\
       &= \frac {1970}{5} \\
       &= 394
\end{aligned}
$$

Variance:

$$
\begin{aligned}
  \sigma^2 &= \frac {(600-394)^2+(470-394)^2+(170-394)^2+(430-394)^2+(300-394)^2} {5} \\
           &= \frac {206^2+76^2+(-224)^2+36^2+(-94)^2} {5} \\
           &= \frac {108520} {5} \\
           &= 21704
\end{aligned}
$$

Standard Deviation:

$$
\begin{aligned}
  \sigma &= \sqrt{21704} \\
         &= 147.32 \\
         &\approx 147
\end{aligned}
$$

### Standard Deviation Formulas

- The "**Population** Standard Deviation":

$$
\sigma = \sqrt{\frac{1}{N}\displaystyle\sum_{i=1}^{N}(x_i-\mu)^2}
$$

- The "**Sample** Standard Deviation":

$$
\sigma = \sqrt{\frac{1}{N-1}\displaystyle\sum_{i=1}^{N}(x_{i}-\bar{x})^2}
$$

> Note: $\mu$ is mean for **Population**, $\bar{x}$ is mean for **Sample**

#### Standard Scores

So to convert a value to Standard Score ("z-score"):

- first subtract the mean,
- the divide by the Standard Deviation

A Normal Distribution -- Standardize --> The Standard Normal Distribution.

The **z-score formula**:

$$
z = \frac{x-\mu}{\sigma}
$$

## Expected Value vs. Mean: What's the Difference?

- **Expected value** is used when we want to calculate the mean of a probability distribution. This represents the average value we expect to occur before collecting any data.
- **Mean** is typically used when we want to calculate the average value of a given sample. This represents the average value of raw data that we've already collected.

### Example: Calculating Expected Value

A probability distribution tells us the probability that a random variable takes on certain values.

> 概率分布告诉我们一个随机变量取某个值的概率.

For example, the following probability distribution tells us the probability that a certain soccer team scores a certain number of goals in a given game:

| Goals (X) | Probability P(x) |
| :-------: | :--------------: |
|     0     |       0.18       |
|     1     |       0.34       |
|     2     |       0.35       |
|     3     |       0.11       |
|     4     |       0.02       |

To calculate the expected value of this probability distribution, we can use the following formula:

$$
\text{Expected Value} = \sum{x \times P(x)}
$$

where:

- **x**: Data value
- **P(x)**: Probability of value

$$
\begin{aligned}
  \text{Expected Value} &= 0 \times 0.18 + 1 \times 0.34 + 2 \times 0.35 + 3 \times 0.11 + 4 \times 0.02 \\
                &= 1.45
\end{aligned}
$$

因为平均值比较好理解这里就不再说明和举例了.

## Errors and Residuals

> References: [WikiPedia](<https://en.wikipedia.org/wiki/Errors_and_residuals#:~:text=The%20error%20(or%20disturbance)%20of,example%2C%20a%20sample%20mean).>)

我们可以将 Errors 翻译成"误差", 把 Residuals 翻译成 "残差".

这章主要解释"误差"和"残差"的区别.

我们可以简单的理解"误差"是观察值与总体均值的差. "残差"是观察值与样本集的均值的差.

假设中国 21 岁男性的平均身高是 1.70 米, 我们随机抽取了 3 个 21 岁的男性, 他们的身高分别为 1.68 米, 1.80 米, 1.75 米.

这里 1.70 是总体均值. 样本均值是 $\frac{1.68+1.80+1.75}{3}=1.74$.

那么对于第一个样本 1.68 米的"误差"是 $1.68-1.70=-0.02$, "残差"是 $1.68-1.74=-0.06$.

"残差"的合计等于零. 这个例子的"残差"合计是 0.01, 这与计算时的样本精度有关, 不用特别介意.
