# Day 008 · 进化的证据 II：化石记录与过渡形态

> **部分** 第一部分 概念基础与证据 ｜ **周次** 第 2 周 进化的证据与树状思维 ｜ **发布日期** 2026-11-10 ｜ **建议用时** 约 80 分钟（讲义 35′ · 主读／主看 35′ · 练习 10′）
> **主读** Yale EEB 122 第 19 讲 *The Fossil Record and Life's History*；*Understanding Evolution*：Evolution 101 生命史部分
> **关键词** stratigraphy · radiometric dating · taphonomy · Lagerstätte · transitional fossil · mosaic evolution · ghost lineage · stratigraphic congruence

## 学习目标

完成本讲后，应能够：

1. 说明地层学的基本原理与放射性定年的原理，并能计算放射性年龄；
2. 解释化石记录不完整的原因，以及为何不完整的记录仍然能够检验进化假说；
3. 以 *Tiktaalik* 为例，说明过渡化石如何作为可检验的预测被发现，以及后续发现如何修正其时间框架；
4. 区分过渡形态与直接祖先，理解"幽灵谱系"的概念；
5. 了解化石记录与系统发育一致性的定量研究。

---

## 1 地层与年代

### 1.1 相对年代

地层学的两条基本原理提供了**相对年代**：

- **叠覆律**（law of superposition）：在未经构造扰动的沉积序列中，下层比上层更老。
- **动物群演替律**（principle of faunal succession）：化石组合按确定的顺序更替，因此可以用化石对比不同地区的地层。

### 1.2 放射性定年

**绝对年代**来自放射性衰变。设母体同位素初始数量为 $N_0$，衰变常数为 $\lambda$，则经过时间 $t$ 后剩余的母体数量为

$$P(t) = N_0\,e^{-\lambda t},\qquad \lambda = \frac{\ln 2}{t_{1/2}},$$

其中 $t_{1/2}$ 为半衰期。若矿物形成时不含子体同位素，且此后体系封闭，则子体数量 $D = N_0 - P$，由此得到年龄

$$t = \frac{1}{\lambda}\,\ln\!\left(1 + \frac{D}{P}\right).$$

**表 1 常用的放射性定年体系（半衰期据 USGS 与美国国家公园管理局资料）**

| 母体 → 子体 | 半衰期 | 适用范围 |
|---|---|---|
| ²³⁸U → ²⁰⁶Pb | 约 45 亿年 | 古老的岩浆岩与锆石 |
| ²³⁵U → ²⁰⁷Pb | 约 7.04 亿年 | 同上，常与 ²³⁸U 体系联合使用 |
| ⁴⁰K → ⁴⁰Ar | 约 12.5 亿年 | 火山岩 |
| ¹⁴C → ¹⁴N | 5730 年 | 约 100 年至 5 万年的有机物 |

化石所在的沉积岩通常无法直接用放射性方法定年，研究者一般测定化石层上下的火山灰等岩浆岩，从而给出化石年龄的范围。地质年代的划分与数值年龄由国际地层委员会（ICS）的《国际年代地层表》给出，并随新数据定期更新。

---

## 2 化石的形成与化石记录的偏差

生物死后要成为化石，通常需要被迅速掩埋、并具有骨骼或外壳等不易分解的硬组织。研究化石形成过程的学科称为**埋藏学**（taphonomy）。在少数特殊条件下，软组织也能保存下来，这样的产地称为**特异埋藏化石库**（Konservat-Lagerstätte）。例如，云南澄江化石地保存了寒武纪早期大量软躯体动物的精细结构，1984 年由侯先光在帽天山发现，2012 年列入世界自然遗产（UNESCO）。辽宁热河生物群中的中华龙鸟（*Sinosauropteryx*）保存了与羽毛起源有关的皮肤衍生结构（Chen et al. 1998）。

化石记录存在系统性偏差：有硬组织的生物、海洋环境中的生物、以及在出露良好且被充分采集的地层中的生物，更可能被记录下来；越古老的岩石保存的信息总体越少（Benton et al. 2000）。达尔文在《物种起源》第 9 章"论地质记录的不完全"中已经专门讨论了这一问题。

---

## 3 不完整的记录如何检验进化

化石记录虽不完整，却可以用来检验一个独立的预测：**系统发育树的分支顺序应当与类群在地层中首次出现的顺序大体一致**。系统发育树由形态或分子性状推断，并不使用化石的年代信息；如果共同由来与这些树都是正确的，两种数据就应当比随机情况下更加吻合。

