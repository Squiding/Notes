
# MA-504 分析课程期末复习指南（Chapter 1–8）

## 第1章 实数系与复数系

### 基本定义与直观理解

**实数域及完备性：**
实数集 <img src="https://latex.codecogs.com/svg.latex?\mathbb{R}"/> 可以定义为一个具有**最小上界性质**的有序域。这意味着：如果一个实数子集有上界，那么必有一个**最小上界**（即上确界）。换句话说，实数填补了有理数的“空隙”，使得任何缺失的极限值都包含在实数范围内。直观上，实数可以看作无限小数或数轴上的所有点。实数的这种完备性是分析学的基石：例如有理数集 <img src="https://latex.codecogs.com/svg.latex?\mathbb{Q}"/> 就不具备完备性（如集合 `{x∈Q :x²<2}` 在有理数中没有上确界，但在实数中有上确界 <img src="https://latex.codecogs.com/svg.latex?\sqrt{2}"/>）。

**顺序与界：**
在实数集中可以比较大小。有序集合中的一个子集如果存在一个元素大于等于该子集所有元素，则称该元素为该子集的一个**上界**；如果某上界小于任何其他上界，则称其为**最小上界（上确界）**。类似地定义下界和**最大下界（下确界）**。例如，区间 `(0,1)` 在 <img src="https://latex.codecogs.com/svg.latex?\mathbb{R}"/> 中的上确界是 <img src="https://latex.codecogs.com/svg.latex?1"/>，下确界是 <img src="https://latex.codecogs.com/svg.latex?0"/>，但这两个点不属于该区间。实数的**最小上界性质**保证每个有上界的非空实数集都存在上确界。同理，每个有下界的非空实数集都存在下确界。

**阿基米德性质与稠密性：**
实数域具有**阿基米德性质**：对于任意实数，总存在足够大的整数超越它；形式化地， <img src="https://latex.codecogs.com/svg.latex?\forall x\in\mathbb{R},\exists n\in\mathbb{N}\;s.t.\;n>x"/>。
同样地，对于任意正实数 <img src="https://latex.codecogs.com/svg.latex?y"/>, 也存在充分大的 <img src="https://latex.codecogs.com/svg.latex?n"/> 使得 <img src="https://latex.codecogs.com/svg.latex?1/n<y"/>。这蕴含了有理数在实数中的**稠密性**：任意两个不相等的实数之间必存在有理数（甚至无理数）。例如，在 <img src="https://latex.codecogs.com/svg.latex?0"/> 和 <img src="https://latex.codecogs.com/svg.latex?1"/> 之间可以找到有理数 <img src="https://latex.codecogs.com/svg.latex?1/2"/>，有理数之间也能找到无理数 <img src="https://latex.codecogs.com/svg.latex?\sqrt{2}/2"/> 等。

**实数的基本性质：**
实数集是一个完全有序域，包含有理数作为子域。实数的四则运算、排序和基本代数性质大家已经熟悉。尤其值得注意的是实数的完备性使得许多极限过程和解析过程在实数范围内都有确定的结果。

**复数的引入：**
复数集 <img src="https://latex.codecogs.com/svg.latex?\mathbb{C}"/> 可以被看作是实数的扩充，形式为 <img src="https://latex.codecogs.com/svg.latex?a+bi"/>，其中 <img src="https://latex.codecogs.com/svg.latex?a,b\in\mathbb{R}"/>， <img src="https://latex.codecogs.com/svg.latex?i"/> 是满足 <img src="https://latex.codecogs.com/svg.latex?i^2=-1"/> 的虚数单位。复数可以在平面上表示为点或向量（称为复平面，又称 Argand 平面），实数对应复平面实轴上的点。复数间定义了加法和乘法，使其成为一个域；但复数集**并非有序集合**（不存在使 <img src="https://latex.codecogs.com/svg.latex?i"/> 满足 <img src="https://latex.codecogs.com/svg.latex?i>0"/> 或 <img src="https://latex.codecogs.com/svg.latex?i<0"/> 的全序关系），因此无法直接比较大小。每个非零复数都可以表示为极坐标形式 <img src="https://latex.codecogs.com/svg.latex?re^{i\theta}"/>，其中 <img src="https://latex.codecogs.com/svg.latex?r=|z|"/> 是复数的模， <img src="https://latex.codecogs.com/svg.latex?\theta=\arg(z)"/> 是辐角。

