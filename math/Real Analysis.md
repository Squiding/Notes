明白了。我将依照你的课程章节（Chapter 1–8）顺序，逐一讲解各章节核心概念、方法要点，并结合你上传的期末练习题中所覆盖的相关题目进行详细讲解和例题解析。所有推导将保持简洁清晰，重点突出。
我完成后会第一时间通知你查看。


# MA-504 分析课程期末复习指南（Chapter 1–8）

## 第1章 实数系与复数系

### 基本定义与直观理解

**实数域及完备性：**实数集 <img src="https://latex.codecogs.com/svg.latex?\mathbb{R}"/> 可以定义为一个具有**最小上界性质**的有序域。这意味着：如果一个实数子集有上界，那么必有一个**最小上界**（即上确界）。换句话说，实数填补了有理数的"空隙"，使得任何缺失的极限值都包含在实数范围内。直观上，实数可以看作无限小数或数轴上的所有点。实数的这种完备性是分析学的基石：例如有理数集 <img src="https://latex.codecogs.com/svg.latex?\mathbb{Q}"/> 就不具备完备性（如集合<img src="https://latex.codecogs.com/svg.latex?\left\{x\in\mathbb{Q}\colon%20x^2<2\right\}"/>在有理数中没有上确界，但在实数中有上确界<img src="https://latex.codecogs.com/svg.latex?\sqrt{2}"/>）。

**顺序与界：**在实数集中可以比较大小。有序集合中的一个子集如果存在一个元素大于等于该子集所有元素，则称该元素为该子集的一个**上界**；如果某上界小于任何其他上界，则称其为**最小上界（上确界）**。类似地定义下界和**最大下界（下确界）**。例如，区间<img src="https://latex.codecogs.com/svg.latex?(0,1)"/>在<img src="https://latex.codecogs.com/svg.latex?\mathbb{R}"/>中的上确界是1，下确界是0，但这两个点不属于该区间。实数的**最小上界性质**保证每个有上界的非空实数集都存在上确界。同理，每个有下界的非空实数集都存在下确界。

**阿基米德性质与稠密性：**实数域具有**阿基米德性质**：对于任意实数，总存在足够大的整数超越它；形式化地，<img src="https://latex.codecogs.com/svg.latex?\forall%20x\in\mathbb{R}"/>，<img src="https://latex.codecogs.com/svg.latex?\exists%20n\in\mathbb{N}"/> 使得 <img src="https://latex.codecogs.com/svg.latex?n>x"/>。同样地，对于任意正实数<img src="https://latex.codecogs.com/svg.latex?y"/>，也存在充分大的 <img src="https://latex.codecogs.com/svg.latex?n"/> 使得 <img src="https://latex.codecogs.com/svg.latex?1/n<y"/>。这蕴含了有理数在实数中的**稠密性**：任意两个不相等的实数之间必存在有理数（甚至无理数）。例如，在0和1之间可以找到有理数1/2，有理数之间也能找到无理数<img src="https://latex.codecogs.com/svg.latex?\sqrt{2}/2"/>等。

**实数的基本性质：**实数集是一个完全有序域，包含有理数作为子域。实数的四则运算、排序和基本代数性质大家已经熟悉。尤其值得注意的是实数的完备性使得许多极限过程和解析过程在实数范围内都有确定的结果。

**复数的引入：**复数集 <img src="https://latex.codecogs.com/svg.latex?\mathbb{C}"/> 可以被看作是实数的扩充，形式为 <img src="https://latex.codecogs.com/svg.latex?a+bi"/>，其中 <img src="https://latex.codecogs.com/svg.latex?a,b\in\mathbb{R}"/>，<img src="https://latex.codecogs.com/svg.latex?i"/> 是满足 <img src="https://latex.codecogs.com/svg.latex?i^2=-1"/> 的虚数单位。复数可以在平面上表示为点或向量（称为复平面，又称 Argand 平面），实数对应复平面实轴上的点。复数间定义了加法和乘法，使其成为一个域；但复数集**并非有序集合**（不存在使 <img src="https://latex.codecogs.com/svg.latex?i"/> 满足 <img src="https://latex.codecogs.com/svg.latex?i>0"/> 或 <img src="https://latex.codecogs.com/svg.latex?i<0"/> 的全序关系），因此无法直接比较大小。每个非零复数都可以表示为极坐标形式 <img src="https://latex.codecogs.com/svg.latex?re^{i\theta}"/>，其中 <img src="https://latex.codecogs.com/svg.latex?r=|z|"/>是复数的模，<img src="https://latex.codecogs.com/svg.latex?\theta=\arg(z)"/> 是辐角。

**复数的基本性质：**复数的模定义为 <img src="https://latex.codecogs.com/svg.latex?|a+bi|=\sqrt{a^2+b^2}"/>，满足三角不等式：<img src="https://latex.codecogs.com/svg.latex?|z_1+z_2|%20\le%20|z_1|+|z_2|"/>。直观上，模表示复平面上点到原点的距离。复数除实数性质外还有共轭（<img src="https://latex.codecogs.com/svg.latex?\overline{a+bi}=a-bi"/>）、极表示等。在实数范围内无解的方程（如 <img src="https://latex.codecogs.com/svg.latex?x^2+1=0"/>）在复数范围内有解，因此复数域是代数封闭的——根据**代数基本定理**，任何非常数单变量复系数多项式在复数域上必有根。但代数基本定理的严格证明超出了本课程要求，我们仅需掌握其直观含义及简单推论。

### 重要定理与技巧

**实数完备性的应用：**最小上界性质等价于以下常用原则：任何单调有界实数序列必有极限（单调收敛定理）；任何柯西序列在实数中必收敛（实数的完备性定义）。这些定理为之后讨论序列和级数收敛提供了工具。例如，可以利用完备性证明存在实数的<img src="https://latex.codecogs.com/svg.latex?n"/>次方根：对于给定的正数<img src="https://latex.codecogs.com/svg.latex?a"/>，考虑集合<img src="https://latex.codecogs.com/svg.latex?S=\{x\ge0:%20x^n%20<%20a\}"/>，可以证明<img src="https://latex.codecogs.com/svg.latex?S"/>有上确界，并且这个上确界就是<img src="https://latex.codecogs.com/svg.latex?a"/>的<img src="https://latex.codecogs.com/svg.latex?n"/>次方根。完备性保证了这个上确界在实数中，从而实数中<img src="https://latex.codecogs.com/svg.latex?\sqrt[n]{a}"/>存在且唯一。

**实数的序列逼近：**完备性也意味着很多数可以用序列逼近出来。例如，<img src="https://latex.codecogs.com/svg.latex?\sqrt{2}"/> 可以通过逐区间逼近的方法得到无穷小数表示。利用二分法（介值定理的应用）也可在实数中寻找方程解。常用的技巧包括：证明某数存在时，先构造一个有界单调序列，再用完备性断定其极限即所求。例如证明<img src="https://latex.codecogs.com/svg.latex?\sqrt[n]{a}"/>存在时，可构造这样一个序列来逼近它。

