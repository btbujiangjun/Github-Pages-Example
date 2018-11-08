---
layout:     post
title:      Logistic Regression, 机器学习的Hello World
category: blog
description: 对于深度学习小白用户，从哪上手比较好呢？ 嗯，当然是hello world——logistic regression
---

## Logistic Regression在深度学习中的位置
如果把深度神经网络看作人体，那Logistic Regression(后简称LR)就是细胞。当然，LR本身也可以工作的很好，想想生命的起源——单细胞动物。

## Logistic Regression与Linear Regression
Logistic Regression与Linear Regression有很大联系。Linear Regression用于对连续值做出预估，其输出集为实数R，如房价预测。Logistic Regression一般用于概率建模，输出一般为\[0,1\](取决于假设/激活函数)，典型应用场景如CTR预估,二分类问题。

> Linear Regression + Hypothesis func = Logistic Regression 。

Linear Regression 因变量y服从高斯分布， Logistic Regression因变量y服从伯努利分布。

## 假设 & 决策函数
> 二分类： h(x) = 1/(1 + e^-x)
> 多分类： softmax

> x = w0 + w1*x1 + w2*x2 + ...

> y^ = 1  if h(x) > 0.5 else y^ = 0

## 代价函数 Cost function
J(0) 度量y^ 与 y 的差异

Linear Regression,一般用MSE(mean square error): J = 1/2m * E(y^ - y)^2
Logistic Regression, 一般用CE(cross entropy): J = -1/m * E(yi*log(yi^) + (1 - yi)*log(1-log(yi^))

## 梯度更新
梯度，代价函数对各个参数的偏导数。
