# Day 019 · 基因组变异的形式与群体测序数据

> **部分** 第一部分 概念基础与证据 ｜ **周次** 第 3 周 遗传变异的来源 ｜ **发布日期** 2026-11-21 ｜ **建议用时** 约 100 分钟（讲义 45′ · 主读／主看 30′ · 练习 25′）
> **主读** EG 第 1 章（Youssef, Budd & Bielawski 2019）；1000 Genomes Project Consortium（2015）
> **关键词** single-nucleotide variant (SNV) · indel · structural variant (SV) · copy-number variant (CNV) · mobile element insertion · aneuploidy · polyploidy · haplotype · phasing · sequencing depth · genotype likelihood · variant call format (VCF) · reference bias · pangenome

## 学习目标

完成本讲后，应能够：

1. 区分 SNV、indel、各类结构变异与倍性变化，并比较它们在变异数目与所影响碱基数上的贡献；
2. 概述从测序读段到个体基因型的基本流程，解释测序深度与基因型不确定性之间的关系；
3. 读懂 VCF 文件的基本结构，并由其中的基因型计算等位基因频率与杂合度；
4. 解释单倍型与定相的概念，以及定相信息在进化分析中的用途；
5. 说明参考偏倚的来源与后果，以及泛基因组参考的动机与初步成果。

---

## 1 从突变到群体中的变异

Day 016–018 讨论了新变异如何产生：点突变、indel、结构变异，以及重组造成的新组合。本讲转向群体中现存的变异：在一个群体样本中，这些变异以什么形式存在，又如何被测量与记录。第二部分（第 4–8 周）的群体遗传学各讲以及此后的许多讲次，都以这类数据为分析对象。

先明确几个术语。在一个样本中存在两个或以上等位基因的位点称为**多态位点**（polymorphic site）。单个碱基位置上的差异统称**单核苷酸变异**（single-nucleotide variant, SNV）；习惯上，**单核苷酸多态性**（single-nucleotide polymorphism, SNP）常指在群体中达到一定频率的 SNV，但许多文献并不区分二者，千人基因组计划就把所有频率的单碱基变异都称为 SNP（1000 Genomes Project Consortium 2015）。阅读文献时应留意作者采用的是哪种用法。

---

## 2 基因组变异的形式

### 2.1 SNV 与短 indel

就数目而言，SNV 与短 **indel**（少量碱基的插入或缺失）占绝对多数。千人基因组计划第三阶段在 2,504 个个体中发现了 8800 多万个变异位点，其中包括 8470 万个 SNP、360 万个短 indel 与 6 万个结构变异；一个典型的个体基因组与参考基因组在 410 万至 500 万个位点上不同，其中 99.9% 以上是 SNP 与短 indel（1000 Genomes Project Consortium 2015）。

### 2.2 结构变异

**结构变异**（structural variant, SV；Day 016）包括大片段的缺失、重复（造成拷贝数变异，CNV）、**倒位**（inversion）、易位，以及插入。插入中重要的一类是**移动元件插入**（mobile element insertion, MEI），即转座元件在基因组中的新拷贝。人类基因组中 L1（LINE-1）、Alu 与 SVA 等非 LTR 逆转座子约占基因组的三分之一，其中仅 L1 就约占 17%；这类元件是人类近期进化中最活跃的转座元件，Alu 与 SVA 自身不能转座，而是借用 L1 的转座机器（Cordaux & Batzer 2009）。这些元件的插入在个体之间存在多态，可用于追溯谱系关系（Day 010）。

结构变异的数目远少于 SNV，但每个变异涉及的碱基多得多。千人基因组计划估计，一个典型基因组含有 2100 至 2500 个结构变异，包括约 1000 个大片段缺失、约 160 个拷贝数变异、约 915 个 Alu 插入、约 128 个 L1 插入、约 51 个 SVA 插入、约 4 个核内线粒体序列插入与约 10 个倒位，共涉及约 2000 万个碱基，多于 SNP 与短 indel 所影响的碱基数（1000 Genomes Project Consortium 2015；练习 1）。换言之，若以变异数目计，个体差异主要是 SNV；若以碱基计，结构变异的贡献更大。

结构变异也较难检测：短读段往往跨不过整个变异，而落在重复序列中的读段难以唯一地比对。第 4.2 节将看到，改用泛基因组参考后，每个单倍型检出的结构变异数目可以成倍增加（Liao et al. 2023）。