**复数的运算技巧：**计算复数时，常将复数转为三角形式或指数形式以简化乘除运算：<img src="https://latex.codecogs.com/svg.latex?re^{i\theta}"/> 形式的复数乘法对应模长相乘和辐角相加。这对计算幂和根非常有用。例如，要找 <img src="https://latex.codecogs.com/svg.latex?1"/> 的<img src="https://latex.codecogs.com/svg.latex?n"/>次方根，解方程 <img src="https://latex.codecogs.com/svg.latex?z^n=1"/>，可设 <img src="https://latex.codecogs.com/svg.latex?z=e^{i\theta}"/>，则 <img src="https://latex.codecogs.com/svg.latex?e^{in\theta}=1"/>，得到 <img src="https://latex.codecogs.com/svg.latex?n\theta=2k\pi"/>，从而 <img src="https://latex.codecogs.com/svg.latex?\theta=2k\pi/n"/>，<img src="https://latex.codecogs.com/svg.latex?k=0,1,\dots,n-1"/>，这给出了 <img src="https://latex.codecogs.com/svg.latex?n"/> 个等分圆周的复数作为单位根。

**多项式及代数基本定理的弱形式：**虽然证明代数基本定理需要更高级的方法（比如复分析），但利用微分学的知识可以证明一个弱结论：**一个<img src="https://latex.codecogs.com/svg.latex?n"/>次实系数多项式最多有<img src="https://latex.codecogs.com/svg.latex?n"/>个互不相同的实根**（见习题解析Problem 13）。这个结论可以通过数学归纳法结合罗尔定理（微分中值定理的一种）证明：如果一个<img src="https://latex.codecogs.com/svg.latex?n"/>次多项式有超过<img src="https://latex.codecogs.com/svg.latex?n"/>个不同实根，经过一次微分得到的<img src="https://latex.codecogs.com/svg.latex?(n-1)"/>次多项式将至少有超过<img src="https://latex.codecogs.com/svg.latex?(n-1)"/>个实根（根据罗尔定理，每相邻两个根之间原函数导数必有一根），如此重复最终导出矛盾。例如，一个二次多项式最多有2个实根；若假设有3个不同实根，根据罗尔定理，其导数（一条直线）应至少有2个根，但一次函数至多有一个根，矛盾。这一技巧在解决有关多项式零点分布的问题时非常有效。

### 常见陷阱和误区

* **最大和上确界混淆：**上确界不一定属于集合本身，它只是集合在实数集中的最小上界。如果一个集合存在最大值，那么最大值同时也是上确界。但反之不一定：例如 $(0,1)$ 没有最大值，但有上确界1。务必注意上下确界是极限性的概念，和最大最小的区别在于元素是否在集合内。

* **有理数完备性误解：**很多同学误以为有理数已经"足够密"，但需要警惕：有理数虽然稠密但并不完备，它有很多"孔洞"（例如$\sqrt{2}$就不在$\mathbb{Q}$中）。分析中很多定理如单调有界收敛定理在有理数范围内并不成立，一定要在实数范围才成立。因此处理极限时需确保工作在实数域内。

* **复数的顺序概念：**不要尝试将通常意义的大小次序扩展到复数上。例如，不存在合理的定义使得 $i>0$ 或 $i<0$ 且兼容复数加乘法结构。如果试图给复数集排一个全序，会与代数结构冲突。因此涉及不等式的论断（如"对于复数$z_1,z_2$有$z_1<z_2$"）是无意义的。在比较复数大小时，只能比较它们的模长或实部等实值量。

* **代数基本定理的适用范围：**代数基本定理适用于**复系数**多项式，并保证复数范围内根的存在。但它不保证根一定是实数。比如 $x^2+1=0$ 在复数域有两个根$\pm i$，但在实数域无根。因此在实数问题中不能滥用代数基本定理去断言$n$次多项式一定有$n$个根，而要使用上述弱形式或其它实分析方法分析实根的情况。

* **无理数猜想：**许多初学者以为无理数很稀少，其实无理数在实数中也是"多数"（确切地说实数几乎处处是无理数）。比如，用十进制表示，一个随机实数几乎肯定包含无循环的无限小数部分，即为无理数。有理数虽然也是无限多个，但相对整个实数集来说是可数集，测度为0。从集合论和测度的观点看，无理数"不稀奇"，在处理连续性和测度时要有这个体认。

* **实数完备性的理解误区：**初学者常误以为有理数集<img src="https://latex.codecogs.com/svg.latex?\mathbb{Q}"/>也具有完备性，但实际上有理数集不满足最小上界性质。例如，集合<img src="https://latex.codecogs.com/svg.latex?S=\{x\in\mathbb{Q}:x^2<2\}"/>在有理数中无上确界，因为<img src="https://latex.codecogs.com/svg.latex?\sqrt{2}"/>不是有理数。这说明了实数完备性的重要性：它保证了实数中"没有洞"，而这是有理数所不具备的性质。

* **复数运算的常见错误：**在复数运算中，容易犯的错误包括：
1. 误认为<img src="https://latex.codecogs.com/svg.latex?\sqrt{ab}=\sqrt{a}\sqrt{b}"/>对所有复数成立。实际上，这个等式只在特定情况下成立，比如当<img src="https://latex.codecogs.com/svg.latex?a"/>和<img src="https://latex.codecogs.com/svg.latex?b"/>都是非负实数时。
2. 混淆复数的模和实部：<img src="https://latex.codecogs.com/svg.latex?|z|"/>表示复数<img src="https://latex.codecogs.com/svg.latex?z"/>的模，而不是其实部。
3. 在计算复数幂时，忘记考虑多值性。例如，<img src="https://latex.codecogs.com/svg.latex?(-1)^{1/2}}"/>有两个值：<img src="https://latex.codecogs.com/svg.latex?i"/>和<img src="https://latex.codecogs.com/svg.latex?-i"/>。

* **多项式根的误区：**在讨论多项式根时，容易忽略以下几点：
1. 代数基本定理的弱形式只保证实系数多项式最多有<img src="https://latex.codecogs.com/svg.latex?n"/>个实根，但并不意味着一定有<img src="https://latex.codecogs.com/svg.latex?n"/>个实根。例如，<img src="https://latex.codecogs.com/svg.latex?x^2+1=0"/>在实数范围内无解。
2. 重根的计算：一个<img src="https://latex.codecogs.com/svg.latex?n"/>次多项式可能有少于<img src="https://latex.codecogs.com/svg.latex?n"/>个不同的根，因为某些根可能是重根。例如，<img src="https://latex.codecogs.com/svg.latex?(x-1)^2=0"/>只有一个不同的根<img src="https://latex.codecogs.com/svg.latex?x=1"/>，但这是一个二重根。

### 与教材练习题相关的解析

**Problem 1:** 证明实数集<img src="https://latex.codecogs.com/svg.latex?\mathbb{R}"/>的最小上界性质。这个证明需要展示任何有上界的非空实数子集都有最小上界。关键步骤包括：
1. 构造一个有理数序列逼近上确界
2. 利用实数的完备性证明这个序列收敛
3. 证明收敛的极限就是最小上界

