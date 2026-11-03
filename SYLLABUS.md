# 逐日课表（Syllabus）

> 26 周 · 182 天 · 每周 6 讲 + 1 次复盘（第 7k 天）· 每日约 60–90 分钟
> 本文件是每日讲义的唯一依据。每讲的完整讲义发布于 [`lessons/`](lessons/README.md)。
> 文献在此仅列"作者 年份"；完整题录与经核实的 DOI 见当日讲义及 [`references.bib`](references.bib)。

## 资源代号

| 代号 | 资源 | 链接 |
|---|---|---|
| OS | OpenStax *Biology 2e*（CC BY 4.0），第 4 单元 Evolutionary Processes（第 18–20 章） | <https://openstax.org/details/books/biology-2e> |
| UE | *Understanding Evolution*（UC Berkeley 古生物博物馆），含 Evolution 101 | <https://evolution.berkeley.edu/> |
| Y | Yale EEB 122 *Principles of Evolution, Ecology and Behavior*（S. C. Stearns，2009） | <https://oyc.yale.edu/ecology-and-evolutionary-biology/eeb-122> |
| Coop | G. Coop，*Population and Quantitative Genetics* 讲义（UC Davis） | <https://github.com/cooplab/popgen-notes> |
| Hol | K. E. Holsinger，*Lecture Notes in Population Genetics*（UConn，CC BY-SA） | <https://darwin.eeb.uconn.edu/uncommon-ground/eeb348/notes> |
| Fel | J. Felsenstein，*Theoretical Evolutionary Genetics*（免费 PDF） | <https://felsenst.github.io/pgbook/pgbook.html> |
| PCM | L. J. Harmon，*Phylogenetic Comparative Methods: Learning from Trees*（CC BY 4.0） | <https://lukejharmon.github.io/pcm/> |
| PGE | Scornavacca, Delsuc & Galtier (eds.)，*Phylogenetics in the Genomic Era*（CC BY-NC-ND 4.0） | <https://hal.archives-ouvertes.fr/hal-02535070/file/book_hyperef_v2_ISBN.pdf> |
| EG | Anisimova (ed.)，*Evolutionary Genomics: Statistical and Computational Methods*（2nd ed.，MiMB 1910，开放获取） | <https://doi.org/10.1007/978-1-4939-9074-0> |
| SPG | Dutheil (ed.)，*Statistical Population Genomics*（MiMB 2090，CC BY 4.0） | <https://doi.org/10.1007/978-1-0716-0199-0> |
| EXP | *Explorations: An Open Invitation to Biological Anthropology*（2nd ed.，CC BY-NC 4.0） | <https://explorations.americananthro.org/> |
| HHMI | HHMI BioInteractive 短片与互动材料 | <https://www.biointeractive.org/> |
| SEP | *Stanford Encyclopedia of Philosophy* 相关条目 | <https://plato.stanford.edu/> |
| DO | *The Complete Work of Charles Darwin Online* | <https://darwin-online.org.uk/> |
| Lewis | P. O. Lewis，UConn EEB 5349 *Phylogenetics* 课程讲义 | <https://plewis.github.io/phylogenetics2026/> |
| msp | msprime / tskit 官方教程 | <https://tskit-dev.github.io/tutorials/> |
| IQ | IQ-TREE 文档与工作坊教程 | <https://iqtree.github.io/> |
| RB | RevBayes 教程 | <https://revbayes.github.io/tutorials> |
| TtB | *Taming the BEAST* 教程 | <https://taming-the-beast.org/> |
| evo | evomics 工作坊学习材料（群体与物种形成基因组学、系统发育基因组学） | <https://evomics.org/learning/population-and-speciation-genomics/> |
| SLiM | SLiM 正向演化模拟（手册与自学工作坊材料） | <https://messerlab.org/slim/> |

> 说明：Yale 讲次编号仅标注已核实者（第 1、2、3、4、6、9、10、12、16、17、36 讲），其余只写讲次标题。各资源的评述见 [RESOURCES.md](RESOURCES.md)。

---

## 第一部分 概念基础与证据（第 1–3 周）

### 第 1 周 导论：问题、概念与思想史
**本周目标**：建立进化生物学的概念框架；理解学科思想史的主线；掌握自然选择的逻辑与适应主义之争。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 001 | 进化生物学导论：研究对象、解释层次与核心问题 | 进化的定义；微进化与宏进化；近因与终极因；Tinbergen 四问；Lewontin 三条件 | UE Evolution 101 引言；Y 第 1 讲 | Dobzhansky 1973；Mayr 1961；Tinbergen 1963；Lewontin 1970 |
| 002 | 进化思想史 I：从自然神学到达尔文与华莱士 | Paley 的设计论证；Lamarck；Cuvier 与 Lyell；Malthus；1858 年林奈学会宣读；《物种起源》的论证结构 | DO：《物种起源》（1859）第 4 章与第 14 章 | Darwin & Wallace 1858；Darwin 1859 |
| 003 | 进化思想史 II：孟德尔遗传与现代综合 | 融合遗传难题；孟德尔学派与生物统计学派之争；Fisher、Haldane、Wright；Dobzhansky、Mayr、Simpson | Y 第 2 讲 Basic Transmission Genetics；SEP 相关条目 | Fisher 1918；Wright 1931；Dobzhansky 1937（书） |
| 004 | 进化思想史 III：中性理论与"扩展综合"之争 | 蛋白质多态性的发现；中性理论；分子钟；扩展进化综合（EES）与标准理论之争 | UE Evolution 101 机制部分 | Lewontin & Hubby 1966；Kimura 1968；King & Jukes 1969；Laland et al. 2014 |
| 005 | 自然选择的逻辑与适应主义 | 适应的定义；扩展适应（exaptation）；副产物；适应主义纲领及其批评；如何检验适应假说 | Y 第 3 讲 Adaptive Evolution: Natural Selection；SEP "Adaptationism" | Gould & Lewontin 1979；Gould & Vrba 1982；Williams 1966（书） |
| 006 | 进化的证据 I：同源性与比较解剖 | 同源与同塑（homoplasy）；系列同源；痕迹结构；胚胎学证据；生物学同源概念 | OS §18.1；UE 进化证据部分 | Wagner 1989 |
| 007 | 第 1 周复盘 | 概念图；综合习题；文献精读 | — | 精读：Gould & Lewontin 1979 |

