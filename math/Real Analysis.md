

# MA-504 分析课程期末复习指南（Chapter 1–8）

## 第1章 实数系与复数系

### 基本定义与直观理解

**实数域及完备性：**
实数集 <img src="https://latex.codecogs.com/svg.latex?\mathbb{R}" alt="\mathbb{R}"/> 可以定义为一个具有**最小上界性质**的有序域。这意味着：如果一个实数子集有上界，那么必有一个**最小上界**（即上确界）。有理数集 <img src="https://latex.codecogs.com/svg.latex?\mathbb{Q}" alt="\mathbb{Q}"/> 就不具备完备性（如集合 <img src="https://latex.codecogs.com/svg.latex?\{x\in\mathbb{Q}\mid x^2<2\}" alt="{x\in\mathbb{Q}\mid x^2<2}"/> 在有理数中没有上确界，但在实数中有上确界 <img src="https://latex.codecogs.com/svg.latex?\sqrt{2}" alt="\sqrt{2}"/>）。

**顺序与界：**
在实数集中可以比较大小。子集若存在一个元素大于等于它所有元素，则称该元素为**上界**；若此上界又最小，则为**上确界**。例如，区间 <img src="https://latex.codecogs.com/svg.latex?(0,1)" alt="(0,1)"/> 的上确界是 <img src="https://latex.codecogs.com/svg.latex?1" alt="1"/>，下确界是 <img src="https://latex.codecogs.com/svg.latex?0" alt="0"/>。

**阿基米德性质与稠密性：**
阿基米德性质： <img src="https://latex.codecogs.com/svg.latex?\forall\,x\in\mathbb{R},\;\exists\,n\in\mathbb{N}\;\text{s.t.}\;n>x" alt="\forall\,x\in\mathbb{R},\;\exists\,n\in\mathbb{N}\;\text{s.t.}\;n>x"/>
稠密性：任意两实数间都存在有理数。

**复数的引入：**
复数集 <img src="https://latex.codecogs.com/svg.latex?\mathbb{C}" alt="\mathbb{C}"/> 元素形如 <img src="https://latex.codecogs.com/svg.latex?a+bi" alt="a+bi"/>，<img src="https://latex.codecogs.com/svg.latex?i^2=-1" alt="i^2=-1"/>。模 <img src="https://latex.codecogs.com/svg.latex?|a+bi|=\sqrt{a^2+b^2}" alt="|a+bi|=\sqrt{a^2+b^2}"/>，复平面表示为 <img src="https://latex.codecogs.com/svg.latex?re^{i\theta}" alt="re^{i\theta}"/>。

---

## 第2章 基本拓扑

**度量空间：** <img src="https://latex.codecogs.com/svg.latex?d:X\times X\to\mathbb{R}_{\ge0}" alt="d:X\times X\to\mathbb{R}_{\ge0}"/>，满足三角不等式。开球 <img src="https://latex.codecogs.com/svg.latex?B(x,r)=\{y:d(x,y)<r\}" alt="B(x,r)=\{y:d(x,y)<r\}"/>。

**开、闭集：** <img src="https://latex.codecogs.com/svg.latex?U"/> 开 ⇔ 每点都有包含于 <img src="https://latex.codecogs.com/svg.latex?U"/> 的邻域。闭集 <img src="https://latex.codecogs.com/svg.latex?F"/> ⇔ <img src="https://latex.codecogs.com/svg.latex?X\setminus F"/> 开。

**极限点与闭包：** <img src="https://latex.codecogs.com/svg.latex?\overline{E}"/> 表示 <img src="https://latex.codecogs.com/svg.latex?E"/> 及其所有极限点的集合。

**紧致性（$\mathbb{R}^n$）：**
闭有界 ⇔ 紧（Heine–Borel 定理）。

**连通性：**
不可分为两个互不相交非空开集。

---

## 第3章 数值序列与级数

### 数列

**极限：** <img src="https://latex.codecogs.com/svg.latex?\lim_{n\to\infty}a_n=L"/> ⇔ <img src="https://latex.codecogs.com/svg.latex?\forall\varepsilon>0,\exists N,\forall n>N,\;|a_n-L|<\varepsilon"/>。

**柯西序列：** <img src="https://latex.codecogs.com/svg.latex?\forall\varepsilon>0,\exists N,\forall m,n>N,\;|a_n-a_m|<\varepsilon"/>。

### 上下极限