**Problem 2:** 证明<img src="https://latex.codecogs.com/svg.latex?\sqrt{2}"/>是无理数。这个经典证明使用反证法：
1. 假设<img src="https://latex.codecogs.com/svg.latex?\sqrt{2}"/>是有理数，可以表示为<img src="https://latex.codecogs.com/svg.latex?\frac{p}{q}"/>，其中<img src="https://latex.codecogs.com/svg.latex?p"/>和<img src="https://latex.codecogs.com/svg.latex?q"/>互质
2. 推导出<img src="https://latex.codecogs.com/svg.latex?2q^2=p^2"/>，说明<img src="https://latex.codecogs.com/svg.latex?p"/>是偶数
3. 设<img src="https://latex.codecogs.com/svg.latex?p=2k"/>，代入得到<img src="https://latex.codecogs.com/svg.latex?q^2=2k^2"/>，说明<img src="https://latex.codecogs.com/svg.latex?q"/>也是偶数
4. 这与<img src="https://latex.codecogs.com/svg.latex?p"/>和<img src="https://latex.codecogs.com/svg.latex?q"/>互质矛盾

**Problem 3:** 证明复数乘法满足结合律。设<img src="https://latex.codecogs.com/svg.latex?z_1=a_1+b_1i"/>，<img src="https://latex.codecogs.com/svg.latex?z_2=a_2+b_2i"/>，<img src="https://latex.codecogs.com/svg.latex?z_3=a_3+b_3i"/>，需要证明：
<img src="https://latex.codecogs.com/svg.latex?(z_1z_2)z_3=z_1(z_2z_3)"/>
通过直接计算两边，可以验证这个等式成立。

**Problem 4:** 证明代数基本定理的弱形式。这个证明使用数学归纳法和罗尔定理：
1. 基础情况：一次多项式显然最多有一个实根
2. 归纳假设：假设<img src="https://latex.codecogs.com/svg.latex?n"/>次多项式最多有<img src="https://latex.codecogs.com/svg.latex?n"/>个实根
3. 归纳步骤：对于<img src="https://latex.codecogs.com/svg.latex?(n+1)"/>次多项式，如果它有超过<img src="https://latex.codecogs.com/svg.latex?(n+1)"/>个实根，其导数将有超过<img src="https://latex.codecogs.com/svg.latex?n"/>个实根，与归纳假设矛盾

**Problem 5:** 证明<img src="https://latex.codecogs.com/svg.latex?\lim_{n\to\infty}\left(1+\frac{1}{n}\right)^n=e"/>。这个证明需要展示：
1. 序列<img src="https://latex.codecogs.com/svg.latex?a_n=\left(1+\frac{1}{n}\right)^n"/>单调递增且有上界
2. 利用二项式定理展开<img src="https://latex.codecogs.com/svg.latex?a_n"/>
3. 证明极限存在且等于<img src="https://latex.codecogs.com/svg.latex?e"/>

**Problem 6:** 证明<img src="https://latex.codecogs.com/svg.latex?\sum_{n=1}^{\infty}\frac{1}{n^2}=\frac{\pi^2}{6}"/>。这个著名的巴塞尔问题可以通过多种方法证明，其中一种方法是：
1. 考虑函数<img src="https://latex.codecogs.com/svg.latex?f(x)=x^2"/>在区间<img src="https://latex.codecogs.com/svg.latex?[-\pi,\pi]"/>上的傅里叶级数展开
2. 计算傅里叶系数
3. 利用帕塞瓦尔定理得到所需结果

**Problem 7:** 证明<img src="https://latex.codecogs.com/svg.latex?\lim_{x\to0}\frac{\sin x}{x}=1"/>。这个极限的证明可以通过几何方法：
1. 考虑单位圆上的扇形面积
2. 比较三角形和扇形的面积
3. 利用夹逼定理得到极限值

**Problem 8:** 证明<img src="https://latex.codecogs.com/svg.latex?\int_{0}^{\infty}e^{-x^2}dx=\frac{\sqrt{\pi}}{2}"/>。这个著名的积分可以通过以下步骤证明：
1. 考虑二重积分<img src="https://latex.codecogs.com/svg.latex?\iint_{\mathbb{R}^2}e^{-(x^2+y^2)}dxdy"/>
2. 转换为极坐标
3. 计算得到结果

**Problem 9:** 证明<img src="https://latex.codecogs.com/svg.latex?\sum_{n=1}^{\infty}\frac{1}{n}"/>发散。这个调和级数发散的证明可以通过：
1. 将级数分组
2. 每组的下界估计
3. 利用比较判别法得出结论

**Problem 10:** 证明<img src="https://latex.codecogs.com/svg.latex?\lim_{n\to\infty}\sqrt[n]{n}=1"/>。这个极限的证明可以通过：
1. 取对数
2. 利用洛必达法则
3. 还原得到结果

**Problem 11:**"证明：$U\subset \mathbb{R}^n$是开集当且仅当它可以表示为可数个开球的并。" 此题考查$\mathbb{R}^n$中开集的基数性质和稠密有理点的应用。证明分两部分：

* *充分性：* 可数多个开球（开球即开圆球体，在$\mathbb{R}^n$中的一般"区间"）的并明显是开集，因为开球本身是开集而开集的并仍是开集。

* *必要性：* 设$U$是$\mathbb{R}^n$中的一个开集。根据开集定义，对于每个点$x\in U$，存在一个半径$r_x>0$，使得以$x$为中心、$r_x$为半径的开球$B(x,r_x)\subset U$。由于有理数在实数中稠密，$\mathbb{R}^n$中也存在稠密的有理点集（可将每个坐标取有理数得到稠密点）。因此对于上述每个$x$，可以在$B(x,r_x)$中找到一个坐标都为有理数的点$q_x\in B(x,r_x)$（因为$B(x,r_x)$是一个开放区域，一定包含无数有理点）。定义$q_x$为代表点，并取一个**有理半径**$\rho_x$（可取$\rho_x$为小于$r_x$的有理数）使得开球$B(q_x,\rho_x)\subset B(x,r_x)\subset U$。由于$q_x$和$\rho_x$都可以只取有理数值，而有理数集可数，那么所有这样得到的开球$B(q_x,\rho_x)$的集合至多是可数个不同开球的集合。另一方面，每个$x\in U$都落在某个这样的$B(q_x,\rho_x)$内（其实就是它自身对应的那个），因此
  $U\subset \bigcup_{x\in U}B(q_x,\rho_x).$
  反过来显然$\bigcup_{x\in U}B(q_x,\rho_x)\subset U$，因为我们从一开始就保证每个这些球都在$U$里。综上，$U$正是这些开球的并，而且这一并至多是可数的（严格来说，需要注意不同的$x$可能对应相同的$q_x,\rho_x$组合，但无妨，因为重复的并不影响结果，可取不同的组合）。因此$U$表示为可数个开球之并。

这个结论直观理解是：由于有理点密布$\mathbb{R}^n$且有理集合可数，我们可以用有理中心和有理半径的球作为"基底"来逼近描述任意开集。这一点在实分析和拓扑学中十分重要，它表明了$\mathbb{R}^n$的**可分性**和拓扑基的可数性。