### 第 2 周 进化的证据与树状思维
**本周目标**：综合评价进化的多重独立证据；正确阅读、解释与比较系统发育树。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 008 | 进化的证据 II：化石记录与过渡形态 | 地层与放射性定年；化石记录的不完整性；过渡化石作为可检验预测（*Tiktaalik*） | Y《The Fossil Record and Life's History》；UE | Daeschler, Shubin & Jenkins 2006；Shubin, Daeschler & Jenkins 2006 |
| 009 | 进化的证据 III：生物地理学 | 替代分布与扩散；Wallace 线；海洋岛与大陆岛；岛屿特有性 | OS §18.1；UE | Wallace 1876（书）；MacArthur & Wilson 1967（书） |
| 010 | 进化的证据 IV：分子证据与普遍共同祖先 | 遗传密码的普遍性；共享假基因与内源逆转录病毒插入；分子系统发育的嵌套层级；普遍共同祖先的形式检验 | UE；Theobald《29+ Evidences for Macroevolution》（TalkOrigins） | Zuckerkandl & Pauling 1965；Theobald 2010 |
| 011 | 正在发生的进化：直接观测 | 达尔文雀喙形的逐年变化；桦尺蛾工业黑化；孔雀鱼引种实验；病原体耐药 | HHMI 达尔文雀短片 | Grant & Grant 2002；Cook et al. 2012；Reznick et al. 1997 |
| 012 | 树状思维 I：如何阅读系统发育树 | 根、节点与枝长；单系、并系、多系；姐妹群；节点旋转等价；"进化阶梯"误读 | OS 第 20 章（§20.1–20.2）；Y《Phylogeny and Systematics》 | Baum, Smith & Donovan 2005；Gregory 2008 |
| 013 | 树状思维 II：系统分类与命名 | 林奈等级与分支分类；共有衍征；系统发育命名（PhyloCode）；"活化石""缺失环节"辨析 | OS §20.3；Lewis 讲义（单系、并系、多系） | Hennig 1965；de Queiroz & Gauthier 1992 |
| 014 | 第 2 周复盘 | 证据整合；读树练习；文献精读 | — | 精读：Theobald 2010 |

### 第 3 周 遗传变异的来源
**本周目标**：理解突变、重组与基因组结构变异如何产生可遗传变异；区分基因型变异与表型变异。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 015 | 遗传学回顾：孟德尔遗传、连锁与重组 | 分离与自由组合；连锁与遗传图距；减数分裂；从 DNA 到表型 | Y 第 2 讲；OS 第 12–13 章 | Mendel 1866；Sturtevant 1913 |
| 016 | 突变 I：类型、速率与测定 | 点突变、插入缺失与结构变异；每代每位点突变率；突变积累实验；亲子三联体测序；父龄效应 | Y 第 6 讲 The Origin and Maintenance of Genetic Variation；Coop | Kong et al. 2012；Lynch et al. 2016 |
| 017 | 突变 II：随机性与适合度效应分布 | 波动检验与影印平板；"突变相对于适应是随机的"的确切含义；DFE 的估计；突变偏向及其争议 | UE 突变部分；Hol | Luria & Delbrück 1943；Lederberg & Lederberg 1952；Eyre-Walker & Keightley 2007；Monroe et al. 2022 |
| 018 | 重组：交叉、基因转换与重组热点 | 交叉干涉；基因转换；PRDM9 与重组热点；重组率的变异 | Coop 连锁与重组相关章节 | Baudat et al. 2010；Myers et al. 2010 |
| 019 | 基因组变异的形式与群体测序数据 | SNV、indel、SV、CNV、TE 插入与倍性变化；单倍型；VCF 数据；参考基因组偏倚与泛基因组 | EG 相关章节 | 1000 Genomes Project Consortium 2015；Sudmant et al. 2015 |
| 020 | 从基因型到表型：上位性、多效性与可塑性 | 基因型–表型图谱；显性与上位性；多效性；反应规范；基因型 × 环境互作 | Y《The Expression of Variation: Reaction Norms》 | Via & Lande 1985；Phillips 2008 |
| 021 | 第 3 周复盘 | 变异来源综合；文献精读（含波动检验的数学） | — | 精读：Luria & Delbrück 1943 |

---

## 第二部分 群体遗传学（第 4–8 周）

### 第 4 周 群体遗传学基础：HWE、连锁不平衡与选择模型
**本周目标**：掌握 Hardy–Weinberg 平衡作为零模型；掌握单位点选择模型与多态的维持机制。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 022 | 等位基因频率与 Hardy–Weinberg 平衡 | 基因型与等位基因频率；HWE 的假设与推导；多等位基因与 X 连锁；零模型的意义 | Coop；Hol；OS §19.1 | Hardy 1908；Weinberg 1908 |
| 023 | 偏离 HWE：近交、选型交配与群体结构 | 近交系数 F 与杂合子缺失；Wahlund 效应；HWE 的统计检验 | Coop；Hol | Wahlund 1928；Wigginton, Cutler & Abecasis 2005 |
| 024 | 连锁不平衡 | D、D′ 与 r²；LD 随重组的衰减；产生 LD 的过程；LD 作图原理 | Coop；Hol | Lewontin & Kojima 1960；Slatkin 2008 |
| 025 | 自然选择 I：单位点选择模型 | 绝对与相对适合度；选择系数；单倍体与二倍体模型；Δp 的推导；频率轨迹 | Coop；Fel；Y《How Selection Changes the Genetic Composition of Populations》 | Haldane 1924 |
| 026 | 自然选择 II：显性、超显性与平衡多态 | 显性度 h；Haldane 筛；杂合子优势；镰状细胞与疟疾；低显性与不稳定平衡 | Coop；Hol | Haldane 1927；Allison 1954 |
| 027 | 自然选择 III：频率依赖、波动选择与多态维持 | 负频率依赖选择（自交不亲和 S 等位基因、MHC）；时空异质选择；平衡选择的基因组印记 | Coop；Hol | Wright 1939；Charlesworth 2006 |
| 028 | 第 4 周复盘 | HWE 与选择模型习题；文献精读 | — | 精读：Lewontin & Hubby 1966 |

