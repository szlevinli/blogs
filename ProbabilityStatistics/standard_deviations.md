# Standard Deviations

> Source: [maths is fun - Standard Deviation and Variance](https://www.mathsisfun.com/data/standard-deviation.html)

The Standard Deviation is a measure of how spread out numbers are.

Its symbol is $\sigma$ (the greek letter sigma)

The formula is easy: it is the **square root** of the **Variance**.

## Variance

To calculate the variance follow these steps:

- Work out the Mean
- Then for each number: substract the Mean and square the result (the *squared difference*)
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

## Standard Deviation Formulas

- The "**Population** Standard Deviation":

$$
\sigma = \sqrt{\frac{1}{N}\displaystyle\sum_{i=1}^{N}(x_i-\mu)^2}
$$

- The "**Sample** Standard Deviation":

$$
\sigma = \sqrt{\frac{1}{N-1}\displaystyle\sum_{i=1}^{N}(x_{i}-\bar{x})^2}
$$

> Note: $\mu$ is mean for **Population**, $\bar{x}$ is mean for **Sample**
