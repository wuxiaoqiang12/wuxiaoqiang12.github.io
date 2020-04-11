---
layout: post
title: Induction, Coinduction, and Fixed Points 解析
categories:
- 逻辑
- CS
- 数学
- 集合论
---

本文是阅读文献[Induction, Coinduction, and Fixed Points: Intuitions and Tutorial](http://arxiv.org/abs/1903.05127)之后整理的笔记。

# Induction

对于 Induction 最常见的情况就是利用归纳法证明(Proof by induction)。例如：证明集合$U$中的元素满足某种性质，采用归纳法证明步骤如下：

- 初始元素满足该性质，
- 一个可以递归的生成其他元素的操作$F$，假设某一个元素$x$满足该性质
- 将操作$F$作用于$x$得到下一个元素$x+1$，证明该元素也具有该性质

即可完成证明。

将该思想应用到集合论中，便可得到Inductive Set，该集合是全集$U$的子集。该集合是包含初始元素且对操作$F$封闭的**最小**集合。对操作封闭意味着只能对该集合中的元素应用**有限**次操作。

# Coinduction

和Induction类似，在生成Coinductive Set的时候可以应用操作无限次。该集合是全集$U$的子集。该集合是包含初始元素且对操作$F$具有一致性的**最大**集合。可以应用有限或无限次操作。

Induction和Coinduction是一对对偶操作。可以直观的理解为Induction在操作过程中由小到大逐步生成满足要求的元素，而Coinduction则是从大到小，逐步剔除不满足要求的元素。

还有一种直观上的定义方式将两者通过集合的补联系起来：集合$X$通过coinductive的方式定义为单调操作$F$的最大不动点**当且仅当**该集合的补是通过inductive方式定义为对偶操作$F^\delta$的最小不动点。可以使用下式表示：

$$\nu X.F(X)=\neg\mu X.\neg F(\neg X)\quad \equiv \quad \nu_F = \neg\mu_{F^\delta}=\neg\mu_{\neg F\neg}$$

其中$\nu$表示最大不动点，$\mu$表示最小不动点，对偶操作：$F^\delta=\neg\circ F\circ\neg$。$F$和它的对偶操作$F^\delta$都是单调的。从集合论的角度有

$$\forall X,Y\subseteq U. X\subseteq Y \quad \Rightarrow\quad F^\delta(X)\subseteq F^\delta(Y) \quad or\quad F(X)\subseteq F(Y) $$

论文中作者给了一个例子来说明这个公式。

# Fixed-point

这个概念在前面已经提到，用处非常广泛。定义就很简单：如果$F(X) = X$，则$X$称为$F$的不动点，注意不动点是一个集合。