### 第 5 周 遗传漂变与有效群体大小
**本周目标**：掌握漂变的随机过程模型与 Nₑ；掌握突变–漂变与突变–选择平衡。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 029 | 遗传漂变：Wright–Fisher 与 Moran 模型 | 二项抽样；马尔可夫链；每代方差 p(1−p)/2N；吸收态；扩散近似的直观 | Coop；Fel；Y 第 4 讲 Neutral Evolution: Genetic Drift；PopG | Wright 1931；Moran 1958 |
| 030 | 杂合度丢失、固定概率与固定时间 | 杂合度按 (1−1/2N) 衰减；中性固定概率等于初始频率；条件固定时间约 4N 代 | Coop；Hol；learnPopGen | Kimura & Ohta 1969 |
| 031 | 有效群体大小 Nₑ | 近交、方差与溯祖 Nₑ；性比、繁殖方差与群体波动（调和平均）；Nₑ/N 比值 | Coop；Hol | Frankham 1995；Charlesworth 2009 |
| 032 | 漂变与选择的相互作用 | Kimura 固定概率公式；有利突变固定概率约 2s；Nₑs 与"有效中性" | Coop；Fel | Haldane 1927；Kimura 1962 |
| 033 | 突变–漂变平衡与中性多样性 | 无限等位基因与无限位点模型；θ = 4Nₑμ；期望杂合度；Ewens 抽样公式（概念） | Coop；Hol | Kimura & Crow 1964；Ewens 1972 |
| 034 | 突变–选择平衡与遗传负荷 | 平衡频率 μ/s（隐性时为 √(μ/s)）；遗传负荷；Haldane–Muller 原理；"选择的代价" | Coop；Fel | Haldane 1937；Muller 1950；Haldane 1957 |
| 035 | 第 5 周复盘 | 漂变模拟练习（PopG / learnPopGen）；文献精读 | — | 精读：Kimura 1962 |

### 第 6 周 迁移、群体结构与近交
**本周目标**：理解基因流与群体结构的度量；掌握近交、亲缘与局部适应的群体遗传学。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 036 | 基因流：岛屿模型与迁移–漂变平衡 | 大陆–岛屿模型；岛屿模型；F_ST ≈ 1/(1+4Nm) 及其局限 | Coop；Hol | Wright 1931；Whitlock & McCauley 1999 |
| 037 | F 统计量 | F_IS、F_ST、F_IT；G_ST；Weir–Cockerham 估计量；F_ST 的解释陷阱 | Hol；Coop | Wright 1951；Weir & Cockerham 1984；Holsinger & Weir 2009 |
| 038 | 距离隔离、PCA 与祖先成分推断 | 距离隔离；遗传 PCA 与地理；STRUCTURE / ADMIXTURE 的模型与误读 | Coop；SPG | Wright 1943；Pritchard, Stephens & Donnelly 2000；Novembre et al. 2008；Lawson, van Dorp & Falush 2018 |
| 039 | 近交与亲缘：IBD、亲缘系数与 ROH | 系谱近交系数；同源相同（IBD）；亲缘矩阵；纯合片段（ROH） | Coop | Malécot 1948（书）；Ceballos et al. 2018 |
| 040 | 近交衰退与杂种优势 | 部分显性与超显性假说；遗传负荷的清除（purging）；育种中的杂种优势 | Coop；Hol | Charlesworth & Charlesworth 1987；Charlesworth & Willis 2009 |
| 041 | 迁移–选择平衡与局部适应 | 迁移–选择平衡；渐变群（cline）；相互移植实验；"本地优势"判据 | Coop；Hol | Haldane 1948；Kawecki & Ebert 2004 |
| 042 | 第 6 周复盘 | 群体结构分析方法比较；文献精读 | — | 精读：Novembre et al. 2008 |

### 第 7 周 溯祖理论
**本周目标**：掌握 Kingman 溯祖及其主要推论；能用溯祖模拟检验多样性统计量的理论期望。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 043 | 溯祖 I：Kingman 溯祖 | 从 Wright–Fisher 到溯祖极限；成对溯祖时间的指数分布；k 个谱系的溯祖速率 | Coop；SPG | Kingman 1982；Hudson 1990 |
| 044 | 溯祖 II：基因树、TMRCA 与 θ 的估计量 | E[TMRCA]；总枝长；分离位点数与 Watterson 估计量；θ_π | Coop；Hol | Watterson 1975；Tajima 1983 |
| 045 | 溯祖 III：人口历史与位点频谱（SFS） | 群体增长与瓶颈对基因树形状的影响；SFS 的期望；基于 SFS 与 PSMC 的人口史推断 | SPG；Coop | Gutenkunst et al. 2009；Li & Durbin 2011 |
| 046 | 溯祖 IV：结构化溯祖与不完全谱系分选 | 结构化溯祖；分裂与迁移模型；不完全谱系分选（ILS）的群体遗传学基础 | Coop；PGE 第 3.3 章 | Pamilo & Nei 1988；Notohara 1990 |
| 047 | 带重组的溯祖：ARG 与树序列 | 祖先重组图；沿基因组变化的局部树；树序列数据结构；全基因组谱系推断（概念） | msp《Getting started with tskit》；SPG | Hudson 1983；Kelleher et al. 2016；Kelleher et al. 2019 |
| 048 | 计算实践：用 msprime 模拟溯祖 | 模拟恒定群体与瓶颈群体；计算 π、θ_W、Tajima's D 与 SFS；与理论期望比较 | msp；SPG 第 9 章（Kelleher & Lohse） | Baumdicker et al. 2022 |
| 049 | 第 7 周复盘 | 溯祖公式速查；模拟结果解读；文献精读 | — | 精读：Rosenberg & Nordborg 2002 |

### 第 8 周 中性理论、近中性理论与连锁选择
**本周目标**：理解中性与近中性理论的预测；掌握连锁选择如何塑造基因组多样性景观。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 050 | 中性理论与分子钟 | 中性替代速率等于突变率；与 Nₑ 无关的推论；中性–选择论之争 | Coop；EG | Kimura 1968；King & Jukes 1969；Kimura 1983（书） |
| 051 | 近中性理论 | 轻微有害突变；Nₑ 与选择效率；世代时间效应；对基因组特征的预测 | Coop | Ohta 1973；Ohta 1992 |
| 052 | 遗传搭车与选择清除 | 硬清除对邻近中性多样性的影响；清除宽度与 s/r；SFS 与 LD 印记 | Coop 连锁选择章节 | Maynard Smith & Haigh 1974；Kaplan, Hudson & Langley 1989 |
| 053 | 背景选择与 Hill–Robertson 干扰 | 有害突变清除对连锁位点的影响；B 值；Hill–Robertson 干扰；多样性–重组率相关 | Coop | Hill & Robertson 1966；Begun & Aquadro 1992；Charlesworth, Morgan & Charlesworth 1993 |
| 054 | Lewontin 悖论 | 多样性与普查群体大小的弱相关；连锁选择、Nₑ 波动与生活史解释 | Coop | Lewontin 1974（书）；Leffler et al. 2012；Buffalo 2021 |
| 055 | 重组的进化：遗传学理论 | Muller 棘轮；Fisher–Muller 加速适应；Hill–Robertson 效应与重组修饰子 | Y 第 9 讲 The Evolution of Sex；Coop | Muller 1964；Felsenstein 1974；Otto & Lenormand 2002 |
| 056 | 第 8 周复盘 | 中性与选择的统一视角；文献精读 | — | 精读：Begun & Aquadro 1992 |

