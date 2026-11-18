# Day 015 · 遗传学回顾：孟德尔遗传、连锁与重组

> **部分** 第一部分 概念基础与证据 ｜ **周次** 第 3 周 遗传变异的来源 ｜ **发布日期** 2026-11-17 ｜ **建议用时** 约 90 分钟（讲义 40′ · 主读／主看 30′ · 练习 20′）
> **主读** OpenStax *Biology 2e* 第 12 章与 §13.1；复习 Yale EEB 122 第 2 讲 *Basic Transmission Genetics*（Day 003 已看过者可略）
> **关键词** meiosis · law of segregation · law of independent assortment · chi-square test · linkage · recombination fraction · centimorgan · genetic map · map function · interference · dominance · genotype–phenotype

## 学习目标

完成本讲后，应能够：

1. 用减数分裂中染色体的行为解释分离律与自由组合律；
2. 用 $\chi^2$ 拟合优度检验评价观察到的分离比是否符合孟德尔比例；
3. 由测交数据计算重组率，用三点测交确定基因顺序、图距、并发系数与干涉；
4. 解释图距与重组率之间的非线性关系，并使用 Haldane 作图函数；
5. 以孟德尔的皱粒基因为例，把孟德尔因子与分子层面的基因、等位基因和显隐性联系起来，并说明重组对进化的意义。

---

## 1 为什么在进化课程中复习遗传学

按 Day 001 的定义，进化是群体遗传组成跨世代的改变。要描述这种改变，首先要知道遗传物质如何从亲代传到子代。第 3 周讨论可遗传变异的来源：突变产生新的等位基因（Day 016–017），重组把已有的等位基因重新组合（Day 018），结构变异改变基因组的构成（Day 019），基因型又通过发育与环境产生表型（Day 020）。本讲复习这些内容的共同基础：孟德尔遗传的传递规则、连锁与重组，以及从 DNA 到表型的基本关系。孟德尔工作的历史背景及其与现代综合的关系已在 Day 003 讨论，本讲侧重定量分析。

---

## 2 减数分裂与孟德尔定律

### 2.1 染色体的行为

二倍体生物的每条染色体都有一条来自父方、一条来自母方的同源染色体。减数分裂使染色体数减半：第一次分裂中同源染色体彼此分离，第二次分裂中姐妹染色单体分离。在第一次分裂前期，同源染色体配对，非姐妹染色单体之间可以发生**交换**（crossing over）。染色体在减数分裂中的这些行为，正是孟德尔定律的细胞学基础，即遗传的染色体学说（OpenStax §13.1；Day 003）：

- **分离律**（law of segregation）：每个配子只得到一对等位基因中的一个，因为同源染色体在减数第一次分裂中彼此分离；
- **自由组合律**（law of independent assortment）：位于不同染色体上的基因独立地分配到配子中，因为不同的同源染色体对在赤道板上的排列方向彼此独立。

### 2.2 分离比与孟德尔的数据

杂合子自交 $Aa \times Aa$ 的子代基因型比例为 $1\,AA : 2\,Aa : 1\,aa$；若 $A$ 对 $a$ 完全显性，表型比例为 3:1。孟德尔报告的 F2 数据中，圆粒与皱粒为 5474:1850（2.96:1），子叶黄色与绿色为 6022:2001（3.01:1）（Mendel 1866）。两对性状同时分离时，$AaBb$ 自交预期得到 9:3:3:1 的表型比例；孟德尔的双因子杂交中，圆黄、圆绿、皱黄、皱绿四类种子分别为 315、108、101 与 32 粒（Mendel 1866）。

这样的数据与理论比例"相符"到什么程度，需要用统计检验来回答。**$\chi^2$ 拟合优度检验**比较各类别的观察数 $O_i$ 与期望数 $E_i$：

$$\chi^2 = \sum_{i=1}^{k} \frac{(O_i - E_i)^2}{E_i},$$