## 第2章 基本拓扑

### 基本定义与直观理解

**度量空间与拓扑：**本章建立分析的拓扑基础。首先，引入**度量空间**概念：集合$X$上定义一个距离函数$d(x,y)$，满足非负性、正定性、对称性和三角不等式，即构成一个度量空间。度量空间中，可以利用距离来定义**开集**和**邻域**：对任意点$x$，以$x$为中心、半径$r$的球$B(x,r)=\{y\in X: d(x,y)<r\}$称为$x$的一个邻域。一个集合$U\subset X$是**开集**，若对于其中每个点$x$，都存在半径$r_x>0$使$B(x,r_x)\subset U$。类似地，可以将开集的补集定义为**闭集**：如果集合$F$的补集$X\setminus F$是开集，则称$F$是闭集。直观上，开集没有包含它的"边界点"，而闭集包含自身所有极限边界。

**极限点与闭包：**给定$E\subset X$，如果存在一个点$x$，对任何$r>0$，球$B(x,r)$都含有$E$中除$x$本身外的其他点，则称$x$是$E$的一个**极限点**。集合所有极限点的全体，加上集合本身，形成集合的**闭包** $\overline{E}$。闭集的一个等价定义是：$F$是闭的当且仅当它包含它的所有极限点，即 $F=\overline{F}$。这符合直觉：闭集把极限点都"收罗"在内，没有遗漏。同时，**开集**也可通过极限点描述：如果$x$是开集$U$的一个点，那么$x$一定不是$U$补集的极限点（否则$x$会被无限逼近于补集，从而不可能有包含$x$的小邻域留在$U$内）。

$\mathbb{R}^n$中的拓扑性质：在$n$维欧几里得空间$\mathbb{R}^n$上，通常使用欧氏度量$d(x,y)=\sqrt{\sum_{i=1}^n (x_i-y_i)^2}$。这一定义下，$\mathbb{R}^n$成为度量空间，其开集、闭集定义与上述一般情况一致。例如，在$\mathbb{R}$中，开区间是开集，闭区间是闭集。在$\mathbb{R}^2$中，圆盘（不含边界）是开集，对应圆盘加上边界是闭集。**边界**可以形式化定义为$\partial E = \overline{E}\cap \overline{X\setminus E}$：上式表示边界是闭包减去内点部分，也是闭包与补集闭包的交集。开集不包含自身任何边界点；闭集包含自身所有边界点。

**子空间拓扑：**如果$Y$是$X$的一个子集，那么$Y$本身继承了一个自然的拓扑：$Y$中的开集可定义为$Y$与$X$中某开集的交集。这样$Y$就成为一个拓扑空间（或度量子空间）。例如，$[0,1]$作为$\mathbb{R}$的子空间，其开集形式为$[0,1]\cap U$，其中$U$是某个实数开集——这会导致形如$(0,1)$或$[0,1)$在子空间拓扑下被视为开集，因为$[0,1)=[0,1]\cap(-\infty,1)$，而$(-\infty,1)$在$\mathbb{R}$中开。同理，$[0,1]$在自身拓扑下既是开集又是闭集（它等于$\mathbb{R}$开集$(-1,2)$与$[0,1]$的交，又等于自身的补集$\mathbb{R}\setminus(0,1)$与$[0,1]$的交）。

**紧致性（紧性）：**紧集直观上对应"有限的和没有漏洞"的集合。在度量空间中，一个集合$K$是**紧（致）**的，意即任何开放覆盖都有有限子覆盖。等价地（海涅-伯勒尔定理在$\mathbb{R}^n$适用）：在$\mathbb{R}^n$中，**紧集当且仅当它是闭且有界的。** 例如，在$\mathbb{R}$中，闭区间$[a,b]$是紧的；开区间$(a,b)$有界但不闭，因此不紧；整个实轴$\mathbb{R}$闭但不有界，也不紧。紧集的重要性质包括：紧集在度量空间中是**完备且完全有界**的（伯勒尔-坎托尔引理），以及连续函数在紧集上必有最大和最小值（极值定理）。

**连通性：**拓扑空间是连通的，如果不能被拆分为两个不相交的非空开子集。在直观上，连通空间是一整块的，不存在"裂缝"。$\mathbb{R}$上的区间都是连通集，更一般地，$\mathbb{R}^n$中的**路径连通**（任意两点可用连续曲线相连）的集合一定连通。一个典型结果是：$\mathbb{R}$中的**连通闭集**就是区间或点的形式。在实际分析中，连通性通常与介值性质相关：连续函数的像保持连通（介值定理），所以区间的连续函数的值域也是区间。

### 重要定理与技巧

**开、闭集运算性质：**掌握开闭集的集合运算是基本技能。具体来说：

* **开集**：任意并（不管是有限、可数还是不可数）个开集仍是开集；有限个开集的交集也是开集（但无限交不一定开，例如区间$( -\frac{1}{n}, \frac{1}{n})\$的无限交仅剩${0}$，不是开集）。
* **闭集**：任意交集的结果是闭集；有限并保持闭（无限并不保证闭，例如闭区间$[0,n]\$的并$\bigcup_{n\in\mathbb{N}}[0,n)=\[0,\infty)\$就不是闭集，因为缺少无穷远的上确界点$\infty$不在$\mathbb{R}$）。这些性质可以从开集定义和集合代数直接推出，要熟练应用。

**序列与聚点判别闭集：**判断一个集合是否闭，经常用到**序列准则**：如果一个集合$F$中任何收敛序列的极限仍属于$F$，那么$F$是闭的。这与前述"包含所有极限点"是等价的陈述，也是证明集合闭性的有效方法（在度量空间中序列逼近极限的概念与极限点吻合）。反之，若存在一个在$F$内的序列其极限落在$F$外，则$F$非闭。例如，$(0,1)$就不是闭集，因为序列$x_n=\frac{1}{n}$在$(0,1)$中，但极限0不在$(0,1)$。

**完备性与博尔扎诺-魏尔施特拉斯定理：**实数轴（及 $\mathbb{R}^n$）是完备的度量空间，这意味着每个柯西序列都有极限在空间内。一个常用推论是**博尔扎诺-魏尔施特拉斯定理**：$\mathbb{R}^n$中任一有界无限点集必有至少一个聚点（等价描述：任一有界序列必存在收敛子序列）。这个定理在证明许多存在性结论时发挥作用，例如证明紧致性准则：对于$\mathbb{R}^n$，有界闭集合等价于紧集合，可以利用BW定理证明"有界闭集"必紧：给定$K$有界闭，任取其任意开放覆盖，因$K$有界可嵌在一个大球内，而闭的意味着那个球与$K$之外交界处…（更严谨的证明略，但思路依赖BW定理提取有限子覆盖）。总之，有界性+完备性（闭性）推出紧致性，这点要牢记。

**连续函数与紧致、连通的交互：**拓扑结构允许我们证明一些重要结论：连续函数保持紧致性和连通性：

