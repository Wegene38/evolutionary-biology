# Day 020 · 从基因型到表型：上位性、多效性与可塑性

> **部分** 第一部分 概念基础与证据 ｜ **周次** 第 3 周 遗传变异的来源 ｜ **发布日期** 2026-11-22 ｜ **建议用时** 约 110 分钟（讲义 45′ · 主读／主看 40′ · 练习 25′）
> **主读** Yale EEB 122 第 8 讲 *The Expression of Variation: Reaction Norms*；OpenStax *Biology 2e* 第 12 章
> **关键词** genotype–phenotype map · dominance · recessiveness · incomplete dominance · codominance · epistasis · functional epistasis · statistical epistasis · pleiotropy · reaction norm · phenotypic plasticity · genotype-by-environment interaction (G×E) · cross-environment genetic correlation

## 学习目标

完成本讲后，应能够：

1. 解释基因型–表型图谱的概念，以及它为什么决定了哪些遗传差异能够被选择"看到"；
2. 区分完全显性、不完全显性与共显性，并用代谢通量理论解释功能缺失突变为何常为隐性；
3. 区分上位性的几种含义，推导双因子杂交中的上位比例，并说明上位性对度量尺度的依赖；
4. 定义多效性，并说明这一术语在不同研究问题中的不同含义；
5. 用反应规范描述表型可塑性与基因型 × 环境互作，说明互作对方差分解与可塑性进化的含义。

---

## 1 基因型–表型图谱

本周的目标之一是区分基因型变异与表型变异。Day 015–019 讨论了遗传变异如何产生、如何被测量；本讲讨论这些变异如何转化为表型。选择作用于表型，而遗传的是基因型，二者之间的对应关系称为**基因型–表型图谱**（genotype–phenotype map, GP map）。

这一图谱有三个对进化至关重要的特点。第一，它通常是多对一的：许多不同的基因型可以产生相同的表型，此时它们之间的差异对选择是"不可见"的。第二，它通常是非线性的：一个等位基因的效应可能取决于同一位点上的另一个等位基因（显性），也可能取决于其他位点上的基因型（上位性）。第三，它依赖于环境：同一基因型在不同环境中可以产生不同的表型（可塑性）。在最简单的线性模型中，可以把个体的表型值写成

$$P = G + E + (G \times E),$$

其中 $P$ 为表型值，$G$ 为基因型的贡献，$E$ 为环境的贡献，$G \times E$ 为二者的互作。数量遗传学还会把 $G$ 进一步分解为加性、显性与上位成分（Day 058–060）。

Wagner 与 Altenberg（1996）强调，基因型–表型图谱的结构，例如它是否具有模块化的组织，决定了突变产生的表型变异能否被选择利用，即系统的**可进化性**（Day 138）。下面依次讨论显性、上位性、多效性与可塑性这四个侧面。

---

## 2 显性与隐性

### 2.1 显性的几种类型

Day 015 指出，显隐性描述的是同一位点的两个等位基因在表型上的相互关系，而不是等位基因本身的属性。若杂合子的表型与某一纯合子相同，称该等位基因**完全显性**，另一个为**隐性**（recessive）。若杂合子的表型介于两种纯合子之间，称为**不完全显性**（incomplete dominance），例如红花与白花金鱼草杂交产生粉红花的杂合子；若杂合子同时表现两个等位基因的产物，称为**共显性**（codominance），例如人类 MN 血型系统（OpenStax 第 12 章）。

显隐性还取决于所考察的表型层次。同一对等位基因，在酶活性层面可能大致是加性的：对许多突变而言，杂合子的酶活性约为野生型的一半（Kacser & Burns 1981）；在机体层面却可能表现为完全显性。下一节说明其原因。

### 2.2 隐性的代谢基础

隐性突变十分普遍。Kacser 与 Burns（1981）从代谢网络的动力学给出了解释：一条代谢途径的通量与其中任一步骤的酶活性之间，是一条收益递减的曲线；酶活性降低一半，通量往往只下降很少。因此，酶活性只有正常水平 50% 的杂合子，通常不会表现出可检测的表型，突变便表现为隐性。他们认为，隐性突变的普遍存在是酶网络动力学结构的必然结果，无须像 Fisher 那样用选择作用于显性修饰基因来解释。

