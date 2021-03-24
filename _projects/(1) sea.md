---
name: 海洋水体渲染
tools: [Unity, Shader]
image: ../assets/img/col/1.png
description: 水体模拟、菲涅尔反射、直射光透射
comments: true
---

<br/>

![avatar](../assets/img/col/1.png)

![avatar](../assets/img/col/2.png)

![avatar](../assets/img/col/3.png)

<br/>

### 水的波形

GPU Gem 第一章笔记：

[Effective Water Simulation from Physical Models](https://friedsoda.github.io/blog/sea)



<br/>

### 水面颜色

水面颜色分为反射分量、折射分量还有加性的高光分量。

折射和反射分量的比重用菲涅尔效应的公式计算。