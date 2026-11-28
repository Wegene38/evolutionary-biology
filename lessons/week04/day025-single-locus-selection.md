# Day 025 · 自然选择 I：单位点选择模型

> **部分** 第二部分 群体遗传学 ｜ **周次** 第 4 周 群体遗传学基础：HWE、连锁不平衡与选择模型 ｜ **发布日期** 2026-11-27 ｜ **建议用时** 约 110 分钟（讲义 45′ · 主读／主看 40′ · 练习 25′）
> **主读** Coop 讲义第 10 章 *One-Locus Models of Selection*；Felsenstein《Theoretical Evolutionary Genetics》第 II 部分 *Natural Selection*；Yale EEB 122 第 5 讲 *How Selection Changes the Genetic Composition of Population*
> **关键词** absolute fitness · relative fitness · selection coefficient · mean fitness · haploid selection · diploid selection · viability selection · genic selection · allele frequency trajectory · logistic dynamics

## 学习目标

完成本讲后，应能够：

1. 区分绝对适合度与相对适合度，并定义选择系数与平均适合度；
2. 推导单倍体模型中等位基因频率的变化及其 logistic 解；
3. 推导二倍体模型中的 $\Delta p$，并说明它与平均适合度梯度的关系；
4. 比较有利等位基因为显性、加性与隐性时的频率轨迹；
5. 用单位点模型由频率变化估计自然群体中的选择强度，并评价这种估计所依赖的假设。

---

## 1 从选择的逻辑到定量模型

Day 005 讨论了自然选择的逻辑：可遗传的变异、适合度的差异，以及由此导致的频率变化。Day 022–024 则建立了没有选择时的零模型。本讲把二者结合起来，问一个定量的问题：给定各基因型的适合度，等位基因频率每代改变多少？这类模型最早由 Haldane、Fisher 与 Wright 在 20 世纪 20–30 年代系统地建立起来（Day 003），至今仍是理解选择的基本工具。

本讲的模型沿用 Day 022 的大部分假设：群体无限大（因此没有漂变，Day 029）、没有突变与迁移、随机交配、世代不重叠，并假定各基因型的适合度恒定、与频率无关（频率依赖的情形见 Day 027）。Yale EEB 122 第 5 讲概括了这类模型的几个定性结论：适应性变化通常先慢、中间快、最后又变慢；无性的单倍体变化最快，有性的二倍体通常最慢；在大群体中，只有选择作用时等位基因频率才会改变（Stearns 2009）。

---

## 2 适合度

一个基因型的**绝对适合度**（absolute fitness）$W$ 是该基因型的个体平均对下一代贡献的后代数，通常可以分解为存活率与繁殖力的乘积。**相对适合度**（relative fitness）$w$ 则是绝对适合度除以某一参照基因型（通常是适合度最高者）的绝对适合度。等位基因频率的变化只取决于相对适合度：把所有基因型的绝对适合度乘以同一个常数，频率的变化不受影响（练习 1）。绝对适合度的平均值决定群体是在增长还是在缩小，这是另一个问题。

在相对适合度的基础上，**选择系数**（selection coefficient，Day 017）$s$ 度量某一基因型相对于参照基因型的适合度差异，例如 $w = 1 - s$ 表示适合度降低了 $s$，$w = 1 + s$ 表示提高了 $s$。群体的**平均适合度**（mean fitness）$\bar w$ 是各基因型相对适合度按频率加权的平均值。适合度是基因型在特定环境中的属性，同一基因型在不同环境中可以有不同的适合度（Day 020）。

选择可以作用于生命周期的不同阶段：合子到成体之间的存活（生存力选择）、成体的交配成功与繁殖力，以及配子阶段。本讲只讨论最简单的生存力选择；繁殖力有时取决于交配双方的基因型组合，不能简单归结为单个基因型的适合度；配子阶段的竞争与分离偏离则将在 Day 111 讨论，性选择将在第九部分讨论。

---

## 3 单倍体模型

先考虑最简单的情形：单倍体生物，两个等位基因 $A$ 与 $a$，相对适合度分别为 $w_A = 1 + s$ 与 $w_a = 1$。若当代 $A$ 的频率为 $p$，选择之后

$$p' = \frac{p(1 + s)}{p(1 + s) + q} = \frac{p(1 + s)}{1 + sp}, \qquad \Delta p = p' - p = \frac{s\,p\,q}{1 + sp}.$$