可以用一个简化的示意模型理解这一论证。设通量 $J$ 与酶量 $e$ 的关系为 $J = e/(e + K)$，其中 $K$ 为常数，野生型纯合子 $e = 1$，杂合子 $e = 0.5$，功能缺失纯合子 $e = 0$。以通量计的显性度可定义为 $h = 1 - J(0.5)/J(1)$：$h$ 接近 0 表示突变隐性，接近 0.5 表示加性。$K$ 越小（通量越接近饱和），$h$ 越小（练习 1）。按照同一逻辑，若某一步骤的酶量直接限制通量，杂合子就会表现出效应。显性度 $h$ 如何影响选择的效率，将在 Day 026 讨论。

---

## 3 上位性

### 3.1 一个术语的三种含义

**上位性**（epistasis）一词由 Bateson 在一个多世纪前提出，此后在不同领域中积累了不同的含义（Phillips 2008）。Phillips 区分了三种用法。**功能上位性**（functional epistasis）指蛋白质等遗传元件之间的分子相互作用。组成上位性（compositional epistasis）对应 Bateson 的原意，即一个位点的基因型遮盖或改变另一个位点等位基因的效应。**统计上位性**（statistical epistasis）源于 Fisher，指在一个群体中，多位点基因型值对加性模型的平均偏离；它是在群体中所有其他基因型上平均得到的，因此取决于等位基因频率（Phillips 2008）。同一种功能上的相互作用，在不同频率的群体中可以贡献大小不同的统计上位方差。

### 3.2 遮盖与上位比例

小鼠毛色提供了一个遮盖的例子。在 *A* 位点上，野鼠色（agouti）等位基因 *A* 对单色 *a* 显性；另一个位点 *C* 是产生色素所必需的，*cc* 个体不能产生色素，无论 *A* 位点的基因型如何都表现为白化，因此 *C* 对 *A* 上位（OpenStax 第 12 章）。两个双杂合子 *AaCc* 杂交时，后代表型不再呈 9:3:3:1，而呈 9 野鼠色 : 3 单色 : 4 白化（练习 2）。偏离 9:3:3:1 的各种比例，是经典遗传学识别上位性的主要线索。

### 3.3 度量尺度

在数量性状或适合度上，常用一个两位点的上位系数度量相互作用。设四种基因型 $ab$、$Ab$、$aB$、$AB$ 的值分别为 $W_{ab}$、$W_{Ab}$、$W_{aB}$、$W_{AB}$，加性尺度上的上位系数为

$$\varepsilon = W_{AB} - W_{Ab} - W_{aB} + W_{ab},$$

乘性尺度上的上位系数则以对数计算：$\varepsilon_{\times} = \ln W_{AB} - \ln W_{Ab} - \ln W_{aB} + \ln W_{ab}$。同一组数据可能在一种尺度上没有上位性，在另一种尺度上却有（练习 3）。因此，"两个突变之间是否存在上位性"只有在指定了度量尺度之后才有确切的含义。上位性塑造了适合度景观的形状与进化可以经过的路径（Day 065），影响蛋白质的进化（Day 096），也是杂种不育的遗传基础（Day 080）。

---

## 4 多效性

一个基因或一个突变影响多个性状的现象称为**多效性**（pleiotropy）。这一术语由德国遗传学家 Ludwig Plate 在 1910 年正式提出（Stearns 2010）。Paaby 与 Rockman（2013）指出，这个词在不同研究中指的是不同种类的"一对多"关系：在分子遗传学中，它可以指一个基因的产物具有多种分子功能；在发育遗传学中，指一个突变影响表型的多个方面；在进化研究中，则关注一个突变对适合度不同组成部分的影响。他们认为，对于任何关于多效性性质或程度的问题，恰当的回答首先是："你指的是哪一种？"

