# Day 017 · 突变 II：随机性与适合度效应分布

> **部分** 第一部分 概念基础与证据 ｜ **周次** 第 3 周 遗传变异的来源 ｜ **发布日期** 2026-11-19 ｜ **建议用时** 约 90 分钟（讲义 40′ · 主读／主看 30′ · 练习 20′）
> **主读** *Understanding Evolution*：*Mutations are random*；Luria & Delbrück（1943）
> **关键词** fluctuation test · Luria–Delbrück distribution · replica plating · indirect selection · random mutation · mutation bias · distribution of fitness effects (DFE) · mutation accumulation · Bateman–Mukai method · effectively neutral

## 学习目标

完成本讲后，应能够：

1. 说明 Luria–Delbrück 波动检验的逻辑：诱导假说与自发突变假说对平行培养中突变体数的分布作出了不同的预测；
2. 解释 Lederberg 影印平板实验与间接选择如何证明抗性突变先于选择而存在；
3. 准确表述"突变相对于适应是随机的"的含义，并评价关于突变偏向的争论；
4. 定义适合度效应分布（DFE），说明其主要估计方法与一般形状；
5. 解释有效群体大小如何决定一个突变是否"近乎中性"。

---

## 1 问题：突变是"按需"出现的吗？

Day 016 讨论了突变的类型与速率。本讲讨论两个更深的问题：突变的发生是否与它对生物是否有利有关？新突变对适合度的影响又是如何分布的？

第一个问题在 20 世纪 40 年代的细菌学中有直接的现实意义。把细菌暴露于噬菌体或抗生素时，总会出现少数抗性菌。这些抗性是接触选择因子之后才被"诱导"出来的（类似于获得性状遗传，Day 002），还是在接触之前就已经由随机突变产生、选择因子只是把它们筛选出来？前者意味着变异是"定向"的，后者则是达尔文式的"随机变异加选择"。

---

## 2 波动检验

Luria 与 Delbrück（1943）设计了一个巧妙的实验来区分这两种假说。他们从很少的细胞出发建立许多平行的培养，让每个培养生长到大致相同的数量，然后把各培养分别涂布到含噬菌体的平板上，计数抗性菌落。

两种假说对各培养之间抗性菌数的分布作出了不同的预测：

- **诱导假说**：每个细胞只在接触噬菌体时以很小的概率获得抗性，各细胞相互独立。于是各培养中的抗性菌数应服从泊松分布，方差约等于均值。
- **自发突变假说**：抗性突变在培养生长期间随机发生。若突变发生得早，突变细胞会在随后的分裂中形成一个很大的克隆；若发生得晚，克隆很小；许多培养中则根本没有发生突变。因此，各培养之间的抗性菌数会剧烈波动，个别培养会出现数量极大的"头奖"（jackpot），方差远大于均值。

"头奖"的大小可以直接算出：若培养共经历 $n$ 代同步分裂，一个在第 $g$ 代发生的突变到最后会形成 $2^{\,n-g}$ 个突变细胞。以 $n = 24$ 为例，在第 4 代发生的突变产生 $2^{20} \approx 10^{6}$ 个突变细胞，而在最后一代发生的突变只产生 1 个。突变发生的时间在各培养之间是随机的，这就造成了巨大的波动。

实验观察到的方差远大于均值，与自发突变假说相符：抗性突变在接触噬菌体之前就已随机发生（Luria & Delbrück 1943）。这种分布今天称为 **Luria–Delbrück 分布**。值得注意的是，各培养中发生的突变事件数仍然服从泊松分布，只是每次突变产生的突变细胞数取决于它发生的时间，才使突变体数偏离泊松分布。

这一实验还可以用来估计突变率。最简单的是**零类法**（$p_0$ method）：若每个培养中突变事件数服从均值为 $m$ 的泊松分布，则没有突变体的培养所占的比例为 $p_0 = e^{-m}$，因此

$$m = -\ln p_0, \qquad \mu \approx \frac{m}{N_t},$$

其中 $N_t$ 为培养最终的细胞数（练习 1）。波动检验背后完整的数学将在第 3 周复盘（Day 021）中精读。

---

## 3 影印平板与间接选择