---

## 第三部分 表型进化与适应（第 9–11 周）

### 第 9 周 数量遗传学
**本周目标**：掌握方差分解、遗传力与选择响应；理解多变量进化与选择的测量。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 057 | 数量性状与多基因遗传 | 连续变异；无穷小模型；从孟德尔遗传到数量遗传 | Coop 数量遗传章节 | Fisher 1918 |
| 058 | 方差分解与遗传力 | V_P = V_A + V_D + V_I + V_E；广义与狭义遗传力；对遗传力的常见误解 | Coop | Visscher, Hill & Wray 2008 |
| 059 | 亲属相似性与遗传力估计 | 亲子回归；同胞与双生子设计；动物模型（REML）；SNP 遗传力 | Coop | Kruuk 2004；Yang et al. 2010 |
| 060 | 育种者方程与选择响应 | R = h²S；选择强度；长期选择响应与选择极限；人工选择实验 | Coop | Lush 1937（书）；Dudley & Lambert 2004 |
| 061 | 多变量进化：Lande 方程与 G 矩阵 | Δz̄ = Gβ；遗传相关与相关响应；遗传约束；"遗传最小阻力线" | Coop | Lande 1979；Schluter 1996 |
| 062 | 自然界中的选择测量 | 选择差与选择梯度；线性、二次与相关选择；选择强度的综合分析 | Coop | Lande & Arnold 1983；Kingsolver et al. 2001 |
| 063 | 第 9 周复盘 | 数量遗传计算题；文献精读 | — | 精读：Lande & Arnold 1983 |

### 第 10 周 适应的遗传学
**本周目标**：理解适应的遗传结构、适应度景观与适应的分子路径；评价进化的可预测性。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 064 | 适应的遗传结构：Fisher 几何模型 | 突变效应大小与有利概率；Kimura 的修正；Orr 的适应步长分布 | Coop | Fisher 1930（书）；Orr 1998；Orr 2005 |
| 065 | 适应度景观与上位性 | Wright 适应峰与转移平衡理论；符号上位性与可达路径；经验适应度景观 | Y 第 3 讲；Coop | Wright 1932；Weinreich et al. 2006；de Visser & Krug 2014 |
| 066 | 硬清除、软清除与多基因适应 | 新突变与常备变异；多起源软清除；多基因适应的频率微移 | Coop | Hermisson & Pennings 2005；Pritchard, Pickrell & Coop 2010 |
| 067 | 常备遗传变异与适应速度 | 常备变异的优势；古老等位基因的再利用；刺鱼 *Eda* | Coop；HHMI 刺鱼短片 | Colosimo et al. 2005；Barrett & Schluter 2008 |
| 068 | 定位适应性位点：QTL、GWAS 与功能验证 | QTL 作图；GWAS 的原理与局限；从关联到因果；*Pitx1* 增强子缺失；*Mc1r* | Coop；EG | Nachman, Hoekstra & D'Agostino 2003；Chan et al. 2010 |
| 069 | 平行进化、趋同与可预测性 | 平行与趋同的遗传基础；进化"热点"基因；约束与偶然性 | HHMI《The Making of the Fittest》系列 | Stern & Orgogozo 2008；Losos 2011；Stern 2013 |
| 070 | 第 10 周复盘 | 适应遗传学综合；文献精读 | — | 精读：Colosimo et al. 2005 |

### 第 11 周 检测自然选择与实验进化
**本周目标**：掌握主要的选择检测方法及其假设、混杂因素与适用时间尺度；理解实验进化的逻辑。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 071 | 选择的分子印记：总览 | 不同时间尺度的信号；零模型；人口史、突变与重组异质性的混杂 | EG 选择检测章节 | Nielsen 2005 |
| 072 | dN/dS 与密码子替代模型 | 同义与非同义位点；NG86；GY94；位点、分支与分支–位点模型；PAML 与 HyPhy | EG；PGE | Nei & Gojobori 1986；Goldman & Yang 1994；Yang & Nielsen 2002；Yang 2007 |
| 073 | McDonald–Kreitman 检验与 α | MK 列联表；中性指数与 α；轻微有害突变造成的偏倚 | Coop；EG | McDonald & Kreitman 1991；Smith & Eyre-Walker 2002 |
| 074 | 基于多态性：SFS 检验与 HKA 检验 | Tajima's D；Fay & Wu's H；HKA 检验；人口史混杂 | Coop；SPG | Hudson, Kreitman & Aguadé 1987；Tajima 1989；Fay & Wu 2000 |
| 075 | 基于单倍型与群体分化的检验 | EHH、iHS 与 XP-EHH；F_ST 离群与 Lewontin–Krakauer 检验；基因组扫描的假阳性与验证 | SPG；evo | Lewontin & Krakauer 1973；Sabeti et al. 2002；Voight et al. 2006 |
| 076 | 实验进化：LTEE 与进化重演 | 长期进化实验；适合度轨迹；Cit⁺ 创新与历史偶然性 | Y 第 1 讲（回顾）；UE | Lenski et al. 1991；Blount, Borland & Lenski 2008 |
| 077 | 第 11 周复盘 | 选择检测方法对照表；文献精读 | — | 精读：Good et al. 2017 |

---

## 第四部分 物种与物种形成（第 12–13 周）

### 第 12 周 物种概念与生殖隔离
**本周目标**：辨析物种概念；掌握生殖隔离的类型、遗传基础与物种形成的地理和生态模式。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 078 | 物种概念 | 生物学物种概念；系统发育与进化物种概念；一般谱系概念；物种界定 | Y《Species and Speciation》；OS §18.2 | Mayr 1942（书）；de Queiroz 2007 |
| 079 | 生殖隔离：类型与测量 | 合子前与合子后隔离；隔离强度的量化；隔离随分化时间的累积 | OS §18.2 | Coyne & Orr 1989；Coyne & Orr 1997 |
| 080 | Dobzhansky–Muller 不相容与 Haldane 法则 | BDM 模型；不相容的"滚雪球"累积；Haldane 法则的解释（显性、快 X、快雄） | Y《Species and Speciation》 | Haldane 1922；Orr 1996；Orr & Turelli 2001；Presgraves 2010 |
| 081 | 物种形成的地理模式 | 异域、边域、邻域与同域；同域物种形成的条件与证据 | OS §18.2 | Bolnick & Fitzpatrick 2007；Savolainen et al. 2006 |
| 082 | 生态物种形成与性选择 | 歧化选择；"魔法性状"；感官驱动；性选择驱动的物种形成 | Y《Species and Speciation》 | Schluter 2009；Servedio et al. 2011；Nosil 2012（书） |
| 083 | 强化作用与杂交带 | 强化的理论与证据；张力带模型；渐变群宽度与选择–扩散平衡 | OS §18.3 | Barton & Hewitt 1985；Servedio & Noor 2003 |
| 084 | 第 12 周复盘 | 物种形成机制对照；文献精读 | — | 精读：Coyne & Orr 1989 |