**复数的基本性质：**
复数的模定义为 <img src="https://latex.codecogs.com/svg.latex?|a+bi|=\sqrt{a^2+b^2}"/>，满足三角不等式： <img src="https://latex.codecogs.com/svg.latex?|z_1+z_2|\le|z_1|+|z_2|"/>。直观上，模表示复平面上点到原点的距离。复数除实数性质外还有共轭（<img src="https://latex.codecogs.com/svg.latex?\overline{a+bi}=a-bi"/>）、极表示等。在实数范围内无解的方程（如 <img src="https://latex.codecogs.com/svg.latex?x^2+1=0"/>）在复数范围内有解，因此复数域是代数封闭的——根据**代数基本定理**，任何非常数单变量复系数多项式在复数域上必有根。

---

## 第2章 基本拓扑

### 基本定义与直观理解

**度量空间与拓扑：**
本章建立分析的拓扑基础。首先，引入**度量空间**概念：集合 <img src="https://latex.codecogs.com/svg.latex?X"/> 上定义一个距离函数 <img src="https://latex.codecogs.com/svg.latex?d(x,y)"/>，满足非负性、正定性、对称性和三角不等式，即构成一个度量空间。度量空间中，可以利用距离来定义**开集**和**邻域**：对任意点 <img src="https://latex.codecogs.com/svg.latex?x"/>，以 <img src="https://latex.codecogs.com/svg.latex?x"/> 为中心、半径 <img src="https://latex.codecogs.com/svg.latex?r"/> 的球 <img src="https://latex.codecogs.com/svg.latex?B(x,r)=\{y\in X:d(x,y)<r\}"/> 称为 <img src="https://latex.codecogs.com/svg.latex?x"/> 的一个邻域。一个集合 <img src="https://latex.codecogs.com/svg.latex?U\subset X"/> 是**开集**，若对于其中每个点 <img src="https://latex.codecogs.com/svg.latex?x"/>，都存在半径 <img src="https://latex.codecogs.com/svg.latex?r_x>0"/> 使 <img src="https://latex.codecogs.com/svg.latex?B(x,r_x)\subset U"/>。类似地，将开集的补集定义为**闭集**：如果集合 <img src="https://latex.codecogs.com/svg.latex?F"/> 的补集 <img src="https://latex.codecogs.com/svg.latex?X\setminus F"/> 是开集，则称 <img src="https://latex.codecogs.com/svg.latex?F"/> 是闭集。直观上，开集没有包含它的“边界点”，而闭集包含自身所有极限边界。

**极限点与闭包：**
给定 <img src="https://latex.codecogs.com/svg.latex?E\subset X"/>，如果存在一个点 <img src="https://latex.codecogs.com/svg.latex?x"/>，对任何 <img src="https://latex.codecogs.com/svg.latex?r>0"/>，球 <img src="https://latex.codecogs.com/svg.latex?B(x,r)"/> 都含有 <img src="https://latex.codecogs.com/svg.latex?E"/> 中除 <img src="https://latex.codecogs.com/svg.latex?x"/> 本身外的其他点，则称 <img src="https://latex.codecogs.com/svg.latex?x"/> 是 <img src="https://latex.codecogs.com/svg.latex?E"/> 的一个**极限点**。集合所有极限点的全体，加上集合本身，形成集合的**闭包** <img src="https://latex.codecogs.com/svg.latex?\overline{E}"/>。闭集的一个等价定义是： <img src="https://latex.codecogs.com/svg.latex?F"/> 是闭的当且仅当它包含它的所有极限点，即 <img src="https://latex.codecogs.com/svg.latex?F=\overline{F}"/>。