波动检验是一个统计推断。Lederberg 与 Lederberg（1952）则用**影印平板**（replica plating）给出了更直接的证明。他们先在不含选择因子的平板上培养细菌，形成许多菌落（"母板"），再用一块无菌的绒布把母板上所有菌落的位置原样"印"到含选择因子的平板上。在选择性平板上长出的抗性菌落，可以按位置追溯回母板上对应的菌落；而母板上的这些菌落从未接触过选择因子。

在此基础上，他们发展了**间接选择**（indirect selection）：从母板上对应位置取菌接种，可以使抗性变异的比例提高约 100 倍；重复这一过程，最终得到纯的、稳定的抗性培养物，而被选出的细菌始终没有接触过选择因子。作者把这种方法比作动物育种中依据同胞或系谱的选择。既然抗性菌可以在完全不接触选择因子的情况下被分离出来，抗性突变就必然在选择之前已经存在（Lederberg & Lederberg 1952）。

---

## 4 "随机"的确切含义

说突变是**随机的**，确切的含义是：一个突变是否发生，与它在当前环境中是否有利无关（University of California Museum of Paleontology, n.d.）。这一命题常被误解，需要澄清它**不**意味着什么：

- **不意味着各种突变的概率相同。**突变谱是不均匀的：某些碱基替换、某些序列背景与某些基因组区域的突变率更高（Day 016）。
- **不意味着突变率不受环境影响。**接触有害化学物质可能提高突变率，但并不会专门产生能抵抗这些化学物质的突变（University of California Museum of Paleontology, n.d.）。
- **不意味着进化是随机的。**突变产生的变异是随机的，而自然选择对这些变异的筛选是非随机的。

### 4.1 关于突变偏向的争论

Monroe 等（2022）对拟南芥突变积累系的分析报告，基因体内的突变频率比周围区域降低一半，必需基因中降低三分之二；表观基因组与物理特征可以解释基因周围突变偏向格局 90% 以上的变异。作者认为，这种与表观基因组相关的偏向减少了有害突变的发生，因此"突变偏向反映了自然选择"。

这一结论随即受到质疑。Liu 与 Zhang（2022）指出，该研究鉴定出的突变数远多于原始数据产生者所报告的数目，也多于按拟南芥突变率所预期的数目；他们在所考察的植物、真菌与动物模型中，都没有发现选择约束较强的区域突变率较低的证据。Wang 等（2023）的重新分析认为，原研究的突变检出中存在大量测序与分析假象，许多核心结论可由这些假象解释；在质量最好的数据中，必需基因每碱基对的编码区突变率反而最高。原作者在同期答复中承认忽略了部分误差来源，但认为这些不足以推翻其结论（[答复全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC10371858)）。

这场争论尚无定论。需要注意，即使突变率在不同基因组区域之间确有差异，并且与功能约束相关，这也是突变率在基因组上的统计偏向，而不是突变"按环境的需要"定向发生。它涉及的问题是：突变率本身能否被选择塑造到如此精细的程度？这与 Day 016 讨论的漂变障碍假说直接相关，后者认为选择难以精细调节各基因的突变率（Lynch et al. 2016）。另一个相关的问题是，突变偏向是否会影响适应所走的路径，例如使某些类型的有利突变更常被固定；这将在讨论平行进化与可预测性时再谈（Day 069）。

---

## 5 适合度效应分布

### 5.1 定义与一般形状

设一个新突变使携带者的相对适合度变为 $1 + s$，$s$ 称为**选择系数**（selection coefficient）。新突变的 $s$ 值的分布称为**适合度效应分布**（distribution of fitness effects, DFE）。DFE 决定了突变为进化提供的"原材料"的性质：有多少是有害的、有多少近乎中性、有多少是有利的。Eyre-Walker 与 Keightley（2007）的综述总结了以下规律：有利突变很少，其中受到强选择的有利突变近似服从指数分布；有害突变的分布较为复杂，常呈多峰形状。

### 5.2 估计方法

- **突变积累实验**：在突变积累系中，有害突变的积累使品系的平均适合度逐代下降，同时使各品系之间的适合度方差逐代增加。设每代平均适合度的下降为 $\Delta M$，品系间方差的增量为 $\Delta V$，每个基因组每代的突变数为 $U$，突变的平均效应为 $\bar s$。若各突变效应相同，则 $\Delta M = U\bar s$、$\Delta V = U\bar s^{2}$；效应不等时 $\Delta V$ 更大，于是