<img src="https://latex.codecogs.com/svg.latex?\limsup_{n\to\infty}a_n=\lim_{n\to\infty}\bigl(\sup_{k\ge n}a_k\bigr)" alt="\limsup_{n\to\infty}a_n=\lim_{n\to\infty}\bigl(\sup_{k\ge n}a_k\bigr)"/>  
<img src="https://latex.codecogs.com/svg.latex?\liminf_{n\to\infty}a_n=\lim_{n\to\infty}\bigl(\inf_{k\ge n}a_k\bigr)" alt="\liminf_{n\to\infty}a_n=\lim_{n\to\infty}\bigl(\inf_{k\ge n}a_k\bigr)"/>  

### 数项级数

**定义：** <img src="https://latex.codecogs.com/svg.latex?S_N=\sum_{n=1}^N a_n"/>，若 <img src="https://latex.codecogs.com/svg.latex?\lim_{N\to\infty}S_N"/> 存在，则收敛。

**判别法：**

* 比较法
* 比值法：<img src="https://latex.codecogs.com/svg.latex?L=\lim_{n\to\infty}\bigl|\tfrac{a_{n+1}}{a_n}\bigr|"/>
* 根值法：<img src="https://latex.codecogs.com/svg.latex?L=\lim_{n\to\infty}\sqrt[n]{|a_n|}"/>
* 交错级数（Leibniz）：<img src="https://latex.codecogs.com/svg.latex?a_n\searrow0"/>

### 幂级数

<center><img src="https://latex.codecogs.com/svg.latex?\sum_{n=0}^\infty c_n(x-a)^n" alt="\sum_{n=0}^\infty c_n(x-a)^n"/></center>  
收敛半径 <img src="https://latex.codecogs.com/svg.latex?R=1/\limsup_{n\to\infty}\sqrt[n]{|c_n|}" alt="R=1/\limsup_{n\to\infty}\sqrt[n]{|c_n|}"/>。

---

## 第4章 连续性

**连续（ε–δ）：** <img src="https://latex.codecogs.com/svg.latex?\forall\varepsilon>0,\exists\delta>0,\forall x,|x-x_0|<\delta\implies|f(x)-f(x_0)|<\varepsilon"/>。

**一致连续：** <img src="https://latex.codecogs.com/svg.latex?\forall\varepsilon>0,\exists\delta>0,\forall x,y,|x-y|<\delta\implies|f(x)-f(y)|<\varepsilon"/>。

**极值定理：** 紧集上连续 ⇒ 达到最大最小值。
**介值定理：** 区间上连续 ⇒ 值域也是区间。

---

## 第5章 导数

**导数定义：** <img src="https://latex.codecogs.com/svg.latex?f'(x_0)=\lim_{h\to0}\frac{f(x_0+h)-f(x_0)}{h}"/>。

**中值定理：**

* Rolle：<img src="https://latex.codecogs.com/svg.latex?f(a)=f(b)\implies\exists c,f'(c)=0"/>。
* Lagrange：<img src="https://latex.codecogs.com/svg.latex?f'(c)=\frac{f(b)-f(a)}{b-a}"/>。

**泰勒公式：** <img src="https://latex.codecogs.com/svg.latex?f(x)=\sum_{k=0}^n\frac{f^{(k)}(a)}{k!}(x-a)^k+R_n(x)" alt="Taylor formula"/>。

---

## 第6章 定积分

**定义（Riemann）：** <img src="https://latex.codecogs.com/svg.latex?\int_a^b f(x)\,dx=\lim_{\|P\|\to0}\sum f(\xi_i)\Delta x_i"/>。

**基本定理：**

* <img src="https://latex.codecogs.com/svg.latex?F(x)=\int_a^x f(t)\,dt\implies F'(x)=f(x)"/>。
* Newton–Leibniz：<img src="https://latex.codecogs.com/svg.latex?\int_a^b f(x)\,dx=F(b)-F(a)"/>。

**技巧：** 置换积分、分部积分、广义积分。

---

## 第7章 函数列与函数项级数

**逐点 vs 一致收敛：**

* 逐点：<img src="https://latex.codecogs.com/svg.latex?\forall x,\;f_n(x)\to f(x)"/>。
* 一致：<img src="https://latex.codecogs.com/svg.latex?\sup_x|f_n(x)-f(x)|\to0"/>。

**Weierstrass M-判别：**
若 <img src="https://latex.codecogs.com/svg.latex?|f_n(x)|\le M_n"/>，<img src="https://latex.codecogs.com/svg.latex?\sum M_n"/> 收敛，则一致绝对收敛。

---

## 第8章 拓扑进阶与度量空间

**完备性：** 所有柯西列收敛。
**全有界：** 任意 ε-网可选有限子网覆盖。
**紧性：** 完备+全有界 ⇒ 紧（一般度量空间）。
**Bolzano–Weierstrass：** 有界序列必有收敛子序列。
**可分性：** 存在稠密可数子集。
**二可数性：** 存在可数拓扑基。


