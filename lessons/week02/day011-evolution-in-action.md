# Day 011 · 正在发生的进化：直接观测

> **部分** 第一部分 概念基础与证据 ｜ **周次** 第 2 周 进化的证据与树状思维 ｜ **发布日期** 2026-11-13 ｜ **建议用时** 约 85 分钟（讲义 35′ · 主读／主看 30′ · 练习 20′）
> **主读** HHMI BioInteractive 短片 *The Origin of Species: The Beak of the Finch*；Cook et al.（2012）
> **关键词** contemporary evolution · heritability · breeder's equation · fluctuating selection · character displacement · industrial melanism · introduction experiment · life-history evolution · drug resistance · darwin · haldane

## 学习目标

完成本讲后，应能够：

1. 说明"直接观测到进化"需要满足的条件，并区分长期监测、自然实验与野外引种实验三类研究设计；
2. 以达尔文雀为例，用育种者方程解释选择、遗传力与进化响应之间的关系，并解释为何进化在短期内可以预测、在长期内难以预测；
3. 评述桦尺蛾工业黑化案例的证据链：频率变化、捕食实验及其方法争议、分子机制；
4. 解释孔雀鱼引种实验的设计逻辑，并能计算以 darwin 与 haldane 为单位的进化速率；
5. 用群体遗传学的推理解释病原体耐药性的快速进化与联合用药的原理，理解进化速率的时间尺度效应。

---

## 1 从格局到过程

Day 006–010 讨论的证据，都是从现存的格局（同源性、化石序列、地理分布、分子相似性）反推历史。本讲转向**过程**：在人类可以观察的时间尺度上，直接记录群体的进化。按 Day 001 的定义，进化是群体遗传组成跨世代的改变。因此，要确认"观察到了进化"，至少需要三方面的证据：

1. **跨世代的变化**：性状分布或等位基因频率在世代之间发生了改变，而不仅仅是同一代个体的存活差异；
2. **遗传基础**：变化源于遗传组成的改变，而不仅是环境引起的**表型可塑性**（phenotypic plasticity；Day 020）；
3. **原因**：最好还能识别出起作用的选择因子，如食物、捕食者或药物。

本讲的四个案例分别代表不同的研究设计：对标记个体的长期野外监测（达尔文雀）、由环境变化造成的自然实验（桦尺蛾）、人为操纵的野外引种实验（孔雀鱼），以及临床观察（病原体耐药）。Hendry 与 Kinnison（1999）讨论了这类在数十年内即可测出的**当代微进化**（contemporary microevolution），指出该领域的速率测定存在相当的含混与不一致，需要统一的度量与更严谨的研究设计（第 6 节）。

---

## 2 达尔文雀：短期可预测，长期难预测

### 2.1 1977 年的干旱

Peter Grant 与 Rosemary Grant 在加拉帕戈斯群岛的大达夫尼岛（Daphne Major）上长期研究中嘴地雀（*Geospiza fortis*）。这座小岛面积小，研究者能够捕捉并追踪几乎所有个体（HHMI BioInteractive 2013）。1977 年的严重干旱中，地雀的存活并非随机，Boag 与 Grant（1981）测得的选择强度是当时脊椎动物群体中记录到的最高值。存活在很大程度上取决于大喙个体啄开坚硬大种子的能力（Grant & Grant 2006）。

### 2.2 选择、遗传力与进化响应

存活个体与原群体之间的差异本身只是同一代内的选择，并不是进化。只有当被选择的性状可以遗传时，下一代的平均值才会改变。数量遗传学用**育种者方程**（breeder's equation）描述这一关系（Day 060 将详细推导）：

$$R = h^{2}S,$$

其中 $S$ 为**选择差**（selection differential），即被选择的亲本平均值与选择前群体平均值之差；$h^{2}$ 为狭义**遗传力**（narrow-sense heritability），即表型方差中可由加性遗传效应解释的比例；$R$ 为**选择响应**（response to selection），即子代平均值相对于原群体的变化。Grant 夫妇的研究表明，在测定选择与遗传参数的基础上，进化在短期内是可以预测的（Grant & Grant 2002；练习 2）。

### 2.3 三十年的记录