### 第 13 周 物种形成基因组学、杂交与多倍化
**本周目标**：理解物种形成的基因组景观；掌握渐渗检测；理解多倍化与适应辐射。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 085 | 物种形成基因组学 | 分化岛；绝对分化（d_XY）与相对分化（F_ST）；连锁选择的混杂；基因组景观 | evo；SPG | Seehausen et al. 2014；Cruickshank & Hahn 2014；Wolf & Ellegren 2017 |
| 086 | 杂交、渐渗与杂交物种形成 | ABBA–BABA（D 统计量）；适应性渐渗；同倍体杂交物种形成 | evo；PGE | Rieseberg et al. 2003；Mallet 2005；Green et al. 2010；Durand et al. 2011 |
| 087 | 多倍化与植物物种形成 | 同源与异源多倍体；未减数配子；三倍体阻隔；多倍体物种形成的频率 | OS §18.2 | Otto & Whitton 2000；Wood et al. 2009；Soltis & Soltis 2009 |
| 088 | 适应辐射 | 生态机会；丽鱼、达尔文雀与安乐蜥；重复辐射中的确定性与偶然性 | HHMI 安乐蜥与达尔文雀短片 | Losos et al. 1998；Brawand et al. 2014；Lamichhaney et al. 2015 |
| 089 | 物种形成速率与大进化 | 物种形成的完成与逆转；物种形成速率与生殖隔离进化速率的解耦 | PCM 第 10 章 | Rabosky & Matute 2013 |
| 090 | 案例研讨：*Heliconius* 的拟态与渐渗 | 拟态基因座；适应性等位基因的跨物种共享；整合群体遗传与物种形成 | evo | Heliconius Genome Consortium 2012 |
| 091 | 第 13 周复盘 | 综合；文献精读 | — | 精读：Lamichhaney et al. 2015 |

---

## 第五部分 分子进化与基因组进化（第 14–16 周）

### 第 14 周 分子进化
**本周目标**：掌握同源关系、替代模型与分子钟；理解密码子偏好、蛋白质进化与突变偏好。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 092 | 同源性：直系同源与旁系同源 | 直系、旁系与异同源；直系同源组推断；对系统发育推断的影响 | PGE 第 2.4 章 | Fitch 1970；Emms & Kelly 2019 |
| 093 | 序列比对与核苷酸替代模型 | 多序列比对与过滤；JC69、K80、HKY85、GTR；+Γ 与 +I；距离校正与饱和 | PGE 第 2.2 章；Lewis | Jukes & Cantor 1969；Kimura 1980；Hasegawa, Kishino & Yano 1985；Yang 1994 |
| 094 | 分子钟 | 严格钟与世代时间效应；局部钟与松弛钟；化石校准；时间依赖的速率 | PGE 第 5 部分；TtB | Zuckerkandl & Pauling 1965；Kumar & Hedges 1998；Ho & Duchêne 2014 |
| 095 | 密码子使用偏好与同义位点选择 | 突变偏好与翻译选择；CAI；Nₑ 与偏好强度 | EG | Sharp & Li 1987；Plotkin & Kudla 2011 |
| 096 | 蛋白质进化：约束、上位性与祖先重建 | 结构与功能约束；上位性与"进化棘轮"；祖先序列重建与复活实验 | EG | Thornton 2004；Bridgham, Carroll & Thornton 2006；Harms & Thornton 2013 |
| 097 | 突变偏好与 GC 偏向基因转换 | 转换与颠换；CpG 突变；gBGC 对 GC 含量与 dN/dS 的影响 | EG | Duret & Galtier 2009；Hershberg & Petrov 2010 |
| 098 | 第 14 周复盘 | 替代模型推导练习；文献精读 | — | 精读：Bridgham, Carroll & Thornton 2006 |

### 第 15 周 基因与基因组的起源
**本周目标**：理解基因复制、全基因组复制与新基因起源的机制与群体遗传学；评价基因组复杂性的适应与非适应解释。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 099 | 基因复制 I：机制与命运 | 不等交换、逆转座与片段复制；假基因化与保留；复制基因的出生–死亡 | EG | Ohno 1970（书）；Lynch & Conery 2000；Innan & Kondrashov 2010 |
| 100 | 基因复制 II：亚功能化、新功能化与剂量平衡 | DDC 模型；逃避适应冲突；剂量平衡假说 | EG | Force et al. 1999；Birchler & Veitia 2007 |
| 101 | 全基因组复制 | 古多倍化证据（共线性、Ks 分布）；脊椎动物两轮 WGD；种子植物与被子植物的 WGD | EG | Dehal & Boore 2005；Jaillon et al. 2007；Jiao et al. 2011；Van de Peer, Mizrachi & Marchal 2017 |
| 102 | 新基因的起源：重排、逆转录与从头起源 | 外显子洗牌；逆转录基因；基因融合与裂变；从头起源基因与原基因；孤儿基因 | EG | Long et al. 2003；Kaessmann 2010；Tautz & Domazet-Lošo 2011；Carvunis et al. 2012 |
| 103 | 转座子与基因组进化 | TE 分类；转座爆发与宿主防御；TE 的驯化与调控网络重塑 | EG（TE 章节） | Wicker et al. 2007；Feschotte 2008；Lisch 2013 |
| 104 | 基因组大小与复杂性：漂变壁垒 | C 值之谜；Nₑ 与非适应性基因组扩张；内含子与 TE 的积累 | EG | Gregory 2001；Lynch & Conery 2003；Lynch 2007（书） |
| 105 | 第 15 周复盘 | 基因组进化的适应与非适应解释；文献精读 | — | 精读：Force et al. 1999 |