$$U \ge \frac{(\Delta M)^{2}}{\Delta V}, \qquad \bar s \le \frac{\Delta V}{\Delta M}.$$

这就是 **Bateman–Mukai 方法**，它给出的是突变率的下限与平均效应的上限（Halligan & Keightley 2009；练习 3）。

- **定点突变**：人为构建大量单突变体并逐一测定其适合度，常用于病毒与微生物。
- **群体遗传学推断**：比较非同义位点与同义位点上多态的频率分布，推断非同义突变的 DFE。由于有害突变不易上升到高频，非同义多态中低频变异的比例会更高，其程度反映了选择的强弱。这类方法将在第 11 周与第五部分讨论。

### 5.3 近乎中性

一个突变在群体中的命运，不仅取决于 $s$，还取决于**有效群体大小** $N_e$。粗略地说，当 $|N_e s| \ll 1$ 时，漂变的作用远强于选择，突变的行为与中性突变无异，称为**有效中性**（effectively neutral）。例如，一个 $s = -10^{-5}$ 的突变，在 $N_e = 10^{4}$ 的群体中 $\lvert N_e s \rvert = 0.1$，基本上像中性突变一样漂变；在 $N_e = 10^{6}$ 的群体中 $\lvert N_e s \rvert = 10$，选择就能有效地将其清除。因此，同一个 DFE 在不同物种中意味着不同比例的有效中性突变：$N_e$ 越大，选择能够"察觉"的效应越小，有效中性的突变越少（练习 4）。这正是 Day 004 提到的近中性理论的基本思想，其群体遗传学推导见第 5 周与第 8 周。

---

## 今日学习材料（均可免费获取）

| 类型 | 材料 | 说明 |
|---|---|---|
| 必读 | *Understanding Evolution*：[Mutations are random](https://evolution.berkeley.edu/mutations-are-random) | "随机"的含义，约 10 分钟 |
| 精读 | Luria & Delbrück（1943）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC1209226) | 重点阅读实验设计与两种假说的预测；数学部分留待 Day 021 |
| 选读 | Lederberg & Lederberg（1952）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC169282) | 影印平板与间接选择 |
| 选读 | Liu & Zhang（2022）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC9372563)；Wang et al.（2023）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC10371861) | 关于突变偏向的争论 |

---

## 思考与练习

1. **（计算）** 一次模拟的波动检验得到 20 个平行培养中的抗性菌数如下（每个培养最终约有 $N_t = 2^{24} \approx 1.68 \times 10^{7}$ 个细胞；本题数据由计算机模拟产生）：0、19、17、2、1、0、1、2、1、25、2、5、10、0、5、6、1、2、0、132。(a) 计算均值、样本方差与方差均值比。(b) 若诱导假说成立（泊松分布，均值同上），一个培养中没有抗性菌的概率是多少？20 个培养中预期有几个这样的培养？(c) 用零类法估计每个培养的平均突变事件数 $m$ 与突变率 $\mu$。
2. **（计算）** 在间接选择中，每一轮从母板对应位置取菌接种，可使抗性变异的比例提高约 100 倍。若最初抗性变异的比例为 $10^{-7}$，至少需要几轮才能使其比例超过 50%？为什么"被选出的细菌从未接触选择因子"是整个论证的关键？
3. **（计算）** 某突变积累实验中，各品系的平均适合度每代下降 $\Delta M = 0.002$，品系间方差每代增加 $\Delta V = 0.0001$（本题数据为假设）。(a) 用 Bateman–Mukai 方法估计 $U$ 的下限与 $\bar s$ 的上限。(b) 为什么得到的是下限与上限，而不是确切值？
4. **（计算）** 设有害突变的 $|s|$ 服从形状参数 $\beta = 0.2$、均值 $\bar s = 0.01$ 的伽马分布（本题参数为假设）。(a) 以 $|s| < 1/N_e$ 作为有效中性的近似判据，分别计算 $N_e = 10^{4}$ 与 $N_e = 10^{6}$ 时有效中性突变所占的比例。(b) 计算 $|s| > 0.01$ 与 $|s| > 0.1$ 的突变所占的比例。(c) 这一分布形状（大量弱效突变加少量强效突变）对进化意味着什么？
5. **（概念）** 判断并纠正：(a) "细菌接触抗生素后，会产生抗药突变来求生。"(b) "突变是随机的，所以基因组中每个位点的突变概率相同。"(c) "压力会提高细菌的突变率，所以突变是定向的。"(d) "Monroe 等（2022）证明了进化不是随机的。"
6. **（文献评论）** 概括 Monroe 等（2022）的主要结论与 Liu 和 Zhang（2022）、Wang 等（2023）的主要质疑。你认为需要什么样的数据或实验，才能判断"必需基因的突变率较低"是否真实？

