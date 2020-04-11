---
layout: post
title: Data Refinement 阅读笔记(4)
categories:
- 形式化方法
- 验证
- Data Refinement
- 读书笔记
tags:
- Data Refinement
---

# Properties of Simulation

Correctness of an implementation $\equiv$ the corresponding diagrams commute weakly.

## Composing Simulation Diagrams

### Concatenation of Simulation Diagrams

![avatar](/assets/image/Def421.png){:width="90%"}
![avatar](/assets/image/Def422.png){:width="90%"}

Note that 3 and 4 doesn't require any condition to $\alpha$.

### Vertical Composition of Simulation Diagrams

![avatar](/assets/image/Cor44.png){:width="90%"}

## Implications between Simulations

![avatar](/assets/image/sum4.png){:width="90%"}

If $\alpha$ is total and functional the four simulations are equivalent.

## Data Invariants and Totality of Abstraction Relations

Using data invariant can convert partial abstraction relation to total one by restricting data type on reachable subset.

## Soundness of Simulation

**Soundness of simulation, that is, simulation between data types implies data refinement.**

**Theorem 4.10 (Soundness of simulation)**

L- and L$^{-1}$-simulation are sound. U-simulation is sound if the abstraction relation is total. U$^{-1}$-simulation is sound if the abstraction relation is functional.

## Maximal Data Type