**\$R^n\$ 中的拓扑性质：**
在 <img src="https://latex.codecogs.com/svg.latex?n"/> 维欧几里得空间 <img src="https://latex.codecogs.com/svg.latex?\mathbb{R}^n"/> 上，通常使用欧氏度量 <img src="https://latex.codecogs.com/svg.latex?d(x,y)=\sqrt{\sum_{i=1}^n(x_i-y_i)^2}"/>。这一定义下， <img src="https://latex.codecogs.com/svg.latex?\mathbb{R}^n"/> 成为度量空间，其开集、闭集定义与上述一般情况一致。例如，在 <img src="https://latex.codecogs.com/svg.latex?\mathbb{R}"/> 中，开区间是开集，闭区间是闭集。在 <img src="https://latex.codecogs.com/svg.latex?\mathbb{R}^2"/> 中，圆盘（不含边界）是开集，对应圆盘加上边界是闭集。

**子空间拓扑：**
如果 <img src="https://latex.codecogs.com/svg.latex?Y"/> 是 <img src="https://latex.codecogs.com/svg.latex?X"/> 的一个子集，那么 <img src="https://latex.codecogs.com/svg.latex?Y"/> 本身继承了一个自然的拓扑： <img src="https://latex.codecogs.com/svg.latex?Y"/> 中的开集可定义为 <img src="https://latex.codecogs.com/svg.latex?Y\cap U"/>，其中 <img src="https://latex.codecogs.com/svg.latex?U"/> 是 <img src="https://latex.codecogs.com/svg.latex?X"/> 中的开集。

**紧致性（紧性）：**
紧集直观上对应“有限的和没有漏洞”的集合。在度量空间中，一个集合 <img src="https://latex.codecogs.com/svg.latex?K"/> 是**紧**的，意即任何开放覆盖都有有限子覆盖。等价地（海涅–伯勒尔定理在 <img src="https://latex.codecogs.com/svg.latex?\mathbb{R}^n"/> 适用）：在 <img src="https://latex.codecogs.com/svg.latex?\mathbb{R}^n"/> 中，**紧集当且仅当它是闭且有界的**。例如，在 <img src="https://latex.codecogs.com/svg.latex?\mathbb{R}"/> 中，闭区间 <img src="https://latex.codecogs.com/svg.latex?[a,b]"/> 是紧的；开区间 <img src="https://latex.codecogs.com/svg.latex?(a,b)"/> 有界但不闭，因此不紧；整个实轴 <img src="https://latex.codecogs.com/svg.latex?\mathbb{R}"/> 闭但不有界，也不紧。

**连通性：**
拓扑空间是连通的，如果不能被拆分为两个不相交的非空开子集。直观上，连通空间是一整块的，不存在“裂缝”。 <img src="https://latex.codecogs.com/svg.latex?\mathbb{R}"/> 上的区间都是连通集。

Thought for a couple of seconds


下面继续按相同格式，为 **第3章–第8章** 编写核心内容（所有行内公式均用 `<img>` 引入 Codecogs SVG，加粗用 `**`）：

---

## 第3章 数值序列与级数

### 数列的极限与收敛

**收敛定义：** 数列 <img src="https://latex.codecogs.com/svg.latex?\{a_n\}"/> 若存在 <img src="https://latex.codecogs.com/svg.latex?L"/>，使得 <img src="https://latex.codecogs.com/svg.latex?\forall\varepsilon>0,\exists N,\forall n>N,\;|a_n-L|<\varepsilon"/>，
则称 <img src="https://latex.codecogs.com/svg.latex?\lim_{n\to\infty}a_n=L"/>。

**柯西序列：** 若 <img src="https://latex.codecogs.com/svg.latex?\forall\varepsilon>0,\exists N,\forall m,n>N,\;|a_n-a_m|<\varepsilon"/>，
则 <img src="https://latex.codecogs.com/svg.latex?\{a_n\}"/> 是柯西序列；在完备实数域中，**柯西⇔收敛**。

### 上极限与下极限

定义 <img src="https://latex.codecogs.com/svg.latex?\limsup_{n\to\infty}a_n=\lim_{n\to\infty}\big(\sup_{k\ge n}a_k\big)"/>, <img src="https://latex.codecogs.com/svg.latex?\liminf_{n\to\infty}a_n=\lim_{n\to\infty}\big(\inf_{k\ge n}a_k\big)"/>。
若 <img src="https://latex.codecogs.com/svg.latex?\limsup=\liminf=L"/>，则数列收敛于 <img src="https://latex.codecogs.com/svg.latex?L"/>。

