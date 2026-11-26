# Day 024 · 连锁不平衡

> **部分** 第二部分 群体遗传学 ｜ **周次** 第 4 周 群体遗传学基础：HWE、连锁不平衡与选择模型 ｜ **发布日期** 2026-11-26 ｜ **建议用时** 约 100 分钟（讲义 45′ · 主读 30′ · 练习 25′）
> **主读** Coop 讲义第 3 章（位点间相关部分）；Holsinger 讲义 *Two-locus population genetics* 一章；Slatkin（2008）
> **关键词** linkage disequilibrium (LD) · linkage equilibrium · haplotype frequency · D · D′ · r² · recombination · drift–recombination balance · admixture LD · association mapping

## 学习目标

完成本讲后，应能够：

1. 由单倍型频率计算连锁不平衡的三种常用度量 $D$、$D'$ 与 $r^{2}$，并说明它们各自反映的信息；
2. 推导连锁不平衡在重组作用下的衰减，并与 Hardy–Weinberg 比例的建立速度相比较；
3. 说明突变、漂变、群体混合、选择与非随机交配如何产生或维持连锁不平衡；
4. 理解漂变与重组之间的平衡，以及连锁不平衡的范围为何反映群体历史；
5. 解释连锁不平衡在关联作图中的作用及其对作图分辨率的影响。

---

## 1 从单位点到两位点

Day 022–023 讨论的都是单个位点。一旦同时考虑两个位点，只知道各自的等位基因频率就不够了：还需要知道等位基因在同一条染色体上的组合方式，也就是单倍型（Day 019）的频率。Holsinger 指出，即使一个群体满足 Hardy–Weinberg 原理的全部假设，在两个位点的情形下也不能只谈等位基因频率（Holsinger, n.d.-b）。

设位点 1 有等位基因 $A$、$a$，位点 2 有 $B$、$b$，四种单倍型的频率为 $p_{AB}$、$p_{Ab}$、$p_{aB}$、$p_{ab}$。若两个位点的等位基因在单倍型中随机组合，则 $p_{AB} = p_A p_B$，依此类推，称为**连锁平衡**（linkage equilibrium）；否则称为**连锁不平衡**（linkage disequilibrium, LD）。直观地说，若 $A$ 几乎总是与 $B$ 出现在同一条单倍型上，那么知道一条染色体在位点 1 上携带 $A$，就几乎可以断定它在位点 2 上携带 $B$。这一术语最早由 Lewontin 与 Kojima（1960）使用；Slatkin（2008）评论说，它是一个不能顾名思义的术语，因为连锁不平衡并不要求两个位点相互连锁，甚至可以存在于不同染色体上的位点之间（第 4 节）。

---

## 2 连锁不平衡的度量

### 2.1 D

最基本的度量是

$$D = p_{AB} - p_A p_B = p_{AB}\,p_{ab} - p_{Ab}\,p_{aB}.$$

由此，四种单倍型的频率都可以写成"随机期望加减 $D$"的形式：$p_{AB} = p_A p_B + D$，$p_{ab} = p_a p_b + D$，$p_{Ab} = p_A p_b - D$，$p_{aB} = p_a p_B - D$。$D$ 的符号取决于等位基因的标记方式，交换 $A$ 与 $a$ 的名称就会使 $D$ 变号；更重要的是，$D$ 的可能取值范围受等位基因频率限制，因而难以在不同位点对之间比较。

计算这些度量需要单倍型频率，而由二倍体的基因型数据并不能直接读出双杂合子的单倍型（Day 019）。实际分析中，要么先对数据定相，要么用统计方法由基因型频率估计单倍型频率（Browning & Browning 2011）；在样本量小或位点稀有时，估计的不确定性需要特别注意。

### 2.2 D′

Lewontin（1964）提出用 $D$ 除以它在给定等位基因频率下可能取到的最大绝对值，得到标准化的 $D'$：