<details>
<summary>答案要点</summary>

1. (a) 均值 11.55，样本方差约 854.6，方差均值比约 74，远大于泊松分布的 1。(b) 泊松分布下 $P(0) = e^{-11.55} \approx 9.6\times10^{-6}$，20 个培养中预期只有约 $1.9\times10^{-4}$ 个；实际有 4 个。同样，在泊松分布下出现一个含 132 个抗性菌的培养的概率小到可以忽略（约 $10^{-89}$）。这两点都与诱导假说矛盾（代码验算）。(c) $p_0 = 4/20 = 0.2$，$m = -\ln 0.2 \approx 1.61$，$\mu \approx 1.61/(1.68\times10^{7}) \approx 9.6\times10^{-8}$。模拟所用的真实值为 $10^{-7}$；只有 20 个培养时，这种估计的误差相当大。
2. $10^{-7} \times 100^{k} \ge 0.5$，得 $k \ge 3.35$，至少需要 4 轮（3 轮后约为 0.1）。由于被选出的细菌始终没有接触选择因子，抗性不可能是由选择因子诱导产生的，只能是在选择之前已经存在的突变。
3. (a) $U \ge (0.002)^{2}/0.0001 = 0.04$，$\bar s \le 0.0001/0.002 = 0.05$（代码验算）。(b) 推导假定各突变效应相同；若效应不等，品系间方差会大于 $U\bar s^{2}$，按相同效应的公式计算就会低估 $U$、高估 $\bar s$，因此只能给出 $U$ 的下限与 $\bar s$ 的上限。此外，效应很小的突变对均值与方差的贡献都很小，难以被检测。
4. (a) $N_e = 10^{4}$ 时约 31%，$N_e = 10^{6}$ 时约 13%（代码验算）。(b) $|s| > 0.01$ 约占 24%，$|s| > 0.1$ 约占 1.3%。(c) 大量突变的效应很弱，它们是否被选择清除取决于 $N_e$：在小群体中，许多弱有害突变会像中性突变一样漂变，甚至被固定，造成适合度的缓慢下降；在大群体中，选择可以清除其中更大的一部分。少量强效突变则无论群体大小都会被迅速清除。
5. (a) 错误。抗性突变在接触抗生素之前已随机产生，抗生素只是筛选出了已有的抗性个体（Luria & Delbrück 1943；Lederberg & Lederberg 1952）。(b) 错误。"随机"指突变的发生与其是否有利无关，并不意味着各位点或各类型的突变概率相同；突变谱与突变率在基因组上都不均匀。(c) 错误。压力可以提高全基因组的突变率，但并不专门产生有利突变；提高的是变异的总量，而不是方向。(d) 错误。即使该结论成立，它表明的也只是突变率在基因组区域之间存在与功能约束相关的偏向，而不是突变按环境需要定向发生；况且这一结论本身仍有争议，进化中的选择本来就是非随机的。
6. Monroe 等：基因体与必需基因中的突变率较低，与表观基因组特征相关，作者认为这种偏向减少了有害突变。Liu 和 Zhang：该研究检出的突变数异常偏多，在其他模型中也未发现约束较强的区域突变率较低。Wang 等：许多信号可由测序与分析假象解释，在最好的数据中必需基因的编码区突变率反而最高。可能的检验：使用更严格、经独立方法验证的突变检出流程；在多个独立的突变积累实验与亲子测序数据中重复检验；控制序列背景、比对难度与覆盖度等可能造成假象的因素；以及通过实验检验所提出的分子机制（例如与特定组蛋白修饰相关的 DNA 修复途径）是否真的降低了这些区域的突变率。