### 数项级数

对数列 <img src="https://latex.codecogs.com/svg.latex?\{a_n\}"/> 考虑级数 <img src="https://latex.codecogs.com/svg.latex?\sum_{n=1}^\infty a_n"/>，定义部分和 <img src="https://latex.codecogs.com/svg.latex?S_N=\sum_{n=1}^N a_n"/>。若 <img src="https://latex.codecogs.com/svg.latex?\lim_{N\to\infty}S_N=S"/> 存在，则称级数收敛于 <img src="https://latex.codecogs.com/svg.latex?S"/>。

**正项级数判别：** 单调增且有界 ⇔ 收敛；常用 **比较判别法**、**比值判别法**、**根值判别法**。

**交错级数（Leibniz 判别）：** 若 <img src="https://latex.codecogs.com/svg.latex?a_n\ge0"/> 单调趋 0，则 <img src="https://latex.codecogs.com/svg.latex?\sum(-1)^n a_n"/> 收敛。

### 幂级数

形式 <img src="https://latex.codecogs.com/svg.latex?\sum_{n=0}^\infty c_n(x-a)^n"/>。其收敛半径 <img src="https://latex.codecogs.com/svg.latex?R=1/\limsup\sqrt[n]{|c_n|}}"/>。当 <img src="https://latex.codecogs.com/svg.latex?|x-a|<R"/> 绝对收敛。

---

## 第4章 连续性

### 连续函数

**ε–δ 定义：** 函数 <img src="https://latex.codecogs.com/svg.latex?f"/> 在 <img src="https://latex.codecogs.com/svg.latex?x_0"/> 连续，当且仅当 <img src="https://latex.codecogs.com/svg.latex?\forall\varepsilon>0,\exists\delta>0,\forall x,|x-x_0|<\delta\implies|f(x)-f(x_0)|<\varepsilon"/>。

**等价特征：** 保持极限（极限与函数值可交换）、开集的逆像为开集。

### 一致连续

**定义：** <img src="https://latex.codecogs.com/svg.latex?f"/> 在域 <img src="https://latex.codecogs.com/svg.latex?D"/> 上**一致连续**，若 <img src="https://latex.codecogs.com/svg.latex?\forall\varepsilon>0,\exists\delta>0,\forall x,y\in D,|x-y|<\delta\implies|f(x)-f(y)|<\varepsilon"/>。

**性质：** 紧集上连续 ⇒ 一致连续（Heine–Cantor 定理）。

### 极值与介值定理

* **极值定理：** 若 <img src="https://latex.codecogs.com/svg.latex?D"/> 紧，且 <img src="https://latex.codecogs.com/svg.latex?f: D\to\mathbb{R}"/> 连续，则 <img src="https://latex.codecogs.com/svg.latex?f"/> 在 <img src="https://latex.codecogs.com/svg.latex?D"/> 上达到最大值和最小值。
* **介值定理：** 若 <img src="https://latex.codecogs.com/svg.latex?f"/> 在区间连续，取值 <img src="https://latex.codecogs.com/svg.latex?f(a),f(b)"/> 之间的任意值，必有一点得此值。

---

## 第5章 导数

### 导数定义与几何意义

**定义：** <img src="https://latex.codecogs.com/svg.latex?f'(x_0)=\lim_{h\to0}\frac{f(x_0+h)-f(x_0)}{h}"/>（若极限存在）。

**几何意义：** 切线斜率。

### 常用可微性结论

* 可微 ⇒ 连续；但连续不一定可微。
* **四则运算可导法则**、**链式法则**。
* **高阶导数**：<img src="https://latex.codecogs.com/svg.latex?f^{(n)}"/>。

### 中值定理

* **Rolle 定理：** 若 <img src="https://latex.codecogs.com/svg.latex?f(a)=f(b)"/> 且连续可导，则 ∃ <img src="https://latex.codecogs.com/svg.latex?c\in(a,b)"/> 使 <img src="https://latex.codecogs.com/svg.latex?f'(c)=0"/>。
* **Lagrange 中值定理：** <img src="https://latex.codecogs.com/svg.latex?\exists c:f'(c)=\frac{f(b)-f(a)}{b-a}"/>。
* **Cauchy 中值定理** 的推广。