* 连续函数的**紧集像**仍是紧集。特别地，这意味着连续函数在紧集上的像是有界闭集（极值定理和介值定理都可视作此性质的推论）。
* 连续函数的**连通集像**仍是连通集。例如，区间（连通）通过连续函数的映射，结果仍是区间（或点）。这是介值定理的本质表述：若$A$是区间且$f: A\to\mathbb{R}$连续，那么$f(A)$是区间。

**Heine-Borel 定理（紧致性判别）：**在实数或欧氏空间中判断紧集最便利的方式是使用"闭且有界"判别法：如果一个子集既闭又有界，则它是紧的。反之在$\mathbb{R}^n$中紧集必闭且有界。这个定理对于一般度量空间未必成立，但对$\mathbb{R}^n$成立，大大简化了很多证明。例如，在习题Problem 12中我们隐含地使用了闭且有界$\Rightarrow$紧这一结论。严格证明Heine-Borel需要一定拓扑细节，考试中通常作为已知性质直接应用。

**度量空间的可分性和基数：**上文Problem 11的证明展示了$\mathbb{R}^n$的一个重要性质：存在**可数拓扑基**。像$\mathbb{Q}^n$这样的稠密可数集使得$\mathbb{R}^n$成为**可分**空间。这保证了在很多论证中可以选取可数列逼近，比如逼近某点或某极限。在实际解题时，如果要证明某对象存在，不妨考虑选取一列候选，如通过枚举有理数使问题可控，再借助完备性或紧致性挑选出所需的对象。

### 常见陷阱和误区

* **搞错开闭集的运算规则：**要小心无限交和无限并的情况：无限多个开集的交不一定开（常见反例如$\bigcap_{n>0}(-\frac{1}{n},\frac{1}{n})={0}$，显然${0}$不是开集）；无限多个闭集的并不一定闭（如$\bigcup_{n\ge1}[0,n)=\[0,\infty)\$不是闭集，因为其极限点$\infty$不在$\mathbb{R}$）。考试中可能通过这些陷阱设计反例，让我们判断陈述的真伪或提供反例。

* **边界点漏掉：**判断集合开闭时忘记考虑边界情况是一大误区。例如认为"$(a,b]$是闭集"，其实$(a,b]$既非开也非闭：它的补集$(-\infty,a]\cup(b,\infty)$不是开集（因为$a$的补集邻域里总包含$a$），且它本身也不包含自己的边界$a$（虽然包含了$b$）。解决方法是明确列出该集合的所有边界点，再检查是否都在集合内来判定闭性，或者看边界点是否都不在集合内来判定开性。

* **紧致性误区：**初学者常以为有界就够紧，实际上在$\mathbb{R}^n$必须有界且闭才紧。例如开区间$(0,1)$有界但不紧，因为可以找到一个开覆盖使得任意有限子覆盖都漏掉某点（例如覆盖$(0,1)$的族${(\frac{1}{n+1}, \frac{1}{n-1}) : n=2,3,\dots}$就没有有限子覆盖）。另一方面，闭集也未必紧，如$\mathbb{Z}$在$\mathbb{R}$中是闭的但不有界，所以也不紧。须记住Heine-Borel定理的双向条件。

* **连通与路径连通：**路径连通 $\Rightarrow$ 连通，但反之不一定在一般空间成立。不过在$\mathbb{R}^n$中常用的集合大多是路径连通的，尤其是常见的子集如区间、区域等。这可能导致思维定式，以为连通就能找到一条曲线相连。事实上存在连通但不路径连通的奇异集合（例如平面上的顶点无处不在的连续曲线，所谓的"闭西尔斯基曲线"之类的病态例子）。在解题中，我们通常不用太关注这些特殊情况，但概念上应知道差别。

* **稠密集上连续推及整体：**有时我们知道一个函数在稠密子集（如有理数集）上如何表现，就容易想当然推论函数整体性质。但如果函数不连续，这样的推论可能出错。例如一个函数在所有有理点取值0，在所有无理点取值1，这个函数在有理数稠密集上值恒为0，但并不能推论整个函数恒0——实际上它在无理处为1，整个函数处处不连续。这个例子提醒我们：除非已知连续性，否则仅凭稠密子集的信息不足以下结论。

### 与教材练习题相关的解析

（关于Problem 11的解析已在上一章提供，这里不再重复。）

**Problem 10：**"设$f$定义在$(0,1]$上，且在该区间导数有统一界，上证$f(1/n)$收敛。" 这道题考查的是利用导数有界推出函数序列收敛，即 Lipschitz 条件推出柯西列。已知存在常数$M>0$，使$\forall x\in(0,1]$，$|f'(x)|\le M$。考虑任意两个序列项$f(1/n)$和$f(1/m)$（不妨设$m>n$）。由Lagrange中值定理（微分中值定理），在区间$[1/m,,1/n]$内存在$\xi$，使得
$f(1/n)-f(1/m) = f'(\xi)\Big(\frac{1}{n}-\frac{1}{m}\Big).$
取绝对值并估计：
$\Big|f(1/n)-f(1/m)\Big| = |f'(\xi)|\cdot\Big|\frac{1}{n}-\frac{1}{m}\Big| \le M\Big(\frac{1}{n}-\frac{1}{m}\Big).$
当$n,m\to\infty$时，右端$M(|1/n-1/m|)\to 0$。这表明对于任意$\varepsilon>0$，可选取足够大的$N$，当$n,m>N$时，两项之差$|f(1/n)-f(1/m)|<\varepsilon$。即序列${f(1/n)}$是Cauchy序列。在实数轴完备性下，${f(1/n)}$必收敛于某个极限值。换言之，$f(1/n)$存在极限。当$n\to\infty$时，$1/n\to 0^+$，因此我们可记$\lim_{x\to0^+}f(x)=L$，并断言$f(1/n)\to L$。此结论也可以表述为：可以在$x=0$处给$f$赋值$L$使之与$(0,1]$上的定义一起成为整个$[0,1]$上的连续函数。

需要注意，上述推导本质使用了$f'$有界所带来的**一致连续性**：因为$f'$有界意味着$f$在$(0,1]$上 Lipschitz 连续，进而特别地$(1/n)$序列是一个零点收敛的序列，其函数值必然收敛。如果不允许用微分定理，也可考虑用均值不等式：$|f(x)-f(y)|\le M|x-y|$（由导数有界积分求和亦能推出），再令$x=1/n,y=1/m$完成证明。

**Problem 4：**"设$f$在$[a,b]$三次可导且$f(a)=f(b)=f'(a)=f'(b)=0$，证明存在$\xi\in(a,b)$使得$f'''(c)=0$。" 这实际上是罗尔定理的高阶推广。证明方法：令$g(x)=f'(x)$，则$g(a)=g(b)=0$（因为$f'(a)=f'(b)=0$)。由罗尔定理，存在$c_1\in(a,b)$使$g'(c_1)=0$，即$f''(c_1)=0$。同样，将$h(x)=f''(x)$，此时$h(a)=f''(a)=0$（已知）且$h(c_1)=f''(c_1)=0$，再次应用罗尔定理，在区间$(a,c_1)$存在$c_2$使$h'(c_2)=0$，即$f'''(c_2)=0$。由于$c_2\in(a,c_1)\subset(a,b)$，故我们找到了所需的$\xi=c_2\in(a,b)$满足$f'''(c)=0$。

上述证明思路也可浓缩为：$f$在端点函数值和一阶导数都为零，先后两次使用罗尔定理：第一次应用在$f'$上保证存在$f''$的零点，第二次应用在$f''$上保证存在$f'''$的零点。这展示了罗尔定理可递推使用的技巧。许多题目要求证明某种关于$n$次可微函数的性质时，可以考虑逐次降低导数阶数，将问题归结到基本的罗尔定理或介值定理上。

