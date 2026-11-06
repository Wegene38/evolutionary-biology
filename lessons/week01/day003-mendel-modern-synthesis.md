# Day 003 · 进化思想史 II：孟德尔遗传与现代综合

> **部分** 第一部分 概念基础与证据 ｜ **周次** 第 1 周 导论 ｜ **发布日期** 2026-11-05 ｜ **建议用时** 约 80 分钟（讲义 35′ · 主读／主看 35′ · 练习 10′）
> **主读** Yale EEB 122 第 2 讲 *Basic Transmission Genetics*；*Stanford Encyclopedia of Philosophy*："Population Genetics"第 1–2 节
> **关键词** blending inheritance · particulate inheritance · eclipse of Darwinism · Mendelians and biometricians · multiple-factor hypothesis · Fisher–Haldane–Wright · Modern Synthesis

## 学习目标

完成本讲后，应能够：

1. 用简单的数学说明，为什么融合遗传会使自然选择难以奏效，而颗粒（孟德尔）遗传能够保存变异；
2. 概述"达尔文主义的日食"时期（约 1880–1920）的主要替代理论，以及 Weismann 种质学说的意义；
3. 说明孟德尔学派与生物统计学派之争的实质，以及 Fisher（1918）如何用多因子模型调和二者；
4. 比较理论群体遗传学奠基者 Fisher、Haldane 与 Wright 的主要贡献与分歧；
5. 概括现代综合的代表著作与核心主张，并指出它留下的问题。

---

## 1 达尔文留下的遗传学难题

### 1.1 泛生论

《物种起源》没有给出遗传机制。达尔文在 1868 年的《动物和植物在家养下的变异》中提出了"泛生论"（pangenesis）的暂定假说：身体各部分产生微小的"微芽"（gemmules），汇集到生殖细胞并传给后代。这一假说同时容纳了获得性状遗传（Darwin 1868）。

### 1.2 融合遗传的困难

19 世纪流行的直觉是**融合遗传**（blending inheritance）：子代性状是父母性状的混合，如同两种颜料调和。设父母表型 $X_m$ 与 $X_f$ 独立、方差均为 $V$，子代表型取父母平均值 $Y = (X_m + X_f)/2$，则

$$\operatorname{Var}(Y) = \frac{V + V}{4} = \frac{V}{2}.$$

即在随机交配下，**群体的可遗传变异每代减半**，7 代后只剩不到 1%（练习 1）。若要维持变异，新变异必须以极高的速率不断产生；而一个罕见的有利变异个体与普通个体交配后，其优势在后代中被不断"稀释"。

1867 年，工程师 Fleeming Jenkin 在《北不列颠评论》上匿名发表长篇书评（Jenkin 1867），从变异的限度、单个变异难以保存等方面批评《物种起源》。达尔文承认自己此前低估了单个变异被保存的困难，并在第 5 版（1869）中作了修改。后人常把 Jenkin 的论证概括为"融合遗传会淹没单个有利变异"；这一概括是否忠实于原文，科学史研究中仍有重新评估（Morris 1994）。

### 1.3 颗粒遗传如何解决问题

孟德尔遗传是**颗粒式**的：控制性状的因子（基因）在杂合子中并不混合，而是完整地分离到配子中。因此，在没有选择、漂变、突变与迁移时，等位基因频率与遗传方差代代保持不变（Hardy–Weinberg 平衡，Day 022）。变异只会因有限群体中的遗传漂变缓慢丧失：在 $N = 10\,000$ 的理想群体中，杂合度减半约需 13,863 代（练习 1）。Fisher（1930）把这一对比作为其《自然选择的遗传理论》的出发点：颗粒遗传使变异得以保存，自然选择才有持续作用的材料。

---

## 2 "达尔文主义的日食"（约 1880–1920）

在《物种起源》出版后的几十年中，"进化"本身迅速被接受，但自然选择作为主要机制却屡受质疑。Huxley（1942）把这一时期称为"达尔文主义的日食"，Bowler（1983）的同名专著将其大致界定为 1880–1920 年。这一时期的主要替代理论包括：

| 理论 | 核心主张 | 代表人物 |
|---|---|---|
| 新拉马克主义 | 获得性状遗传是适应的主要来源 | Cope 等 |
| 直生论（orthogenesis） | 进化受内在因素驱动，沿预定方向进行 | Eimer 等 |
| 突变论 / 跃变论（mutationism / saltationism） | 新物种由大幅度的不连续突变一步产生，选择只起淘汰作用 | de Vries |