多效性具有重要的进化后果。它使不同性状之间产生遗传相关，一个性状的进化因而会牵动其他性状；一个影响许多性状的突变，在某一性状上有利，却可能在其他性状上有害，这被认为限制了适应的步伐（Day 064）。在生活史中，早期有利而晚期有害的拮抗多效性是衰老进化理论的支柱之一（Day 152）。而只在特定组织中起作用的模块化调控元件，可以使一个多效的基因只在一个性状上发生改变（Day 143）。

---

## 5 反应规范、可塑性与基因型 × 环境互作

### 5.1 反应规范

**反应规范**（reaction norm）描述的是一个基因型在不同环境中所能产生的表型范围（Yale EEB 122 第 8 讲）。把环境放在横轴、表型放在纵轴，每个基因型对应一条曲线。曲线不水平，说明这一基因型具有**表型可塑性**（phenotypic plasticity），即它的表型随环境而改变。不同基因型的反应规范若彼此平行，环境对它们的影响相同；若斜率不同，就存在**基因型 × 环境互作**（genotype-by-environment interaction, G×E）；若反应规范相互交叉，各基因型的优劣次序会随环境而颠倒。

### 5.2 互作与方差分解

Lewontin（1974）在一篇经典文章中讨论了方差分析与原因分析之间的区别。他以基因型、环境及其互作构建方差分析模型，并用反应规范图说明：当存在互作时，把表型方差划分为"遗传"与"环境"两部分的结果，只适用于所观察的那组基因型与环境，不能告诉我们一般意义上的原因各起多大作用。在练习 4 的例子中，各基因型在每个环境中差别明显，但由于反应规范交叉，基因型的主效应只占总平方和的不到 10%，绝大部分归于互作。

### 5.3 可塑性的进化

可塑性本身可以进化。Via 与 Lande（1985）把同一性状在两种环境中的表达看作两个遗传相关的性状，考察在粗粒度的异质环境中、在软选择与硬选择下群体平均表型的进化。他们的主要结论是：若两种环境中性状状态之间的遗传相关不等于 ±1，每个环境中的平均表型最终都会达到该环境的最优值，这就是可塑性的进化；但很高的正相关或负相关会显著减慢进化，并可能在到达联合最优之前，使群体在某一环境中暂时变得更不适应。可塑性先导假说与遗传同化等问题将在 Day 146 讨论。

---

## 6 案例研究：苯丙酮尿症

**问题** 一种典型的单基因遗传病，能否同时说明显隐性、多效性与基因型 × 环境互作？

**事实** 苯丙酮尿症（phenylketonuria, PKU）由 *PAH* 基因的变异引起，该基因编码苯丙氨酸羟化酶；它是常染色体隐性遗传病，两个携带者的每个孩子有 1/4 的概率患病。保留部分酶活性的变异导致较轻的类型，如变异型 PKU 与非 PKU 型高苯丙氨酸血症（MedlinePlus, n.d.）。若不治疗，苯丙氨酸在体内积累到有害水平，导致智力障碍；癫痫发作、发育迟缓、行为问题与精神障碍也很常见；未经治疗的患者可能带有霉味或鼠臭味；经典型 PKU 患儿的皮肤和头发颜色常比未患病的家庭成员浅，并常有湿疹等皮肤病（MedlinePlus, n.d.）。

**干预与结果** 到 1953 年，研究者已开发出一种特殊的低蛋白饮食，若在出生后立即开始，可使患儿正常发育（NICHD, n.d.-a）；美国各州现已要求对新生儿进行 PKU 筛查，筛查与立即开始的饮食治疗相结合，几乎消除了 PKU 作为智力障碍原因的作用（NICHD, n.d.-b）。

**意义** 第一，PKU 是隐性的：杂合携带者不患病。第二，一个基因的缺陷同时影响神经发育、色素沉着与气味等多个性状，是多效性的典型例子；不同变异造成不同的严重程度，说明同一位点的等位基因构成一个从轻到重的系列。第三，同一基因型的表型取决于饮食环境，它的反应规范很陡：在普通饮食中导致严重的智力障碍，在低苯丙氨酸饮食中则接近正常。"遗传的"并不意味着"不可改变的"；任何关于遗传与环境相对重要性的说法，都只适用于特定的环境范围（Lewontin 1974）。

