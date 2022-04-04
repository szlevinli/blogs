---
title_: Statistical Significance
trans: 统计显著性
catagories: Probability and Statistics
date: 2022-3-12
---

# Statistical Significance

Statistical Significance refers to whether any differences observed between groups being studies are "real" or whether they are simple due to chance.

> 统计显著性指的是被研究的组间观察到的任何差异是"真实"的还是仅仅是偶尔的.

让我们考虑这样一项研究, 评估一款新出的减肥药. A 组吃了这款减肥药在 7 周内平均减掉了 4kg. B 组没有吃这款减肥药在 7 周内平均减掉了 1kg. 现在的问题是: 我们能说这种药在减肥方面比不吃药能多减 3 公斤吗? 或者说 A 组只是恰巧多减了 3 公斤.

统计测试从一些不可能的假设开始: 两组人从一开始就完全一样. 这意味着每组的平均其实重量是相同的, 而且较轻的人和较重的人的比例也是一样的.

然后用数学程序来检查各组结果(减肥)的差异. 我们的目标是确定在这种情况下观察到的差异, 即平均减重 3 公斤的差异有多大可能是偶然发生的.

## The "p" value

科学家们使用术语"p"这个词来描述在两组完全相同的人身上纯粹偶然观察到如此巨大差异的概率. 在科学研究中, 这被称为"p"值 (p-value).

如果结果的差异不太可能仅仅是偶然发生的, 那么这种差异就被称为"统计显著性".

在大多数科学中, p-value 为 0.05 的结果被认为是在统计显著性的边界. 如果 p-vale 小于 0.01, 则认为结果具有统计显著性; 如果 p-value 小于 0.005, 则认为结果具有高度统计显著性.

回到我们的减肥研究, 如果结果产生 0.05 的 p 值, 这就是说: "假设被比较的两组人从一开始就完全相同, 那么这 3 公斤的差异有 95% 的可能性不是偶然发生的."根据这一发现, 科学家们会推断出这种减肥药确实有效.