**Weismann 的种质学说.** Weismann（1892）区分了传递给后代的**种质**与构成身体的体质，认为体细胞的改变不能传入种质，从而否定了获得性状遗传。只承认自然选择的这一立场后来被称为"新达尔文主义"。

**de Vries 的突变论.** de Vries（1901–1903）根据对拉马克月见草（*Oenothera lamarckiana*）的观察提出突变论。后来的细胞遗传学研究表明，月见草中许多"突变"源于其特殊的染色体结构（相互易位形成的染色体复合体）与多倍化，而不是典型意义上的新基因突变（Bowler 1983）。

---

## 3 孟德尔的再发现与早期遗传学

- **孟德尔（1866）**：豌豆杂交实验于 1865 年在布尔诺自然科学学会宣读，1866 年发表，提出分离律与自由组合律（Mendel 1866）。
- **1900 年的"再发现"**：de Vries、Correns 与 Tschermak 几乎同时发表了与孟德尔一致的结果。
- **术语与概念**：Bateson 于 1905 年在私人信件中提出"genetics"一词，1906 年首次公开使用；Johannsen（1909）提出"基因"（gene）、"基因型"（genotype）与"表型"（phenotype），并以菜豆纯系实验说明：在遗传上同质的纯系内部，对表型差异的选择无效。
- **染色体理论**：Morgan 及其学生在果蝇中建立了遗传的染色体理论（Morgan et al. 1915）。

---

## 4 孟德尔学派与生物统计学派之争

20 世纪初，围绕"进化依靠什么样的变异"发生了激烈争论（Provine 1971）：

| | 生物统计学派（biometricians） | 孟德尔学派（Mendelians） |
|---|---|---|
| 代表人物 | Galton、Pearson、Weldon | Bateson、de Vries |
| 研究对象 | 身高、形态测量等连续变异 | 豌豆颜色等不连续性状 |
| 方法 | 回归、相关等统计方法 | 杂交实验与分离比 |
| 对进化的看法 | 自然选择作用于微小的连续差异 | 进化依靠不连续的大变异 |

这场争论在很大程度上是一场"错位"的冲突：双方研究的是不同类型的性状。Yule 早在 1902 年就指出，如果一个性状受许多孟德尔因子控制，就会表现出连续变异；Nilsson-Ehle 对小麦粒色、East 对玉米的研究随后为**多因子假说**提供了实验证据（Provine 1971）。

**Fisher（1918）的调和.** Fisher 证明，在多个孟德尔位点共同作用、并存在环境影响的条件下，可以定量地推导出亲属之间的相关，从而解释生物统计学派观察到的连续变异与亲属相似性。这篇论文首次使用了统计学中的"方差"（variance）一词，并把表型方差分解为加性、显性与上位性等成分（Day 058）。

一个最简单的情形：$n$ 个独立的加性位点，每个位点两个等位基因频率均为 1/2，每个"+"等位基因使性状增加 $a$。个体的基因型值为 $G = aK$，其中 $K$ 服从二项分布 $\mathrm{Bin}(2n, 1/2)$，因此

$$\operatorname{E}(G) = na, \qquad \operatorname{Var}(G) = 2n \cdot \tfrac{1}{4}\, a^2 = \frac{n a^2}{2}.$$

当 $n$ 增大并叠加环境变异时，表型分布趋于连续的正态分布（中心极限定理）。

---

## 5 理论群体遗传学的奠基

**Hardy–Weinberg 原理（1908）.** Hardy（1908）在给《科学》的一封短信中回应 Yule 的一个疑问——显性性状是否会在群体中逐渐增加到 3∶1——证明在随机交配的大群体中，基因型频率在一代之后即保持稳定，显性等位基因不会自动扩散，隐性等位基因也不会自动消失。Weinberg（1908）独立得到了相同的结论。

**三位奠基者**（Provine 1971, 1986）：

| | R. A. Fisher | J. B. S. Haldane | Sewall Wright |
|---|---|---|---|
| 代表著作 | 1918 年论文；《自然选择的遗传理论》（1930） | 系列论文《自然选择与人工选择的数学理论》（1924–1934）；《进化的原因》（1932） | 《孟德尔群体中的进化》（1931） |
| 主要贡献 | 方差分解；自然选择基本定理；大群体中加性遗传方差上的选择 | 选择、突变、迁移的定量模型；用实际数据（如桦尺蛾工业黑化）估算选择强度 | 近交系数（Wright 1922）与通径分析；漂变的定量理论；适应度景观与转移平衡理论（Day 065） |
| 对群体结构与漂变的看法 | 大的随机交配群体为主，漂变作用很小 | 介于二者之间 | 群体分化为许多半隔离的小群体，漂变与选择、迁移共同作用 |

