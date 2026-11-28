# Day 026 · 自然选择 II：显性、超显性与平衡多态

> **部分** 第二部分 群体遗传学 ｜ **周次** 第 4 周 群体遗传学基础：HWE、连锁不平衡与选择模型 ｜ **发布日期** 2026-11-28 ｜ **建议用时** 约 100 分钟（讲义 45′ · 主读 30′ · 练习 25′）
> **主读** Coop 讲义第 10 章 *One-Locus Models of Selection*（显性与杂合子优势部分）；Holsinger 讲义中关于自然选择的各章
> **关键词** dominance coefficient (h) · Haldane's sieve · heterozygote advantage · overdominance · balanced polymorphism · underdominance · stable and unstable equilibria · segregational load · sickle-cell anaemia · malaria hypothesis

## 学习目标

完成本讲后，应能够：

1. 用显性度 $h$ 参数化二倍体选择，推导 $\Delta p$ 并说明 $h$ 如何决定稀有等位基因的命运；
2. 解释"Haldane 筛"的含义及其对适应遗传基础的预测；
3. 推导杂合子优势下的平衡频率，并判断平衡的稳定性；
4. 以镰状细胞与疟疾为例，评价杂合子优势作为平衡多态维持机制的证据；
5. 分析低显性（杂合子劣势）下的不稳定平衡及其进化后果。

---

## 1 显性度 h

Day 025 推导了二倍体模型中的 $\Delta p$。为了系统地比较显隐性的作用，常把三种基因型的相对适合度写成

$$w_{AA} = 1 + s, \qquad w_{Aa} = 1 + hs, \qquad w_{aa} = 1,$$

其中 $s$ 为 $AA$ 相对于 $aa$ 的选择系数，$h$ 为**显性度**（dominance coefficient）：$h = 0$ 时 $A$ 的效应隐性，$h = 1$ 时显性，$h = 1/2$ 时加性。代入 Day 025 的一般公式，得

$$\Delta p = \frac{s\,p\,q\left[h + p(1 - 2h)\right]}{\bar w}.$$

注意这里的"显性"是就适合度而言的，与 Day 020 讨论的表型显隐性相关，但不必相同：一个等位基因对某一表型可以是隐性的，对适合度却可以表现出部分显性。Day 020 介绍的代谢通量理论说明，功能缺失突变在表型上常为隐性（Kacser & Burns 1981），因此它们对适合度的效应也可能近乎隐性。实证上，Agrawal 与 Whitlock（2011）利用酵母中数千个基因敲除突变估计了显性度的分布，发现有害突变平均而言是部分隐性的，纯合效应越大的突变越倾向于隐性；而且显性度的分布方差很大、明显偏斜，仅凭平均显性度进行的分析可能有很大误差。

$h$ 的作用在等位基因稀有时最为突出。当 $p \to 0$ 时，方括号趋于 $h$，$\Delta p \approx s\,h\,p$：稀有等位基因几乎只存在于杂合子中，它能否被选择"看到"完全取决于杂合子的适合度。当 $p \to 1$ 时，方括号趋于 $1 - h$，剩余的 $a$ 几乎都在杂合子中，清除它们的速度取决于 $1 - h$（练习 1）。$h = 0.5$ 时，两端的变化速度大致对称，这正是 Day 025 练习 4 中加性情形的轨迹近乎对称的原因。

---

## 2 Haldane 筛

Haldane（1927）在《自然选择与人工选择的数学理论》第五部分中证明：在大群体中，一个在杂合子中具有优势 $k$ 的新显性有利突变，即使只出现一次，也有约 $2k$ 的概率最终存留下来，而不会被随机丢失。按后来发展的理论（Day 032），部分显性的新有利突变在大群体中存留的概率约为 $2hs$：例如 $s = 0.1$ 时，$h = 0.5$ 的突变约为 0.1，$h = 0.05$ 的突变只有约 0.01。一个新突变总是以单拷贝出现在杂合子中，因此它能否逃脱漂变的随机丢失、进而被选择推高，主要取决于它在杂合子中的效应：隐性的有利突变即使在纯合时优势很大，在稀有阶段也几乎得不到选择的帮助（固定概率的一般理论见 Day 032）。

由此得到的预测是：在由新突变推动的适应中，被固定的有利突变应当偏向显性。这一"筛选"效应常被称为 **Haldane 筛**（Haldane's sieve）。不过，若适应利用的是群体中早已存在的变异（即现存变异，standing variation），等位基因从较高的频率起步，隐性等位基因也能以纯合子的形式暴露给选择。Orr 与 Betancourt（2001）表明，若有利等位基因原本处于突变–选择平衡之中，其固定概率大体上与显性度无关，Haldane 筛便不再成立。

