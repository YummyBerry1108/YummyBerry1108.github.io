---
layout: custom_post
title: "如何用生成函數解遞迴關係式"
date: 2025-11-27
update: 2025-11-27
author: "Berry"
tags: [離散數學, 生成函數]
---

我真的快被這鬼東西搞爆了，趕快在我剛懂得時候記錄下來

# 什麼是生成函數(Generating Function)

把數列包裝成一個多項式

$$
A(x) = \sum_{n=0}^{\infty}a_nx^n = a_0 + a_1x + a_2x^2 + ...
$$

考慮一個遞迴關係式

$$
a_n = 3a_{n-1} + 2 \space (n \ge 1) \space 且 \space a_0 = 1
$$

套換成無限級數的形式 

也就是說可以想像成左式 a_1 對應 右式 a_0 + 2 

然後這樣無限對應下去