### 第 16 周 比较基因组学、调控进化与基因组冲突
**本周目标**：掌握比较基因组学的主要分析框架；理解调控进化、内共生、特化代谢进化与基因组冲突。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 106 | 比较基因组学方法 | 全基因组比对与共线性；基因家族扩张与收缩（CAFE）；系统发育谱 | EG | De Bie et al. 2006；Tang et al. 2008 |
| 107 | 水平基因转移与泛基因组 | HGT 的机制与检测；核心与可变基因组；"生命之网" | EG | Doolittle 1999；Ochman, Lawrence & Groisman 2000；Tettelin et al. 2005 |
| 108 | 内共生与细胞器基因组进化 | 线粒体与质体的内共生起源；内共生基因转移；细胞器基因组缩减 | Y 第 17 讲 Key Events in Evolution | Sagan 1967；Martin & Müller 1998；Timmis et al. 2004 |
| 109 | 调控进化：顺式与反式 | 等位基因特异表达；顺式与反式效应的分解；顺式调控突变的进化意义 | EG | King & Wilson 1975；Wittkopp, Haerum & Clark 2004；Wray 2007 |
| 110 | 植物特化代谢的进化 | 酶的混杂性；基因复制与新功能；生物合成基因簇；化学多样性的起源 | 开放获取综述 | Pichersky & Lewinsohn 2011；Weng, Philippe & Noel 2012；Moghe & Last 2015；Nützmann, Huang & Osbourn 2016 |
| 111 | 基因组冲突与自私遗传元件 | 减数分裂驱动；B 染色体；细胞质雄性不育；印记的亲本冲突假说 | Y 第 10 讲 Genomic Conflict | Burt & Trivers 2006（书）；Werren 2011；Lindholm et al. 2016 |
| 112 | 第 16 周复盘 | 比较基因组学分析流程设计；文献精读 | — | 精读：Wittkopp, Haerum & Clark 2004 |

---

## 第六部分 系统发育推断与比较方法（第 17–18 周）

### 第 17 周 系统发育推断
**本周目标**：理解简约、距离、似然与贝叶斯方法的原理与假设；能独立完成一次最大似然建树。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 113 | 系统发育推断概论与分支系统学 | 性状与同源；共有衍征；最优化准则与基于模型的推断；树空间 | Lewis（trees & optimality） | Hennig 1965 |
| 114 | 简约法与距离法 | 最大简约与 Fitch 算法；长枝吸引；UPGMA 与邻接法 | Lewis；Coursera *Molecular Evolution* | Felsenstein 1978；Saitou & Nei 1987 |
| 115 | 最大似然法 | 似然函数；Felsenstein 剪枝算法；树搜索；模型选择 | Lewis；IQ | Felsenstein 1981；Kalyaanamoorthy et al. 2017 |
| 116 | 贝叶斯系统发育 | 先验、后验与 MCMC；收敛诊断；树先验 | RB；Lewis | Yang & Rannala 1997；Huelsenbeck et al. 2001 |
| 117 | 支持度与拓扑检验 | 非参数自展；UFBoot；后验概率；AU 检验 | IQ | Felsenstein 1985a（*Evolution*）；Shimodaira 2002；Hoang et al. 2018 |
| 118 | 计算实践：用 IQ-TREE 构建最大似然树 | 比对 → 模型选择 → 建树 → 自展 → 可视化 | IQ 工作坊教程 | Nguyen et al. 2015；Minh et al. 2020 |
| 119 | 第 17 周复盘 | 方法对照表；文献精读 | — | 精读：Felsenstein 1981 |

### 第 18 周 系统发育基因组学与比较方法
**本周目标**：理解基因树–物种树不一致与多物种溯祖；掌握分歧时间估计与系统发育比较方法的核心模型。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 120 | 基因树与物种树 | ILS、HGT、复制与丢失导致的不一致；异常基因树区 | PGE 第 3.2–3.3 章 | Maddison 1997；Degnan & Rosenberg 2009 |
| 121 | 多物种溯祖与系统发育基因组学 | 串联与溯祖方法；ASTRAL；BPP；系统误差 | PGE 第 3.3 章；evo | Rannala & Yang 2003；Mirarab et al. 2014；Zhang et al. 2018 |
| 122 | 分歧时间估计 | 松弛钟模型；化石校准；总证据定年；时间先验 | PGE 第 5.1–5.2 章；TtB；RB | Drummond et al. 2006；Ronquist et al. 2012；dos Reis, Donoghue & Yang 2016 |
| 123 | 比较方法 I：独立对比与 PGLS | 物种数据的非独立性；PIC；PGLS；系统发育信号（λ 与 K） | PCM 第 1–4 章 | Felsenstein 1985b（*Am Nat*）；Grafen 1989；Revell, Harmon & Collar 2008 |
| 124 | 比较方法 II：性状演化模型 | 布朗运动；OU 模型与适应峰；离散性状 Mk 模型；祖先状态重建 | PCM 第 3–9 章 | Hansen 1997；Pagel 1999；Butler & King 2004 |
| 125 | 比较方法 III：多样化速率 | 出生–死亡模型；LTT 图；状态依赖多样化（BiSSE）及其问题；可识别性 | PCM 第 10–13 章 | Nee, May & Harvey 1994；Maddison, Midford & Otto 2007；Rabosky & Goldberg 2015；Louca & Pennell 2020 |
| 126 | 第 18 周复盘 | 用 R（ape / phytools）完成 PGLS 与祖先状态重建；文献精读 | — | 精读：Felsenstein 1985b |

---

## 第七部分 生命史与大进化（第 19–20 周）

### 第 19 周 生命的早期历史
**本周目标**：了解生命起源、LUCA、真核生物起源、主要进化转变、动物起源与植物登陆的证据与争论。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 127 | 生命起源 | 前生物合成；RNA 世界；原细胞；早期地球环境 | Y 第 17 讲 Key Events in Evolution | Miller 1953；Gilbert 1986；Joyce 2002 |
| 128 | LUCA 与生命之树的根 | 三域与二域；LUCA 的基因组与生理推断；生命之树的定根 | Y 第 17 讲；UE | Woese & Fox 1977；Woese, Kandler & Wheelis 1990；Williams et al. 2013；Weiss et al. 2016；Moody et al. 2024 |
| 129 | 真核生物的起源 | Asgard 古菌；线粒体获得的时机；真核复杂性的能量学解释 | Y 第 17 讲 | Martin & Müller 1998；Lane & Martin 2010；Spang et al. 2015；Zaremba-Niedzwiedzka et al. 2017；Imachi et al. 2020；Eme et al. 2023 |
| 130 | 主要进化转变与多细胞性 | 进化个体性的转变；分工与冲突抑制；多细胞性的多次起源与实验进化 | SEP 生物个体相关条目 | Szathmáry & Maynard Smith 1995；Grosberg & Strathmann 2007；Ratcliff et al. 2012 |
| 131 | 寒武纪大爆发与动物起源 | 埃迪卡拉生物群；分子钟与化石的时间差；生态与发育解释 | Y《Major Events in the Geological Theatre》 | Budd & Jensen 2000；Erwin et al. 2011 |
| 132 | 植物登陆与陆地植物早期演化 | 链形植物；陆地植物系统发育；角质层、维管组织与种子等关键创新 | 开放获取综述 | Kenrick & Crane 1997；Wickett et al. 2014；Puttick et al. 2018；One Thousand Plant Transcriptomes Initiative 2019 |
| 133 | 第 19 周复盘 | 生命史时间线；文献精读 | — | 精读：Imachi et al. 2020 |