$$D' = \frac{D}{D_{\max}}, \qquad D_{\max} = \begin{cases}\min(p_A p_b,\; p_a p_B), & D > 0,\\[2pt] \min(p_A p_B,\; p_a p_b), & D < 0.\end{cases}$$

$\lvert D' \rvert = 1$ 当且仅当四种单倍型中至少有一种不存在，常称为"完全"连锁不平衡。这通常意味着两个位点之间在样本的历史中没有发生过可检测的重组（或重复突变），因此 $D'$ 常被用来描述重组的历史。

### 2.3 r²

另一种常用度量是两个位点等位基因状态之间相关系数的平方：

$$r^{2} = \frac{D^{2}}{p_A\,p_a\,p_B\,p_b}.$$

$r^{2} = 1$ 要求只存在两种单倍型，且两个位点的等位基因频率相同，此时知道一个位点的等位基因就能完全确定另一个位点的等位基因。因此，$r^{2}$ 衡量的是一个位点能在多大程度上"代表"另一个位点，这正是关联作图所关心的（第 5 节）。同一对位点的 $D'$ 可以很高而 $r^{2}$ 很低，例如一个稀有等位基因只出现在某一种单倍型上时（练习 1）。Slatkin（2008）指出，人们之所以提出多种不同的度量，正是因为它们反映了非随机关联的不同侧面。

---

## 3 重组使连锁不平衡衰减

在随机交配的大群体中，下一代的 $AB$ 单倍型有两个来源：以概率 $1 - c$ 未在两个位点之间发生重组，直接由亲代的 $AB$ 单倍型传来；以概率 $c$ 发生重组，由来自两条不同单倍型的 $A$ 与 $B$ 拼接而成，其频率为 $p_A p_B$。其中 $c$ 为两个位点之间的重组率（Day 015 记为 $r$，本讲为避免与 $r^{2}$ 混淆改记为 $c$）。于是

$$p_{AB,\,t+1} = (1 - c)\,p_{AB,\,t} + c\,p_A p_B \quad\Longrightarrow\quad D_{t+1} = (1 - c)\,D_t, \qquad D_t = D_0(1 - c)^{t}.$$

$D$ 的半衰期约为 $\ln 2/c$ 代。与 Hardy–Weinberg 比例一代即可建立不同，即使两个位点位于不同的染色体上（$c = 1/2$），连锁不平衡也只是每代减半，而不会一代消失；紧密连锁的位点之间，连锁不平衡可以维持成百上千代（练习 2）。因此，单个位点上的基因型比例很快就能恢复平衡，而位点之间的关联却可以长期保留，这使连锁不平衡成为记录群体历史的"慢变量"。在很短的距离上，基因转换还会加快衰减（Day 018）。单倍型频率的这一递推关系及其向多个位点的推广，可参阅 Holsinger 讲义的两位点一章（Holsinger, n.d.-a）。

---

## 4 产生与维持连锁不平衡的过程

**突变.** 一个新突变产生于某一条特定的单倍型上，因此它与附近所有的多态位点之间起初都处于完全连锁不平衡（$\lvert D' \rvert = 1$）。随着时间推移，重组逐渐把它与原来的单倍型背景拆开；携带它的单倍型越长，突变往往越年轻，这是基于单倍型的选择检验的基础（Day 075）。

**遗传漂变.** 在有限群体中，单倍型频率的随机波动会不断产生连锁不平衡，而重组又不断使之衰减。二者达到平衡时，$r^{2}$ 的期望近似为

$$E[r^{2}] \approx \frac{1}{1 + 4N_e c},$$

其中 $N_e$ 为有效群体大小（Day 031），$c$ 以摩为单位（Sved 1971）。这一近似说明，连锁不平衡延伸的物理距离取决于 $N_e c$：有效群体越小，或近期经历过瓶颈，连锁不平衡就延伸得越远。反过来，可以由连锁不平衡的程度估计有效群体大小（练习 4）。对不连锁的位点（$c = 1/2$），这一近似给出 $E[r^{2}] \approx 1/(1 + 2N_e)$，在大群体中可以忽略；漂变造成的显著连锁不平衡主要存在于连锁的位点之间。

