# Day 004 · 进化思想史 III：中性理论与"扩展综合"之争

> **部分** 第一部分 概念基础与证据 ｜ **周次** 第 1 周 导论 ｜ **发布日期** 2026-11-06 ｜ **建议用时** 约 80 分钟（讲义 35′ · 主读 35′ · 练习 10′）
> **主读** Kimura（1968）与 King & Jukes（1969）原文；*Understanding Evolution*：Evolution 101 进化机制部分
> **关键词** protein polymorphism · molecular clock · neutral theory · nearly neutral theory · neutralist–selectionist debate · extended evolutionary synthesis · niche construction · developmental bias

## 学习目标

完成本讲后，应能够：

1. 说明 20 世纪 60 年代的分子数据（蛋白质序列与电泳多态性）如何给现代综合提出新问题；
2. 推导"中性替代速率等于突变率"，并说明中性理论对分子钟、功能约束与多态性的预测；
3. 概述中性论与选择论之争的主要阶段，以及当代的两种代表性立场；
4. 说明扩展进化综合（EES）的主要主题与因果主张，以及反对者的主要论点；
5. 区分 EES 之争中的经验问题（各过程的相对重要性）与概念问题（是否需要新的理论框架）。

---

## 1 分子数据进入进化生物学

### 1.1 分子钟

Zuckerkandl 与 Pauling（1965）比较了多个物种的珠蛋白氨基酸序列，发现两物种间的序列差异大致随分歧时间线性增加，于是提出可能存在一个"分子进化钟"（molecular evolutionary clock）。值得注意的是，两位作者当时认为分子钟与自然选择是相容的；分子钟后来才成为中性理论的核心论据之一。

### 1.2 自然群体中有多少遗传变异？

现代综合内部长期存在一个分歧（Lewontin 1974）：

- **经典学派**（classical school，以 Muller 为代表）认为，大多数位点上群体基本固定为一个"野生型"等位基因，变异稀少且多为有害；
- **平衡学派**（balance school，以 Dobzhansky 为代表）认为，许多位点保持多态，并由杂合子优势等平衡选择维持。

在 DNA 测序出现之前，这个问题无法直接回答。1966 年，蛋白质凝胶电泳首次提供了对自然群体遗传变异的近乎无偏的估计：Lewontin 与 Hubby（1966）发现拟暗果蝇（*Drosophila pseudoobscura*）约 39% 的被检测位点存在变异；Harris（1966）在人类酶蛋白中也发现了大量多态（Charlesworth et al. 2016）。

这一结果对两派都构成难题：经典学派无法解释如此多的变异；而若这些变异都靠杂合子优势维持，群体将承受难以置信的遗传负荷（Lewontin 1974）。

---

## 2 中性理论

### 2.1 Kimura（1968）与 King & Jukes（1969）

Kimura（1968）根据蛋白质的氨基酸替代速率推算，哺乳类群体的整个基因组大约每两年就发生一次核苷酸替代。这远远高于 Haldane 根据"选择的代价"（Day 034）估算的上限（约每 300 代一次）。如果每次替代都由正选择驱动，群体将无法承受相应的代价；因此，**大多数分子替代必定是选择中性的**，由遗传漂变固定。

次年，King 与 Jukes（1969）以《非达尔文进化》为题发表了类似观点，其论据还包括非编码重复 DNA 的存在与"C 值悖论"等。

### 2.2 核心推导：中性替代速率等于突变率

考虑一个大小为 $N$ 的二倍体群体（理想群体，$N_e = N$），每个位点每代的中性突变率为 $\mu_0$：

- 每代新出现的中性突变数为 $2N\mu_0$；
- 每个新的中性突变最终被固定的概率等于其初始频率 $1/(2N)$（Day 030）；

因此中性替代速率为

$$k_0 = 2N\mu_0 \times \frac{1}{2N} = \mu_0 .$$

替代速率与群体大小无关，只取决于突变率。

### 2.3 中性理论的主要预测

1. **分子钟**：若突变率大致恒定，中性替代以近似恒定的速率累积。
2. **功能约束**：设新突变中中性的比例为 $f_0$，则 $k = f_0\,\mu$。功能越重要的区域，有害突变比例越高、$f_0$ 越小，进化越慢。因此同义位点通常比非同义位点进化快，功能约束很弱的蛋白质（如纤维蛋白肽）比高度保守的蛋白质（如组蛋白）进化快（Kimura 1983）。
3. **多态与替代是同一过程的两个阶段**：群体内的中性多态，就是正在漂变、最终可能被固定或丢失的突变；群体内多样性由突变与漂变的平衡决定（$\theta = 4N_e\mu$，Day 033）。