Fisher 与 Wright 之间关于漂变与群体结构重要性的长期争论，是群体遗传学史上最重要的理论分歧之一（Provine 1986）。几乎同时，苏联遗传学家 Chetverikov（1926/1961）指出，野生果蝇群体中隐藏着大量杂合状态的隐性变异；他所代表的研究传统经由 Dobzhansky 影响了现代综合。

---

## 6 现代综合（约 1936–1950）

理论群体遗传学为进化提供了数学基础，但它需要与自然群体、系统学、古生物学和植物学的证据结合。这一整合过程被称为**现代综合**（Modern Synthesis，又称进化综合）。

| 著作 | 作者与年份 | 贡献领域 |
|---|---|---|
| *Genetics and the Origin of Species* | Dobzhansky 1937 | 把群体遗传学与自然群体的遗传变异（如果蝇染色体倒位）联系起来 |
| *Evolution: The Modern Synthesis* | Huxley 1942 | 为这一综合命名并作全面概述 |
| *Systematics and the Origin of Species* | Mayr 1942 | 系统学；生物学物种概念与地理物种形成 |
| *Tempo and Mode in Evolution* | Simpson 1944 | 古生物学：化石记录与群体遗传学相容 |
| *Variation and Evolution in Plants* | Stebbins 1950 | 植物：多倍化与杂交 |

1946 年美国成立进化研究学会（Society for the Study of Evolution），次年创办期刊 *Evolution*，标志着这一综合在学科建制上的确立（Smocovitis 1996）。Dobzhansky 后来在其书第 3 版中写道："进化是群体遗传组成的改变，对进化机制的研究属于群体遗传学的范围"（Dobzhansky 1951）。

**核心主张**（据 Mayr & Provine 1980 等概括）：

1. 进化表现为群体中等位基因频率的改变；
2. 突变与重组提供变异，自然选择是主要的方向性力量，遗传漂变与基因流也起作用；
3. 宏进化可以由微进化过程在长时间中的累积来解释；
4. 物种形成主要通过地理隔离后生殖隔离的演化而实现；
5. 获得性状遗传、直生论与跃变论被否定。

**"硬化"与遗留问题.** Gould（1983）认为，现代综合从 20 世纪 40 年代的多元立场，逐渐"硬化"为更强调适应与自然选择的立场。综合时期的理论也留下了后来才被深入研究的问题：分子水平的进化与中性理论（Day 004、050）、发育在进化中的作用（第 21 周）、宏进化格局能否完全由微进化外推（第 20 周），以及可塑性等因素的地位（Day 146、177）。

---

## 今日学习材料（均可免费获取）