Grant 与 Grant（2002）总结了 1972–2001 年间大达夫尼岛上中嘴地雀与仙人掌地雀（*G. scandens*）的变化：两个物种的体型与两项喙部性状都发生了显著进化；自然选择时而单向、时而振荡，时而突发、时而渐进；偶发的种间杂交增加了仙人掌地雀的表型方差，并改变了其喙形。作者的结论是，两个物种三十年后的状态在研究开始时是无法预测的。

选择的方向确实可以逆转。大地雀（*G. magnirostris*）于 1982 年在岛上建立种群；在 2004–2005 年的干旱中，两种地雀共同耗尽了食物，这一次喙较小的中嘴地雀更具优势，中嘴地雀的喙随之变小，即**性状替换**（character displacement）（Grant & Grant 2006）。同样是干旱，1977 年偏好大喙，2004–2005 年却偏好小喙，原因在于生态背景（竞争者与食物组成）不同。这种**波动选择**（fluctuating selection）是长期进化难以预测的重要原因（Day 027）。

---

## 3 桦尺蛾：工业黑化

### 3.1 现象与假说

桦尺蛾（*Biston betularia*）有浅色带斑点的典型型（*typica*）和黑化型（*carbonaria*）。工业革命期间，黑化型在英国的工业污染区迅速扩散；20 世纪中叶以后空气污染得到治理，它又迅速衰退（Cook 2003）。经典的解释是鸟类的视觉捕食：桦尺蛾白天停歇在树上，在被烟尘熏黑、地衣消失的树皮上，黑化型更不易被发现。这种由工业污染引起的黑化型频率上升，称为**工业黑化**（industrial melanism）。

### 3.2 经典实验及其争议

Kettlewell（1955）在受污染的伯明翰林地进行了标记—释放—重捕实验，并在后来的实验中与未受污染的多塞特林地对照，据此认为黑化型在污染环境中具有更高的适合度。后来的批评集中在实验设计上：蛾子常被放置在树干上，而树干是否为自然停歇位置受到质疑；释放密度远高于自然密度；部分捕食实验使用了固定的死蛾（Cook et al. 2012）。

### 3.3 Majerus 的最后实验

为回应这些批评，Majerus 设计了一项为期六年的大规模实验，共释放 4864 只蛾子，是同类研究中规模最大的一次；他以接近自然的低密度释放本地的黑化型与典型型，并记录野外蛾子的自然停歇位置。Majerus 于 2009 年去世，Cook 等（2012）整理发表了这项研究。结果显示，鸟类对黑化型的捕食明显更强，每日的选择系数约为 $s \approx 0.1$，其大小与方向足以解释后工业时代英国黑化型的迅速衰退（练习 3）。

### 3.4 分子机制

van't Hof 等（2016）发现，英国工业黑化的突变是一个大型、串联重复的转座元件插入到 *cortex* 基因的第一个内含子中；根据重组单倍型的分布推断，这一插入大约发生在 1819 年，与历史记录相符。该插入在翅芽发育早期提高了 *cortex* 转录本的丰度。至此，这一案例的证据链从"频率变化"延伸到"选择因子"和"致因突变"：我们不仅知道黑化型的频率发生了变化，还知道选择来自何处、变化发生在哪个基因上，以及突变大约出现在什么时候。由于英国的工业黑化源自一次突变事件，而且这次突变出现在工业化时期，这一案例属于选择作用于新突变的情形，而不是作用于群体中早已存在的古老变异；这两种适应来源的比较见 Day 067。

---

## 4 孔雀鱼：野外引种实验

特立尼达的山溪为孔雀鱼（*Poecilia reticulata*）研究提供了天然的重复实验：瀑布下游有大型捕食性鱼类，如慈鲷科的 *Crenicichla alta*，瀑布上游则缺少大型捕食者。高捕食地点的孔雀鱼成熟更早，并把更多资源投入繁殖（Reznick et al. 1997）。Endler（1980）用温室中的人工池塘以及随后的野外实验表明，雄鱼的体色会随捕食压力而进化。