$\Delta p$ 正比于 $pq$：当 $A$ 很稀有或接近固定时，频率变化都很慢，中间最快。这一递推式有简单的解。两种等位基因频率之比每代乘以 $1 + s$，

$$\frac{p_t}{q_t} = \frac{p_0}{q_0}(1 + s)^{t}, \qquad \ln\frac{p_t}{q_t} = \ln\frac{p_0}{q_0} + t\ln(1 + s),$$

即频率的对数几率（logit）随时间线性增加，频率本身的轨迹是一条 S 形的 logistic 曲线。这一性质提供了由时间序列估计选择系数的简单方法：若在若干世代中测得等位基因频率，把 $\ln(p_t/q_t)$ 对 $t$ 作线性回归，斜率就是 $\ln(1 + s)$ 的估计；这一思路可以推广到实验进化等时间序列数据，但需要考虑取样误差与漂变造成的随机波动。由此，从 $p_0$ 增加到 $p_t$ 所需的代数为

$$t = \frac{\ln(p_t/q_t) - \ln(p_0/q_0)}{\ln(1 + s)} \approx \frac{1}{s}\ln\frac{p_t\,q_0}{q_t\,p_0}.$$

在连续时间的近似下，$dp/dt = spq$，其解为 $p(t) = p_0e^{st}/(1 - p_0 + p_0e^{st})$；当 $A$ 很稀有时，$q \approx 1$，频率近似按 $e^{st}$ 指数增长。例如 $s = 0.01$ 时，一个等位基因由 0.1% 增加到 99.9% 约需 1400 代：这在生态时间尺度上很慢，在地质时间尺度上却极快。Coop 讲义用抗药病毒的数据说明，单倍体模型可以描述快速的选择响应（Coop, n.d.）。

---

## 4 二倍体模型

### 4.1 Δp 的推导

对二倍体，设三种基因型的相对适合度为 $w_{AA}$、$w_{Aa}$、$w_{aa}$，选择作用于合子到成体之间的存活（**生存力选择**，viability selection）。随机交配使合子处于 Hardy–Weinberg 比例；选择之后，成体中 $A$ 的频率为

$$p' = \frac{p^{2}w_{AA} + pq\,w_{Aa}}{\bar w}, \qquad \bar w = p^{2}w_{AA} + 2pq\,w_{Aa} + q^{2}w_{aa},$$

于是

$$\Delta p = \frac{pq\left[p\left(w_{AA} - w_{Aa}\right) + q\left(w_{Aa} - w_{aa}\right)\right]}{\bar w}.$$

方括号中的量是 $A$ 等位基因相对于 $a$ 的平均"超额"适合度：一个 $A$ 拷贝以概率 $p$ 与另一个 $A$ 组成 $AA$，以概率 $q$ 与 $a$ 组成 $Aa$。这些成体随机交配产生下一代合子，基因型比例又回到 Hardy–Weinberg 比例（Day 022），于是同样的计算可以逐代重复。需要注意的是，选择之后、交配之前的成体一般不符合 Hardy–Weinberg 比例：例如杂合子适合度最高时，成体中的杂合子就多于由其等位基因频率预期的数目。因此，检验 Hardy–Weinberg 比例时，取样处于生命周期的哪个阶段会影响结论（Day 023）。

### 4.2 选择与平均适合度

上式还可以写成

$$\Delta p = \frac{pq}{2\bar w}\,\frac{d\bar w}{dp}.$$

这一形式说明，在适合度恒定的单位点模型中，等位基因频率总是朝着使平均适合度增加的方向变化，并在 $\bar w$ 对 $p$ 的极大值或边界处停止（练习 3）。这与 Wright 的适合度景观思想相联系（Day 065）；在频率依赖选择下，这一结论不再成立（Day 027）。

### 4.3 几种特殊情形

若 $w_{AA} = (1 + s)^{2}$、$w_{Aa} = 1 + s$、$w_{aa} = 1$，即每个 $A$ 拷贝使适合度乘以 $1 + s$（乘性或**基因选择**，genic selection），二倍体模型的递推式与单倍体模型完全相同（练习 3）。若 $w_{AA} = 1 + s$、$w_{Aa} = 1 + s/2$、$w_{aa} = 1$（加性），当 $s$ 很小时 $\Delta p \approx \frac{s}{2}pq$。当 $s$ 很小时，基因选择与加性选择几乎等价：$(1 + s)^{2} \approx 1 + 2s$，相当于加性模型中纯合子的优势为 $2s$、杂合子为 $s$。因此在弱选择下，"每个等位基因拷贝使适合度增加 $s$"是一个方便的近似。更一般的参数化 $w_{Aa} = 1 + hs$ 引入了显性度 $h$，它将在 Day 026 讨论。