### 泰勒公式

若 <img src="https://latex.codecogs.com/svg.latex?f"/> 在 <img src="https://latex.codecogs.com/svg.latex?[a,b]"/> 上具有 <img src="https://latex.codecogs.com/svg.latex?n+1"/> 阶连续导数，则 <img src="https://latex.codecogs.com/svg.latex?f(x)=\sum_{k=0}^n\frac{f^{(k)}(a)}{k!}(x-a)^k+R_n(x)}"/>，
余项可用 Lagrange 形式或 Peano 形式表示。

---

## 第6章 定积分

### 不定积分与原函数

**原函数定义：** 若 <img src="https://latex.codecogs.com/svg.latex?F' = f"/>，则称 <img src="https://latex.codecogs.com/svg.latex?F"/> 为 <img src="https://latex.codecogs.com/svg.latex?f"/> 的原函数。所有原函数相差常数。

### Riemann 定积分

**上下和定义：** 对划分 <img src="https://latex.codecogs.com/svg.latex?P"/>，定义下和 <img src="https://latex.codecogs.com/svg.latex?L(f,P)"/>、上和 <img src="https://latex.codecogs.com/svg.latex?U(f,P)"/>；若上下和极限相等，则称可积，值记 <img src="https://latex.codecogs.com/svg.latex?\int_a^b f(x)\,dx"/>。

**可积性条件：** 有界函数在紧区间上若间断点集测度 0 ⇒ 可积。

### 基本定理

* **第一基本定理：** \<img src="[https://latex.codecogs.com/svg.latex?F(x)=\int\_a^x](https://latex.codecogs.com/svg.latex?F%28x%29=\int_a^x) f(t),dt}/> 连续，若 <img src="https://latex.codecogs.com/svg.latex?f"/> 连续则可导且 <img src="https://latex.codecogs.com/svg.latex?F'(x)=f(x)"/>。
* **第二基本定理（Newton–Leibniz）：** 若 <img src="https://latex.codecogs.com/svg.latex?F"/> 是 <img src="https://latex.codecogs.com/svg.latex?f"/> 的任一原函数，则 <img src="https://latex.codecogs.com/svg.latex?\int_a^b f(x)\,dx=F(b)-F(a)"/>。

### 积分技巧

**置换积分**、**分部积分**；常见被积函数表格法；**广义积分**（无穷区间或被积函数非有界）。

---

## 第7章 函数列与函数项级数

### 逐点收敛与一致收敛

* **逐点收敛：** 对每个 <img src="https://latex.codecogs.com/svg.latex?x"/>，<img src="https://latex.codecogs.com/svg.latex?\lim_{n\to\infty}f_n(x)=f(x)"/>。
* **一致收敛：** <img src="https://latex.codecogs.com/svg.latex?\sup_{x\in D}|f_n(x)-f(x)|\to0"/>。

一致收敛可交换极限与连续、可积、可导等运算。

### Weierstrass 判别法

若存在 <img src="https://latex.codecogs.com/svg.latex?M_n"/> 使 <img src="https://latex.codecogs.com/svg.latex?|f_n(x)|\le M_n"/> 且 <img src="https://latex.codecogs.com/svg.latex?\sum M_n"/> 收敛，则 <img src="https://latex.codecogs.com/svg.latex?\sum f_n"/> 一致绝对收敛。

### 幂级数一致收敛

幂级数在 <img src="https://latex.codecogs.com/svg.latex?|x-a|<R"/> 任意紧子区间上一致收敛，可做逐项微分和积分。

---

## 第8章 拓扑进阶与度量空间

### 度量空间基本概念

* **开放球**、**闭包**、**边界**、**极限点**。
* **完备度量空间**：所有柯西列收敛。
* **全有界** 与 **紧性**：在一般度量空间中，完备+全有界 ⇔ 紧。

### 紧性判别

* **Bolzano–Weierstrass 定理**：有界序列必有收敛子序列。
* **Heine–Borel 定理**（Rⁿ）：闭有界 ⇔ 紧。

### 可分性与可数基

* **可分空间**：含有稠密可数子集。
* **可数拓扑基**：若度量空间有可数基，则为**二可数**。