### 2.3 倍性变化

个别染色体数目的增减称为**非整倍性**（aneuploidy），整套染色体组的增加称为多倍化。在群体测序数据中，倍性决定一个位点上可能的基因型数目：对两个等位基因而言，二倍体有 3 种基因型，四倍体有 5 种，标准的二倍体基因型模型因此不能直接用于多倍体。多倍化及其在植物物种形成中的作用将在 Day 087 讨论。

---

## 3 从测序读段到基因型

### 3.1 变异识别与测序深度

高通量测序产生大量短的**读段**（read）。分析时先把读段比对到参考基因组上，再在每个位置比较读段与参考序列，判断个体在该处的基因型，这一过程称为**变异识别**（variant calling）。覆盖某一位置的读段数称为**测序深度**（sequencing depth）。

基因型是由读段推断的，而不是直接观察到的。对一个杂合位点，每条读段大致以 1/2 的概率来自两条同源染色体中的任一条；深度较低时，所有读段可能恰好都来自同一条染色体，杂合子便会被误判为纯合子。现代方法因此计算**基因型似然**（genotype likelihood），即在每种可能的基因型下观察到这些读段的概率，而不是只给出一个硬性判断（练习 4）。

千人基因组计划第三阶段对每个个体进行了平均深度 7.4× 的低覆盖度全基因组测序与平均 65.7× 的外显子测序，并结合了高密度芯片分型（1000 Genomes Project Consortium 2015）。这样的设计以较低的成本覆盖大量个体，代价是单个个体在单个位点上的基因型不确定性较大。

### 3.2 VCF 格式

**VCF**（variant call format）是为存储最常见的几类序列变异而设计的标准格式（Danecek et al. 2011）。文件以 `##` 开头的元信息行描述各字段的含义，随后是一行列标题与每个变异位点一行的数据。前 8 列依次为染色体（CHROM）、位置（POS）、标识符（ID）、参考等位基因（REF）、替代等位基因（ALT，多个时以逗号分隔）、质量值（QUAL）、过滤状态（FILTER，通过时为 PASS）与附加信息（INFO）；第 9 列（FORMAT）说明各样本列中字段的顺序，此后每列对应一个样本。

最重要的样本字段是基因型（GT）：0 表示 REF，1 表示第一个 ALT，2 表示第二个 ALT，依此类推；两个等位基因之间用 `/` 分隔表示未定相，用 `|` 分隔表示已定相；`.` 表示缺失。按 VCF 规范，indel 的 REF 与 ALT 都包含事件前的一个碱基，例如在 C 之后插入一个 T 记为 REF = C、ALT = CT。VCF 的规范仍在更新，截至本讲撰写时检索到的最新版本为 VCFv4.5（hts-specs 项目，2025）。

### 3.3 单倍型与定相

同一条染色体上一组相邻位点的等位基因组合称为**单倍型**（haplotype）。由短读段得到的基因型通常是未定相的：一个在两个位点上都杂合的个体，可能携带 AB 与 ab 两条单倍型，也可能携带 Ab 与 aB。若个体在 $k$ 个位点上杂合，与其基因型相容的单倍型组合共有 $2^{k-1}$ 种（练习 3）。

确定每个等位基因位于哪条同源染色体上的过程称为**定相**（phasing）。定相可以利用系谱（父母与子女的基因型）、同时覆盖多个杂合位点的长读段，或者群体中共享的单倍型模式（统计定相）；Browning 与 Browning（2011）综述了这些方法，尤其是统计方法。千人基因组计划的结构变异也被统计定相到单倍型区块上（Sudmant et al. 2015）。单倍型信息是连锁不平衡分析（Day 024）、亲缘与 IBD 分析（Day 039）以及基于单倍型的选择检验（Day 075）的基础。

---

## 4 参考基因组偏倚与泛基因组

### 4.1 参考偏倚

参考基因组只是一个具体的组装序列，其上的等位基因既不一定是祖先型，也不一定是群体中最常见的类型。以它为坐标比对读段会带来系统性偏差，称为**参考偏倚**（reference bias）：携带非参考等位基因的读段与参考序列至少多一个错配，比对时得分较低，甚至可能比对失败；参考基因组中完全没有的序列，其读段则无处可放。Degner 等（2009）表明，在存在序列变异的情况下准确比对短读段，对检测等位基因特异表达至关重要，比对偏差会显著影响结果。Günther 与 Nettelblad（2019）发现，已发表的史前人类古 DNA 数据中普遍存在参考偏倚；大多数基因组区域的偏倚很小，但少数有偏位点就可能影响相关位点的分析，或使全基因组估计略有偏差；比对后的过滤策略可以显著减轻其影响。