</details>

---

## 关键术语

| 中文 | English | 释义 |
|---|---|---|
| 波动检验 | fluctuation test | 比较平行培养中突变体数的方差与均值，以区分自发突变与诱导突变的实验 |
| Luria–Delbrück 分布 | Luria–Delbrück distribution | 生长过程中随机发生的突变所产生的突变体数的分布，方差远大于均值 |
| 零类法 | $p_0$ method | 由无突变体培养所占比例估计平均突变事件数的方法 |
| 影印平板 | replica plating | 用绒布把母板上菌落的位置原样转移到其他平板上的方法 |
| 间接选择 | indirect selection | 不让被选个体接触选择因子，而依据其同胞克隆的表现进行选择 |
| 随机突变 | random mutation | 突变的发生与其在当前环境中是否有利无关 |
| 突变偏向 | mutation bias | 不同类型或不同基因组区域的突变率之间的系统性差异 |
| 选择系数 | selection coefficient | 突变使相对适合度改变的量 $s$ |
| 适合度效应分布 | distribution of fitness effects (DFE) | 新突变选择系数的分布 |
| Bateman–Mukai 方法 | Bateman–Mukai method | 由突变积累系适合度均值的下降与方差的增加估计突变率下限与平均效应上限的方法 |
| 有效中性 | effectively neutral | $\lvert N_e s \rvert \ll 1$、命运主要由漂变决定的突变状态 |

---

## 参考文献

- Eyre-Walker, A., & Keightley, P. D. (2007). The distribution of fitness effects of new mutations. *Nature Reviews Genetics, 8*(8), 610–618. https://doi.org/10.1038/nrg2146
- Halligan, D. L., & Keightley, P. D. (2009). Spontaneous mutation accumulation studies in evolutionary genetics. *Annual Review of Ecology, Evolution, and Systematics, 40*, 151–172.（DOI 未核实）
- Lederberg, J., & Lederberg, E. M. (1952). Replica plating and indirect selection of bacterial mutants. *Journal of Bacteriology, 63*(3), 399–406. https://doi.org/10.1128/jb.63.3.399-406.1952 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC169282)］
- Liu, H., & Zhang, J. (2022). Is the mutation rate lower in genomic regions of stronger selective constraints? *Molecular Biology and Evolution, 39*(8), msac169. https://doi.org/10.1093/molbev/msac169 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC9372563)］
- Luria, S. E., & Delbrück, M. (1943). Mutations of bacteria from virus sensitivity to virus resistance. *Genetics, 28*(6), 491–511. https://doi.org/10.1093/genetics/28.6.491 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC1209226)］
- Lynch, M., Ackerman, M. S., Gout, J.-F., Long, H., Sung, W., Thomas, W. K., & Foster, P. L. (2016). Genetic drift, selection and the evolution of the mutation rate. *Nature Reviews Genetics, 17*(11), 704–714. https://doi.org/10.1038/nrg.2016.104
- Monroe, J. G., Srikant, T., Carbonell-Bejerano, P., Becker, C., Lensink, M., Exposito-Alonso, M., Klein, M., Hildebrandt, J., Neumann, M., Kliebenstein, D., Weng, M.-L., Imbert, E., Ågren, J., Rutter, M. T., Fenster, C. B., & Weigel, D. (2022). Mutation bias reflects natural selection in *Arabidopsis thaliana*. *Nature, 602*(7895), 101–105. https://doi.org/10.1038/s41586-021-04269-6
- Wang, L., Ho, A. T., Hurst, L. D., & Yang, S. (2023). Re-evaluating evidence for adaptive mutation rate variation. *Nature, 619*(7971), E52–E56. https://doi.org/10.1038/s41586-023-06314-y ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC10371861)］

**网络资源**（访问日期 2026-11-19）

- University of California Museum of Paleontology. (n.d.). *Mutations are random*. Understanding Evolution. https://evolution.berkeley.edu/mutations-are-random

---

**上一讲** [Day 016 · 突变 I：类型、速率与测定](day016-mutation-rates.md) ｜ **下一讲** [Day 018 · 重组：交叉、基因转换与重组热点](day018-recombination-hotspots.md)