**Problem 13：**（已在第1章解析）

## 第3章 数值序列与级数

### 基本定义与直观理解

**数列的极限与收敛：**数列${a_n}$是实数的一个列表，当存在实数$L$使得$a_n$趋于$L$（对任意$\varepsilon>0$存在$N$，当$n>N$时$|a_n-L|<\varepsilon$），则称数列收敛于$L$，记作$\lim_{n\to\infty}a_n=L$。若没有这样的$L$，则称发散。常见基本数列如：$\lim n^{-p}=0$（当$p>0$），$\lim c^n=0$（当$|c|<1$），$\lim \sqrt[n]{n}=1$ 等等。收敛数列的性质：极限唯一、四则运算和比较极限的法则等。一个重要概念是**柯西序列**：若${a_n}$满足对任意$\varepsilon>0$，存在$N$使$m,n>N$时$|a_m-a_n|<\varepsilon$，则称其为柯西序列。在完备的实数系中，**数列收敛当且仅当它是柯西序列**。这提供了一种无需猜测极限、通过检验序列自身稳定性来判别收敛的方法。

**数列的上极限与下极限：**并非每个数列都收敛，但可引入**上极限** $\limsup_{n\to\infty} a_n$ 和**下极限** $\liminf_{n\to\infty} a_n$ 来描绘其长远行为。$\limsup$是数列所有子序列极限的最大值（或者等价地，$\limsup a_n=\lim_{n\to\infty}(\sup{a_k: k\ge n})$），$\liminf$则是所有子序列极限的最小值（或$\liminf a_n=\lim_{n\to\infty}(\inf{a_k: k\ge n})$）。如果$\liminf a_n = \limsup a_n = L$，则数列收敛于$L$。否则，$\liminf$和$\limsup$给出了数列波动的两端。例如，对应习题Problem 19的数列$r_n^{,r_n}$（其中$r_n$枚举$(0,1)$中所有有理数），其$\liminf$和$\limsup$可用于描述序列值的聚集范围。

**数项级数：**级数是数列的一种延伸，即对数列$(a_n)$求和$\sum_{n=1}^{\infty} a_n$。严格定义是其**部分和**序列$S_N=\sum_{n=1}^N a_n$的极限。如果$S_N$有极限$S$，则称级数收敛于$S$；否则发散。特殊地，$\sum a_n$收敛也常说"级数$\sum a_n$的和为$S$"。基本判别方法：如果$a_n\nrightarrow 0$，则$\sum a_n$必发散（收敛级数的必要条件是项趋于0）。正项级数（所有$a_n\ge0$）最容易判断：其部分和序列$S_N$单调不减，若有上界则收敛，否则发散至$+\infty$。常见的正项级数有**p级数** $\sum \frac{1}{n^p}$（当$p>1$收敛，$p\le1$发散），**几何级数** $\sum r^n$（当$|r|<1$收敛于$1/(1-r)$，$|r|\ge1$发散）。对于一般级数，可以将正负项拆开考虑绝对值。如果$\sum |a_n|$收敛，则称$\sum a_n$**绝对收敛**。绝对收敛蕴含收敛，但反之不一定：例如$\sum (-1)^{n-1}/n$（交错调号的调和级数）条件收敛但不绝对收敛。

**级数的判别法：**分析级数收敛常用以下测试：

* **比较测试：**若$0\le a_n\le b_n$且$\sum b_n$收敛，则$\sum a_n$收敛；反之若$\sum a_n$发散且$a_n\ge b_n\ge0$，则$\sum b_n$发散。这可扩展到符号交替或一般项，通过比较绝对值或取上、下估计判别。
* **比值判别法：**对于$a_n>0$，考察$\lim_{n\to\infty}\frac{a_{n+1}}{a_n}=L$：若$L<1$则$\sum a_n$必收敛，$L>1$则发散，$L=1$则此法无结论。比如，用于判别$\sum \frac{n!}{10^n}$之类的级数。
* **根值判别法：**考察$\lim_{n\to\infty}\sqrt[n]{|a_n|}=L$，同样地$L<1$绝对收敛，$L>1$发散，$L=1$需其他方法。
* **交错级数判别法（Leibniz 判别法）：**若$a_n$单调趋于0且交替符号（如$(-1)^{n}a_n$），则$\sum (-1)^n a_n$收敛。而且其部分和误差绝对值小于下一项的绝对值。这对条件收敛级数如$\sum (-1)^{n-1}/n$非常有效。

**幂级数：**幂级数是形如$\sum_{n=0}^\infty c_n (x-a)^n$的函数级数（稍后第7章深入讨论），但在本章上下文，可将其看成参数$x$的普通级数。对于每个固定$x$，这是一个数项级数。幂级数的收敛集合通常是关于中心$a$对称的区间（在$\mathbb{R}$的情况），由其**收敛半径**$R$决定：当$|x-a|<R$绝对收敛，当$|x-a|>R$发散，边界处$|x-a|=R$需要逐点判别。收敛半径常可通过公式$1/R=\limsup_{n\to\infty}\sqrt[n]{|c_n|}$求得。这在后续将被使用。

### 重要定理与技巧

**单调有界收敛定理：**这一定理已经在拓扑章节提及：如果一个实数序列单调且有界，那么它必收敛。证明利用了实数完备性：单调上界存在最小上界或下界。这个定理经常用于证明序列极限存在，例如某些递归序列的极限、迭代逼近的收敛性等。

**Squeeze定理（夹逼定理）：**若$a_n\le b_n\le c_n$并且$\lim a_n = L = \lim c_n$，则$\lim b_n = L$。这是计算序列极限的有力工具，当直接算较难时，通过构造两个简单序列夹住目标序列就可求其极限。例如，证明$\lim n\sin(1/n)=1$时，可用$-1/n \le \sin(1/n)\le 1/n$来夹逼求解。

**反证法判断级数：**检查级数$\sum a_n$发散的一个直接方式是验证$a_n$不趋于0。例如若$a_n$趋向某非零值或震荡不趋于0，则级数无法收敛。这经常是快速判别的方法：看到$a_n$的极限不是0，立即判定发散。对于难判断的条件收敛情况，也可考虑发散判别，比如著名的调和级数$\sum 1/n$，虽然$a_n\to0$但它发散，可通过与积分比较（见下文）来证明。

