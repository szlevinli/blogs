---
title_: Combinations and Permutations
trans: 排列和组合
catagories: Mathematical Basis
date: 2022-3-12
---

# Combinations and Permutations

## What's the Difference?

- When the order doesn't matter, it is **Combination**
- When the order does matter, it is **Permutations**

In other words: **A permutation is an ordered Combination**

## Permutations

There are basically two types of permutation:

- **Repetition is Allowed**: such as the lock above. It could be "333"
- **No Repetition**: for example the first three people in a running race. You can't be first and second.

### Permutations with Repetition

Notation:

$$
P_n^r = n^r
$$

Where $n$ is the number of things to choose from, and we choose $r$ of them, repetition is allowed, and order matters.

### Permutations without Repetition

比如说, 16 个台球有多少种排列顺序? 也就是拿出 14 号台球后, 就不能再选择 14 号了. 这种情况下, 第 1 次我们有 16 种情况, 第 2 次我们有 15 种情况, 第 3 次我们有 14 中情况, 依次类推, 第 16 次我们只有 1 中情况:

$$
P = 16 \times 15 \times 14 \times \cdots 1 = 20,922,789,888,000
$$

但是, 如果我们说不需要 16 个台球全排列, 而只是拿出其中的 3 个的话那么情况是:

$$
P = 16 \times 15 \times 14 \times 13 = 3,360
$$

换句话来说, 就是我们有 3,360 种排列方式从 16 个球中拿出 3 个球.

Notation:

$$
P_n^r = \frac{n!}{(n - r)!}
$$

Where $n$ is the number of things to choose from, and we choose $r$ of them, no repetition, order matters.

## Combinations

There are also types of combinations (remember the order does not matter):

- **Repetition is Allowed**: such as coins in you pocket (5,5,510,10)
- **No Repetition**: such as lottery numbers (2,14,15,27,30,33)

### Combinations without Repetition

This is how lotteries work.

The easiest way to explain it is to:

- assume that the order does matter (ie. permutations),
- the alter it so the order does not matter

For example, let us say balls 1, 2 and 3 are chosen. These are the possibilities:

| Order does matter | Order doesn't matter |
| :---------------: | :------------------: |
|       1 2 3       |
|       1 3 2       |
|       2 1 3       |        1 2 3         |
|       2 3 1       |
|       3 1 2       |
|       3 2 1       |

So, the permutation have 6 times as many possibility.

Notation:

$$
C_n^r = \binom{n}{r} = \frac{n!}{r!(n-r)!}
$$

Where $n$ is the number of things to choose from, and we choose $r$ of them, no repetition, order doesn't matter.

It is often called "n choose r". And is also known as the `Binomial Coefficient`.

### Combinations with Repetition

这里使用了一个非常好的方法来解释这个问题.

问题是这样的, 我们有五种口味的冰激凌: 香蕉, 巧克力, 柠檬, 草莓和香草. 我们有三个勺子, 那么我们可以有多少种可能的组合.

- {巧克力, 巧克力, 巧克力} 表示舀了三勺巧克力
- {香蕉, 柠檬, 香草} 表示我们分别舀了一勺香蕉, 一勺柠檬和一勺香草
- {香蕉, 香草, 香草} 表示我们分别舀了一勺香蕉和两勺香草

用更清晰的方式来说: 我们有 5 种口味的冰激凌, 你可以舀 3 勺, 可以重复且与顺序无关, 那么有多少种可能性.

我们可以这么考虑, 把 5 种冰激凌想象成 5 个盒子, 从左到右的排好(香蕉, 巧克力, 柠檬, 草莓和香草), 上面有个勺子从左至右开始舀 3 次, 我们用 O 来表示舀了一勺, 用 -> 表示移动, 那么:

香蕉 巧克力 柠檬 草莓 香草

- {巧克力, 巧克力, 巧克力}可以表示为: -> O O O -> -> ->
- {香蕉, 柠檬, 香草}可以表示为: O -> -> O -> -> O
- {香蕉, 香草, 香草}可以表示为: O -> -> -> -> O O

我们可以把问题改为: 上面的 O 和 -> 有多少种组合方式.

注意这里总是有 3 个 O 和 4 个 ->, 因此我们抽象的说这里有 $r+(n-1)$ 个位置, 这里的 $r$ 表示三勺, $n$ 表示五种口味.

将上面的结果带入组合不能重复的公式中就可以得到组合能重复的公式了.

Notation:

$$
C_n^r = \binom{r+n-1}{r} = \frac{(r+n-1)!}{r!(n-1)!}
$$

## In Conclusion

|                             $\ddots$ |       Repeats Allowed       |      No Repeats       |
| -----------------------------------: | :-------------------------: | :-------------------: |
|         Permutations (order matter): |            $n^r$            |  $\frac{n!}{(n-r)!}$  |
| Combinations (order doesn't matter): | $\frac{(r+n-1)!}{r!(n-1)!}$ | $\frac{n!}{r!(n-r)!}$ |