其中 $k$ 为类别数。当原假设（例如 3:1）成立且各类期望数不太小时，$\chi^2$ 近似服从自由度为 $k - 1$ 的 $\chi^2$ 分布。$\chi^2$ 越大，数据与假设比例的偏离越大（练习 1–2）。这一近似要求各类别的期望数不太小（常用的经验标准是不小于 5）；样本很小时，应改用精确检验。还要注意，检验"不能拒绝"某一比例，并不等于证明了该比例：它只说明在现有样本量下，数据与该比例之间的偏离不足以被检测出来。

### 2.3 概率规则与多个位点

孟德尔遗传的计算建立在两条概率规则之上（OpenStax 第 12 章）：相互独立的事件同时发生的概率等于各自概率之**积**（乘法法则）；互斥事件中任一事件发生的概率等于各自概率之**和**（加法法则）。例如，在 $AaBbCc \times AaBbCc$ 的杂交中，若三个位点相互独立，子代为 $aabbcc$ 的概率为 $(1/4)^3 = 1/64$。更一般地，一个在 $n$ 个独立位点上都杂合的个体可产生 $2^n$ 种配子，其自交后代有 $3^n$ 种基因型；在完全显性的情况下，表型类别数为 $2^n$，其中在所有位点上都表现显性性状的个体比例为 $(3/4)^n$。可见，即使只有少数几个分离的位点，后代中可能的组合数也会迅速增加，这正是有性生殖能够产生大量遗传组合的原因。

### 2.4 测交

把待测个体与隐性纯合子（$aa$）杂交，称为**测交**（test cross）。由于隐性纯合子只产生携带隐性等位基因的配子，子代的表型比例直接反映了待测个体所产生配子的比例：$Aa \times aa$ 得到 1:1 的子代。测交是检验分离、自由组合与连锁最直接的方法。

---

## 3 连锁与重组

### 3.1 连锁与重组率

位于同一条染色体上的基因倾向于一起遗传，称为**连锁**（linkage）。若两个基因完全连锁，双杂合子只产生两种亲本型配子；若它们之间发生交换，就会产生**重组型**配子。在测交中，重组型子代所占的比例称为**重组率**（recombination fraction），记为 $r$。$r$ 介于 0（完全连锁）与 0.5 之间；$r = 0.5$ 时，两个基因的表现与位于不同染色体上无异（OpenStax §13.1）。例如，Morgan 在 1912 年观察到果蝇翅长与体色之间的重组率为 17%（OpenStax §13.1）。

### 3.2 第一张遗传图

Sturtevant 当时是 Morgan 在哥伦比亚大学实验室的学生。他推论，若基因沿染色体线性排列，两基因之间的距离越远，其间发生交换的机会就越大，因此重组率可以作为距离的度量（Sturtevant 1913）。他据此分析了果蝇六个性连锁因子的连锁数据，把它们排成一条直线，从而建立了第一张遗传图（Sturtevant 1913；另见 Embryo Project Encyclopedia, n.d.）。按现行的约定，1% 的重组率对应 1 个图距单位，即 1 **厘摩**（centimorgan, cM）（OpenStax §13.1）。

### 3.3 三点测交与干涉

同时分析三个连锁基因，可以确定它们的顺序。若三个基因的顺序为 $a$–$b$–$c$，两个区段内同时发生交换（**双交换**）的子代最少；与亲本型相比，双交换子代中只有位于中间的基因改变了组合方式，据此即可判断哪个基因位于中间。两个相邻区段的图距相加，得到两端基因之间的图距；而直接由两端基因计算的重组率会偏小，因为双交换使两端基因恢复为亲本组合，在测交中无法被识别（练习 3）。

若两个区段的交换相互独立，双交换的期望频率等于两个区段重组率之积。观察到的双交换频率与这一期望之比称为**并发系数**（coefficient of coincidence），$c$；$I = 1 - c$ 称为**干涉**（interference）。$I > 0$ 表示一个区段内的交换会降低邻近区段发生交换的概率。

### 3.4 作图函数

图距 $d$（以摩，即 Morgan 计）的定义是两个位点之间、在一个配子所获得的染色单体上平均发生的交换次数。当两个位点相距较远时，多次交换中只有奇数次交换产生可见的重组，因此重组率会低估图距。若交换沿染色体随机发生且没有干涉（交换次数服从泊松分布），重组率与图距之间满足 **Haldane 作图函数**（Haldane 1919）：