### 第 20 周 大进化的模式与过程
**本周目标**：理解化石记录的性质、间断平衡、大灭绝、关键创新与大进化趋势；评价微进化到大进化的外推。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 134 | 化石记录的性质与偏差 | 埋藏学；采样偏差；化石记录质量的评估；Paleobiology Database | Y《The Fossil Record and Life's History》 | Kidwell & Holland 2002 |
| 135 | 间断平衡与停滞 | 间断平衡与系统渐变；停滞的解释；化石谱系中的进化模式 | — | Eldredge & Gould 1972；Gould & Eldredge 1977；Hunt 2007 |
| 136 | 大灭绝与复苏 | 显生宙大灭绝；K–Pg 撞击假说；选择性灭绝与复苏 | Y《Major Events in the Geological Theatre》 | Alvarez et al. 1980；Raup & Sepkoski 1982；Jablonski 2001 |
| 137 | 关键创新与被子植物辐射 | 关键创新的检验难题；被子植物起源与达尔文的"讨厌之谜" | PCM 第 13 章 | Hodges & Arnold 1995；Friedman 2009；Magallón et al. 2015 |
| 138 | 进化新颖性与可进化性 | 新颖性的定义；可进化性；变异的结构 | — | Kirschner & Gerhart 1998；Wagner & Lynch 2010 |
| 139 | 趋势、物种选择与"进步" | 被动与驱动趋势；Cope 法则；物种选择与物种分选；复杂性趋势 | — | McShea 1996；Alroy 1998；Jablonski 2008；Payne et al. 2009 |
| 140 | 第 20 周复盘 | 微进化–大进化外推问题讨论；文献精读 | — | 精读：Alvarez et al. 1980 |

---

## 第八部分 进化发育生物学（第 21 周）

### 第 21 周 Evo-Devo
**本周目标**：理解发育工具包、深度同源与顺式调控进化；评价可塑性与发育偏好在进化理论中的地位。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 141 | Evo-devo 概论：发育工具包与深度同源 | 工具包基因；深度同源；*Pax6* 与眼的进化 | Y《The Importance of Development in Evolution》 | Halder, Callaerts & Gehring 1995；Shubin, Tabin & Carroll 2009 |
| 142 | Hox 基因与体轴模式 | Hox 基因簇与共线性；Hox 表达域的变化与形态多样性 | — | Lewis 1978；Carroll 1995 |
| 143 | 顺式调控进化与形态进化 | 多效性基因的模块化增强子；顺式调控假说及其争论 | HHMI 刺鱼短片 | Prud'homme et al. 2006；Hoekstra & Coyne 2007；Carroll 2008 |
| 144 | 模块性、发育约束与发育偏好 | 模块性的进化；约束与选择；发育偏好与调控网络视角 | — | Wagner, Pavlicev & Cheverud 2007；Uller et al. 2018 |
| 145 | 植物发育的进化：花与 MADS-box 基因 | ABC(E) 模型；MADS-box 基因家族的复制与功能分化；花的起源 | — | Coen & Meyerowitz 1991；Theißen 2001 |
| 146 | 表型可塑性、遗传同化与扩展进化综合 | 可塑性先导假说；遗传同化；EES 的主张与批评 | — | Waddington 1953；West-Eberhard 2003（书）；Pfennig et al. 2010；Laland et al. 2015 |
| 147 | 第 21 周复盘 | Evo-devo 与群体遗传学的整合；文献精读 | — | 精读：Prud'homme et al. 2006 |

---

## 第九部分 性、生活史、社会行为与共进化（第 22–23 周）

### 第 22 周 性与生活史
**本周目标**：理解性的进化之谜、性选择、性别分配、生活史权衡与衰老理论；了解植物交配系统的进化。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 148 | 性的进化：代价与生态学解释 | 两倍代价；红皇后与纠缠河岸假说；无性谱系的命运 | Y 第 9 讲 The Evolution of Sex | Maynard Smith 1978（书）；Hamilton, Axelrod & Tanese 1990；Otto 2009；Morran et al. 2011 |
| 149 | 性选择 I：配偶选择 | 异配生殖与性别角色；Fisher 失控；良好基因与障碍原理；感官偏好 | Y《Sexual Selection》 | Zahavi 1975；Lande 1981；Andersson 1982；Kirkpatrick & Ryan 1991 |
| 150 | 性选择 II：精子竞争与性冲突 | 交配后性选择；精子竞争；隐秘雌性选择；性拮抗共进化 | Y《Sexual Selection》 | Parker 1970；Rice 1996；Arnqvist & Rowe 2005（书） |
| 151 | 性别分配与性比 | Fisher 性比理论；局部配偶竞争；Trivers–Willard 假说 | Y 第 12 讲 Sex Allocation | Hamilton 1967；Trivers & Willard 1973；Charnov 1982（书）；West 2009（书） |
| 152 | 生活史进化与衰老 | 权衡与繁殖投入；衰老的进化理论（突变积累、拮抗多效、可弃体细胞） | Y《Life History Evolution》 | Medawar 1952；Williams 1957；Kirkwood 1977；Stearns 1989 |
| 153 | 植物交配系统的进化 | 自交与异交；自交不亲和系统；自交综合征；自交是否是"进化死胡同" | — | Barrett 2002；Tsuchimatsu et al. 2010；Igic & Busch 2013 |
| 154 | 第 22 周复盘 | 综合；文献精读 | — | 精读：Andersson 1982 |