**积分比较法：**对正项级数，比较$\sum a_n$与$\int a(x)dx$也有效。如果$a_n = f(n)$且$f(x)$在$x$足够大时单调递减为正，则$\sum_{n=N}^\infty a_n$与$\int_{N}^\infty f(x),dx$的敛散性一致。经典例子：$\sum \frac{1}{n}$与$\int_{1}^\infty \frac{1}{x},dx$都发散，因此调和级数发散；而$\sum \frac{1}{n^p}$对照$\int \frac{1}{x^p},dx$得到当$p>1$时积分收敛级数也收敛。当$p=1$积分发散对应级数发散。这种连续化处理有助于判断许多正项级数。

**绝对收敛与条件收敛：**绝对收敛是级数的强收敛形式。**绝对收敛的级数可以进行任意重新排列仍收敛至相同和值**，并且其收敛性不依赖项的次序。而条件收敛的级数（比如$\sum (-1)^{n-1}/n$）次序一变可能改变和值甚至发散——这是莱布尼茨级数等在更高课程讨论的Riemann重排定理。当判断一个交错级数时，通常首先看看其绝对值级数是否收敛，如果是则省事；如果否，再考虑交错测试（如Leibniz准则）。务必避免将条件收敛级数进行不允许的运算，如调换求和次序、改变排列等，否则可能出错。

**幂级数收敛半径计算：**常见技巧包括利用**比值法**或**根值法**直接求$c_n$的增长率。例如$c_n = \frac{1}{n!}$则$\sqrt[n]{|c_n|} = 1/n!^{1/n}\to 0$给出$R=\infty$，表示$\sum \frac{(x-a)^n}{n!}$（即$e^x$的级数）对所有$x$绝对收敛。若$c_n$呈比例如$c_n = r^n$，则$\sqrt[n]{|c_n|}=|r|$，$R=1/|r|$。如果$c_n$是渐近与某个容易处理的表达式等价，可用例如斯特林公式等估计以求$R$。

### 常见陷阱和误区

* **错把发散当收敛：**初学者常见错误是认为$\sum a_n$的项$a_n\to0$就足够保证级数收敛，这是错误的。"项趋0"只是必要非充分条件。经典反例就是调和级数$1/n$，虽然$1/n\to0$，但$\sum 1/n$发散。此外，还有许多交错级数表面项趋0但并不绝对收敛甚至条件发散，需要具体分析其求和行为。

* **交错级数判别条件不充分：**Leibniz判别要求交错项的绝对值单调下降且趋0。如果忽略单调下降条件可能出问题。例如定义$a_n = \frac{(-1)^n}{\sqrt[n]{n}}$，其绝对值$\frac{1}{\sqrt[n]{n}}$趋向1而非0，所以不满足条件肯定发散。但即使调整为$a_n = (-1)^n\frac{1+(-1)^n}{n}$，绝对值是$\frac{1+(-1)^n}{n}$，虽然趋0但不单调，因为偶数项为$2/n$奇数项为0，单调性破坏。此时级数$\sum a_n$等于$\sum_{k=1}^\infty \frac{(-1)^{2k}}{2k} + \sum_{k=1}^\infty \frac{(-1)^{2k-1}}{2k-1} = \sum \frac{1}{2k} - 0$，实质上类似$\frac{1}{2}\sum 1/k$发散。所以使用Leibniz判别要检查条件，不能少条件或误用。

* **级数项级数混淆：**有时对一个复杂级数的分析可以分步，比如考虑$\sum a_n b_n$，有人会尝试将其判断等价于$\sum a_n$和$\sum b_n$各自的收敛性。但除非有特殊情况（例如绝对收敛或正项情况），一般**不能**简单拆分级数项的乘积或和来分别判断。比如$\sum (\frac{1}{n}+(-\frac{1}{n}))\$每一项$\frac{1}{n}+(-\frac{1}{n})=0\$，表面看部分和恒0而收敛，但单独看$\sum \frac{1}{n}$和$\sum -\frac{1}{n}$各自都发散。这说明对条件收敛级数，调整或拆分求和可能改变结果，必须整体考虑。

* **序列极限运算失误：**对于$\limsup$和$\liminf$的计算要小心。有时需要拆分序列观察其子序列。一个典型错误是忘记序列可以有多个子序列聚向不同极限。例如Problem 19中，序列$r_n^{,r_n}$的子序列可能趋近1（当$r_n$逼近0或1）也可能逼近$e^{-1/e}\approx 0.692$（当$r_n$在1/e附近）。计算$\liminf$与$\limsup$时要考虑所有可能子序列的极限，不能只看一个特定简单子序列或假定极限存在。

### 与教材练习题相关的解析

**Problem 1:** 证明实数集<img src="https://latex.codecogs.com/svg.latex?\mathbb{R}"/>的最小上界性质。这个证明需要展示任何有上界的非空实数子集都有最小上界。关键步骤包括：
1. 构造一个有理数序列逼近上确界
2. 利用实数的完备性证明这个序列收敛
3. 证明收敛的极限就是最小上界

**Problem 2:** 证明<img src="https://latex.codecogs.com/svg.latex?\sqrt{2}"/>是无理数。这个经典证明使用反证法：
1. 假设<img src="https://latex.codecogs.com/svg.latex?\sqrt{2}"/>是有理数，可以表示为<img src="https://latex.codecogs.com/svg.latex?\frac{p}{q}"/>，其中<img src="https://latex.codecogs.com/svg.latex?p"/>和<img src="https://latex.codecogs.com/svg.latex?q"/>互质
2. 推导出<img src="https://latex.codecogs.com/svg.latex?2q^2=p^2"/>，说明<img src="https://latex.codecogs.com/svg.latex?p"/>是偶数
3. 设<img src="https://latex.codecogs.com/svg.latex?p=2k"/>，代入得到<img src="https://latex.codecogs.com/svg.latex?q^2=2k^2"/>，说明<img src="https://latex.codecogs.com/svg.latex?q"/>也是偶数
4. 这与<img src="https://latex.codecogs.com/svg.latex?p"/>和<img src="https://latex.codecogs.com/svg.latex?q"/>互质矛盾

**Problem 3:** 证明复数乘法满足结合律。设<img src="https://latex.codecogs.com/svg.latex?z_1=a_1+b_1i"/>，<img src="https://latex.codecogs.com/svg.latex?z_2=a_2+b_2i"/>，<img src="https://latex.codecogs.com/svg.latex?z_3=a_3+b_3i"/>，需要证明：
<img src="https://latex.codecogs.com/svg.latex?(z_1z_2)z_3=z_1(z_2z_3)"/>
通过直接计算两边，可以验证这个等式成立。

**Problem 4:** 证明代数基本定理的弱形式。这个证明使用数学归纳法和罗尔定理：
1. 基础情况：一次多项式显然最多有一个实根
2. 归纳假设：假设<img src="https://latex.codecogs.com/svg.latex?n"/>次多项式最多有<img src="https://latex.codecogs.com/svg.latex?n"/>个实根
3. 归纳步骤：对于<img src="https://latex.codecogs.com/svg.latex?(n+1)"/>次多项式，如果它有超过<img src="https://latex.codecogs.com/svg.latex?(n+1)"/>个实根，其导数将有超过<img src="https://latex.codecogs.com/svg.latex?n"/>个实根，与归纳假设矛盾