---

## 5 频率轨迹

显隐性对轨迹的形状影响很大（练习 4）。若有利等位基因为显性，它稀有时几乎都以杂合子形式存在，而杂合子已经表现出全部优势，因此起初增加很快；但接近固定时，剩余的不利等位基因几乎都隐藏在表型与 $AA$ 相同的杂合子中，选择难以清除它们，最后阶段极其缓慢。若有利等位基因为隐性，情形恰好相反：稀有时它几乎只存在于不受选择青睐的杂合子中，起初增加极慢，一旦频率较高则迅速固定。加性的情形介于二者之间，轨迹接近对称的 logistic 曲线。

这些差异有重要的进化含义。新出现的有利突变总是从很低的频率开始，因此显性的有利突变比隐性的更容易被选择"看到"；有害的隐性等位基因则可以长期隐藏在杂合子中（Day 022）。这些问题将在 Day 026 讨论。选择的时间尺度也可以由第 3 节的公式估计。在基因选择下，一个以单拷贝出现（$p_0 = 1/2N$）的有利等位基因若不被漂变丢失，增加到 $1 - 1/2N$ 约需 $2\ln(2N)/s$ 代：$N = 10^{4}$、$s = 0.01$ 时约 2000 代，$s = 0.1$ 时约 200 代。这一时间只随群体大小的对数增长，因此即使在很大的群体中，选择也能在相对短的时间内完成一次替代。

还需要注意，本讲的模型是确定性的：一个刚出现的有利突变在频率极低时首先要逃过漂变的随机丢失，才能进入这里描述的轨迹（Day 032）。

---

## 6 案例研究：Haldane（1924）与桦尺蛾

**问题** Day 011 介绍了英国工业区桦尺蛾（*Biston betularia*）黑化型频率的上升。要在几十代内造成这样的变化，选择需要多强？

**方法** Haldane 在 1924 年发表的《自然选择与人工选择的数学理论》第一部分中，用桦尺蛾黑化型频率的上升来说明自然群体中可以存在很强的选择（Haldane 1924；Cook & Turner 2020）。据 Cook 与 Turner（2020）的考察，Haldane 依据当时的文献，设黑化型在 1848 年的频率约为 1%，大约 50 代之后上升到 99%，并用单位点选择模型计算所需的选择强度。

**结果** Cook 与 Saccheri（2013）指出，Haldane 的一种计算表明黑化型的优势可高达约 30%，其所需的选择强度远大于当时人们通常认为进化变化所涉及的水平。用本讲的模型可以重现这一量级：设黑化等位基因为显性，若黑化型表型频率在 50 代内由 1% 上升到 99%，黑化型的相对适合度约为浅色型的 1.43 倍，即浅色型的适合度只有黑化型的约 70%（练习 5）。

**意义** 这一计算是由频率变化反推选择强度的最早尝试之一，它表明自然选择可以很强，强到可以在人类的观察时间内改变一个群体的组成。它也依赖若干假设：起始频率（不同文献对 1848 年的频率记载不一）、每年一代、选择强度恒定，以及不存在迁移；后来的捕食实验与致因突变的鉴定，从其他方向检验了这一解释（Day 011）。Cook 与 Turner（2020）还专门考察了 Haldane 这一计算的内容、后人对它的接受，以及一些被归于他的说法的来源：引用经典结论时，应当回到原文。

---

## 今日学习材料（均可免费获取）