- Benton 与 Hitchin（1997）分析了 384 个已发表的分支图（涉及棘皮动物、鱼类与四足动物），发现基于性状的系统发育与基于年代的化石顺序总体一致。
- Benton 等（2000）扩大到 1000 个系统发育，发现越古老的岩石平均保存的信息越少；但在"阶"的地层精度与"科"的分类精度上，过去约 5.4 亿年的化石记录对生命史提供了总体上同样良好的记录。

这类比较中一个有用的概念是**幽灵谱系**（ghost lineage）。姊妹群在同一时刻由共同祖先分化而来；如果其中一支的最早化石明显晚于另一支，那么在两者之间就存在一段没有化石记录、但根据系统发育必然存在过的谱系。系统发育树所隐含的幽灵谱系总长越短，说明它与地层记录越一致（练习 2）。

---

## 4 过渡化石：作为可检验的预测

### 4.1 *Tiktaalik*：从预测到发现

化石与比较解剖学表明，四足动物起源于肉鳍鱼类。按照这一认识，介于鱼类与早期四足动物之间、兼具两者特征的类型，应当出现在年代与沉积环境都合适的地层中。2006 年发表的 *Tiktaalik roseae* 正是这样一个例子（Daeschler et al. 2006；Shubin et al. 2006）：

- **产地与年代**：加拿大努纳武特地区埃尔斯米尔岛南部的 Fram 组，属陆相碎屑沉积；孢粉生物地层学将其定为晚泥盆世弗拉阶（Frasnian）早—中期，通常引用的年代约为 3.75 亿年前。
- **镶嵌特征**：下颌与吻部仍保留鱼类特征，而颅骨扁平、呈三角形，后部更接近有肢的四足动物；胸鳍中具有与四足动物上臂、前臂和腕部同源的骨骼，但仍保留鳍条。Shubin 等（2006）认为，其胸鳍在形态与功能上都处于鳍与肢之间的过渡状态。

### 4.2 后续发现如何修正时间框架

Niedźwiedzki 等（2010）报道了波兰圣十字山脉 Zachełmie 采石场的四足动物足迹，年代为中泥盆世早期（艾菲尔阶，约 3.9 亿年前），不仅早于 *Tiktaalik*，也早于大多数四足形类鱼类化石。如果这一解释成立，四足动物的起源要比原先认为的更早，而 *Tiktaalik* 只是一个较晚存续的过渡类群，并非四足动物的直接祖先；在它与更早的四足动物之间存在一段幽灵谱系。这些痕迹的解释本身仍有争议：Lucas（2015）认为它们可能是鱼类活动留下的痕迹。

这一过程说明了过渡化石作为证据的逻辑：*Tiktaalik* 所体现的**形态镶嵌**这一预测依然成立，而关于**起源时间**的推断则随新证据而修正。

### 4.3 其他过渡序列

- **鲸类**：Thewissen 等（2001）报道的早始新世巴基鲸类骨骼表明，这些早期鲸类是陆生哺乳动物，并支持鲸类与偶蹄类的亲缘关系比与中爪兽类更近；Gingerich 等（2001）在巴基斯坦的原鲸类化石中发现了偶蹄类特征的踝骨。分子证据也支持鲸类位于偶蹄类之内（Day 010）。
- **鸟类与恐龙**：热河生物群中保存皮肤衍生结构的兽脚类恐龙（Chen et al. 1998）等发现，为羽毛与鸟类的起源提供了一系列中间形态。
- **哺乳类中耳**：从颌关节骨到听小骨的化石序列（Day 006）。

---

## 5 过渡形态不等于直接祖先

过渡化石通常不是现生类群的直接祖先，而是系统发育树上的**侧支**：它们与某个现生类群拥有较近的共同祖先，并保留了祖先与后裔特征的镶嵌组合。因此，过渡化石证明的是"中间形态曾经存在"，而不是"找到了祖先本身"。所谓"缺失环节"的说法暗含一条线性的进化阶梯，误解了生命之树的分支结构；Day 012–013 将用"冠群"与"干群"等概念精确地描述这类化石的位置。

---

## 今日学习材料（均可免费获取）