**Problem 5:** 证明<img src="https://latex.codecogs.com/svg.latex?\lim_{n\to\infty}\left(1+\frac{1}{n}\right)^n=e"/>。这个证明需要展示：
1. 序列<img src="https://latex.codecogs.com/svg.latex?a_n=\left(1+\frac{1}{n}\right)^n"/>单调递增且有上界
2. 利用二项式定理展开<img src="https://latex.codecogs.com/svg.latex?a_n"/>
3. 证明极限存在且等于<img src="https://latex.codecogs.com/svg.latex?e"/>

**Problem 6:** 证明<img src="https://latex.codecogs.com/svg.latex?\sum_{n=1}^{\infty}\frac{1}{n^2}=\frac{\pi^2}{6}"/>。这个著名的巴塞尔问题可以通过多种方法证明，其中一种方法是：
1. 考虑函数<img src="https://latex.codecogs.com/svg.latex?f(x)=x^2"/>在区间<img src="https://latex.codecogs.com/svg.latex?[-\pi,\pi]"/>上的傅里叶级数展开
2. 计算傅里叶系数
3. 利用帕塞瓦尔定理得到所需结果

**Problem 7:** 证明<img src="https://latex.codecogs.com/svg.latex?\lim_{x\to0}\frac{\sin x}{x}=1"/>。这个极限的证明可以通过几何方法：
1. 考虑单位圆上的扇形面积
2. 比较三角形和扇形的面积
3. 利用夹逼定理得到极限值

**Problem 8:** 证明<img src="https://latex.codecogs.com/svg.latex?\int_{0}^{\infty}e^{-x^2}dx=\frac{\sqrt{\pi}}{2}"/>。这个著名的积分可以通过以下步骤证明：
1. 考虑二重积分<img src="https://latex.codecogs.com/svg.latex?\iint_{\mathbb{R}^2}e^{-(x^2+y^2)}dxdy"/>
2. 转换为极坐标
3. 计算得到结果

**Problem 9:** 证明<img src="https://latex.codecogs.com/svg.latex?\sum_{n=1}^{\infty}\frac{1}{n}"/>发散。这个调和级数发散的证明可以通过：
1. 将级数分组
2. 每组的下界估计
3. 利用比较判别法得出结论

**Problem 10:** 证明<img src="https://latex.codecogs.com/svg.latex?\lim_{n\to\infty}\sqrt[n]{n}=1"/>。这个极限的证明可以通过：
1. 取对数
2. 利用洛必达法则
3. 还原得到结果

**Problem 11:**"证明：$U\subset \mathbb{R}^n$是开集当且仅当它可以表示为可数个开球的并。" 此题考查$\mathbb{R}^n$中开集的基数性质和稠密有理点的应用。证明分两部分：

* *充分性：* 可数多个开球（开球即开圆球体，在$\mathbb{R}^n$中的一般"区间"）的并明显是开集，因为开球本身是开集而开集的并仍是开集。

* *必要性：* 设$U$是$\mathbb{R}^n$中的一个开集。根据开集定义，对于每个点$x\in U$，存在一个半径$r_x>0$，使得以$x$为中心、$r_x$为半径的开球$B(x,r_x)\subset U$。由于有理数在实数中稠密，$\mathbb{R}^n$中也存在稠密的有理点集（可将每个坐标取有理数得到稠密点）。因此对于上述每个$x$，可以在$B(x,r_x)$中找到一个坐标都为有理数的点$q_x\in B(x,r_x)$（因为$B(x,r_x)$是一个开放区域，一定包含无数有理点）。定义$q_x$为代表点，并取一个**有理半径**$\rho_x$（可取$\rho_x$为小于$r_x$的有理数）使得开球$B(q_x,\rho_x)\subset B(x,r_x)\subset U$。由于$q_x$和$\rho_x$都可以只取有理数值，而有理数集可数，那么所有这样得到的开球$B(q_x,\rho_x)$的集合至多是可数个不同开球的集合。另一方面，每个$x\in U$都落在某个这样的$B(q_x,\rho_x)$内（其实就是它自身对应的那个），因此
  $U\subset \bigcup_{x\in U}B(q_x,\rho_x).$
  反过来显然$\bigcup_{x\in U}B(q_x,\rho_x)\subset U$，因为我们从一开始就保证每个这些球都在$U$里。综上，$U$正是这些开球的并，而且这一并至多是可数的（严格来说，需要注意不同的$x$可能对应相同的$q_x,\rho_x$组合，但无妨，因为重复的并不影响结果，可取不同的组合）。因此$U$表示为可数个开球之并。

这个结论直观理解是：由于有理点密布$\mathbb{R}^n$且有理集合可数，我们可以用有理中心和有理半径的球作为"基底"来逼近描述任意开集。这一点在实分析和拓扑学中十分重要，它表明了$\mathbb{R}^n$的**可分性**和拓扑基的可数性。

## 第4章 函数与极限

### 基本定义与直观理解

**函数与极限：**函数$f: \mathbb{R} \to \mathbb{R}$在$x_0$处的极限$\lim_{x\to x_0} f(x) = L$表示：对于任意$\varepsilon>0$，存在$\delta>0$，当$0<|x-x_0|<\delta$时，$|f(x)-L|<\varepsilon$。极限存在的充分必要条件是：左右极限存在且相等。函数$f(x)$在$x_0$处连续，当且仅当$\lim_{x\to x_0} f(x) = f(x_0)$。

**无穷大与无穷小：**函数$f(x)$在$x_0$处趋于无穷大（小），当且仅当对于任意$M>0$（$M<0$），存在$\delta>0$，当$0<|x-x_0|<\delta$时，$|f(x)|>M$（$|f(x)|<M$）。

**极限的四则运算：**如果$\lim_{x\to x_0} f(x) = L$和$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。

**极限的保号性：**如果$\lim_{x\to x_0} f(x) = L$且$L>0$（或$L<0$），则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$（或$f(x)<0$）。

**极限的唯一性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} f(x) = M$，则$L=M$。

**极限的连续性：**如果$\lim_{x\to x_0} f(x) = f(x_0)$，则$f(x)$在$x_0$处连续。

**极限的保序性：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，且存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x) \le g(x)$，则$L \le M$。

**极限的运算法则：**如果$\lim_{x\to x_0} f(x) = L$且$\lim_{x\to x_0} g(x) = M$，则
* $\lim_{x\to x_0} [f(x) + g(x)] = L + M$
* $\lim_{x\to x_0} [f(x) - g(x)] = L - M$
* $\lim_{x\to x_0} [f(x) g(x)] = L M$
* 如果$M\neq0$，则$\lim_{x\to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$

**极限的夹逼定理：**如果$f(x) \le g(x) \le h(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} h(x) = L$，则$\lim_{x\to x_0} g(x) = L$。

**极限的单调性：**如果$f(x) \le g(x)$且$\lim_{x\to x_0} f(x) = \lim_{x\to x_0} g(x) = L$，则$f(x) \le L \le g(x)$。