Reznick 等（1997）把这一比较变成了实验：在 El Cedro 河与 Aripo 河的两条支流中，他们把瀑布下方高捕食地点的孔雀鱼移入瀑布上方的低捕食地点，并在引入后数年内测定其生活史性状。结果，雄鱼的成熟年龄推迟、成熟时的体型增大，方向与天然低捕食种群一致；变化在引入后约 4 年即可检出。按 darwin 单位计算，这些性状的进化速率为 3700–45,000 darwin，与人工选择实验的速率（12,000–200,000 darwin，几何平均约 58,000）相当，远高于化石记录推断的速率（化石记录中各组速率的几何平均为 0.7–3.7 darwin）。雄性性状的变化快于雌性，作者认为这与雄性具有更多的遗传变异有关。

---

## 5 病原体耐药

病原体的群体极大、世代极短，药物又施加了极强的选择，因此耐药性的进化往往在数月到数年内就能观察到。其逻辑与自然选择完全相同：群体中存在（或不断产生）携带耐药突变的变异体，药物杀死敏感个体，耐药个体随之扩增。

人类免疫缺陷病毒（HIV）提供了一个早期的临床例证。Larder、Darby 与 Richman（1989）从长期接受齐多夫定（zidovudine，AZT）单药治疗的患者体内，分离出对 AZT 敏感性降低的 HIV。若单个耐药突变的出现概率为 $\mu$，则在病毒群体规模为 $N$ 时，治疗开始前预先存在的耐药变异体期望数为 $N\mu$；若需要同时对 $k$ 种药物耐药，且各突变相互独立，期望数降为 $N\mu^{k}$。这就是联合用药能够显著延缓耐药的原理（练习 4）。病原体进化与抗生素耐药将在 Day 170–171 专门讨论。

---

## 6 进化速率与时间尺度

为了比较不同研究中的进化速率，需要统一的度量。Haldane（1949）提出 **darwin** 单位：

$$r_{\mathrm{d}} = \frac{\ln \bar x_2 - \ln \bar x_1}{\Delta t},$$

其中 $\bar x_1$、$\bar x_2$ 为起止时刻的性状平均值，$\Delta t$ 以百万年计；1 darwin 相当于每百万年发生 $e$ 倍的变化。darwin 只依赖绝对时间，不考虑世代长度与群体内的变异幅度。**haldane** 单位则以每代变化多少个标准差来度量：

$$r_{\mathrm{h}} = \frac{(\bar y_2 - \bar y_1)/s_{p}}{g},$$

其中 $\bar y$ 为对数转换后性状的平均值，$s_{p}$ 为合并标准差，$g$ 为所经历的世代数。Hendry 与 Kinnison（1999）建议当代微进化研究采用 haldane。

比较速率时必须注意时间尺度。Gingerich（1983）发现，测量的时间间隔越长，算得的速率越低。原因之一正是达尔文雀所展示的波动：短期内的快速变化在长时间尺度上相互抵消，净变化因此远小于各段变化之和。因此，当代进化"比化石记录快几个数量级"，并不意味着两者矛盾，而在很大程度上反映了测量间隔的差异（练习 1）。

上述案例把"进化"从推断变成了可以测量的过程。直接观测补充而不是取代前几讲的格局证据：格局证据说明生物之间存在共同的历史，直接观测则说明自然选择等机制能够在可测的时间内改变群体的遗传组成，并且其强度足以产生可观的变化。不过，这些案例记录的主要是物种内部的微进化；微进化如何累积为物种形成与大进化格局，是第二至第七部分要回答的问题。

---

## 今日学习材料（均可免费获取）