---

## 3 杂合子优势与平衡多态

### 3.1 平衡频率

若杂合子的适合度高于两种纯合子，称为**杂合子优势**（heterozygote advantage）或**超显性**（overdominance）。设

$$w_{AA} = 1 - s, \qquad w_{Aa} = 1, \qquad w_{aa} = 1 - t, \qquad s, t > 0,$$

由 $\Delta p = 0$ 并排除 $p = 0$ 与 $p = 1$ 两个边界，得到内部平衡

$$\hat p = \frac{t}{s + t},$$

其中 $\hat p$ 为 $A$ 的平衡频率。若 $p < \hat p$，$\Delta p > 0$；若 $p > \hat p$，$\Delta p < 0$；因此无论从哪一侧出发，频率都会回到 $\hat p$，这是一个稳定平衡。在平衡附近，频率与平衡值之差每代大约缩小 $\hat p\hat q(s + t)/\bar w$ 的比例。用第 1 节的参数化表示，当 $s > 0$ 时，杂合子优势对应于 $h > 1$，低显性则对应于 $h < 0$。选择在这里维持而不是消除变异，由此形成的多态称为**平衡多态**（balanced polymorphism）。由 Day 025 的结论，这一平衡正是平均适合度 $\bar w$ 的极大值所在。

### 3.2 平衡的代价

在平衡时，群体中仍有比例为 $\hat p^{2}$ 与 $\hat q^{2}$ 的纯合子，其适合度低于杂合子。由于孟德尔分离，两个杂合子交配总会产生一半纯合的后代，这种适合度的损失无法通过选择消除。平衡时的平均适合度为

$$\bar w = 1 - \frac{st}{s + t},$$

$\frac{st}{s + t}$ 称为**分离负荷**（segregational load），即群体平均适合度相对于最优基因型的减少（练习 4）。遗传负荷的一般概念及其争论将在 Day 034 讨论。

---

## 4 镰状细胞与疟疾

人类的镰状细胞等位基因是杂合子优势最著名的例子。*HBB* 基因的一个变异产生异常的 β-珠蛋白，即血红蛋白 S（HbS）（MedlinePlus, n.d.）。HbS 纯合子患镰状细胞贫血，在缺乏医疗条件时适合度很低；携带一个拷贝的杂合子（镰状细胞性状）通常没有严重症状。在恶性疟流行的地区，杂合子对疟疾具有一定的保护作用，从而同时优于两种纯合子。

这一解释最早的直接证据来自 Allison。他在东非 35 个部落中调查了镰状细胞性状的发生率，发现在疟疾高度流行的地区，该性状的频率高于 10%，而在疟疾只是间歇流行的地区则低于这一水平，并据此认为该性状与一定程度的抗疟能力有关（Allison 1954b）；同年，他还报告了镰状细胞性状对恶性疟原虫感染的保护作用（Allison 1954a）。半个多世纪后，Piel 等（2010）建立了 HbS 等位基因频率的全球地图，并与干预前的疟疾流行程度相比较：HbS 在撒哈拉以南非洲、中东与印度最为常见，二者的地理关联在全球尺度上支持"疟疾假说"，在非洲尤其明显，但在美洲与亚洲则无法分辨。

用第 3 节的模型可以理解这一多态。若取 $w_{AA} = 0.88$、$w_{AS} = 1$、$w_{SS} = 0.2$（本节数值为说明而设的假设值），HbS 的平衡频率为 $0.12/(0.12 + 0.8) \approx 0.13$。反过来，平衡公式也可以用来推断维持一个观察到的频率需要多大的杂合子优势。记 HbS 的平衡频率为 $\hat q$，由 $\hat q = s/(s + t)$ 得 $s = t\hat q/(1 - \hat q)$：若 $t = 0.8$、$\hat q = 0.1$，只需 $s \approx 0.09$，即正常纯合子的适合度比杂合子低约 9%；若 $\hat q = 0.2$，则需 $s = 0.2$。可见，维持一个 10% 左右的 HbS 频率并不需要极强的选择，但这种推断假定群体已处于平衡，而且没有迁移与漂变的显著作用。这个模型也作出一个预测：一旦疟疾被消除，杂合子不再具有优势，HbS 就只承受针对隐性纯合子的选择。由于它此时大多隐藏在杂合子中，频率的下降起初较快、随后越来越慢（练习 5）。

