---
title: 一元函数积分概念和计算
subtitle: 不定积分存在定理介绍，常用积分手段
date: 2022-10-12T13:57:23.358Z
draft: false
featured: false
tags:
  - Math
image:
  filename: 2835-1024.jpg
  focal_point: Smart
  preview_only: false
---
# 一元函数积分概念和计算

## 不定积分存在定理

1. 连续函数$f(x)$必有原函数$F(x)$
2. $f(x)$在区间内包含第一类间断点和无穷间断点必没有原函数。（震荡间断点可能有）

## 定积分存在定理

1. 必要条件：可积函数$f(x)$在有限的积分区间必有界。
2. 充分条件：$f(x)$在积分区间连续或单调，或者有界且有有限个间断点。



## 积分计算方法

**凑微分法：** $\int f[g(x)]g'(x)dx = \int f[g(x)]d[g(x)] = \int f(u)du$

**换元法：**$\int f(x)dx $令$x = g(u)$ ,可得$\int f[g(u)]d[g(u)] = \int f[g(u)]g'(u)du$ .注意如果是定积分需要改变积分区间，一定不能忘记

**分部积分法：**$\int udv = uv - \int vdu$

**有理函数积分：**$\int \frac{P_n(x)}{Q_m(x)}dx(n<m)$, 其中$P_n(x),Q_m(x)$分别是x的n次多项式和m次多项式。 将分母因式分解在分别积分相加。分解原则：

![img](picture/2835-1024.jpg)

**定积分定义求解：****主要针对无法使用夹逼准则的极限和。**  $\int_0^1 f(x) dx = \lim\limits_{n \to \infty} \sum_{i=1}^n f(\frac{i}{n}) \frac {1}{n}$.  主要从式子右边凑出 $\frac{i}{n}$，令其等于$x$, 凑出$\frac{1}{n}$，令其等于$dx$.



### 一些定积分计算性质：

* $f(x)$为偶函数则 $\int_{-a}^a f(x)dx = 2\int_0^a f(x)dx$
* $f(x)$为奇函数则$\int_{-a}^a f(x)dx = 0$
* $f(x)$是周期为T的连续函数，则$\int_a^{a+T}f(x)dx = \int_0^T f(x)dx$
* $f(x)$为连续函数则 $\int_a^bf(x)dx = \int_a^bf(a+b-x)dx$ , 又叫区间再现公式
* $\int_0^{\frac{\pi}{2}} \sin^nxdx = \int_0^{\frac{\pi}{2}} \cos^nxdx = \begin{cases} \frac{n-1}{n} \cdot \frac{n-3}{n-2} ... \frac{2}{3} \cdot 1 |n是奇数 \\ \frac{n-1}{n} \cdot \frac{n-3}{n-2} ... \frac{1}{2} \cdot \frac{\pi}{2} | n是偶数 \end{cases}  $
* 三角函数族正交性${1,\cos x, \sin x,\cos n x, \sin n x}$. 任意两个在区间$[-\pi , \pi]$相乘积分为0.例如：$\int_{- \pi}^{\pi} 1 \cdot \cos nx dx = 0$ 或者 $\int_{- \pi}^{\pi} \cos nx \sin mx dx = 0$其中 $n \neq m$。

## 反常积分

**基础概念：**积分区间无穷或者被积函数无界的积分。其中$f(x)$越小， 则$\int_a^{+ \infty}f(x)dx$越容易收敛。

**注意：有一些定积分积分区间虽然有限，但是当中存在某些瑕点使被积函数无界。**

### 反常积分收敛判断

### 	**比较审敛：**

$0 \leq f(x) \leq g(x)$, 若 $\int_a^{+ \infty}g(x)$收敛，则$f(x)$也收敛。若$\int_a^{+ \infty}f(x)$发散，则$g(x)$的反常积分也发散。 **简记：大的收敛，小的一定收敛，大的发散，小的也一定发散。**

### **无穷区间极限审敛**

若$p>1, \lim\limits_{x \to + \infty} x^pf(x) = C$存在， 则积分收敛。 若$p=1, \lim\limits_{x \to +\infty}xf(x) = d >0$, 则积分发散。

 **注：一般$f(x)$带有分母乘一个$x^p$后求极限可以判断收敛**

### 	**无界函数极限审敛：**

 设函数$f(x)$在区间$(a,b]$上连续，且$f(x) \ge 0, x=a$为$f(x)$的瑕点，如果存在常数$0<q<1$， 使得$\lim\limits_{x \to a^+}(x-a)^q f(x)$存在，反常积分$\int_a^bf(x)dx$收敛。如果$\lim\limits_{x \to a^+}(x-a)f(x) = d >0$那么反常积分发散。 e.g 判断$\int_1^3 \frac{dx}{\ln x}$的收敛性。

**助记：无穷区间大于1，无界函数小于1，等于1都发散**

### 重要结论：

无穷区间的反常积分 $\int_1^{+ \infty} \frac{dx}{x^p}$, p >1收敛，$p \leq 1$发散。

无界函数的反常积分$\int_0^1 \frac{dx}{x^p}$, p<1收敛， p>=1发散。

## **无穷大比阶**

$n \to \infty$时，$\ln n < n^k < k^n < n! < n^n$

 e.g $\lim\limits_{n \to \infty} \frac{x^k}{e^x} = 0$
