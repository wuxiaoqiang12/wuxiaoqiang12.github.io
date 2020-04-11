---
layout: post
title: Data Refinement 阅读笔记(1)
categories:
- 形式化方法
- 验证
- Data Refinement
- 读书笔记
tags:
- Data Refinement
---

这是一个占坑贴，这本书已经读了一遍半了。计划重新读顺便记录笔记。

&emsp;&emsp;《Data Refinement: Model-oriented Proof Methods and their Comparison》本书对于形式化方法中的**精化**做了详细的数学推导，并对现有几种不同的形式化方法进行了对比。

# Introduction to Data Refinement
**Some definitions**:
- **Refinement**: The observations of the concrete program are contained in those of the corresponding abstract program.
- **Abstract data type**: is defined by a set of operators and a set of axioms, typically given in the form of equations.

![avatar](/assets/image/DataRefinement.png)
![avatar](/assets/image/define171.png)
![avatar](/assets/image/define172.png)

In above definition 1.7, the important is normal variables $\vec {x}$ representation variables $\vec a$ and their value space $\Sigma^{\text{N}} = [\vec x \rightarrow \mathbb{V}]$, $\Sigma_{\text{A}} = [\vec a \rightarrow \mathbb{V}^{\text{A}}]$, respectively. The notion $\sigma$ is used to map specific variable to its value, like $\sigma(x) = \text{some value}$.