---

## 5 低显性与不稳定平衡

若杂合子的适合度低于两种纯合子，称为**低显性**（underdominance）。染色体结构的改变常被用作例子：若杂合子在减数分裂中产生一部分不平衡的配子，其生育力就会降低。此时第 3.1 节的公式仍给出一个内部平衡（$s$、$t$ 均取负值），但它是不稳定的：频率稍高于平衡值就会继续升高直到固定，稍低于平衡值就会下降直到丢失。哪一个等位基因最终被固定，取决于初始频率落在平衡点的哪一侧；适合度较高的纯合子对应的"吸引域"更大（练习 3）。

低显性有两个重要后果。第一，它不能维持多态，而是使不同群体可能固定不同的等位基因，并且这种差异一旦形成就难以被基因流消除；在两个群体的交界处，杂合子的劣势会阻碍基因交流，这与物种形成中的杂种劣势相联系（第四部分）。第二，一个新出现的低显性等位基因在稀有时几乎只存在于劣势的杂合子中，很难在大群体中扩散；它要越过不稳定平衡点，往往需要漂变的帮助，例如在小群体中（Day 029）。因此，低显性的变异更可能在小的或相对隔离的群体中被固定，并在不同群体之间积累差异；这一机制在物种形成中的作用将在第四部分讨论。

---

## 6 案例研究：镰状细胞多态的证据链

**问题** 一个导致严重遗传病的等位基因，为什么能在某些人类群体中维持较高的频率？

**证据** 第一，地理相关：Allison（1954b）发现镰状细胞性状的频率与疟疾的流行程度相关，Piel 等（2010）在全球尺度上用地理统计模型确认了这种关联，尤其是在非洲。第二，个体层面的保护：Allison（1954a）报告了镰状细胞性状对恶性疟原虫感染的保护作用。第三，机制与模型：杂合子优势模型预测了一个稳定的中间频率，并解释了为什么纯合子患病个体会持续出现。

**评价** 地理相关本身不能确立因果：等位基因频率的地理差异也可能来自群体历史，因此需要个体层面的证据与机制研究来补充。Piel 等也指出，他们的地图反映的是干预前的情形，不应被解读为当代的分布，而且这种关联在美洲与亚洲无法分辨，那里的群体历史与疟疾流行史都更复杂。此外，现代医疗可以提高 SS 个体的存活，模型中的适合度参数也会随之改变（练习 5）。

**意义** 镰状细胞多态说明了平衡选择的两面：选择可以维持变异，但维持变异的代价是每一代都有一部分个体处于适合度较低的纯合状态。平衡选择的其他机制，如负频率依赖选择与时空异质选择，将在 Day 027 讨论。

---

## 今日学习材料（均可免费获取）