需要澄清一个常见误解：中性理论讨论的是**分子水平**的变异与替代，它并不否认适应性的表型进化由自然选择造成；它也承认大量新突变是有害的，会被净化选择清除（Kimura 1983）。

### 2.4 近中性理论

Ohta（1973）扩展了中性理论：许多突变是**轻微有害**的，其命运取决于 $N_e s$ 的大小。在小群体中，漂变的作用相对较强，轻微有害突变更容易被固定。由此可以预测，有效群体较小的谱系会积累更多轻微有害的替代（Day 051）。

### 2.5 中性论–选择论之争

| 阶段 | 代表性工作 | 要点 |
|---|---|---|
| 蛋白质时代（1960–70 年代） | Kimura 1968；King & Jukes 1969；Ohta 1973 | 由替代速率与多态性水平论证中性 |
| DNA 序列时代（1980–90 年代） | Kreitman（1983）测定了 11 个 *Adh* 等位基因的序列：43 处变异中只有 1 处改变氨基酸；Gillespie（1991）提出选择论的替代模型 | 多态主要出现在同义位点，与蛋白质水平的净化选择一致；选择检验方法发展（Day 071–075） |
| 基因组时代（2000 年至今） | Kern & Hahn（2018）与 Jensen et al.（2019）的争论 | 前者认为基因组数据已可否定中性理论的普遍性，并强调连锁选择的作用；后者认为前者对中性理论的定义过窄，连锁选择反而凸显了漂变的基础作用 |

今天的多数研究者至少在一点上一致：中性理论是检验选择的**零模型**（null model），各种选择检验都以它为基准（第 11 周）。争论的焦点在于：适应性替代在基因组中占多大比例，以及连锁选择在多大程度上塑造了遗传多样性（第 8 周）。

---

## 3 1970 年代以来的其他理论争论

现代综合之后，进化生物学内部出现了多个方向的修正与争论，本课程将在后续各周展开：

| 争论 | 核心问题 | 课程位置 |
|---|---|---|
| 对适应主义的批评 | 性状是否都应被解释为适应（Gould & Lewontin 1979） | Day 005 |
| 间断平衡 | 化石记录中的停滞与快速变化如何解释 | Day 135 |
| 选择的层次 | 选择作用于基因、个体还是群体 | Day 155–156 |
| 进化发育生物学 | 发育如何影响变异的产生与形态进化 | 第 21 周 |
| 基因组结构的非适应解释 | 基因组大小与复杂性是否主要由漂变与突变决定 | Day 104 |

---

## 4 扩展进化综合之争

### 4.1 2014 年的《自然》辩论

2014 年，《自然》刊出一组正反双方的评论（Laland et al. 2014）。正方（Laland、Uller、Jablonka 等）主张进化理论需要"重新思考"；反方（Wray、Hoekstra、Futuyma、Lenski 等）认为正方所强调的现象已在现有理论中得到研究，并认为正方描述的"标准进化理论"是一种过于僵化的漫画式概括。

### 4.2 EES 的主张

Laland 等（2015）系统阐述了**扩展进化综合**（extended evolutionary synthesis, EES）。它涉及四个研究领域：进化发育生物学（发育偏好）、发育可塑性、包容性遗传（表观遗传、生态与文化遗传），以及生态位构建。EES 保留进化理论的基本原理，但强调**建构性发育**（constructive development）与**互惠因果**（reciprocal causation，Day 001）：发育偏好、包容性遗传与生态位构建，和自然选择一起决定进化的方向与速率。

**表 1 标准进化理论与 EES 在侧重点上的差异（据 Laland et al. 2015 概括）**

| 方面 | 标准进化理论的典型侧重 | EES 的侧重 |
|---|---|---|
| 变异的产生 | 遗传变异相对于选择没有方向 | 发育偏好使表型变异的产生具有结构与方向 |
| 遗传 | 以基因传递为主 | 包容性遗传：表观遗传、生态与文化等多种途径 |
| 选择的来源 | 环境提出"问题"，生物适应环境 | 生物通过生态位构建改变环境，从而改变自身所受的选择 |
| 因果结构 | 近因与终极因分离 | 近因过程可以反馈影响选择（互惠因果） |