| 类型 | 材料 | 说明 |
|---|---|---|
| 必看 | HHMI BioInteractive：[*The Origin of Species: The Beak of the Finch*](https://www.biointeractive.org/classroom-resources/origin-species-beak-finch) | 约 16 分钟，配有学习指南 |
| 精读 | Cook et al.（2012）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC3391436) | 篇幅短，适合完整阅读；注意实验如何回应既有批评 |
| 选读 | Reznick et al.（1997）：[作者主页 PDF](https://faculty.ucr.edu/~gupy/Reznick%20edit/Publications/Science1997.pdf) | 重点阅读研究设计与速率比较 |
| 选读 | *Understanding Evolution*：[Endler 的孔雀鱼实验](https://evolution.berkeley.edu/evolibrary/article/0_0_0/lines_15) | 约 10 分钟 |

---

## 思考与练习

1. **（计算）** 某引种种群雄鱼成熟时的平均体重在 7 年内从 60 mg 增加到 75 mg（本题数值为假设值）。(a) 以 darwin 为单位计算进化速率。(b) 若对数转换后体重的合并标准差为 0.15，且 7 年间经历了 14 个世代，以 haldane 为单位计算速率。(c) 若同样的净变化在 100 万年内完成，速率是多少 darwin？结合 Gingerich（1983）的发现，解释为什么不能直接用这两个数值判断"当代进化太快"或"化石记录中的进化太慢"。
2. **（计算）** 某次干旱前，地雀群体的平均喙深为 9.2 mm，标准差为 1.0 mm；存活个体的平均喙深为 9.7 mm。设喙深的狭义遗传力 $h^{2} = 0.75$（本题数值为假设值）。(a) 计算选择差 $S$、以标准差为单位的选择强度以及预期的选择响应 $R$。(b) 预测子代的平均喙深，并计算相对变化。(c) 若次年雨水充沛、小种子丰富，预测会怎样改变？这对长期预测意味着什么？
3. **（计算）** 设 *carbonaria* 等位基因 $C$ 对 *typica* 等位基因 $c$ 完全显性，黑化型（$CC$ 与 $Cc$）的相对适合度为 $1 - s$，典型型（$cc$）为 1，随机交配。(a) 写出 $C$ 等位基因频率 $p$ 的递推式。(b) 分别取 $s = 0.1$、$0.2$，计算黑化型表型频率从 90% 降到 10% 所需的世代数。(c) Cook 等（2012）估计的是每日选择系数 $s \approx 0.1$。若成虫在繁殖前平均暴露 3 天，且各天的存活相互独立，每代的选择系数约为多少？此时需要多少世代？
4. **（计算）** 设病毒群体规模 $N = 10^{9}$，对每种药物产生耐药的突变概率均为 $10^{-5}$，且相互独立（本题数值为假设值）。分别计算对 1 种、2 种和 3 种药物同时耐药的预存变异体的期望数，以及至少存在 1 个这种变异体的概率。据此解释 AZT 单药治疗为何很快失效，以及联合用药的原理。
5. **（概念）** 对于达尔文雀、桦尺蛾、孔雀鱼与 HIV 这四个案例，分别说明研究者可以用什么证据把"遗传变化"与"表型可塑性"区分开来。哪一个案例的遗传证据最为直接？
6. **（文献评论）** 列出对 Kettlewell 实验的主要批评，并说明 Majerus 的实验设计如何回应了每一点。这项研究还留下了哪些尚未解决的问题？为什么一个经典案例的方法受到质疑，并不等于其结论被推翻？

<details>
<summary>答案要点</summary>

1. (a) $\ln(75/60) = 0.223$，$\Delta t = 7 \times 10^{-6}$ 百万年，速率约为 31,900 darwin，落在 Reznick 等（1997）报道的范围之内。(b) $0.223/0.15/14 \approx 0.106$ haldane。(c) $0.223$ darwin，相差约 14 万倍。速率随测量间隔的延长而系统性下降：长时间尺度上的净变化包含了大量方向相反、相互抵消的变化以及长期的停滞，因此短间隔与长间隔的速率不能直接比较；比较时应在相同的时间尺度上进行，或采用随时间尺度换算的方法。
2. (a) $S = 9.7 - 9.2 = 0.5$ mm，选择强度 $i = S/\sigma = 0.5$；$R = 0.75 \times 0.5 = 0.375$ mm。(b) 子代平均喙深约为 9.58 mm，增加约 4.1%。(c) 若环境逆转、选择偏好小喙，$S$ 变为负值，下一代的响应方向随之反转。短期预测只需要知道当期的 $S$ 与 $h^{2}$，而长期预测还需要预测未来的环境序列与生态变化（如竞争者的到来），后者往往无法预测，这正是 Grant 与 Grant（2002）的结论。
3. (a) 平均适合度 $\bar w = 1 - s(1 - q^{2})$，其中 $q = 1 - p$；由于 $CC$ 与 $Cc$ 的适合度相同，$p' = p(1 - s)/\bar w$。(b) $s = 0.1$ 时约需 55 代，$s = 0.2$ 时约需 26 代（代码验算）。(c) 每代的相对适合度约为 $0.9^{3} \approx 0.729$，即 $s \approx 0.27$，约需 18 代。若每年一代，几十年内即可从以黑化型为主转变为以典型型为主。注意，这里假定了每日存活相互独立、各天选择强度相同，并且忽略了迁移等因素。另一个值得注意的现象是：当显性的黑化型受到选择时，杂合子同样暴露在选择之下，因此 $C$ 即使变得稀少也会被持续清除；反之，当选择偏好显性型时，稀有的隐性等位基因 $c$ 大多藏在杂合子中，最后阶段的变化会很慢。
4. 期望数 $N\mu^{k}$：$k = 1$ 时为 $10^{4}$，至少 1 个的概率约为 1；$k = 2$ 时为 0.1，概率约为 0.095；$k = 3$ 时为 $10^{-6}$，概率约为 $10^{-6}$。单药治疗时，耐药变异体在治疗开始前几乎必然已经存在，药物只是把它们筛选出来，因此耐药很快出现；同时使用三种药物时，预存的三重耐药变异体几乎不可能存在，而病毒复制受到压制后，新突变产生的机会也随之减少。
5. 达尔文雀：亲子回归估计遗传力，并检验子代平均值的实际变化与 $R = h^{2}S$ 的预测是否一致。桦尺蛾：体色型按孟德尔方式遗传，致因突变（*cortex* 中的转座元件插入）已经确定，可以直接对等位基因计数。孔雀鱼：在共同的实验室环境中饲养引种群体与源群体的后代（共同园实验），若差异在相同环境下依然存在，就说明差异具有遗传基础。HIV：对病毒基因组测序，直接检测耐药突变，并在体外测定药物敏感性。遗传证据最直接的是桦尺蛾和 HIV，因为它们的致因突变已被鉴定。
6. 主要批评与回应：(1) 把蛾子放在树干上，而树干被认为不是自然停歇位置；Majerus 记录了野外蛾子的自然停歇位置，并让释放的个体自行选择停歇处。(2) 释放密度远高于自然密度，可能吸引鸟类针对性捕食；Majerus 以低的、接近自然的密度释放。(3) 部分实验使用了固定的死蛾；Majerus 使用活的本地个体。尚未完全解决的问题包括：各地区、各年份的选择强度是否相同；迁移对局部频率的影响；以及除鸟类捕食之外的其他选择因素。方法上的缺陷只削弱了某一项实验的证据力，并不直接说明结论错误；改进设计后重复实验得到一致结果，反而增强了结论的可信度，这正是科学自我纠正的过程。

</details>

---

## 关键术语

| 中文 | English | 释义 |
|---|---|---|
| 当代微进化 | contemporary microevolution | 在数十年乃至数年内可以直接测量的群体遗传组成与性状的变化 |
| 表型可塑性 | phenotypic plasticity | 同一基因型在不同环境中产生不同表型的能力 |
| 选择差 | selection differential | 被选择个体的性状平均值与选择前群体平均值之差 |
| 狭义遗传力 | narrow-sense heritability | 表型方差中可由加性遗传方差解释的比例 |
| 选择响应 | response to selection | 选择之后子代平均值相对于原群体的变化 |
| 育种者方程 | breeder's equation | 选择响应等于狭义遗传力与选择差之积，$R = h^{2}S$ |
| 波动选择 | fluctuating selection | 方向或强度随时间改变的自然选择 |
| 性状替换 | character displacement | 亲缘物种在共存时因竞争等相互作用而在性状上发生分化 |
| 工业黑化 | industrial melanism | 工业污染环境中黑化型个体频率上升的现象 |
| 标记—释放—重捕 | mark–release–recapture | 标记个体后释放，再通过重捕比例估计存活或种群参数的方法 |
| 引种实验 | introduction experiment | 把生物移入新环境，以检验特定选择压力所引起的进化 |
| 共同园实验 | common-garden experiment | 在相同环境中饲养或栽培不同来源的个体，以区分遗传差异与环境效应 |
| 耐药性 | drug resistance | 病原体在药物存在下仍能存活与增殖的能力 |
| 达尔文单位 | darwin | 进化速率单位：每百万年 $e$ 倍的性状变化 |
| 霍尔丹单位 | haldane | 进化速率单位：每代变化的标准差数 |

---

## 参考文献

- Boag, P. T., & Grant, P. R. (1981). Intense natural selection in a population of Darwin's finches (Geospizinae) in the Galápagos. *Science, 214*(4516), 82–85. https://doi.org/10.1126/science.214.4516.82
- Cook, L. M. (2003). The rise and fall of the *carbonaria* form of the peppered moth. *The Quarterly Review of Biology, 78*(4), 399–417. https://doi.org/10.1086/378925
- Cook, L. M., Grant, B. S., Saccheri, I. J., & Mallet, J. (2012). Selective bird predation on the peppered moth: The last experiment of Michael Majerus. *Biology Letters, 8*(4), 609–612. https://doi.org/10.1098/rsbl.2011.1136 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC3391436)］
- Endler, J. A. (1980). Natural selection on color patterns in *Poecilia reticulata*. *Evolution, 34*(1), 76–91. https://doi.org/10.1111/j.1558-5646.1980.tb04790.x
- Gingerich, P. D. (1983). Rates of evolution: Effects of time and temporal scaling. *Science, 222*, 159–161.（DOI 未核实）
- Grant, P. R., & Grant, B. R. (2002). Unpredictable evolution in a 30-year study of Darwin's finches. *Science, 296*(5568), 707–711. https://doi.org/10.1126/science.1070315
- Grant, P. R., & Grant, B. R. (2006). Evolution of character displacement in Darwin's finches. *Science, 313*(5784), 224–226. https://doi.org/10.1126/science.1128374
- Haldane, J. B. S. (1949). Suggestions as to quantitative measurement of rates of evolution. *Evolution, 3*(1), 51–56. https://doi.org/10.1111/j.1558-5646.1949.tb00004.x
- Hendry, A. P., & Kinnison, M. T. (1999). The pace of modern life: Measuring rates of contemporary microevolution. *Evolution, 53*(6), 1637–1653. https://doi.org/10.1111/j.1558-5646.1999.tb04550.x
- Kettlewell, H. B. D. (1955). Selection experiments on industrial melanism in the Lepidoptera. *Heredity, 9*(3), 323–342. https://doi.org/10.1038/hdy.1955.36
- Larder, B. A., Darby, G., & Richman, D. D. (1989). HIV with reduced sensitivity to zidovudine (AZT) isolated during prolonged therapy. *Science, 243*(4899), 1731–1734. https://doi.org/10.1126/science.2467383
- Reznick, D. N., Shaw, F. H., Rodd, F. H., & Shaw, R. G. (1997). Evaluation of the rate of evolution in natural populations of guppies (*Poecilia reticulata*). *Science, 275*(5308), 1934–1937. https://doi.org/10.1126/science.275.5308.1934 ［[作者主页 PDF](https://faculty.ucr.edu/~gupy/Reznick%20edit/Publications/Science1997.pdf)］
- van't Hof, A. E., Campagne, P., Rigden, D. J., Yung, C. J., Lingley, J., Quail, M. A., Hall, N., Darby, A. C., & Saccheri, I. J. (2016). The industrial melanism mutation in British peppered moths is a transposable element. *Nature, 534*(7605), 102–105. https://doi.org/10.1038/nature17951

**网络资源**（访问日期 2026-11-13）

- HHMI BioInteractive. (2013). *The origin of species: The beak of the finch* [Film]. Howard Hughes Medical Institute. https://www.biointeractive.org/classroom-resources/origin-species-beak-finch
- University of California Museum of Paleontology. (n.d.). [Page on John Endler's guppy experiments]. Understanding Evolution. https://evolution.berkeley.edu/evolibrary/article/0_0_0/lines_15

---

**上一讲** [Day 010 · 进化的证据 IV：分子证据与普遍共同祖先](day010-molecular-evidence.md) ｜ **下一讲** Day 012 · 树状思维 I：如何阅读系统发育树