---

## 今日学习材料（均可免费获取）

| 类型 | 材料 | 说明 |
|---|---|---|
| 必看 | [Yale EEB 122](https://oyc.yale.edu/ecology-and-evolutionary-biology/eeb-122) 第 8 讲 *The Expression of Variation: Reaction Norms* | 反应规范与可塑性，约 50 分钟 |
| 必读 | [OpenStax *Biology 2e* 第 12 章](https://openstax.org/books/biology-2e/pages/12-introduction)，重点为 [§12.3 Laws of Inheritance](https://openstax.org/books/biology-2e/pages/12-3-laws-of-inheritance) | 不完全显性、共显性与上位性，约 15 分钟 |
| 精读 | Lewontin（1974）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC1762622) | 方差分析与原因分析，基因型 × 环境互作的经典讨论 |
| 精读 | Kacser & Burns（1981）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC1214416) | 显性的代谢基础，重点阅读引言与讨论 |
| 选读 | Paaby & Rockman（2013）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC3558540) | 多效性的不同含义 |
| 选读 | Wagner & Altenberg（1996）：[作者主页全文](https://dynamics.org/Altenberg/PAPERS/CAEE/) | 基因型–表型图谱、模块化与可进化性 |
| 选读 | MedlinePlus Genetics：[Phenylketonuria](https://medlineplus.gov/genetics/condition/phenylketonuria) | 案例研究的背景资料 |

---

## 思考与练习

1. **（计算）** 按第 2.2 节的示意模型 $J = e/(e + K)$，分别计算 $K = 0.05$、1 与 10 时杂合子与野生型纯合子的通量之比，以及以通量计的显性度 $h = 1 - J(0.5)/J(1)$（本题参数为假设）。哪种情况下功能缺失突变表现为隐性？为什么？
2. **（推导与计算）** (a) 用棋盘法推导 *AaCc* × *AaCc* 杂交后代中野鼠色、单色与白化的比例。(b) 某次杂交得到 160 只后代：野鼠色 86 只、单色 32 只、白化 42 只（本题数据为假设）。用卡方拟合优度检验判断数据是否符合 (a) 的比例。
3. **（计算）** 四种基因型的适合度为 $W_{ab} = 1.0$、$W_{Ab} = 1.2$、$W_{aB} = 1.5$、$W_{AB} = 1.8$（本题数据为假设）。(a) 分别计算加性尺度与乘性尺度上的上位系数。(b) $W_{AB}$ 取何值时，两种尺度上分别不存在上位性？(c) 这说明了什么？
4. **（计算）** 三个基因型在两种环境中的平均表型如下（本题数据为假设）：G1 为 10 与 14，G2 为 12 与 13，G3 为 14 与 12（依次为环境 E1 与 E2）。(a) 计算总平均、各基因型平均与各环境平均，并画出反应规范的示意图。(b) 计算基因型、环境与互作的平方和及其所占比例。(c) 计算三个基因型在两种环境中表型值的相关系数。若这三个基因型代表了群体的全部遗传变异，按 Via 与 Lande（1985）的结论，选择能否使群体在两种环境中都达到各自的最优值？
5. **（概念）** 判断并纠正：(a)"显性等位基因在群体中通常更常见。"(b)"两个基因之间存在上位性，说明它们的蛋白质产物在物理上相互结合。"(c)"PKU 是遗传病，所以环境无法改变患者的表型。"(d)"如果某性状的表型方差有 80% 来自遗传差异，那么在任何环境中都是如此。"
6. **（文献评论）** 阅读 Lewontin（1974），并结合 Via 与 Lande（1985）的结论讨论：(a) 为什么在存在基因型 × 环境互作时，方差分析不能把原因"分开"？(b) Via 与 Lande 所说的"遗传相关不等于 ±1"在生物学上意味着什么？(c) 两篇文章分别从什么角度看待 G×E：一种需要避免的统计麻烦，还是进化的原材料？

<details>
<summary>答案要点</summary>

1. $K = 0.05$：通量比约 0.955，$h \approx 0.045$；$K = 1$：约 0.667，$h \approx 0.333$；$K = 10$：约 0.524，$h \approx 0.476$（代码验算）。$K$ 很小时通量接近饱和，酶量减半对通量影响很小，突变近乎隐性；$K$ 很大时通量近似与酶量成正比，杂合子介于两种纯合子之间，突变近乎加性。这正是 Kacser 与 Burns（1981）论证的核心：隐性源于通量对酶量的收益递减。
2. (a) 16 种等概率组合中，*A_C_* 占 9 份（野鼠色），*aaC_* 占 3 份（单色），*cc* 占 4 份（*A_cc* 3 份与 *aacc* 1 份，均为白化），即 9:3:4。(b) 期望数为 90、30、40；$\chi^{2} = 4^{2}/90 + 2^{2}/30 + 2^{2}/40 \approx 0.41$，自由度 2，$P \approx 0.81$（代码验算），不能拒绝 9:3:4 的假设。
3. (a) 加性尺度：$\varepsilon = 1.8 - 1.2 - 1.5 + 1.0 = 0.1$；乘性尺度：$\varepsilon_{\times} = \ln(1.8 \times 1.0) - \ln(1.2 \times 1.5) = 0$（代码验算）。(b) 加性尺度上 $W_{AB} = 1.7$，乘性尺度上 $W_{AB} = 1.8$。(c) 上位性的有无与大小取决于度量尺度；在适合度这类以乘积方式组合的量上，通常以乘性（对数）尺度作为"无相互作用"的基准。
4. (a) 总平均 12.5；基因型平均分别为 12、12.5、13；环境平均分别为 12 与 13。反应规范：G1 上升，G2 略升，G3 下降，G1 与 G3 交叉。(b) $SS_G = 1.0$（约 8.7%），$SS_E = 1.5$（约 13.0%），$SS_{G \times E} = 9.0$（约 78.3%），总和 11.5（代码验算）。(c) 相关系数为 −1：在 E1 中表型越高的基因型，在 E2 中表型越低。若群体的遗传变异只有这三个基因型，两种环境中的性状状态完全负相关，选择提高 E1 中的表型就必然降低 E2 中的表型，群体无法同时独立地到达两个环境的最优值；只有遗传相关不等于 ±1 时才可能（Via & Lande 1985）。当然，用三个基因型的平均值计算的相关系数只是示意，不是对遗传相关的可靠估计。
5. (a) 错误。显隐性描述杂合子的表型，与等位基因频率无关；隐性等位基因可以很常见，显性等位基因也可以很稀有。(b) 错误。组成上位性与统计上位性都不要求分子之间直接接触；遮盖可以通过同一代谢或发育途径中的上下游关系实现（Phillips 2008）。(c) 错误。出生后立即开始特殊饮食，可使患儿正常发育（NICHD, n.d.-a）；PKU 基因型的表型取决于饮食环境。(d) 错误。这一比例只适用于所研究的那组基因型与环境；存在互作或环境范围改变时，结果可以完全不同（Lewontin 1974）。
6. (a) 存在互作时，一个因素的效应取决于另一个因素的水平，"遗传方差"与"环境方差"的大小随所取样的基因型与环境组合而变；分解结果只描述该样本，并不对应可分离的独立原因（Lewontin 1974）。(b) 遗传相关不等于 ±1，意味着存在只影响一种环境中表型、或在两种环境中影响方向或程度不同的遗传变异，选择因此可以分别调整两种环境中的表型，即可塑性可以进化（Via & Lande 1985）。(c) Lewontin 强调互作使"遗传与环境各占多少"这一问题本身失去一般意义，是对过度解读方差分解的警告；Via 与 Lande 则把 G×E 表述为遗传相关，把它视为可塑性得以进化的遗传基础。两种角度是互补的。

</details>

---

## 关键术语

| 中文 | English | 释义 |
|---|---|---|
| 基因型–表型图谱 | genotype–phenotype map (GP map) | 基因型与其所产生表型之间的对应关系，通常是多对一、非线性且依赖环境的 |
| 隐性 | recessive | 等位基因只在纯合时才表现其表型效应 |
| 不完全显性 | incomplete dominance | 杂合子的表型介于两种纯合子之间 |
| 共显性 | codominance | 杂合子同时表现两个等位基因的表型 |
| 上位性 | epistasis | 一个位点等位基因的效应取决于其他位点基因型的现象 |
| 功能上位性 | functional epistasis | 蛋白质等遗传元件之间的分子相互作用 |
| 统计上位性 | statistical epistasis | 群体中多位点基因型值对加性模型的平均偏离，取决于等位基因频率 |
| 多效性 | pleiotropy | 一个基因或突变影响多个性状的现象 |
| 反应规范 | reaction norm | 一个基因型在不同环境中所产生的表型的集合，常表示为表型对环境的函数 |
| 表型可塑性 | phenotypic plasticity | 同一基因型在不同环境中产生不同表型的能力 |
| 基因型 × 环境互作 | genotype-by-environment interaction (G×E) | 不同基因型对环境变化的反应不同，表现为反应规范不平行 |
| 跨环境遗传相关 | cross-environment genetic correlation | 同一性状在不同环境中的表达之间的遗传相关 |

---

## 参考文献

- Kacser, H., & Burns, J. A. (1981). The molecular basis of dominance. *Genetics, 97*(3–4), 639–666. https://doi.org/10.1093/genetics/97.3-4.639 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC1214416)］
- Lewontin, R. C. (1974). The analysis of variance and the analysis of causes. *American Journal of Human Genetics, 26*(3), 400–411.（DOI 未核实）［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC1762622)］
- Paaby, A. B., & Rockman, M. V. (2013). The many faces of pleiotropy. *Trends in Genetics, 29*(2), 66–73. https://doi.org/10.1016/j.tig.2012.10.010 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC3558540)］
- Phillips, P. C. (2008). Epistasis — the essential role of gene interactions in the structure and evolution of genetic systems. *Nature Reviews Genetics, 9*(11), 855–867. https://doi.org/10.1038/nrg2452
- Stearns, F. W. (2010). One hundred years of pleiotropy: A retrospective. *Genetics, 186*(3), 767–773. https://doi.org/10.1534/genetics.110.122549
- Via, S., & Lande, R. (1985). Genotype-environment interaction and the evolution of phenotypic plasticity. *Evolution, 39*(3), 505–522. https://doi.org/10.1111/j.1558-5646.1985.tb00391.x
- Wagner, G. P., & Altenberg, L. (1996). Perspective: Complex adaptations and the evolution of evolvability. *Evolution, 50*(3), 967–976.（DOI 未核实）［[作者主页全文](https://dynamics.org/Altenberg/PAPERS/CAEE/)］

**网络资源**（访问日期 2026-11-22）

- MedlinePlus. (n.d.). *Phenylketonuria*. U.S. National Library of Medicine. https://medlineplus.gov/genetics/condition/phenylketonuria
- National Institute of Child Health and Human Development. (n.d.-a). *NICHD mission & scientific accomplishments: Phenylketonuria (PKU)*. https://www.nichd.nih.gov/about/accomplishments/pku
- National Institute of Child Health and Human Development. (n.d.-b). *Phenylketonuria (PKU) and newborn screening*. https://www.nichd.nih.gov/about/overview/mission/Pages/pku.aspx
- OpenStax. (n.d.). *Biology 2e*, Chapter 12 Mendel's experiments and heredity. https://openstax.org/books/biology-2e/pages/12-introduction
- Stearns, S. C. (2009). *EEB 122: Principles of evolution, ecology and behavior* [Video lectures]. Open Yale Courses. https://oyc.yale.edu/ecology-and-evolutionary-biology/eeb-122

---

**上一讲** [Day 019 · 基因组变异的形式与群体测序数据](day019-genomic-variation-data.md) ｜ **下一讲** Day 021 · 第 3 周复盘