$$r = \frac{1}{2}\left(1 - e^{-2d}\right) \quad\Longleftrightarrow\quad d = -\frac{1}{2}\ln(1 - 2r).$$

$d$ 很小时 $r \approx d$；随着 $d$ 增大，$r$ 趋近 0.5 而不会超过它（练习 4）。其他作图函数在这一框架中进一步考虑了干涉。

---

## 4 从 DNA 到表型

孟德尔所说的"因子"，今天称为**基因**：通常是编码蛋白质或功能 RNA 的 DNA 序列；同一基因的不同变体称为**等位基因**（allele）。个体在某些位点上的等位基因组成称为**基因型**（genotype），可观察的性状称为**表型**（phenotype）。

孟德尔的圆粒与皱粒性状提供了一个把两个层次联系起来的例子。Bhattacharyya 等（1990）发现，皱粒（$rr$）豌豆中编码淀粉分支酶 I（SBEI）的基因被一段约 0.8 kb 的插入序列打断，这段序列与玉米的 Ac/Ds 转座元件相似；皱粒种子的发育胚中缺少 SBEI 活性，种子中淀粉的合成因而改变，最终表现为皱缩的种子。这个例子说明了**显性**（dominance）的分子含义：杂合子中的一个功能拷贝就足以产生圆粒，因而功能丧失的等位基因 $r$ 表现为**隐性**（recessive）。显隐性描述的是不同等位基因在表型上的相互关系，而不是等位基因本身固有的属性。耐人寻味的是，孟德尔的皱粒等位基因与 Day 011 讨论的桦尺蛾黑化突变一样，都源于转座元件的插入。

孟德尔研究的七个性状中，有四个基因的分子身份到 2011 年已被确定，*R* 是其中第一个被克隆的（Reid & Ross 2011）。2025 年发表的研究报告了其余三个性状，即豆荚形状、豆荚颜色与花的位置相关基因的分子身份（Feng et al. 2025）。不过，孟德尔所选的性状在他的杂交中都表现出简单的分离比，这在遗传学中是较为特殊的情形；大多数性状受许多位点与环境共同影响（Day 003、Day 020）。

---

## 5 重组与进化

重组为进化提供了新的等位基因组合。在群体层面，两个位点上等位基因之间的统计关联称为**连锁不平衡**（Day 024）。在随机交配的大群体中，每一代的重组都会使这种关联按 $(1 - r)$ 的比例衰减：

$$D_t = D_0\,(1 - r)^{t},$$

其中 $D_t$ 为第 $t$ 代的连锁不平衡系数。不连锁的位点（$r = 0.5$）之间的关联一代就减半；而紧密连锁的位点（例如 $r = 0.001$）之间的关联可以维持数百代（练习 5）。因此，与有利突变紧密连锁的中性位点，会随之一起上升频率，这就是**遗传搭便车**的基础（第 2 部分）。重组在基因组中的分布并不均匀，并涉及交叉干涉、基因转换与重组热点等现象，这些内容将在 Day 018 讨论。重组本身也是进化的产物：它会打破已经被选择组合在一起的有利等位基因组合，那么重组为什么能够维持？这是进化生物学中的一个经典问题，将在 Day 055（重组进化的遗传学理论）与 Day 148（性的进化）讨论。

---

## 今日学习材料（均可免费获取）