| 类型 | 材料 | 说明 |
|---|---|---|
| 必读 | Coop，*Population and Quantitative Genetics*：[第 10 章 One-Locus Models of Selection](https://bio.libretexts.org/Bookshelves/Genetics/Population_and_Quantitative_Genetics_(Coop)/10%3A_One-Locus_Models_of_Selection) | 显性度、杂合子优势与低显性的各节，约 20 分钟 |
| 必读 | Holsinger，*Lecture Notes in Population Genetics*：[figshare 存档](https://figshare.com/articles/Lecture_notes_in_population_genetics/100687) | 自然选择的各章，约 15 分钟 |
| 精读 | Allison（1954a）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC2093356) | 镰状细胞性状对恶性疟的保护作用 |
| 选读 | Piel et al.（2010）：[开放获取全文](https://doi.org/10.1038/ncomms1104) | 镰状细胞基因的全球分布与疟疾假说 |

---

## 思考与练习

1. **（计算）** 设 $s = 0.1$，分别取 $h = 0$、0.5 与 1，计算 $p = 0.01$ 与 $p = 0.99$ 时的 $\Delta p$，并验证第 1 节的公式。比较 $\Delta p/(spq)$ 的数值，说明 $h$ 如何影响有利等位基因在稀有时与接近固定时的变化速度。
2. **（概念）** (a) 为什么 Haldane 筛预测由新突变推动的适应偏向显性的有利突变？(b) 若适应主要利用现存变异，这一预测会如何改变？(c) 若在某一类群中观察到许多适应性等位基因是隐性的，可能说明什么？
3. **（推导与计算）** (a) 由 $\Delta p = 0$ 推导第 3.1 节的平衡频率，并证明当 $s, t > 0$ 时平衡稳定。(b) 设 $w_{AA} = 1$、$w_{Aa} = 0.9$、$w_{aa} = 1$，分别从 $p_0 = 0.45$ 与 0.55 出发，频率最终走向何处？(c) 若 $w_{AA} = 1$、$w_{Aa} = 0.9$、$w_{aa} = 0.95$，不稳定平衡点在哪里？从 $p_0 = 0.30$ 与 0.36 出发，结果各如何？
4. **（计算）** 按第 4 节的假设值（$w_{AA} = 0.88$、$w_{AS} = 1$、$w_{SS} = 0.2$）：(a) 求 HbS 的平衡频率、平衡时的平均适合度与分离负荷。(b) 从 HbS 频率 0.01 与 0.5 出发，各需多少代才能使频率与平衡值之差小于 0.001？
5. **（计算与概念）** 设疟疾被完全消除后，适合度变为 $w_{AA} = w_{AS} = 1$、$w_{SS} = 0.2$（本题数值为假设）。(a) 从第 4 题的平衡频率出发，HbS 的频率减半需要多少代？(b) 为什么在频率降低之后，下降会越来越慢？(c) 现代医疗使 SS 个体的存活率提高，这对 HbS 频率的变化有什么影响？
6. **（文献评论）** 结合 Allison（1954a、1954b）与 Piel 等（2010）：(a) 地理相关、个体层面的保护与理论模型三类证据各自能说明什么，不能说明什么？(b) 为什么这种关联在美洲与亚洲难以分辨？(c) 还需要什么证据，才能更完整地确立杂合子优势这一解释？

<details>
<summary>答案要点</summary>

1. $h = 0$：$p = 0.01$ 时 $\Delta p \approx 1.0 \times 10^{-5}$，$p = 0.99$ 时约 $8.9 \times 10^{-4}$；$h = 0.5$：分别约 $4.95 \times 10^{-4}$ 与 $4.50 \times 10^{-4}$；$h = 1$：分别约 $9.78 \times 10^{-4}$ 与 $9 \times 10^{-6}$，与公式一致（代码验算）。$\Delta p/(spq)$ 在稀有时约等于 $h$，接近固定时约等于 $1 - h$：隐性有利等位基因稀有时几乎不增加，显性有利等位基因接近固定时几乎不再前进，加性时两端相近。
2. (a) 新突变以单拷贝出现在杂合子中，只有杂合子中的效应能帮助它逃脱随机丢失；显性突变在杂合子中即表现出优势，更容易存留并扩散（Haldane 1927）。(b) 现存变异已有一定频率，隐性等位基因也会以纯合子的形式出现并受到选择；Orr 与 Betancourt（2001）表明，对于原本处于突变–选择平衡中的等位基因，固定概率大体上与显性度无关。(c) 可能提示适应主要利用了现存变异，或者群体较小、近交较多，使隐性等位基因较常以纯合子形式出现。
3. (a) 在 $\Delta p$ 的分子中，$p(w_{AA} - w_{Aa}) + q(w_{Aa} - w_{aa}) = -ps + qt$，令其为 0 得 $\hat p = t/(s + t)$；当 $s, t > 0$ 时，$p < \hat p$ 使该式为正，$p > \hat p$ 使其为负，故平衡稳定。(b) 此时 $s = t = -0.1$，$\hat p = 0.5$ 为不稳定平衡；从 0.45 出发频率降向 0，从 0.55 出发升向 1（代码验算）。(c) 相对于杂合子，$s \approx -0.111$、$t \approx -0.056$，$\hat p = t/(s + t) \approx 1/3$；从 0.30 出发 $A$ 丢失，从 0.36 出发 $A$ 被固定。适合度较高的纯合子 $AA$ 拥有更大的吸引域（$p > 1/3$）。
4. (a) $s = 0.12$、$t = 0.8$，HbS 的平衡频率为 $0.12/0.92 \approx 0.130$，$\bar w = 1 - 0.096/0.92 \approx 0.896$，分离负荷约 0.104。(b) 从 0.01 出发约需 59 代，从 0.5 出发约需 38 代（代码验算）。
5. (a) 约 10 代（代码验算）。(b) 此时只有 SS 个体受到选择，而 SS 的频率为 $q^{2}$；$q$ 越小，HbS 越多地隐藏在杂合子中，每代被清除的比例越低（Day 022）。(c) 若 SS 个体的存活与生育接近正常，针对 SS 的选择减弱，HbS 频率的下降将更为缓慢；频率的变化还会受到迁移与群体历史的影响。
6. (a) 地理相关显示 HbS 频率与疟疾流行程度相关，但不能排除群体历史造成的相关；个体层面的保护说明杂合子确实对感染或疾病有一定抵抗力，但不直接给出适合度的大小；理论模型说明在杂合子优势下会形成稳定的中间频率，但其参数需要由实际数据估计。(b) 美洲与亚洲的群体经历了复杂的迁移与混合，疟疾的流行史也与非洲不同，频率的地理格局因而难以简单地与疟疾对应（Piel et al. 2010）。(c) 例如：直接测定不同基因型在疟区的存活与生育差异；分子与细胞机制研究；以及群体遗传学证据，如 HbS 所在单倍型的年龄与分布是否与疟疾选择的时间尺度相符。

</details>

---

## 关键术语

| 中文 | English | 释义 |
|---|---|---|
| 显性度 | dominance coefficient (h) | 杂合子的适合度在两种纯合子之间所处的位置，h = 0 为隐性，h = 1 为显性 |
| Haldane 筛 | Haldane's sieve | 由新突变推动的适应中，显性有利突变比隐性有利突变更易存留并被固定的效应 |
| 杂合子优势 | heterozygote advantage (overdominance) | 杂合子的适合度高于两种纯合子 |
| 平衡多态 | balanced polymorphism | 由选择维持在稳定中间频率上的多态 |
| 分离负荷 | segregational load | 杂合子优势下因孟德尔分离不断产生纯合子而导致的平均适合度降低 |
| 低显性 | underdominance | 杂合子的适合度低于两种纯合子，导致不稳定平衡 |

---

## 参考文献

- Agrawal, A. F., & Whitlock, M. C. (2011). Inferences about the distribution of dominance drawn from yeast gene knockout data. *Genetics, 187*(2), 553–566. https://doi.org/10.1534/genetics.110.124560 ［[作者主页全文](https://agrawal.eeb.utoronto.ca/agrawal/files/2013/06/yeastdominance2011.pdf)］
- Allison, A. C. (1954a). Protection afforded by sickle-cell trait against subtertian malarial infection. *British Medical Journal, 1*(4857), 290–294. https://doi.org/10.1136/bmj.1.4857.290 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC2093356)］
- Allison, A. C. (1954b). The distribution of the sickle-cell trait in East Africa and elsewhere, and its apparent relationship to the incidence of subtertian malaria. *Transactions of the Royal Society of Tropical Medicine and Hygiene, 48*(4), 312–318. https://doi.org/10.1016/0035-9203(54)90101-7
- Haldane, J. B. S. (1927). A mathematical theory of natural and artificial selection, Part V: Selection and mutation. *Proceedings of the Cambridge Philosophical Society, 23*, 838–844.（DOI 未核实）
- Kacser, H., & Burns, J. A. (1981). The molecular basis of dominance. *Genetics, 97*(3–4), 639–666. https://doi.org/10.1093/genetics/97.3-4.639 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC1214416)］
- Orr, H. A., & Betancourt, A. J. (2001). Haldane's sieve and adaptation from the standing genetic variation. *Genetics, 157*(2), 875–884.（DOI 未核实）［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC1449620)］
- Piel, F. B., Patil, A. P., Howes, R. E., Nyangiri, O. A., Gething, P. W., Williams, T. N., Weatherall, D. J., & Hay, S. I. (2010). Global distribution of the sickle cell gene and geographical confirmation of the malaria hypothesis. *Nature Communications, 1*, 104. https://doi.org/10.1038/ncomms1104

**网络资源**（访问日期 2026-11-28）

- Coop, G. (n.d.). *Population and quantitative genetics*, Chapter 10 One-locus models of selection. LibreTexts. https://bio.libretexts.org/Bookshelves/Genetics/Population_and_Quantitative_Genetics_(Coop)/10%3A_One-Locus_Models_of_Selection
- Holsinger, K. E. (n.d.). *Lecture notes in population genetics*. figshare. https://figshare.com/articles/Lecture_notes_in_population_genetics/100687
- MedlinePlus. (n.d.). *HBB gene*. U.S. National Library of Medicine. https://medlineplus.gov/genetics/gene/hbb

---

**上一讲** [Day 025 · 自然选择 I：单位点选择模型](day025-single-locus-selection.md) ｜ **下一讲** Day 027 · 自然选择 III：频率依赖、波动选择与多态维持