| 类型 | 材料 | 说明 |
|---|---|---|
| 必读 | Coop，*Population and Quantitative Genetics*：[第 10 章 One-Locus Models of Selection](https://bio.libretexts.org/Bookshelves/Genetics/Population_and_Quantitative_Genetics_(Coop)/10%3A_One-Locus_Models_of_Selection) | 单倍体与二倍体选择模型，约 25 分钟 |
| 必读 | Felsenstein，[*Theoretical Evolutionary Genetics*](https://felsenst.github.io/pgbook/pgbook.html) | 第 II 部分 Natural Selection 中无性与二倍体选择的各节，约 20 分钟 |
| 必看 | [Yale EEB 122](https://oyc.yale.edu/ecology-and-evolutionary-biology/eeb-122) 第 5 讲 *How Selection Changes the Genetic Composition of Population* | 约 50 分钟 |
| 精读 | Cook & Turner（2020）：[白玫瑰大学联盟存档](https://eprints.whiterose.ac.uk/160446/) | Haldane（1924）桦尺蛾计算的内容与流传 |
| 选读 | Cook & Saccheri（2013）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC3668657) | 桦尺蛾工业黑化作为自然选择案例的演变 |

---

## 思考与练习

1. **（计算）** 三种基因型的存活率分别为 $AA$ 0.9、$Aa$ 0.9、$aa$ 0.6，存活个体的平均后代数分别为 4、4、5（本题数据为假设）。(a) 计算各基因型的绝对适合度、相对适合度与 $aa$ 的选择系数。(b) 若 $p = 0.7$，计算平均相对适合度与下一代的 $p$。(c) 用绝对适合度直接计算下一代的 $p$，结果是否相同？为什么？
2. **（计算）** 单倍体模型中 $s = 0.05$，$p_0 = 0.01$。(a) 用递推式逐代计算，$A$ 的频率首次超过 0.5 与 0.99 各需多少代？(b) 用 logistic 解计算，并与 (a) 比较。(c) 用 $t \approx \frac{1}{s}\ln\frac{p_t q_0}{q_t p_0}$ 近似，误差有多大？
3. **（推导）** (a) 由第 4.1 节的 $p'$ 推导 $\Delta p$。(b) 设 $w_{AA} = 1$、$w_{Aa} = 0.9$、$w_{aa} = 0.7$，分别在 $p = 0.3$ 与 0.6 时用三种方式计算 $\Delta p$：第 4.1 节的公式、$p' - p$ 的直接计算，以及 $\frac{pq}{2\bar w}\frac{d\bar w}{dp}$。(c) 证明基因选择下二倍体模型与单倍体模型的递推式相同。
4. **（计算）** 设 $s = 0.1$，比较有利等位基因 $A$ 为显性（$1 + s$, $1 + s$, $1$）、加性（$1 + s$, $1 + s/2$, $1$）与隐性（$1 + s$, $1$, $1$）三种情形，从 $p_0 = 0.01$ 出发，分别计算达到 0.5 与 0.99 所需的代数，以及由 0.5 到 0.99 所需的代数。解释结果。
5. **（计算）** 按第 6 节的设定，黑化等位基因为显性，黑化型表型频率在 50 代内由 1% 上升到 99%，并设每年一代、选择强度恒定。(a) 起始与终止时黑化等位基因的频率各是多少？(b) 求黑化型相对于浅色型的适合度 $1 + s$，以及浅色型相对于黑化型的适合度。(c) 若起始频率为 2%，结果如何变化？这说明了什么？
6. **（概念）** 判断并纠正：(a)"只要知道各基因型的绝对适合度，就必须用绝对适合度才能算出频率变化。"(b)"在任何选择模型中，等位基因频率都朝着平均适合度增加的方向变化。"(c)"有利等位基因的频率随时间线性增加。"(d)"$s = 0.01$ 的选择太弱，不可能造成明显的进化。"

<details>
<summary>答案要点</summary>

1. (a) 绝对适合度 $W$ 为 3.6、3.6、3.0；相对适合度 $w$ 为 1、1、约 0.833；$aa$ 的选择系数 $s \approx 0.167$。(b) $\bar w = 0.49 + 0.42 + 0.09 \times 0.833 = 0.985$，$p' = (0.49 + 0.21)/0.985 \approx 0.7107$。(c) 用绝对适合度计算得到相同的 $p' \approx 0.7107$（代码验算），因为分子分母中的公共因子相互抵消，频率变化只取决于相对适合度；绝对适合度的平均值 3.546 则决定群体大小的变化。
2. (a) 分别需 95 代与 189 代。(b) logistic 解给出约 94.2 代与 188.4 代，即第 95 与 189 代首次超过阈值，与逐代计算一致。(c) 近似给出约 91.9 代与 183.8 代，偏小约 2.4%，因为 $\ln(1 + s) < s$（代码验算）。
3. (a) $\Delta p = p' - p = [p^{2}w_{AA} + pqw_{Aa} - p\bar w]/\bar w$，展开 $\bar w$ 并利用 $p + q = 1$ 整理即得。(b) $p = 0.3$ 时三种方式都给出 $\Delta p \approx 0.0440$，$p = 0.6$ 时都给出约 0.0372（代码验算）。(c) 代入 $w_{AA} = (1 + s)^{2}$、$w_{Aa} = 1 + s$、$w_{aa} = 1$：分子为 $p(1 + s)[p(1 + s) + q]$，分母为 $[p(1 + s) + q]^{2}$，约去公因子即得 $p' = p(1 + s)/(1 + sp)$，与单倍体模型相同。
4. 到 0.5：显性 59 代，加性 95 代，隐性 1031 代；到 0.99：显性 1184 代，加性 193 代，隐性 1089 代；由 0.5 到 0.99：显性 1125 代，加性 99 代，隐性 59 代（代码验算）。显性有利等位基因稀有时增加最快，但接近固定时极慢，因为剩余的 $a$ 几乎都在不受选择的杂合子中；隐性有利等位基因正好相反；加性介于二者之间且大致对称。
5. (a) 由隐性浅色型的频率 $q^{2}$ 推算：起始时 $q^{2} = 0.99$，黑化等位基因频率约 0.0050；终止时 $q^{2} = 0.01$，约为 0.90。(b) $1 + s \approx 1.43$；浅色型相对于黑化型的适合度约 0.70，即约低 30%（代码验算），与 Cook 与 Saccheri（2013）所述 Haldane 计算的量级一致。(c) 起始频率为 2% 时，$1 + s \approx 1.40$，浅色型相对适合度约 0.71。结论对起始频率并不十分敏感，但它依赖于每年一代、选择恒定与无迁移等假设，而这些假设本身需要独立的证据。
6. (a) 错误。相对适合度足以决定频率变化，绝对适合度中的公共因子会被抵消。(b) 错误。这一结论只适用于适合度恒定的单位点模型；在频率依赖选择下，频率可以朝平均适合度下降的方向变化（Day 027）。(c) 错误。轨迹是 S 形的：$\Delta p \propto pq$，在频率接近 0 或 1 时变化很慢。(d) 错误。$s = 0.01$ 时，一个有利等位基因从 0.1% 增加到 99.9% 约需 1400 代，在进化时间尺度上非常快。

</details>

---

## 关键术语

| 中文 | English | 释义 |
|---|---|---|
| 绝对适合度 | absolute fitness | 某一基因型的个体平均对下一代贡献的后代数，可分解为存活率与繁殖力之积 |
| 相对适合度 | relative fitness | 某一基因型的绝对适合度除以参照基因型的绝对适合度 |
| 平均适合度 | mean fitness | 群体中各基因型相对适合度按频率加权的平均值 |
| 生存力选择 | viability selection | 作用于合子到成体之间存活率差异的选择 |
| 基因选择 | genic selection | 每个等位基因拷贝对适合度有独立的乘性效应的选择方式，二倍体模型此时与单倍体模型等价 |

---

## 参考文献

- Cook, L. M., & Saccheri, I. J. (2013). The peppered moth and industrial melanism: Evolution of a natural selection case study. *Heredity, 110*(3), 207–212. https://doi.org/10.1038/hdy.2012.92 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC3668657)］
- Cook, L. M., & Turner, J. R. G. (2020). Fifty per cent and all that: What Haldane actually said. *Biological Journal of the Linnean Society, 129*(3), 765–771. https://doi.org/10.1093/biolinnean/blz169 ［[白玫瑰大学联盟存档](https://eprints.whiterose.ac.uk/160446/)］
- Haldane, J. B. S. (1924). A mathematical theory of natural and artificial selection. Part I. *Transactions of the Cambridge Philosophical Society, 23*, 19–41.（DOI 未核实）

**网络资源**（访问日期 2026-11-27）

- Coop, G. (n.d.). *Population and quantitative genetics*, Chapter 10 One-locus models of selection. LibreTexts. https://bio.libretexts.org/Bookshelves/Genetics/Population_and_Quantitative_Genetics_(Coop)/10%3A_One-Locus_Models_of_Selection
- Felsenstein, J. (n.d.). *Theoretical evolutionary genetics*. https://felsenst.github.io/pgbook/pgbook.html
- Stearns, S. C. (2009). *EEB 122: Principles of evolution, ecology and behavior* [Video lectures]. Open Yale Courses. https://oyc.yale.edu/ecology-and-evolutionary-biology/eeb-122

---

**上一讲** [Day 024 · 连锁不平衡](day024-linkage-disequilibrium.md) ｜ **下一讲** [Day 026 · 自然选择 II：显性、超显性与平衡多态](day026-dominance-overdominance.md)