### 4.2 泛基因组

一个物种的**泛基因组**（pangenome）指该物种多个个体基因组序列的集合。这一概念最初在细菌中提出（Sherman & Salzberg 2020），细菌中的核心基因组与可变基因组将在 Day 107 讨论。Sherman 与 Salzberg（2020）指出，单一参考基因组不能代表整个群体，构建人类泛基因组可以增强把遗传变异与人类多样性及疾病联系起来的能力。

人类泛基因组参考联盟发表的初稿包含来自 47 个遗传背景多样的个体的定相二倍体组装（94 个单倍型）。与参考基因组 GRCh38 相比，它增加了 1.19 亿个碱基的常染色质多态序列与 1115 个基因重复，其中约 9000 万个碱基来自结构变异；用它分析短读段数据时，小变异的检出错误减少了 34%，每个单倍型检出的结构变异增加了 104%（Liao et al. 2023）。这说明，以单一参考为坐标的群体数据系统性地遗漏了一部分变异，尤其是结构变异。

---

## 5 案例研究：千人基因组计划第三阶段

**问题** 一个典型的人类基因组携带多少、什么类型的变异？这些变异在群体之间如何分布？

**方法** 研究者对 26 个群体的 2,504 个个体结合使用低覆盖度全基因组测序、深度外显子测序与高密度芯片分型（1000 Genomes Project Consortium 2015）；结构变异分析组则用短读段数据识别并分型了八类结构变异，并将它们统计定相到单倍型区块上（Sudmant et al. 2015）。

**结果** 第一，大多数变异是稀有的：常染色体上约 6400 万个变异的频率低于 0.5%，约 1200 万个介于 0.5% 与 5% 之间，只有约 800 万个高于 5%。第二，非洲血统群体中的个体携带的变异位点最多，这与人类起源的走出非洲模型的预测一致（1000 Genomes Project Consortium 2015）。第三，整合图谱包含 68,818 个结构变异；其中一些与基因相交的结构变异在群体之间存在分层，自然存在的纯合基因敲除提示多种人类基因并非不可或缺；结构变异在全基因组关联研究所识别的单倍型上富集，并富集表达数量性状位点（Sudmant et al. 2015）。

**意义** 这一数据集为后续讲次提供了实例：稀有变异的优势与位点频谱（Day 045）、群体结构（Day 036–038）以及选择的检测（Day 071–075）。它的局限也正是本讲讨论的问题：低深度设计对单个个体基因型的推断不确定（练习 4），以单一参考为坐标的短读段数据会遗漏一部分结构变异（第 4.2 节）。

---

## 今日学习材料（均可免费获取）