| 类型 | 材料 | 说明 |
|---|---|---|
| 必读 | [OpenStax *Biology 2e* 第 12 章 Mendel's Experiments and Heredity](https://openstax.org/books/biology-2e/pages/12-introduction) | 孟德尔实验、概率规则与遗传定律，约 20 分钟 |
| 必读 | [OpenStax *Biology 2e* §13.1 Chromosomal Theory and Genetic Linkage](https://openstax.org/books/biology-2e/pages/13-1-chromosomal-theory-and-genetic-linkage) | 染色体学说、连锁与 Sturtevant 的作图方法，约 10 分钟 |
| 复习 | [Yale EEB 122](https://oyc.yale.edu/ecology-and-evolutionary-biology/eeb-122) 第 2 讲 *Basic Transmission Genetics* | Day 003 已看过者可略 |
| 精读 | Mendel（1866）英译本：[MendelWeb](https://cs.brown.edu/people/rblumber/MendelWeb/home.html) | 重点阅读描述 F2 分离比与双因子杂交的部分 |
| 选读 | Embryo Project Encyclopedia：[Sturtevant（1913）的遗传图](https://embryo.asu.edu/pages/linear-arrangement-six-sex-linked-factors-drosophila-shown-their-mode-association-1913-alfred) | 第一张遗传图的背景与逻辑 |
| 选读 | Reid & Ross（2011）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC3176118) | 孟德尔七个基因的分子研究进展 |

---

## 思考与练习

1. **（计算）** 用 $\chi^2$ 拟合优度检验分别检验孟德尔的两组 F2 数据是否符合 3:1：圆粒 5474、皱粒 1850；黄色 6022、绿色 2001。写出期望数、$\chi^2$ 值、自由度与近似 $P$ 值（自由度为 1 时，$\alpha = 0.05$ 的临界值为 3.841）。
2. **（计算）** 孟德尔双因子杂交的 F2 为圆黄 315、圆绿 108、皱黄 101、皱绿 32。(a) 检验其是否符合 9:3:3:1（自由度为 3 时，$\alpha = 0.05$ 的临界值为 7.815）。(b) 分别统计种子形状与子叶颜色两对性状，各自检验是否符合 3:1。(c) 9:3:3:1 的成立需要哪两个条件？
3. **（计算）** 三个连锁基因 $a$、$b$、$c$ 的三杂合子（亲本型为 $a\,b\,c$ 与 $+\,+\,+$）与隐性纯合子测交，得到 1000 个子代（本题数据为假设）：

   | 子代表型 | 个体数 |
   |---|---|
   | $a\,b\,c$ | 357 |
   | $+\,+\,+$ | 353 |
   | $a\,+\,+$ | 46 |
   | $+\,b\,c$ | 44 |
   | $a\,b\,+$ | 96 |
   | $+\,+\,c$ | 94 |
   | $a\,+\,c$ | 5 |
   | $+\,b\,+$ | 5 |

   (a) 哪两类是双交换？哪个基因位于中间？(b) 计算相邻基因之间的图距，以及两端基因之间直接算得的重组率；二者为何不同？(c) 计算并发系数与干涉。
4. **（计算）** 按 Haldane 作图函数：(a) 把重组率 $r = 0.05$、$0.2$、$0.4$ 换算为图距；(b) 把图距 $d = 0.1$、$0.5$、$1.0$ 摩换算为重组率。(c) 为什么相距很远的两个基因的重组率不会超过 0.5？这对构建遗传图意味着什么？
5. **（计算）** 按 $D_t = D_0(1 - r)^t$，分别计算 $r = 0.5$、$0.1$、$0.01$、$0.001$ 时连锁不平衡衰减一半所需的代数。据此解释：为什么与有利突变紧密连锁的中性等位基因会随之一起上升频率？
6. **（概念）** (a) 用 SBEI 的例子解释，为什么功能丧失的等位基因往往表现为隐性。(b) 为什么说显隐性是等位基因之间在表型上的关系，而不是等位基因固有的属性？(c) 孟德尔所选的七个性状都表现出简单的分离比。若他选择的是株高的连续变异，可能会得到什么结果？这与 Day 003 讨论的孟德尔学派与生物统计学派之争有何联系？

<details>
<summary>答案要点</summary>

1. 种子形状：$N = 7324$，期望 5493 与 1831，$\chi^2 \approx 0.263$，自由度 1，$P \approx 0.61$；子叶颜色：$N = 8023$，期望 6017.25 与 2005.75，$\chi^2 \approx 0.015$，$P \approx 0.90$。两者都远低于临界值 3.841，不能拒绝 3:1 的假设（代码验算）。
2. (a) 期望数为 312.75、104.25、104.25、34.75，$\chi^2 \approx 0.47$，自由度 3，$P \approx 0.93$，符合 9:3:3:1。(b) 形状：圆 423、皱 133，$\chi^2 \approx 0.345$（$P \approx 0.56$）；颜色：黄 416、绿 140，$\chi^2 \approx 0.010$（$P \approx 0.92$），各自符合 3:1。(c) 两对等位基因各自按 3:1 分离（完全显性），并且两个位点相互独立地分配到配子中（自由组合，即两个基因不连锁或重组率为 0.5）。
3. (a) 个体数最少的 $a\,+\,c$ 与 $+\,b\,+$ 是双交换；与亲本型相比，只有 $b$ 改变了组合，所以 $b$ 位于中间，顺序为 $a$–$b$–$c$。(b) $a$–$b$：$(46 + 44 + 5 + 5)/1000 = 0.10$，即 10 cM；$b$–$c$：$(96 + 94 + 5 + 5)/1000 = 0.20$，即 20 cM；两端之和为 30 cM。直接由 $a$ 与 $c$ 计算的重组率为 $(46 + 44 + 96 + 94)/1000 = 0.28$，比 30 cM 小，因为双交换使 $a$ 与 $c$ 恢复为亲本组合，未被计为重组。(c) 期望双交换数 $0.10 \times 0.20 \times 1000 = 20$，观察到 10，并发系数 $c = 0.5$，干涉 $I = 0.5$（代码验算）。
4. (a) $r = 0.05$、$0.2$、$0.4$ 分别对应 $d \approx 0.053$、$0.255$、$0.805$ 摩。(b) $d = 0.1$、$0.5$、$1.0$ 摩分别对应 $r \approx 0.091$、$0.316$、$0.432$（代码验算）。(c) 两个位点之间发生奇数次交换时才产生重组；距离很远时，奇数次与偶数次交换的概率趋于相等，重组率趋近 0.5。因此遗传图应当由紧密连锁的相邻位点逐段累加构建，而不能直接用远距离位点的重组率代替图距。
5. 半衰期 $t_{1/2} = \ln 0.5/\ln(1 - r)$：$r = 0.5$ 时为 1 代，$0.1$ 时约 6.6 代，$0.01$ 时约 69 代，$0.001$ 时约 693 代（代码验算）。有利突变在选择下迅速上升频率；与它紧密连锁的中性等位基因因为很少通过重组与之分离，在这段时间里与有利突变保持关联，于是一起上升频率，即遗传搭便车。
6. (a) 对许多酶而言，一个功能拷贝产生的酶量已足以维持正常表型，因此杂合子与显性纯合子表型相同，功能丧失的等位基因表现为隐性；在 SBEI 的例子中，杂合子的一个功能拷贝足以产生圆粒。(b) 同一对等位基因在不同性状、不同测量层次上可以表现出不同的显隐关系：例如在酶活性的层次上，杂合子的活性可能介于两种纯合子之间，而在种子形状上却表现为完全显性。因此显隐性取决于我们观察的表型，而不是等位基因的固有属性。(c) 株高等连续变异通常受多个位点与环境共同影响，难以得到简单的分离比；这正是生物统计学派研究的性状类型。Fisher（1918）证明连续变异可以由许多孟德尔因子共同解释，从而调和了两派（Day 003）。

</details>

---

## 关键术语

| 中文 | English | 释义 |
|---|---|---|
| 减数分裂 | meiosis | 使染色体数减半、产生单倍体配子的细胞分裂 |
| 交换 | crossing over | 减数分裂中同源染色体的非姐妹染色单体之间交换片段 |
| 分离律 | law of segregation | 每个配子只得到一对等位基因中的一个 |
| 自由组合律 | law of independent assortment | 不同染色体上的基因独立地分配到配子中 |
| 测交 | test cross | 与隐性纯合子杂交，以子代表型推断待测个体所产生配子的比例 |
| 卡方拟合优度检验 | chi-square goodness-of-fit test | 比较观察数与假设比例下期望数之间差异的统计检验 |
| 连锁 | linkage | 同一染色体上的基因倾向于一起遗传的现象 |
| 重组率 | recombination fraction | 测交子代中重组型所占的比例，介于 0 与 0.5 之间 |
| 遗传图 | genetic map | 依据重组率确定的基因在染色体上的顺序与相对距离 |
| 厘摩 | centimorgan (cM) | 遗传图距单位，1 cM 对应约 1% 的重组率 |
| 作图函数 | map function | 描述重组率与图距之间关系的函数 |
| 并发系数 | coefficient of coincidence | 观察到的双交换频率与独立假设下期望频率之比 |
| 干涉 | interference | 一个区段内的交换降低邻近区段交换概率的现象，$I = 1 - c$ |
| 等位基因 | allele | 同一基因的不同变体 |
| 基因型 | genotype | 个体在某些位点上的等位基因组成 |
| 表型 | phenotype | 个体可观察的性状 |
| 显性 | dominance | 杂合子的表型与某一纯合子相同时，该等位基因相对于另一等位基因为显性 |

---

## 参考文献

- Bhattacharyya, M. K., Smith, A. M., Ellis, T. H. N., Hedley, C., & Martin, C. (1990). The wrinkled-seed character of pea described by Mendel is caused by a transposon-like insertion in a gene encoding starch-branching enzyme. *Cell, 60*, 115–122. https://doi.org/10.1016/0092-8674(90)90721-P
- Feng, C., Chen, B., Hofer, J., Shi, Y., Jiang, M., Song, B., Cheng, H., Lu, L., Wang, L., Howard, A., Bendahmane, A., Fouchal, A., Zhao, X., Li, X., Sun, Y., Huang, Z., Wu, Z., Deng, X. W., Steuernagel, B., … Cheng, S. (2025). Genomic and genetic insights into Mendel's pea genes. *Nature, 642*(8069), 980–989. https://doi.org/10.1038/s41586-025-08891-6
- Fisher, R. A. (1918). The correlation between relatives on the supposition of Mendelian inheritance. *Transactions of the Royal Society of Edinburgh, 52*, 399–433. https://doi.org/10.1017/S0080456800012163
- Haldane, J. B. S. (1919). The combination of linkage values, and the calculation of distances between the loci of linked factors. *Journal of Genetics, 8*, 299–309.（DOI 未核实）
- Mendel, G. (1866). Versuche über Pflanzen-Hybriden. *Verhandlungen des naturforschenden Vereines in Brünn, 4*, 3–47. ［[MendelWeb 英译](https://cs.brown.edu/people/rblumber/MendelWeb/home.html)］
- Reid, J. B., & Ross, J. J. (2011). Mendel's genes: Toward a full molecular characterization. *Genetics, 189*(1), 3–10. https://doi.org/10.1534/genetics.111.132118 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC3176118)］
- Sturtevant, A. H. (1913). The linear arrangement of six sex-linked factors in *Drosophila*, as shown by their mode of association. *Journal of Experimental Zoology, 14*, 43–59.（DOI 未核实）

**网络资源**（访问日期 2026-11-17）

- Embryo Project Encyclopedia. (n.d.). *"The linear arrangement of six sex-linked factors in Drosophila, as shown by their mode of association" (1913), by Alfred Sturtevant*. Arizona State University. https://embryo.asu.edu/pages/linear-arrangement-six-sex-linked-factors-drosophila-shown-their-mode-association-1913-alfred
- OpenStax. (n.d.). *Biology 2e*, Chapter 12 Mendel's experiments and heredity. https://openstax.org/books/biology-2e/pages/12-introduction
- OpenStax. (n.d.). *Biology 2e*, §13.1 Chromosomal theory and genetic linkage. https://openstax.org/books/biology-2e/pages/13-1-chromosomal-theory-and-genetic-linkage
- Stearns, S. C. (2009). *EEB 122: Principles of evolution, ecology and behavior* [Video lectures]. Open Yale Courses. https://oyc.yale.edu/ecology-and-evolutionary-biology/eeb-122

---

**上一讲** [Day 014 · 第 2 周复盘：进化的证据与树状思维](../week02/day014-week02-review.md) ｜ **下一讲** [Day 016 · 突变 I：类型、速率与测定](day016-mutation-rates.md)