| 类型 | 材料 | 说明 |
|---|---|---|
| 必看 | [Yale EEB 122](https://oyc.yale.edu/ecology-and-evolutionary-biology/eeb-122) 第 2 讲 *Basic Transmission Genetics* | 约 50 分钟，附讲稿 |
| 必读 | *Stanford Encyclopedia of Philosophy*：[Population Genetics](https://plato.stanford.edu/entries/population-genetics/)（Okasha） | 第 1–2 节（学科起源与 Hardy–Weinberg 原理），约 25 分钟 |
| 精读 | Hardy（1908）：[DOI 链接](https://doi.org/10.1126/science.28.706.49) | 仅两页的经典短信 |
| 精读 | Fisher（1918）：[阿德莱德大学 Fisher 文献库扫描本](https://digital.library.adelaide.edu.au/dspace/handle/2440/15097) | 读引言与结论部分 |
| 选读 | Wright（1931）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC1201091/) | 浏览引言与总结 |
| 选读 | Mendel（1866）英译本：[MendelWeb](https://cs.brown.edu/people/rblumber/MendelWeb/home.html) | 原始论文的英译与注释 |

---

## 思考与练习

1. **（推导与计算）** (a) 证明在融合遗传与随机交配下，子代表型方差是亲代的一半。多少代后方差降至初始值的 1% 以下？用模拟（例如 10,000 个个体）验证。(b) 在孟德尔遗传下，若只有遗传漂变起作用，杂合度满足 $H_t = H_0\,(1 - 1/2N)^t$。$N = 10\,000$ 时，杂合度减半需要多少代？(c) 据此解释，为什么颗粒遗传对达尔文的理论至关重要。
2. **（计算）** 按 §4 的多基因加性模型：(a) 基因型值可能取多少个不同的值？(b) 当 $n = 10$ 时，所有 $2n$ 个等位基因都是"+"的个体在群体中的频率是多少？(c) 解释为什么持续的选择能使性状均值超出初始群体中实际观察到的范围。
3. **（概念）** 孟德尔学派与生物统计学派争论的核心是什么？为什么说它在很大程度上是一场"错位"的冲突？
4. **（比较）** 从群体结构、遗传漂变的作用、上位性的地位与适应的方式四个方面比较 Fisher 与 Wright 的观点。什么样的经验数据可以帮助区分二者？
5. **（评论）** "现代综合把宏进化看作微进化在长时间中的外推。"举出两条后来对这一主张提出挑战或修正的研究方向，并说明它们挑战的是哪一点。

<details>
<summary>答案要点</summary>

1. (a) $\operatorname{Var}(Y) = \tfrac14[\operatorname{Var}(X_m) + \operatorname{Var}(X_f)] = V/2$；$(1/2)^t \le 0.01$ 得 $t = 7$（剩余 0.78%）。模拟（$N = 10\,000$）得到的方差比依次约为 0.495、0.252、0.128、0.064、0.033、0.016、0.008，与理论一致。(b) $t_{1/2} = \ln 0.5 / \ln(1 - 1/2N) \approx 2N\ln 2 \approx 13\,863$ 代。(c) 两者相差约四个数量级：融合遗传下变异每代减半，自然选择缺乏持续作用的材料；颗粒遗传下变异得以保存，选择可以在多代中累积作用于已有变异。
2. (a) $2n + 1$ 个（$K = 0, 1, \dots, 2n$）。(b) $(1/2)^{20} \approx 9.5 \times 10^{-7}$，约百万分之一，在数千个个体的样本中几乎不会出现。(c) 选择提高每个位点上"+"等位基因的频率，重组把原本分散在不同个体中的"+"等位基因组合到同一个体中，因此可以产生初始群体中从未观察到的极端表型。
3. 核心在于进化依靠连续的微小变异还是不连续的大变异，以及孟德尔遗传能否解释连续变异。"错位"在于双方研究的性状类型不同：多因子遗传表明连续变异同样由孟德尔因子控制，双方各自正确地描述了问题的一个方面。
4. Fisher：大的随机交配群体；漂变作用很小；上位性次要，关注加性方差；适应通过大群体中的集体选择实现。Wright：分化的半隔离小群体；漂变重要；上位性使适应度景观有多个峰；适应通过漂变、局部群体间的选择与迁移的转移平衡实现。可区分的数据包括：自然群体的有效大小与群体结构、上位性的普遍程度与适应度景观的形状、适应性等位基因的起源与扩散方式（Day 031、065）。
5. 例如：间断平衡与物种选择（第 20 周）——挑战渐变与外推的充分性；进化发育生物学（第 21 周）——强调发育对变异的结构与方向的影响；中性理论（Day 004、050）——挑战"分子进化主要由选择驱动"。

</details>

---

## 关键术语

| 中文 | English | 释义 |
|---|---|---|
| 泛生论 | pangenesis | 达尔文的暂定遗传假说：身体各部分产生的微芽汇集到生殖细胞中 |
| 融合遗传 | blending inheritance | 认为子代性状是父母性状混合的遗传观念；在随机交配下会使变异每代减半 |
| 颗粒遗传 | particulate inheritance | 遗传因子在杂交中不混合、完整传递的遗传方式（孟德尔遗传） |
| 种质学说 | germ-plasm theory | Weismann 的学说：种质与体质分离，体细胞的改变不能传给后代 |
| 达尔文主义的日食 | eclipse of Darwinism | 约 1880–1920 年间自然选择学说受到普遍质疑的时期 |
| 直生论 | orthogenesis | 认为进化受内在因素驱动、沿预定方向进行的学说 |
| 突变论 | mutationism | 认为新物种由大幅度不连续突变一步产生的学说 |
| 生物统计学派 | biometricians | 以统计方法研究连续变异的学派（Galton、Pearson、Weldon） |
| 孟德尔学派 | Mendelians | 以杂交实验研究不连续性状遗传的学派（Bateson 等） |
| 多因子假说 | multiple-factor hypothesis | 连续性状由多个孟德尔因子共同控制的假说 |
| 现代综合 | Modern Synthesis | 约 1936–1950 年间遗传学与自然选择学说、系统学、古生物学等的整合 |

---

## 参考文献

- Bowler, P. J. (1983). *The eclipse of Darwinism: Anti-Darwinian evolution theories in the decades around 1900*. Johns Hopkins University Press.
- Chetverikov, S. S. (1961). On certain aspects of the evolutionary process from the standpoint of modern genetics (M. Barker, Trans.; I. M. Lerner, Ed.). *Proceedings of the American Philosophical Society, 105*(2), 167–195.（原文 1926 年以俄文发表；DOI 未核实）
- Darwin, C. (1868). *The variation of animals and plants under domestication* (Vols. 1–2). John Murray.
- de Vries, H. (1901–1903). *Die Mutationstheorie: Versuche und Beobachtungen über die Entstehung von Arten im Pflanzenreich* (Vols. 1–2). Veit.
- Dobzhansky, T. (1937). *Genetics and the origin of species*. Columbia University Press.
- Dobzhansky, T. (1951). *Genetics and the origin of species* (3rd ed.). Columbia University Press.
- Fisher, R. A. (1918). The correlation between relatives on the supposition of Mendelian inheritance. *Transactions of the Royal Society of Edinburgh, 52*, 399–433. https://doi.org/10.1017/S0080456800012163 ［[阿德莱德大学扫描本](https://digital.library.adelaide.edu.au/dspace/handle/2440/15097)］
- Fisher, R. A. (1930). *The genetical theory of natural selection*. Clarendon Press.
- Gould, S. J. (1983). The hardening of the modern synthesis. In M. Grene (Ed.), *Dimensions of Darwinism: Themes and counterthemes in twentieth-century evolutionary theory*. Cambridge University Press.
- Haldane, J. B. S. (1932). *The causes of evolution*. Longmans, Green.
- Hardy, G. H. (1908). Mendelian proportions in a mixed population. *Science, 28*(706), 49–50. https://doi.org/10.1126/science.28.706.49
- Huxley, J. (1942). *Evolution: The modern synthesis*. Allen & Unwin.
- Jenkin, F. (1867). [Review of the book *On the origin of species*, by C. Darwin]. *The North British Review, 46*, 277–318.（匿名发表）
- Johannsen, W. (1909). *Elemente der exakten Erblichkeitslehre*. Gustav Fischer.
- Mayr, E. (1942). *Systematics and the origin of species*. Columbia University Press.
- Mayr, E., & Provine, W. B. (Eds.). (1980). *The evolutionary synthesis: Perspectives on the unification of biology*. Harvard University Press.
- Mendel, G. (1866). Versuche über Pflanzen-Hybriden. *Verhandlungen des naturforschenden Vereines in Brünn, 4*, 3–47. ［[MendelWeb 英译](https://cs.brown.edu/people/rblumber/MendelWeb/home.html)］
- Morgan, T. H., Sturtevant, A. H., Muller, H. J., & Bridges, C. B. (1915). *The mechanism of Mendelian heredity*. Henry Holt.
- Morris, S. W. (1994). Fleeming Jenkin and *The Origin of Species*: A reassessment. *The British Journal for the History of Science, 27*(3), 313–343. https://doi.org/10.1017/S0007087400032209
- Provine, W. B. (1971). *The origins of theoretical population genetics*. University of Chicago Press.
- Provine, W. B. (1986). *Sewall Wright and evolutionary biology*. University of Chicago Press.
- Simpson, G. G. (1944). *Tempo and mode in evolution*. Columbia University Press.
- Smocovitis, V. B. (1996). *Unifying biology: The evolutionary synthesis and evolutionary biology*. Princeton University Press.
- Stebbins, G. L. (1950). *Variation and evolution in plants*. Columbia University Press.
- Weinberg, W. (1908). Über den Nachweis der Vererbung beim Menschen. *Jahreshefte des Vereins für vaterländische Naturkunde in Württemberg, 64*, 369–382.
- Weismann, A. (1892). *Das Keimplasma: Eine Theorie der Vererbung*. Gustav Fischer.
- Wright, S. (1922). Coefficients of inbreeding and relationship. *The American Naturalist, 56*(645), 330–338. https://doi.org/10.1086/279872
- Wright, S. (1931). Evolution in Mendelian populations. *Genetics, 16*(2), 97–159. https://doi.org/10.1093/genetics/16.2.97 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC1201091/)］

**网络资源**（访问日期 2026-11-05）

- Okasha, S. *Population genetics*. In *Stanford Encyclopedia of Philosophy*. https://plato.stanford.edu/entries/population-genetics/
- Stearns, S. C. (2009). *EEB 122: Principles of evolution, ecology and behavior* [Video lectures]. Open Yale Courses. https://oyc.yale.edu/ecology-and-evolutionary-biology/eeb-122

---

**上一讲** [Day 002 · 进化思想史 I：从自然神学到达尔文与华莱士](day002-history-darwin-wallace.md) ｜ **下一讲** [Day 004 · 进化思想史 III：中性理论与"扩展综合"之争](day004-neutral-theory-ees.md)