| 类型 | 材料 | 说明 |
|---|---|---|
| 必读 | EG 第 1 章：Youssef, Budd & Bielawski（2019）[Introduction to genome biology and diversity](https://doi.org/10.1007/978-1-4939-9074-0_1) | 基因组作为生物多样性的结构与信息单元，开放获取，浏览约 30 分钟 |
| 精读 | 1000 Genomes Project Consortium（2015）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC4750478) | 研究设计与主要结果 |
| 精读 | Sudmant et al.（2015）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC4617611) | 八类结构变异的整合图谱 |
| 选读 | Danecek et al.（2011）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC3137218)；[VCF 规范（hts-specs）](https://github.com/samtools/hts-specs) | VCF 格式的设计与现行规范 |
| 选读 | Sherman & Salzberg（2020）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC7752153)；Liao et al.（2023）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC10172123) | 泛基因组的概念与人类泛基因组参考初稿 |
| 实践 | [IGSR 数据门户](https://www.internationalgenome.org/) | 浏览千人基因组计划的样本与变异数据 |

---

## 思考与练习

1. **（计算）** 设人类单倍体基因组约 $3.1 \times 10^{9}$ bp（本题取近似值）。(a) 一个典型基因组与参考基因组在 410 万至 500 万个位点上不同，这相当于全部碱基的百分之几？(b) 若每个 SNV 或短 indel 位点只影响 1 至数个碱基，而结构变异共涉及约 2000 万个碱基，二者所影响的碱基数之比大约是多少？(c) 为什么"变异数目"与"变异所影响的碱基数"会给出不同的图景？
2. **（计算）** 下面是一个虚构的 VCF 片段（4 个二倍体个体）。

   ```
   #CHROM  POS  ID  REF  ALT  QUAL  FILTER   INFO  FORMAT  I1   I2   I3   I4
   ctg1    101  .   G    A    50    PASS     .     GT      0|0  0|1  1|1  0|1
   ctg1    245  .   C    G    50    PASS     .     GT      0|1  0|0  0|0  0|0
   ctg1    380  .   C    CT   40    PASS     .     GT      0/1  0/0  ./.  1/1
   ctg1    512  .   G    A,C  60    PASS     .     GT      0|2  1|2  0|0  0|1
   ctg1    777  .   TA   T    35    LowQual  .     GT      0/0  0/1  0/1  0/0
   ```

   (a) 判断每个位点的变异类型，并计算各 ALT 等位基因的频率（只计入非缺失的基因型）。(b) 计算 101 与 512 两个位点的观察杂合度与期望杂合度（$1 - \sum_i p_i^{2}$）。(c) 写出 I2 在 101 与 512 两个位点上的两条单倍型。(d) 在只使用高质量数据的分析中，哪个位点应被排除？
3. **（计算）** (a) 一个未定相的个体在 $k$ 个位点上杂合，为什么与其基因型相容的单倍型组合有 $2^{k-1}$ 种？分别计算 $k = 2$、10 与 20 时的数目。(b) 为什么群体中共享的单倍型模式可以帮助定相？
4. **（计算）** 某个体在一个位点上杂合。设覆盖该位点的读段相互独立，每条读段来自两条同源染色体的概率相等；又设携带 ALT 的读段比对成功的概率是携带 REF 读段的 $w$ 倍（本题参数为假设）。(a) 当 $w = 1$ 与 $w = 0.9$ 时，比对后的读段中 ALT 读段的期望比例各是多少？(b) 若比对后的深度为 4、7 与 30，在上述两种情况下所有读段都不含 ALT 的概率各是多少？(c) 这对低覆盖度测序的群体数据意味着什么？
5. **（概念）** 判断并纠正：(a)"SNV 的数目远多于结构变异，所以个体之间的序列差异主要来自 SNV。"(b)"VCF 中 `0/1` 与 `0|1` 表示相同的信息。"(c)"参考基因组上的等位基因就是人类的祖先型或'正常'型。"(d)"测序深度只影响检测灵敏度，不会使等位基因频率的估计产生系统偏差。"
6. **（文献评论）** 比较千人基因组计划第三阶段（1000 Genomes Project Consortium 2015；Sudmant et al. 2015）与人类泛基因组参考初稿（Liao et al. 2023）的研究设计。两者分别能可靠地回答哪些问题？对依赖这些数据的进化推断（例如估计遗传多样性或检测选择）而言，参考偏倚与结构变异的遗漏可能带来什么问题？

<details>
<summary>答案要点</summary>

1. (a) 约 0.13% 至 0.16%（代码验算）。(b) 约 2000 万 : 400 万至 500 万，即结构变异影响的碱基数约为 SNV 与短 indel 的 4 至 5 倍（若 indel 平均影响不止 1 个碱基，倍数会略小）。(c) 每个 SNV 只改变 1 个碱基，而一个结构变异可涉及成百上千乃至更多碱基；因此 SNV 在数目上占绝对多数（99.9% 以上），结构变异却影响更多碱基（1000 Genomes Project Consortium 2015）。
2. (a) 101、245：SNV，ALT 频率分别为 0.5 与 0.125；380：插入（C→CT），I3 缺失，在 6 个等位基因中 ALT 频率为 0.5；512：多等位 SNV，A 与 C 的频率均为 0.25；777：缺失（TA→T），ALT 频率 0.25。(b) 101：观察杂合度 2/4 = 0.5，期望杂合度 $2pq = 0.5$；512：观察杂合度 3/4 = 0.75，期望杂合度 $1 - (0.5^{2} + 0.25^{2} + 0.25^{2}) = 0.625$（代码验算）。只有 4 个个体时，这样的差异不足以说明偏离 Hardy–Weinberg 平衡（Day 022–023）。(c) 两个位点都已定相：I2 的第一条单倍型为 G（101）–A（512），第二条为 A（101）–C（512）。(d) 777 位点的 FILTER 为 LowQual，应被排除。
3. (a) 每个杂合位点上的两个等位基因可以分配到两条单倍型中的任一条，共 $2^{k}$ 种分配；交换两条单倍型的名称得到的是同一组合，故为 $2^{k-1}$：$k = 2$ 时 2 种，$k = 10$ 时 512 种，$k = 20$ 时 524,288 种。(b) 群体中的单倍型由共同祖先传承而来，在短距离内只有少数几种常见组合；与群体中已知单倍型相符的组合可能性更大，统计定相正是利用这种共享模式（Browning & Browning 2011）。
4. (a) $w/(1 + w)$：$w = 1$ 时为 0.5，$w = 0.9$ 时约为 0.474。(b) $(1 - f)^{n}$：$w = 1$ 时依次约为 0.0625、0.0078 与 $9.3 \times 10^{-10}$；$w = 0.9$ 时依次约为 0.077、0.011 与 $4.3 \times 10^{-9}$（代码验算）。(c) 低深度下，杂合子有相当的概率被误判为纯合参考型，而参考偏倚使这一误差系统地偏向 REF，导致非参考等位基因的频率与杂合度被低估；因此低覆盖度数据需要用基因型似然、并结合多个个体的信息进行分析，而不能逐个个体硬性判定基因型。
5. (a) 部分正确：以变异数目计确实主要是 SNV，但以碱基计，结构变异影响的碱基更多（1000 Genomes Project Consortium 2015）。(b) 错误。`/` 表示未定相，`|` 表示已定相，后者表示在同一定相区块内，各位点上写在前面的等位基因位于同一条单倍型上。(c) 错误。参考基因组只是一个具体的组装序列，其上的等位基因可能是衍生型，也可能是稀有型；单一参考不能代表整个群体（Sherman & Salzberg 2020）。(d) 错误。低深度会使杂合子被误判为纯合子，参考偏倚又使误判偏向参考等位基因，二者都会造成系统偏差（练习 4；Günther & Nettelblad 2019）。
6. 千人基因组计划第三阶段：样本量大、覆盖多个群体，适合估计常见变异的频率与群体间差异，并提供了结构变异的群体图谱；但低深度短读段设计对单个个体的基因型、稀有变异与复杂结构变异的推断有限，而且以单一参考为坐标。泛基因组初稿：个体数少，但每个个体都有高质量的定相组装，能发现参考基因组中缺失的序列与复杂结构变异，并改善短读段分析（Liao et al. 2023）；目前尚不足以估计各群体中的变异频率。对进化推断而言，参考偏倚会系统地低估非参考等位基因的频率，并可能在数据质量不同的样本之间造成虚假的差异（Günther & Nettelblad 2019）；遗漏的结构变异则使多样性被低估，并可能遗漏受选择的变异。

</details>

---

## 关键术语

| 中文 | English | 释义 |
|---|---|---|
| 多态位点 | polymorphic site | 样本中存在两个或以上等位基因的位点 |
| 单核苷酸变异 | single-nucleotide variant (SNV) | 单个碱基位置上的序列差异，不论其在群体中的频率 |
| 单核苷酸多态性 | single-nucleotide polymorphism (SNP) | 习惯上指在群体中达到一定频率的单核苷酸变异，许多文献与 SNV 混用 |
| 插入缺失 | insertion–deletion (indel) | 少量碱基的插入或缺失 |
| 倒位 | inversion | 染色体片段方向颠倒的结构变异 |
| 移动元件插入 | mobile element insertion (MEI) | 转座元件的新拷贝插入基因组造成的结构变异 |
| 非整倍性 | aneuploidy | 个别染色体数目增加或减少的状态 |
| 变异识别 | variant calling | 由比对到参考基因组的读段推断各位点变异与基因型的过程 |
| 测序深度 | sequencing depth | 覆盖基因组某一位置的读段数 |
| 基因型似然 | genotype likelihood | 在某一基因型下观察到现有读段数据的概率 |
| VCF 格式 | variant call format (VCF) | 存储序列变异与样本基因型的标准文本格式 |
| 单倍型 | haplotype | 同一条染色体上一组相邻位点的等位基因组合 |
| 定相 | phasing | 确定杂合位点上各等位基因分别位于哪条同源染色体上的过程 |
| 参考偏倚 | reference bias | 以参考基因组为坐标分析数据时，偏向参考等位基因的系统误差 |
| 泛基因组 | pangenome | 一个物种多个个体基因组序列的集合 |

---

## 参考文献

- 1000 Genomes Project Consortium. (2015). A global reference for human genetic variation. *Nature, 526*(7571), 68–74. https://doi.org/10.1038/nature15393 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC4750478)］
- Browning, S. R., & Browning, B. L. (2011). Haplotype phasing: Existing methods and new developments. *Nature Reviews Genetics, 12*(10), 703–714. https://doi.org/10.1038/nrg3054 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC3217888)］
- Cordaux, R., & Batzer, M. A. (2009). The impact of retrotransposons on human genome evolution. *Nature Reviews Genetics, 10*(10), 691–703. https://doi.org/10.1038/nrg2640 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC2884099)］
- Danecek, P., Auton, A., Abecasis, G., Albers, C. A., Banks, E., DePristo, M. A., Handsaker, R. E., Lunter, G., Marth, G. T., Sherry, S. T., McVean, G., Durbin, R., & 1000 Genomes Project Analysis Group. (2011). The variant call format and VCFtools. *Bioinformatics, 27*(15), 2156–2158. https://doi.org/10.1093/bioinformatics/btr330 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC3137218)］
- Degner, J. F., Marioni, J. C., Pai, A. A., Pickrell, J. K., Nkadori, E., Gilad, Y., & Pritchard, J. K. (2009). Effect of read-mapping biases on detecting allele-specific expression from RNA-sequencing data. *Bioinformatics, 25*(24), 3207–3212. https://doi.org/10.1093/bioinformatics/btp579 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC2788925)］
- Günther, T., & Nettelblad, C. (2019). The presence and impact of reference bias on population genomic studies of prehistoric human populations. *PLoS Genetics, 15*(7), e1008302. https://doi.org/10.1371/journal.pgen.1008302 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC6685638)］
- Liao, W.-W., Asri, M., Ebler, J., Doerr, D., Haukness, M., Hickey, G., Lu, S., Lucas, J. K., Monlong, J., Abel, H. J., Buonaiuto, S., Chang, X. H., Cheng, H., Chu, J., Colonna, V., Eizenga, J. M., Feng, X., Fischer, C., Fulton, R. S., … Paten, B. (2023). A draft human pangenome reference. *Nature, 617*(7960), 312–324. https://doi.org/10.1038/s41586-023-05896-x ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC10172123)］
- Sherman, R. M., & Salzberg, S. L. (2020). Pan-genomics in the human genome era. *Nature Reviews Genetics, 21*(4), 243–254. https://doi.org/10.1038/s41576-020-0210-7 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC7752153)］
- Sudmant, P. H., Rausch, T., Gardner, E. J., Handsaker, R. E., Abyzov, A., Huddleston, J., Zhang, Y., Ye, K., Jun, G., Hsi-Yang Fritz, M., Konkel, M. K., Malhotra, A., Stütz, A. M., Shi, X., Casale, F. P., Chen, J., Hormozdiari, F., Dayama, G., Chen, K., … Korbel, J. O. (2015). An integrated map of structural variation in 2,504 human genomes. *Nature, 526*(7571), 75–81. https://doi.org/10.1038/nature15394 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC4617611)］
- Youssef, N., Budd, A., & Bielawski, J. P. (2019). Introduction to genome biology and diversity. In M. Anisimova (Ed.), *Evolutionary genomics: Statistical and computational methods* (2nd ed., Methods in Molecular Biology, Vol. 1910, pp. 3–31). Humana Press. https://doi.org/10.1007/978-1-4939-9074-0_1

**网络资源**（访问日期 2026-11-21）

- hts-specs. (2025). *The Variant Call Format specification, VCFv4.5 and BCFv2.2*. https://github.com/samtools/hts-specs
- International Genome Sample Resource. (n.d.). *IGSR: The International Genome Sample Resource*. EMBL-EBI. https://www.internationalgenome.org/

---

**上一讲** [Day 018 · 重组：交叉、基因转换与重组热点](day018-recombination-hotspots.md) ｜ **下一讲** [Day 020 · 从基因型到表型：上位性、多效性与可塑性](day020-genotype-to-phenotype.md)