**群体混合与群体结构.** 把等位基因频率不同的群体混合在一起，即使两个位点不连锁，也会产生连锁不平衡。设两个群体以 1:1 混合，各自处于连锁平衡，则混合群体中

$$D = \frac{1}{4}\left(p_{A1} - p_{A2}\right)\left(p_{B1} - p_{B2}\right),$$

其中 $p_{A1}$、$p_{A2}$ 为 $A$ 在两个群体中的频率，$p_{B1}$、$p_{B2}$ 同理。这是 Wahlund 效应（Day 023）在两位点上的对应物：单位点上的杂合子缺失来自频率在亚群体间的方差，两位点上的连锁不平衡则来自两个位点频率差异的协方差。混合之后，这种连锁不平衡按 $(1 - c)^{t}$ 衰减，不连锁的位点之间很快消失，紧密连锁的位点之间则保留较久；连锁不平衡随距离衰减的方式因而保存了关于过去事件的信息（Slatkin 2008；练习 3）。

**选择.** 若两个位点上的等位基因组合对适合度有上位效应（Day 020），选择可以维持连锁不平衡；Lewontin 与 Kojima（1960）讨论的正是连锁与上位选择的共同作用。此外，一个有利突变在扩散时会带动与之连锁的中性等位基因一起上升，产生大范围的连锁不平衡（遗传搭车，Day 052）。

**非随机交配.** 正选型交配会使影响同一性状的等位基因在不同位点之间产生正相关（Day 023；Yengo et al. 2018）。

---

## 5 连锁不平衡与关联作图

连锁不平衡是关联作图的基础。在全基因组关联研究中，真正影响性状的变异往往并未被直接分型；但只要被分型的标记与它处于较强的连锁不平衡，标记本身就会表现出与性状的关联（Holsinger, n.d.-b；Slatkin 2008）。这带来两个结果。第一，所需的标记密度取决于连锁不平衡的范围：连锁不平衡延伸越远，覆盖基因组所需的标记越少。第二，作图的分辨率也取决于它：连锁不平衡越长，与性状关联的区域越宽，越难确定致病变异的位置。由于 $r^{2}$ 直接衡量一个标记能在多大程度上代表另一个位点，它是评价标记覆盖程度时最常用的度量。同样由于连锁不平衡，一个关联信号往往同时涉及若干个彼此高度相关的候选变异，统计上难以区分；比较连锁不平衡模式不同的多个群体，或结合功能证据，有助于把信号缩小到真正的致病变异。从关联到因果的推断及其局限，将在 Day 068 讨论。

---

## 6 案例研究：人类基因组中连锁不平衡的范围

**问题** 人类基因组中的连锁不平衡延伸多远？这一问题既关系到能否在全基因组范围内进行关联作图，也反映了人类群体的历史。

**方法** Reich 等（2001）在 44 名北欧血统的无亲缘个体中，围绕一些核心 SNP 分型了距离不等的 SNP，测定连锁不平衡随距离下降到一半时的距离，并与尼日利亚样本进行比较（Reich et al. 2001）。

**结果** 北欧血统样本中的连锁不平衡延伸得远比不考虑近期剧烈人口事件的理论预期更远；作者认为，这一格局是由大约 2.7 万至 5.3 万年前的一次显著的人口事件塑造的。相比之下，尼日利亚样本中的连锁不平衡延伸距离要短得多（Reich et al. 2001）。

**意义** 这项研究表明，连锁不平衡的范围首先反映的是群体历史：瓶颈等人口事件使有效群体变小，从而使连锁不平衡延伸更远（第 4 节）。它也说明，在连锁不平衡较长的群体中较少的标记就能覆盖基因组，而在连锁不平衡较短的群体中可以获得更高的作图分辨率。人口历史如何塑造遗传变异的格局，将在 Day 045 与第十部分进一步讨论。

