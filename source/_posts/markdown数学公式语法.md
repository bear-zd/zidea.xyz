---
title: markdown数学公式语法
date: 2020-10-08 22:04:38
tags: markdown语法
mathjax: true
---
之前的博文中有提到，markdown可以实现数学公式，在预览中也看到了其效果，真不戳！，所以专门开了一篇博文用来说明markdown的数学公式语法，同时也是加固自己的印象，为以后推更多技术性的文章打下基础
___
## 行内和独行公式
在进行公式语法的讲解前，首先需要知道如何创建一个数学公式
```
$公式内容$
$$公式内容$$
```
这两者有什么区别呢，前者是行内公式，即将公式插入本行$xyz$，是的，就像这样。
<br />后者是独行公式，是将公式插入到新的一行并居中，效果如下
$$xyz$$

所以很容易就可以知道两者的使用环境了。
___
## 上标、下标与组合
```
上标符号： ^ , 如$x^4$
下标符号： _ , 如$x_1$
组合符号： {} , 如$^{16}_{8}O^{2+}_{2}$
```
接下来是刚才三个例子的预览效果：
$$x^4$$
$$x_1$$
$$^{16}_{8}O^{2+}_{2}$$
___
## 汉字、字体与格式
```
1.汉字形式，符号：\mbox{}，如：$V_{\mbox{初始}}$
2.字体控制，符号：\displaystyle，如：$\displaystyle \frac{x+y}{y+z}$
3.下划线符号，符号：\underline，如：$\underline{x+y}$
4.标签，符号\tag{数字}，如：$\tag{11}$
5.上大括号，符号：\overbrace{算式}，如：$\overbrace{a+b+c+d}^{2.0}$
6.下大括号，符号：\underbrace{算式}，如：$a+\underbrace{b+c}_{1.0}+d$
7.上位符号，符号：\stacrel{上位符号}{基位符号}，如：$\vec{x}\stackrel{\mathrm{def}}{=}{x_1,\dots,x_n}$

```
上述例子的预览效果：
$$\mathrm{初始}$$
$$\frac{x+y}{y+z}$$
$$\underline{x+y}$$
$$\overbrace{a+b+c+d}^{2.0}$$
$$a+\underbrace{b+c}_{1.0}+d$$
$$\vec{x}\stackrel{\mathrm{def}}{=}{x_1,\dots,x_n}$$
___
## 占位符
```
1.两个quad空格 符号：\qquad，如：$x \qquad y$
2.quad空格 符号：\quad，如：$x \quad y$
3.大空格 符号\，如：$x \ y$
4.中空格，符号\:，如：$x : y$
5.小空格，符号\,，如：$x , y$
6.没有空格，符号``，如：$xy$
7.紧贴，符号\!，如：$x ! y$
```
<center>**注意，需要加反斜杠**</center>

$$x \qquad y$$
$$x \quad  y$$
$$x \ y$$
$$x \: y$$
$$x \, y$$
$$xy$$
$$x \! y$$
___
## 定界符与组合
```
1.括号 符号：（）\big(\big) \Big(\Big) \bigg(\bigg) \Bigg(\Bigg)，如：$（）\big(\big) \Big(\Big) \bigg(\bigg) \Bigg(\Bigg)$
2.中括号 符号：[]，如：$[x+y]$
3.大括号 符号：\{ \}，如：${x+y}$
4.自适应括号 符号：\left \right，如：$\left(x\right)$，$\left(x{yz}\right)$
5.组合公式 符号：{上位公式 \choose 下位公式}，如：${n+1 \choose k}={n \choose k}+{n \choose k-1}$
6.组合公式 符号：{上位公式 \atop 下位公式}，如：$\sum_{k_0,k_1,\ldots>0 \atop k_0+k_1+\cdots=n}A_{k_0}A_{k_1}\cdots$
```
$$（）\big(\big) \Big(\Big) \bigg(\bigg) \Bigg(\Bigg)$$
$$[x+y]$$
$${x+y}$$
$$\left(x\right)$$
$$\left(x{yz}\right)$$
$${n+1 \choose k}={n \choose k}+{n \choose k-1}$$
$$\sum_{k_0,k_1,\ldots>0 \atop k_0+k_1+\cdots=n}A_{k_0}A_{k_1}\cdots$$
___
## 四则运算
符号表述|符号|效果
-|-|-|-
加法运算|+|$x+y=z$
减法运算|-|$x-y=z$
加减运算|\pm|$x \pm y=z$
减甲运算|\mp|$x \mp y=z$
乘法运算|\times|$x \times y=z$
点乘运算|\cdot|$x \cdot y=z$
星乘运算|\ast|$x \ast y=z$
除法运算|\div|$x \div y=z$
斜法运算|/|$x/y=z$
分式表示|\frac{分子}{分母}|$\frac{x+y}{y+z}$
分式表示|{分子} \voer {分母}|${x+y} \over {y+z}$
```
绝对值： || 如：|x+y| (因为与表格产生冲突而单独列出，日后会找到解决方案)
```
 $|x+y|$