| 类型 | 材料 | 说明 |
|---|---|---|
| 必看 | [Yale EEB 122](https://oyc.yale.edu/ecology-and-evolutionary-biology/eeb-122) 第 19 讲 *The Fossil Record and Life's History* | 约 48 分钟，附讲稿 |
| 必读 | [*Understanding Evolution*：Evolution 101](https://evolution.berkeley.edu/evolution-101/) | 生命史（history of life）部分，约 20 分钟 |
| 选读 | Benton & Hitchin（1997）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC1688444) | 化石记录与系统发育的一致性 |
| 选读 | USGS：[Radiometric Time Scale](https://pubs.usgs.gov/gip/geotime/radiometric.html) | 放射性定年的简明说明 |
| 工具 | ICS：[《国际年代地层表》](https://stratigraphy.org/chart) | 查阅地质年代的最新数值年龄 |

---

## 思考与练习

1. **（计算）** (a) 某锆石中放射成因 ²⁰⁶Pb 与剩余 ²³⁸U 的原子数之比 $D/P = 0.0600$。取 ²³⁸U 半衰期为 $4.5 \times 10^9$ 年，计算其年龄，并指出它大致属于哪个地质时期。(b) 某木炭样品中 ¹⁴C 只剩原有的 25%，其年龄是多少？(c) 5 万年后 ¹⁴C 还剩多少？为什么不能用 ¹⁴C 测定恐龙化石的年龄？
2. **（计算）** 四个类群的最早化石年代（百万年前）为：A = 10，B = 20，C = 40，D = 60。比较两棵候选树 T1 = (((A,B),C),D) 与 T2 = (((A,D),C),B)：假定每个内部节点的年龄等于其后裔中最早化石的年代，计算每棵树隐含的幽灵谱系总长。哪棵树与地层记录更一致？
3. **（概念）** 概括 *Tiktaalik* 作为"可检验预测"的逻辑。Zachełmie 足迹（若解释成立）推翻了这一预测的哪一部分，又保留了哪一部分？
4. **（概念）** 为什么大多数过渡化石不是现生类群的直接祖先？这对"缺失环节"的说法意味着什么？
5. **（评论）** 有人说："化石记录如此不完整，不能作为进化的证据。"结合 Benton 等（1997、2000）的研究评价这一说法。

<details>
<summary>答案要点</summary>

1. (a) $\lambda = \ln 2 / (4.5 \times 10^9) \approx 1.540 \times 10^{-10}$ /年，$t = \ln(1.06)/\lambda \approx 3.783 \times 10^8$ 年，约 3.78 亿年，属泥盆纪（与 *Tiktaalik* 的年代相近）。(b) 25% 即经过两个半衰期，约 11,460 年。(c) $0.5^{50000/5730} \approx 0.0024$，即只剩约 0.24%；非鸟恐龙的化石至少有 6600 万年历史，相当于一万多个半衰期，残留的 ¹⁴C 实际上为零，因此必须使用 U–Pb、⁴⁰Ar/³⁹Ar 等长半衰期体系，测定化石层上下的火山岩。
2. T1：节点 (A,B) 的年龄为 20，A 的幽灵谱系 10；节点 ((A,B),C) 的年龄为 40，(A,B) 支系的幽灵谱系 20；根节点年龄为 60，((A,B),C) 支系的幽灵谱系 20；合计 50（百万年）。T2：节点 (A,D) 的年龄为 60，A 的幽灵谱系 50；节点 ((A,D),C) 的年龄为 60，C 的幽灵谱系 20；根节点处 B 的幽灵谱系 40；合计 110。T1 隐含的未记录谱系更少，与地层记录更一致。
3. 逻辑：根据已知的鱼类与四足动物化石及其年代，预测介于两者之间的镶嵌类型应出现在特定年代与环境的地层中，并据此寻找。若 Zachełmie 足迹确为四足动物所留，则受到修正的是"过渡类型出现的时间"——四足动物在 *Tiktaalik* 之前已经存在；而"存在兼具鱼类与四足动物特征的过渡形态"这一形态学预测仍然成立。*Tiktaalik* 应被理解为一个较晚存续的过渡类群，而非祖先本身。
4. 任何一个化石物种恰好是某现生类群直接祖先的概率很低；更常见的是，我们找到的是与祖先亲缘很近的侧支，它们保留了相似的镶嵌特征。"缺失环节"暗含线性阶梯，而系统发育是分支的；过渡化石的意义在于证明中间形态曾经存在，而不在于定位祖先个体。
5. 不完整性主要导致记录的缺口与采样偏差，但并不意味着记录是随机或无序的。系统发育由独立的性状数据推断，而它与化石出现顺序的一致性显著；越古老的记录信息越少，但在适当的精度上记录总体可靠。此外，预测性的发现（如 *Tiktaalik*）以及多条相互独立的过渡序列，都表明化石记录可以用来检验进化假说。

</details>

---

## 关键术语

| 中文 | English | 释义 |
|---|---|---|
| 叠覆律 | law of superposition | 未经扰动的沉积序列中，下层比上层更老 |
| 动物群演替律 | principle of faunal succession | 化石组合按确定的顺序更替，可用于对比地层 |
| 放射性定年 | radiometric dating | 根据放射性同位素的衰变测定岩石或矿物的绝对年龄 |
| 半衰期 | half-life | 放射性母体同位素衰变掉一半所需的时间 |
| 埋藏学 | taphonomy | 研究生物死亡后如何被掩埋、保存为化石的学科 |
| 特异埋藏化石库 | Konservat-Lagerstätte | 保存了软组织等精细结构的特殊化石产地 |
| 过渡化石 | transitional fossil | 兼具祖先类群与后裔类群特征的化石类型 |
| 镶嵌进化 | mosaic evolution | 不同性状以不同速率、在不同时间发生演化，使一个类群兼具原始与衍生特征 |
| 幽灵谱系 | ghost lineage | 根据系统发育必然存在、但尚无化石记录的谱系段 |
| 地层一致性 | stratigraphic congruence | 系统发育的分支顺序与类群在地层中首次出现顺序的吻合程度 |

---

## 参考文献

- Benton, M. J., & Hitchin, R. (1997). Congruence between phylogenetic and stratigraphic data on the history of life. *Proceedings of the Royal Society of London. Series B: Biological Sciences, 264*, 885–890. https://doi.org/10.1098/rspb.1997.0123 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC1688444)］
- Benton, M. J., Wills, M. A., & Hitchin, R. (2000). Quality of the fossil record through time. *Nature, 403*(6769), 534–537. https://doi.org/10.1038/35000558
- Chen, P.-J., Dong, Z.-M., & Zhen, S.-N. (1998). An exceptionally well-preserved theropod dinosaur from the Yixian Formation of China. *Nature, 391*(6663), 147–152. https://doi.org/10.1038/34356
- Daeschler, E. B., Shubin, N. H., & Jenkins, F. A., Jr. (2006). A Devonian tetrapod-like fish and the evolution of the tetrapod body plan. *Nature, 440*(7085), 757–763. https://doi.org/10.1038/nature04639
- Darwin, C. (1859). *On the origin of species by means of natural selection, or the preservation of favoured races in the struggle for life*. John Murray. ［[Project Gutenberg](https://www.gutenberg.org/ebooks/22764)］
- Gingerich, P. D., ul Haq, M., Zalmout, I. S., Khan, I. H., & Malkani, M. S. (2001). Origin of whales from early artiodactyls: Hands and feet of Eocene Protocetidae from Pakistan. *Science, 293*, 2239–2242.（DOI 未核实）
- Lucas, S. G. (2015). *Thinopus* and a critical review of Devonian tetrapod footprints. *Ichnos, 22*(3–4).（页码与 DOI 未核实）
- Niedźwiedzki, G., Szrek, P., Narkiewicz, K., Narkiewicz, M., & Ahlberg, P. E. (2010). Tetrapod trackways from the early Middle Devonian period of Poland. *Nature, 463*(7277), 43–48. https://doi.org/10.1038/nature08623
- Shubin, N. H., Daeschler, E. B., & Jenkins, F. A., Jr. (2006). The pectoral fin of *Tiktaalik roseae* and the origin of the tetrapod limb. *Nature, 440*(7085), 764–771. https://doi.org/10.1038/nature04637
- Thewissen, J. G. M., Williams, E. M., Roe, L. J., & Hussain, S. T. (2001). Skeletons of terrestrial cetaceans and the relationship of whales to artiodactyls. *Nature, 413*(6853), 277–281. https://doi.org/10.1038/35095005

**网络资源**（访问日期 2026-11-10）

- International Commission on Stratigraphy. *International chronostratigraphic chart*. https://stratigraphy.org/chart
- National Park Service. *Radiometric age dating*. https://www.nps.gov/subjects/geology/radiometric-age-dating.htm
- Stearns, S. C. (2009). *EEB 122: Principles of evolution, ecology and behavior* [Video lectures]. Open Yale Courses. https://oyc.yale.edu/ecology-and-evolutionary-biology/eeb-122
- UNESCO World Heritage Centre. *Chengjiang fossil site*. https://whc.unesco.org/en/list/1388
- U.S. Geological Survey. *Geologic time: Radiometric time scale*. https://pubs.usgs.gov/gip/geotime/radiometric.html

---

**上一讲** [Day 007 · 第 1 周复盘：进化生物学的问题、概念与思想史](../week01/day007-week01-review.md) ｜ **下一讲** Day 009 · 进化的证据 III：生物地理学