---

## 今日学习材料（均可免费获取）

| 类型 | 材料 | 说明 |
|---|---|---|
| 必读 | Coop，*Population and Quantitative Genetics*：[第 3 章 Population Structure and Correlations Among Loci](https://bio.libretexts.org/Bookshelves/Genetics/Population_and_Quantitative_Genetics_(Coop)/03%3A_Population_Structure_and_Correlations_Among_Loci) | 位点间相关（连锁不平衡）部分，约 20 分钟 |
| 必读 | Holsinger，*Lecture Notes in Population Genetics*：[figshare 存档](https://figshare.com/articles/Lecture_notes_in_population_genetics/100687) | *Two-locus population genetics* 一章，约 15 分钟 |
| 精读 | Slatkin（2008）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC5124487) | 连锁不平衡的度量、成因与应用 |
| 选读 | Reich et al.（2001）：[作者实验室全文](https://reich.hms.harvard.edu/sites/reich.hms.harvard.edu/files/inline-files/2001_Reich_Nature.pdf) | 案例研究原文 |
| 选读 | Holsinger：[Association mapping: a (very) brief overview](https://darwin.eeb.uconn.edu/eeb348-notes/association-intro.html) | 关联作图与两位点遗传学的简要介绍 |

---

## 思考与练习

1. **（计算）** 在 1000 条单倍型中，$AB$ 470、$Ab$ 30、$aB$ 130、$ab$ 370（本题数据为假设）。(a) 计算 $p_A$、$p_B$、$D$（用两种公式），以及 $D'$ 与 $r^{2}$。(b) 若某个稀有等位基因只出现在一种单倍型上，为什么它与邻近位点的 $\lvert D' \rvert$ 等于 1，而 $r^{2}$ 可能很小？
2. **（计算）** 设初始 $D_0 = 0.2$。分别就 $c = 0.5$、0.1、0.01 与 0.001，计算 10 代后的 $D$、$D$ 的半衰期，以及使 $D < 0.01$ 所需的代数。这些结果说明了什么？
3. **（计算）** 两个各自处于连锁平衡的群体以 1:1 混合，$A$ 的频率分别为 0.9 与 0.1，$B$ 的频率分别为 0.8 与 0.2。(a) 计算混合群体中的 $p_{AB}$、$D$、$D'$ 与 $r^{2}$，并用第 4 节的公式验证 $D$。(b) 若两个位点不连锁，混合后 1、5、20 代的 $D$ 是多少？若 $c = 0.01$ 呢？(c) 为什么混合产生的连锁不平衡随距离衰减的方式可以用来推断混合发生的时间？
4. **（计算）** 设 $N_e = 10{,}000$，每碱基每代的重组率为 $10^{-8}$（本题参数为假设）。(a) 按 Sved 的近似，计算相距 1 kb、10 kb 与 100 kb 的位点之间 $r^{2}$ 的期望。(b) 若在另一个群体中观察到相距 10 kb 的位点之间平均 $r^{2} = 0.2$，估计其有效群体大小。(c) 实际应用中，有限样本本身也会使 $r^{2}$ 的估计偏高，这对 (b) 的估计有什么影响？
5. **（概念）** (a) 下列过程中，哪些能在不连锁的位点之间产生连锁不平衡：新突变、群体混合、正选型交配、遗传漂变、上位选择？(b) 为什么说"连锁不平衡"这一名称容易引起误解？(c) 比较 $D'$ 与 $r^{2}$：研究重组历史时更常用哪一个？评价标记能否代表致病位点时呢？
6. **（文献评论）** 阅读 Reich 等（2001）。(a) 为什么瓶颈会使连锁不平衡延伸得更远？(b) 除人口历史之外，还有哪些因素可能导致不同群体之间连锁不平衡范围的差异？(c) 这一发现对关联研究的设计有何启示？

<details>
<summary>答案要点</summary>

1. (a) $p_A = 0.5$，$p_B = 0.6$，$p_{AB} = 0.47$；$D = 0.47 - 0.30 = 0.17$，或 $D = 0.47 \times 0.37 - 0.03 \times 0.13 = 0.17$。$D > 0$，$D_{\max} = \min(0.5 \times 0.4,\, 0.5 \times 0.6) = 0.2$，$D' = 0.85$；$r^{2} = 0.17^{2}/(0.5 \times 0.5 \times 0.6 \times 0.4) \approx 0.48$（代码验算）。(b) 稀有等位基因只出现在一种单倍型上，四种单倍型中缺失一种，因此 $\lvert D' \rvert = 1$；但由于两个位点的等位基因频率相差很大，知道邻近位点的等位基因并不能很好地预测是否携带这个稀有等位基因，$r^{2}$ 的上限受频率差异限制，可能很小。
2. $c = 0.5$：10 代后约 $2.0 \times 10^{-4}$，半衰期 1 代，5 代即低于 0.01；$c = 0.1$：约 0.070，半衰期约 6.6 代，需 29 代；$c = 0.01$：约 0.181，半衰期约 69 代，需 299 代；$c = 0.001$：约 0.198，半衰期约 693 代，需 2995 代（代码验算）。紧密连锁位点之间的连锁不平衡可以保留极长的时间，而不连锁位点之间的连锁不平衡衰减很快，但也需要数代，而不是一代即消失。
3. (a) $p_A = p_B = 0.5$，$p_{AB} = (0.9 \times 0.8 + 0.1 \times 0.2)/2 = 0.37$，$D = 0.37 - 0.25 = 0.12$，与 $\frac{1}{4}(0.8)(0.6) = 0.12$ 一致；$D' = 0.12/0.25 = 0.48$，$r^{2} = 0.12^{2}/0.0625 \approx 0.23$（代码验算）。(b) 不连锁时依次为 0.06、0.00375、约 $10^{-7}$；$c = 0.01$ 时依次约为 0.119、0.114、0.098。(c) 混合后经过的代数越多，较远位点之间的连锁不平衡衰减得越多；比较连锁不平衡随遗传距离衰减的速率（近似为 $e^{-ct}$ 的形式），就可以估计混合以来经过的代数。
4. (a) $c = 10^{-5}$、$10^{-4}$、$10^{-3}$，$E[r^{2}]$ 依次约为 0.71、0.20、0.024（代码验算）。(b) $\hat N_e = (1/r^{2} - 1)/(4c) = (5 - 1)/(4 \times 10^{-4}) = 10{,}000$。(c) 有限样本使 $r^{2}$ 的估计值系统偏高，若不加校正，会低估有效群体大小；实际应用中需要扣除样本量带来的期望值。此外，这一近似本身也有局限，Sved 后来曾修正过推导中的一些问题。
5. (a) 群体混合、正选型交配、遗传漂变与上位选择都可以；新突变产生的连锁不平衡主要存在于它所在的单倍型附近，在不连锁位点之间迅速被重组打散。(b) 它并不要求位点相互连锁，指的其实是等位基因在单倍型中的非随机关联（Slatkin 2008）。(c) 研究重组历史时常用 $D'$，因为 $\lvert D' \rvert = 1$ 意味着没有观察到重组产生的第四种单倍型；评价标记能否代表致病位点时用 $r^{2}$，因为它直接衡量一个位点对另一个位点的预测能力。
6. (a) 瓶颈使有效群体变小，漂变产生连锁不平衡的作用增强；瓶颈之后的时间若不长，重组还来不及打散瓶颈期间形成的单倍型关联，因此连锁不平衡延伸更远（第 4 节）。(b) 局部重组率的差异、样本量与标记的选择方式（例如只选择在某一群体中常见的 SNP）、群体结构与混合，都可能造成差异。(c) 在连锁不平衡较长的群体中，较少的标记就能覆盖基因组；而在连锁不平衡较短的群体中，可以把关联区域缩小到更窄的范围，有利于精细定位。

</details>

---

## 关键术语

| 中文 | English | 释义 |
|---|---|---|
| 连锁不平衡 | linkage disequilibrium (LD) | 不同位点的等位基因在单倍型中的非随机关联，不要求位点相互连锁 |
| 连锁平衡 | linkage equilibrium | 单倍型频率等于各位点等位基因频率之积的状态 |
| 单倍型频率 | haplotype frequency | 某一单倍型在群体全部单倍型中所占的比例 |
| 标准化连锁不平衡系数 | normalized linkage disequilibrium (D′) | D 除以给定等位基因频率下 D 可能取到的最大绝对值 |
| 连锁不平衡相关系数平方 | squared correlation coefficient (r²) | 两个位点等位基因状态之间相关系数的平方，衡量一个位点对另一个位点的预测能力 |
| 混合连锁不平衡 | admixture linkage disequilibrium | 等位基因频率不同的群体混合后产生的连锁不平衡 |

---

## 参考文献

- Browning, S. R., & Browning, B. L. (2011). Haplotype phasing: Existing methods and new developments. *Nature Reviews Genetics, 12*(10), 703–714. https://doi.org/10.1038/nrg3054 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC3217888)］
- Lewontin, R. C. (1964). The interaction of selection and linkage. I. General considerations; heterotic models. *Genetics, 49*(1), 49–67. https://doi.org/10.1093/genetics/49.1.49
- Lewontin, R. C., & Kojima, K. (1960). The evolutionary dynamics of complex polymorphisms. *Evolution, 14*(4), 458–472.（DOI 未核实）
- Reich, D. E., Cargill, M., Bolk, S., Ireland, J., Sabeti, P. C., Richter, D. J., Lavery, T., Kouyoumjian, R., Farhadian, S. F., Ward, R., & Lander, E. S. (2001). Linkage disequilibrium in the human genome. *Nature, 411*(6834), 199–204. https://doi.org/10.1038/35075590 ［[作者实验室全文](https://reich.hms.harvard.edu/sites/reich.hms.harvard.edu/files/inline-files/2001_Reich_Nature.pdf)］
- Slatkin, M. (2008). Linkage disequilibrium — understanding the evolutionary past and mapping the medical future. *Nature Reviews Genetics, 9*(6), 477–485. https://doi.org/10.1038/nrg2361 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC5124487)］
- Sved, J. A. (1971). Linkage disequilibrium and homozygosity of chromosome segments in finite populations. *Theoretical Population Biology, 2*(2), 125–141.（DOI 未核实）
- Yengo, L., Robinson, M. R., Keller, M. C., Kemper, K. E., Yang, Y., Trzaskowski, M., Gratten, J., Turley, P., Cesarini, D., Benjamin, D. J., Wray, N. R., Goddard, M. E., Yang, J., & Visscher, P. M. (2018). Imprint of assortative mating on the human genome. *Nature Human Behaviour, 2*(12), 948–954. https://doi.org/10.1038/s41562-018-0476-3 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC6705135)］

**网络资源**（访问日期 2026-11-26）

- Coop, G. (n.d.). *Population and quantitative genetics*, Chapter 3 Population structure and correlations among loci. LibreTexts. https://bio.libretexts.org/Bookshelves/Genetics/Population_and_Quantitative_Genetics_(Coop)/03%3A_Population_Structure_and_Correlations_Among_Loci
- Holsinger, K. E. (n.d.-a). *Lecture notes in population genetics*. figshare. https://figshare.com/articles/Lecture_notes_in_population_genetics/100687
- Holsinger, K. E. (n.d.-b). *Association mapping: A (very) brief overview*. University of Connecticut. https://darwin.eeb.uconn.edu/eeb348-notes/association-intro.html

---

**上一讲** [Day 023 · 偏离 HWE：近交、选型交配与群体结构](day023-departures-from-hwe.md) ｜ **下一讲** Day 025 · 自然选择 I：单位点选择模型