### 第 23 周 社会进化、博弈与共进化
**本周目标**：掌握亲缘选择、Price 方程与进化博弈论；理解合作与共进化的理论与证据。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 155 | 亲缘选择与 Hamilton 法则 | 广义适合度；rb > c；亲缘系数；单倍二倍性与真社会性 | Y 第 36 讲 Selfishness and Altruism；SEP "Biological Altruism" | Hamilton 1964 |
| 156 | 选择的层次与 Price 方程 | Price 方程的推导；多层次选择的分解；群体选择之争 | SEP "Units and Levels of Selection" | Price 1970；Okasha 2006（书）；Gardner 2008 |
| 157 | 进化博弈论 | 进化稳定策略（ESS）；鹰–鸽博弈；复制子动力学 | Y《Evolutionary Game Theory: Fighting and Contests》；SEP "Evolutionary Game Theory" | Maynard Smith & Price 1973；Maynard Smith 1982（书） |
| 158 | 合作的进化 | 互惠利他；重复囚徒困境；合作的机制；真社会性之争 | Y 第 36 讲 | Trivers 1971；Axelrod & Hamilton 1981；Nowak 2006；West, Griffin & Gardner 2007；Nowak, Tarnita & Wilson 2010；Abbot et al. 2011 |
| 159 | 共进化 I：宿主–寄生物与红皇后 | 军备竞赛；基因对基因与匹配等位基因模型；共进化的地理镶嵌 | Y《Coevolution》 | Van Valen 1973；Dawkins & Krebs 1979；Brodie, Ridenhour & Brodie 2002；Thompson 2005（书） |
| 160 | 共进化 II：植物–昆虫互作与化学生态 | 逃逸–辐射共进化；硫代葡萄糖苷与粉蝶；基因与基因组复制推动的军备竞赛 | — | Ehrlich & Raven 1964；Futuyma & Agrawal 2009；Edger et al. 2015 |
| 161 | 第 23 周复盘 | 综合；文献精读 | — | 精读：Hamilton 1964（第 I 部分） |

---

## 第十部分 人类进化（第 24 周）

### 第 24 周 人类进化
**本周目标**：掌握人族演化的化石与基因组证据；理解古 DNA、基因渗入与人类近期适应。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 162 | 灵长类系统发育与人科演化 | 灵长类分类；人科与人族；人–黑猩猩分歧与 ILS | EXP 灵长类相关章节 | Scally et al. 2012 |
| 163 | 人族化石记录 | 南方古猿与傍人；早期人属；直立人的扩散；双足行走与脑容量演化 | EXP；Smithsonian Human Origins | Wood & Collard 1999 |
| 164 | 智人的起源 | 非洲起源模型；Jebel Irhoud；"泛非"起源 | EXP；Smithsonian Human Origins | Hublin et al. 2017；Richter et al. 2017；Stringer 2016 |
| 165 | 古 DNA 与古人类基因渗入 | 尼安德特人与丹尼索瓦人基因组；渗入片段的分布与选择 | EXP | Green et al. 2010；Reich et al. 2010；Prüfer et al. 2014；Sankararaman et al. 2014 |
| 166 | 人类的近期适应 | 乳糖酶持续性；高原适应；适应性渐渗（*EPAS1*） | Coop | Tishkoff et al. 2007；Yi et al. 2010；Huerta-Sánchez et al. 2014 |
| 167 | 基因–文化共进化与文化进化 | 双重遗传理论；文化进化模型；基因–文化共进化案例 | — | Boyd & Richerson 1985（书）；Laland, Odling-Smee & Myles 2010 |
| 168 | 第 24 周复盘 | 综合；文献精读 | — | 精读：Green et al. 2010 |

---

## 第十一部分 应用与综合（第 25–26 周）

### 第 25 周 进化生物学的应用
**本周目标**：将进化理论应用于医学、病原体、癌症、农业与保护问题。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 169 | 进化医学 | 进化失配；防御与症状；权衡与衰老；研究议程 | Y《Evolutionary Medicine》；*Evolution, Medicine & Public Health* | Nesse & Williams 1994（书）；Stearns 2012 |
| 170 | 病原体进化与系统动力学 | 病原体的快速进化；系统动力学；抗原进化 | TtB 系统动力学教程 | Grenfell et al. 2004；Pybus & Rambaut 2009；Volz, Koelle & Bedford 2013 |
| 171 | 抗生素耐药性的进化 | 耐药突变与 HGT；适合度代价与补偿进化；耐药进化的空间动态 | — | Andersson & Hughes 2010；Baym et al. 2016 |
| 172 | 癌症：体细胞进化 | 克隆进化；肿瘤内异质性；治疗中的选择 | — | Nowell 1976；Greaves & Maley 2012；Gerlinger et al. 2012 |
| 173 | 驯化与作物进化 | 驯化综合征；驯化基因 *tb1*；驯化瓶颈与"驯化代价" | — | Doebley, Stec & Hubbard 1997；Doebley, Gaut & Smith 2006；Studer et al. 2011；Meyer & Purugganan 2013 |
| 174 | 保护遗传学与基因组学 | 小种群范式；近交衰退与遗传拯救；基因组学在保护中的作用 | — | Frankham 2005；Allendorf, Hohenlohe & Luikart 2010；Whiteley et al. 2015；Kardos et al. 2021 |
| 175 | 第 25 周复盘 | 综合；文献精读 | — | 精读：Baym et al. 2016 |

### 第 26 周 综合与研究实践
**本周目标**：理解模型与模拟在进化推断中的作用；整合全课程，形成研究设计能力。

| Day | 主题 | 核心概念 | 主读 / 主看（免费） | 原始文献 |
|---|---|---|---|---|
| 176 | 模型、模拟与推断 | 模型在进化生物学中的作用；正向模拟（SLiM）与溯祖模拟；近似贝叶斯计算（ABC） | SLiM 手册与工作坊材料；msp | Beaumont, Zhang & Balding 2002；Servedio et al. 2014；Haller & Messer 2019 |
| 177 | 再论扩展进化综合 | 生态位构建；非遗传性遗传；发育偏好；争论现状 | — | Laland et al. 2014；Laland et al. 2015 |
| 178 | 进化的可预测性与重复性 | 重复进化；偶然性与决定性；预测进化的条件 | — | Lässig, Mustonen & Walczak 2017；Blount, Lenski & Losos 2018 |
| 179 | 如何阅读与评价进化生物学论文 | 强推理；多重工作假说；常见统计与推断陷阱 | — | Chamberlin 1890；Platt 1964 |
| 180 | 研究设计：从问题到数据与模型 | 可检验问题的构建；比较、实验与基因组方法的选择；可重复性 | — | Kokko 2007（书） |
| 181 | 总结：核心问题与开放问题 | 全课程回顾；开放问题清单 | — | — |
| 182 | 第 26 周复盘：结业复盘与后续学习路线 | 全课程自测；方向进阶建议；文献精读（双方观点） | — | 精读：Laland et al. 2014 |

---

## 完成 182 天之后

课程结束后，每日更新转入"延伸阅读"模式：每天精读一篇经典或近期开放获取的进化生物学论文（问题—方法—结果—评价—与课程的联系），存放于 `lessons/extension/`。规则见 [AUTHORING.md](AUTHORING.md)。