___
## 高级运算
符号表述|符号|事例|效果
-|-|-|-|-
平均数运算|\overline{算式}|\$\overline{xyz}$|$\overline{xyz}$
开二次方运算|\sqrt|\$\sqrt x$|$\sqrt x$
开方运算|\sqrt[开方数]{被开方数}|\$\sqrt[3]{x+y}$|$\sqrt[3]{x+y}$
对数运算 |\log|\$\log(x)$|$\log(x)$
极限运算|\lim|\$\lim^{x \to \infty}_{y \to 0}{\frac{x}{y}}$|$\lim^{x \to \infty}_{y \to 0}{\frac{x}{y}}$
极限运算|\displaystyle \lim|\$\displaystyle \lim^{x \to \infty}_{y \to 0}{\frac{x}{y}}$|$\displaystyle \lim^{x \to \infty}_{y \to 0}{\frac{x}{y}}$
求和运算|\sum|\$\sum^{x \to \infty}_{y \to 0}{\frac{x}{y}}$|$\sum^{x \to \infty}_{y \to 0}{\frac{x}{y}}$
求和运算|\displaystyle \sum|\$\displaystyle \sum^{x \to \infty}_{y \to 0}{\frac{x}{y}}$|$\displaystyle \sum^{x \to \infty}_{y \to 0}{\frac{x}{y}}$
积分运算|\int|\$\int^{\infty}_{0}{xdx}$|$\int^{\infty}_{0}{xdx}$
积分运算|\displaystyle \int|\$\displaystyle \int^{\infty}_{0}{xdx}$|$\displaystyle \int^{\infty}_{0}{xdx}$
微分运算|\partial|\$\frac{\partial x}{\partial y}$|$\frac{\partial x}{\partial y}$
```
矩阵表示： \begin{matrix} \end{matrix} 如：\$\left[ \begin{matrix} 1 &2 &\cdots &4\5 &6 &\cdots &8\\vdots &\vdots &\ddots &\vdots\13 &14 &\cdots &16\end{matrix} \right]$
```
$$\left[ \begin{matrix} 1 &2 &\cdots &4&5 &6 &\cdots &8\\\vdots &\vdots &\ddots &\vdots\quad13 &14 &15&\cdots &16\\\end{matrix} \right]$$
## 逻辑运算
符号表述|符号|效果
-|-|-|-|-
等于运算 |\=|$x+y=z$
大于运算 |\>|$x+y>z$
小于运算 |\<|$x+y<z$
大于等于运算|\\geq|$x+y \geq z$
小于等于运算|\\leq|$x+y \leq z$
不等于运算|\\neq|$x+y \neq z$
不大于等于运算|\\ngeq|$x+y \ngeq z$
不大于等于运算|\\not\geq|$x+y \not\geq z$
不小于等于运算|\\nleq|$x+y \nleq z$
不小于等于运算|\\not\leq|$x+y \not\leq z$
约等于运算|\\approx|$x+y \approx z$
恒定等于运算|\\equiv|$x+y \equiv z$
___
## 集合运算
符号表述|符号|事例|效果
-|-|-|-|-
属于运算 |\in|\$x \in y$|$x \in y$
不属于运算 |\notin|\$x \notin y$|$x \notin y$
不属于运算 |\not\in|\$x \not\in y$|$x \not\in y$
子集运算 |\subset|\$x \subset y$|$x \subset y$
子集运算 |\supset|\$x \supset y$|$x \supset y$
真子集运算 |\subseteq|\$x \subseteq y$|$x \subseteq y$
非真子集运算 |\subsetneq|\$x \subsetneq y$|$x \subsetneq y$
真子集运算 |\supseteq|\$x \supseteq y$|$x \supseteq y$
非真子集运算 |\supsetneq|\$x \supsetneq y$|$x \supsetneq y$
非子集运算 |\not\subset|\$x \not\subset y$|$x \not\subset y$
非子集运算 |\not\supset|\$x \not\supset y$|$x \not\supset y$
并集运算 |\cup|\$x \cup y$|$x \cup y$
交集运算 |\cap|\$x \cap y$|$x \cap y$
差集运算 |\setminus|\$x \setminus y$|$x \setminus y$
同或运算 |\bigodot|\$x \bigodot y$|$x \bigodot y$
同与运算 |\bigotimes|\$x \bigotimes y$|$x \bigotimes y$
实数集合 |\mathbb{R}|\$\mathbb{R}$|$\mathbb{R}$
自然数集合 |\mathbb{Z}|\$\mathbb{Z}$|$\mathbb{Z}$
空集 |\emptyset|\$\emptyset$|$\emptyset$
___
## 数学符号
符号表述|符号|事例|效果
-|-|-|-|-
无穷 |\infty |\$\infty$|$\infty$
虚数 |\imath|\$\imath$|$\imath$
虚数 |\jmath|\$\jmath$|$\jmath$
数学符号 |\hat{a}|\$\hat{a}$|$\hat{a}$
数学符号 |\check{a}|\$\check{a}$|$\check{a}$
数学符号 |\breve{a}|\$\breve{a}$|$\breve{a}$
数学符号 |\tilde{a}|\$\tilde{a}$|$\tilde{a}$
数学符号 |\bar{a}|\$\bar{a}$|$\bar{a}$
矢量符号 |\vec{a}|\$\vec{a}$|$\vec{a}$
数学符号 |\acute{a}|\$\acute{a}$|$\acute{a}$
数学符号 |\grave{a}|\$\grave{a}$|$\grave{a}$
数学符号 |\mathring{a}|\$\mathring{a}$|$\mathring{a}$
一阶导数符号 |\dot{a}|\$\dot{a}$|$\dot{a}$
二阶导数符号 |\ddot{a}|\$\ddot{a}$|$\ddot{a}$
上箭头 |\uparrow|\$\uparrow$|$\uparrow$
上箭头 |\Uparrow|\$\Uparrow$|$\Uparrow$
下箭头 |\downarrow|\$\downarrow$|$\downarrow$
下箭头 |\Downarrow|\$\Downarrow$|$\Downarrow$
左箭头 |\leftarrow|\$\leftarrow$|$\leftarrow$
左箭头 |\Leftarrow|\$\Leftarrow$|$\Leftarrow$
右箭头 |\rightarrow|\$\rightarrow$|$\rightarrow$
右箭头 |\Rightarrow|\$\Rightarrow$|$\Rightarrow$
底端对齐的省略号 |符号：\ldots|\$1,2,\ldots,n$|$1,2,\ldots,n$
中线对齐的省略号 |符号：\cdots|\$x_1^2 + x_2^2 + \cdots + x_n^2$|$x_1^2 + x_2^2 + \cdots + x_n^2$
竖直对齐的省略号 |符号：\vdots|\$\vdots$|$\vdots$
斜对齐的省略号 |符号：\ddots|\$\ddots$|$\ddots$
___
## 希腊字母
字母|实现|字母|实现
-|-|-|-|-
A|A |α|\alpha
B|	B|	β	|\beta
Γ|	\Gamma|	γ	|\gamma
Δ|	\Delta|	δ	|\delta
E|	E|	ϵ	|\epsilon
Z|	Z|	ζ	|\zeta
H|	H|	η	|\eta
Θ|	\Theta|	θ|	\theta
I|	I|	ι	|\iota
K|	K|	κ	|\kappa
Λ|	\Lambda|	λ|	\lambda
M|	M|	μ	|\mu
N|	N|	ν	|\nu
Ξ|	\Xi|	ξ|	\xi
O|	\Omicron|	ο	|\omicron
Π|	\Pi|	π|	\pi
P|	\Rho|	ρ	|\rho
Σ|	\Sigma|	σ|	\sigma
T|	\Tau|	τ	|\tau
Υ|	\Upsilon|	υ|	\upsilon
Φ|	\Phi|	ϕ|	\phi
X|	\Chi	|χ	|\chi
Ψ|	\Psi|	ψ|	\psi
Ω|	\Omega	|ω|	\omega
___
**以上就是一些常用的数学公式，预览效果确实很好（在此过程中有涉及到hexo对数学公式种类的支持操作，可以参见：[在HEXO博客中使用LaTeX公式的简单方法](https://blog.csdn.net/weixin_43318626/article/details/89407031)），也为今后做笔记扫除了一个障碍。不求全部记忆，但求可以熟练使用。**