### 4.3 如何评价

反方并不否认发育、可塑性或生态位构建的存在，而是认为这些过程已经可以纳入现有理论；Futuyma（2017）也对这一争论作了系统评述。评价 EES 时，区分两类问题会很有帮助：

- **经验问题**：这些过程在自然界中的作用有多大？例如，跨代表观遗传的状态能稳定维持多少代？发育偏好在多大程度上决定了适应的方向？
- **概念问题**：即使这些过程很重要，它们是否要求改变进化解释的基本结构，还是只是在现有框架中增加新的研究对象？

本课程将在 Day 146 与 Day 177 结合具体证据回到这一问题。

---

## 今日学习材料（均可免费获取）

| 类型 | 材料 | 说明 |
|---|---|---|
| 必读 | [*Understanding Evolution*：Evolution 101](https://evolution.berkeley.edu/evolution-101/) | 进化机制部分，重点读遗传漂变的内容，约 15 分钟 |
| 精读 | Kimura（1968）：[Caltech 分子进化文献档案](https://authors.library.caltech.edu/5456/1/hrst.mit.edu/hrs/evolution/public/papers/kimura1968/kimura1968.html) | 三页短文，约 20 分钟 |
| 精读 | King & Jukes（1969）：[Caltech 分子进化文献档案](https://authors.library.caltech.edu/5456/1/hrst.mit.edu/hrs/evolution/public/papers/kingjukes1969/kingjukes1969.html) | 读引言与结论 |
| 选读 | Charlesworth et al.（2016）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC4981259) | 对 1966 年电泳研究的回顾 |
| 选读 | Kern & Hahn（2018）：[作者主页 PDF](https://hahnlab.sitehost.iu.edu/Publications/KernHahn2018.pdf)；Jensen et al.（2019）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC6496948) | 对照阅读当代争论 |
| 选读 | Laland et al.（2015）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC4632619)；Futuyma（2017）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC5566807) | 对照阅读 EES 之争 |
| 选看 | [Yale EEB 122](https://oyc.yale.edu/ecology-and-evolutionary-biology/eeb-122) 第 4 讲 *Neutral Evolution: Genetic Drift* | 约 50 分钟 |

---

## 思考与练习

1. **（推导与计算）** (a) 按 §2.2 推导 $k_0 = \mu_0$，并写出这一推导依赖的假设。(b) 对有利突变，当 $4Ns \gg 1$ 时其固定概率约为 $2s$，因此适应性替代速率约为 $k_a \approx 2N\mu_a \cdot 2s = 4N\mu_a s$。设每位点每代中性突变率 $\mu_0 = 10^{-8}$，有利突变率 $\mu_a = 10^{-11}$，$s = 0.001$。分别计算 $N = 10^4$ 与 $N = 10^6$ 时，适应性替代在全部替代中所占的比例。(c) 这一结果对比较不同物种中"适应性替代比例"（Day 073）有什么启示？
2. **（计算）** 两个物种某基因同义位点的观测差异比例 $p = 0.06$。设同义位点的替代速率 $r = 10^{-9}$ /位点/年，并用 Jukes–Cantor 公式 $d = -\tfrac34 \ln\!\left(1 - \tfrac43 p\right)$ 校正多重替代。估计两物种的分歧时间；不校正时结果是多少？（提示：两条谱系各自独立积累替代。）
3. **（计算）** 在中性无限等位基因模型下，平衡时的期望杂合度为 $H = \theta/(1+\theta)$，$\theta = 4N_e\mu$。设每位点（以电泳可检测的变异计）$\mu = 10^{-7}$，分别计算 $N_e = 10^4$、$10^6$、$10^8$ 时的 $H$。如果中性理论成立且群体处于平衡，不同物种的杂合度应如何随群体大小变化？（这与 Day 054 的"Lewontin 悖论"有关。）
4. **（概念）** 为什么 1966 年的电泳结果同时给经典学派和平衡学派带来了困难？Kimura（1968）基于"选择的代价"的论证为争论增加了什么？
5. **（文献评论）** 对照阅读 Laland et al.（2015）与 Futuyma（2017）。从 EES 的四个领域中选一个，提出一个可检验的经验预测，使其结果能够帮助判断"需要扩展的框架"还是"现有理论已经足够"。

<details>
<summary>答案要点</summary>

1. (a) 假设：理想的随机交配群体；突变严格中性；每个新突变出现时只有一个拷贝（频率为 $1/2N$）；突变率不随时间改变。(b) 中性替代速率在两种情形下都是 $10^{-8}$；适应性替代速率在 $N = 10^4$ 时为 $4 \times 10^{-10}$，占全部替代的约 3.8%；在 $N = 10^6$ 时为 $4 \times 10^{-8}$，约占 80%（此时 $4Ns = 4000 \gg 1$；Kimura 的精确固定概率为 0.001998，与 $2s = 0.002$ 几乎相同）。(c) 适应性替代速率随群体大小增加，中性替代速率不随之变化，因此有效群体大的物种预期有更高的适应性替代比例。比较物种时需要考虑 $N_e$ 的差异。
2. $d = -0.75\ln(1 - 0.08) \approx 0.0625$；分歧时间 $T = d/(2r) \approx 31.3$ 百万年；不校正时 $T = p/(2r) = 30.0$ 百万年。差异较小，是因为 $p$ 较小、多重替代不多；差异比例越大，校正越重要（Day 093）。
3. $N_e = 10^4$：$\theta = 0.004$，$H \approx 0.0040$；$N_e = 10^6$：$\theta = 0.4$，$H \approx 0.286$；$N_e = 10^8$：$\theta = 40$，$H \approx 0.976$。在中性平衡下，杂合度应随群体大小在几个数量级的范围内变化；而实际观察到的物种间多样性差异远小于群体大小的差异，这正是 Lewontin 悖论（Day 054）。
4. 经典学派预测变异稀少，与观察不符；平衡学派若用杂合子优势解释所有多态，会导致难以承受的分离负荷。Kimura 的论证指出，观察到的分子替代速率过高，用正选择解释同样会带来难以承受的代价，从而为"大部分分子变异与替代是中性的"提供了独立论据。
5. 示例（发育偏好）：如果发育偏好显著影响适应方向，那么在多个独立谱系中，适应性进化应沿着突变或发育产生变异最多的方向（例如"遗传最小阻力线"，Day 061）重复出现，其程度超过仅由选择环境所能解释的程度；可以通过比较突变方差–协方差矩阵（M 矩阵）与长期分化方向来检验。

</details>

---

## 关键术语

| 中文 | English | 释义 |
|---|---|---|
| 分子钟 | molecular clock | 分子序列的替代以近似恒定速率累积，因而可用于估计分歧时间的假说 |
| 经典学派与平衡学派 | classical and balance schools | 关于自然群体中遗传变异多寡及其维持机制的两种立场 |
| 中性理论 | neutral theory of molecular evolution | 认为分子水平的大多数替代与多态源于选择中性突变的遗传漂变的理论 |
| 中性突变 | neutral mutation | 对适合度没有影响、或影响小到其命运主要由漂变决定的突变 |
| 替代速率 | substitution rate | 单位时间内在谱系中被固定的突变数 |
| 功能约束 | functional constraint | 因功能重要而使大多数突变有害、被净化选择清除，从而减慢序列进化的作用 |
| 近中性理论 | nearly neutral theory | Ohta 的扩展：轻微有害突变的命运取决于 $N_e s$，在小群体中更容易被固定 |
| 零模型 | null model | 用于检验某一过程（如选择）是否存在的基准模型 |
| 扩展进化综合 | extended evolutionary synthesis (EES) | 强调发育偏好、可塑性、包容性遗传与生态位构建作用的理论主张 |
| 生态位构建 | niche construction | 生物改变自身或其他生物所处的环境，从而改变选择的过程 |
| 发育偏好 | developmental bias | 发育系统使某些表型变异比另一些更容易产生的倾向 |
| 包容性遗传 | inclusive inheritance | 除基因之外，经由表观遗传、生态与文化等途径的跨代传递 |

---

## 参考文献

- Charlesworth, B., Charlesworth, D., Coyne, J. A., & Langley, C. H. (2016). Hubby and Lewontin on protein variation in natural populations: When molecular genetics came to the rescue of population genetics. *Genetics, 203*(4), 1497–1503. https://doi.org/10.1534/genetics.115.185975 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC4981259)］
- Futuyma, D. J. (2017). Evolutionary biology today and the call for an extended synthesis. *Interface Focus, 7*(5), 20160145. https://doi.org/10.1098/rsfs.2016.0145 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC5566807)］
- Gillespie, J. H. (1991). *The causes of molecular evolution*. Oxford University Press.
- Gould, S. J., & Lewontin, R. C. (1979). The spandrels of San Marco and the Panglossian paradigm: A critique of the adaptationist programme. *Proceedings of the Royal Society of London. Series B, Biological Sciences, 205*(1161), 581–598.（DOI 未核实）
- Harris, H. (1966). Enzyme polymorphisms in man. *Proceedings of the Royal Society of London. Series B, Biological Sciences, 164*(995), 298–310. https://doi.org/10.1098/rspb.1966.0032
- Jensen, J. D., Payseur, B. A., Stephan, W., Aquadro, C. F., Lynch, M., Charlesworth, D., & Charlesworth, B. (2019). The importance of the Neutral Theory in 1968 and 50 years on: A response to Kern and Hahn 2018. *Evolution, 73*(1), 111–114. https://doi.org/10.1111/evo.13650 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC6496948)］
- Kern, A. D., & Hahn, M. W. (2018). The neutral theory in light of natural selection. *Molecular Biology and Evolution, 35*(6), 1366–1371. https://doi.org/10.1093/molbev/msy092 ［[作者主页 PDF](https://hahnlab.sitehost.iu.edu/Publications/KernHahn2018.pdf)］
- Kimura, M. (1968). Evolutionary rate at the molecular level. *Nature, 217*(5129), 624–626. https://doi.org/10.1038/217624a0
- Kimura, M. (1983). *The neutral theory of molecular evolution*. Cambridge University Press.
- King, J. L., & Jukes, T. H. (1969). Non-Darwinian evolution. *Science, 164*(3881), 788–798. https://doi.org/10.1126/science.164.3881.788
- Kreitman, M. (1983). Nucleotide polymorphism at the alcohol dehydrogenase locus of *Drosophila melanogaster*. *Nature, 304*(5925), 412–417. https://doi.org/10.1038/304412a0
- Laland, K., Uller, T., Feldman, M., Sterelny, K., Müller, G. B., Moczek, A., Jablonka, E., Odling-Smee, J., Wray, G. A., Hoekstra, H. E., Futuyma, D. J., Lenski, R. E., Mackay, T. F. C., Schluter, D., & Strassmann, J. E. (2014). Does evolutionary theory need a rethink? *Nature, 514*(7521), 161–164. https://doi.org/10.1038/514161a
- Laland, K. N., Uller, T., Feldman, M. W., Sterelny, K., Müller, G. B., Moczek, A., Jablonka, E., & Odling-Smee, J. (2015). The extended evolutionary synthesis: Its structure, assumptions and predictions. *Proceedings of the Royal Society B: Biological Sciences, 282*(1813), 20151019. https://doi.org/10.1098/rspb.2015.1019 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC4632619)］
- Lewontin, R. C. (1974). *The genetic basis of evolutionary change*. Columbia University Press.
- Lewontin, R. C., & Hubby, J. L. (1966). A molecular approach to the study of genic heterozygosity in natural populations. II. Amount of variation and degree of heterozygosity in natural populations of *Drosophila pseudoobscura*. *Genetics, 54*(2), 595–609. https://doi.org/10.1093/genetics/54.2.595
- Ohta, T. (1973). Slightly deleterious mutant substitutions in evolution. *Nature, 246*(5428), 96–98. https://doi.org/10.1038/246096a0
- Zuckerkandl, E., & Pauling, L. (1965). Evolutionary divergence and convergence in proteins. In V. Bryson & H. J. Vogel (Eds.), *Evolving genes and proteins* (pp. 97–166). Academic Press.

**网络资源**（访问日期 2026-11-06）

- University of California Museum of Paleontology. *Understanding Evolution: Evolution 101*. https://evolution.berkeley.edu/evolution-101/

---

**上一讲** [Day 003 · 进化思想史 II：孟德尔遗传与现代综合](day003-mendel-modern-synthesis.md) ｜ **下一讲** Day 005 · 自然选择的逻辑与适应主义
