# Day 018 · 重组：交叉、基因转换与重组热点

> **部分** 第一部分 概念基础与证据 ｜ **周次** 第 3 周 遗传变异的来源 ｜ **发布日期** 2026-11-20 ｜ **建议用时** 约 100 分钟（讲义 45′ · 主读／主看 30′ · 练习 25′）
> **主读** OpenStax *Biology 2e* §11.1；Coop 讲义第 3 章（位点间相关部分）；Myers et al.（2010）
> **关键词** meiotic recombination · double-strand break (DSB) · SPO11 · double Holliday junction · crossover · non-crossover · obligate crossover · crossover homeostasis · Kosambi map function · gene conversion · GC-biased gene conversion · recombination hotspot · PRDM9 · hotspot conversion paradox · heterochiasmy

## 学习目标

完成本讲后，应能够：

1. 描述减数分裂重组的分子过程（程序性双链断裂、链入侵、双 Holliday 连接），区分交叉与非交叉两种结果；
2. 解释交叉保证、干涉与交叉稳态，并比较 Haldane 与 Kosambi 作图函数；
3. 说明基因转换的机制，推导偏向基因转换造成的传递偏离及其群体后果；
4. 概述重组热点的发现与 PRDM9 决定热点位置的证据，解释热点转换悖论及其可能的解决方式；
5. 描述重组率在基因组区域、两性、个体与物种之间的变异，并说明其进化意义。

---

## 1 从遗传图到分子机制

Day 015 从经典遗传学的角度讨论了重组：两个位点之间的重组率 $r$、以厘摩计的图距、干涉，以及把重组率换算为图距的 Haldane 作图函数。那里把交换看作沿染色体随机散布的点事件。本讲转向机制层面，回答三个问题：交换在分子上是如何发生的？它在基因组中的位置由什么决定？重组过程还会造成哪些不表现为交换的序列改变？

这些问题并不只属于细胞生物学。重组率在基因组中的分布决定了连锁不平衡（Day 024）与连锁选择（Day 052–053）的强弱；基因转换会改变等位基因的传递比例，其效果在群体层面类似于选择；而决定重组位置的基因本身进化极快，并与物种形成有关（第 6 节）。

---

## 2 减数分裂重组的分子过程

### 2.1 程序性双链断裂与链交换

在细胞学上，减数分裂前期 I 的同源染色体由**联会复合体**（synaptonemal complex）沿全长连在一起；沿联会复合体分布着称为重组结的大型蛋白复合体。交换完成后，可以在显微镜下看到同源染色体之间的**交叉结**（chiasma）（OpenStax §11.1）。

在分子上，减数分裂重组始于有计划的 DNA 损伤：蛋白 SPO11 在染色体上切出**双链断裂**（double-strand break, DSB）。Keeney 等（1997）在酿酒酵母中纯化出与断裂末端共价相连的蛋白，鉴定其为 Spo11，有力地表明 Spo11 是减数分裂 DNA 切割活性的催化亚基；他们还指出，这一蛋白家族在裂殖酵母、线虫乃至古菌中都有成员。

Szostak 等（1983）提出的**双链断裂修复模型**（double-strand break repair model, DSBR）概括了断裂之后的步骤：断裂两侧的 5′ 端被切除，留下 3′ 单链尾；单链尾侵入同源染色体的一条非姐妹染色单体，并以之为模板延伸合成；另一个断裂末端随后被捕获，形成含有两个四链交叉结构的**双 Holliday 连接**（double Holliday junction, dHJ）。根据这一中间体被拆解的方式，两侧的序列可能在两条同源染色体之间互换，即**交叉**（crossover, CO），也就是 Day 015 所说的交换在分子水平上的结果；也可能不互换，称为**非交叉**（non-crossover, NCO）。

### 2.2 断裂多、交叉少：交叉保证、干涉与稳态

DSB 的数目远多于交叉。Cole 等（2012）指出，小鼠中只有约 10% 的减数分裂 DSB 被修复为交叉。交叉的数目与位置受到严格调控，表现为三条规律。

第一，**交叉保证**（obligate crossover）：每对同源染色体通常至少发生一次交叉（Cole et al. 2012）。交叉结把同源染色体连在一起直到后期 I，每条染色体至少需要一个交叉结，同源染色体才能在第一次减数分裂中正确分离（OpenStax §11.1）。第二，**干涉**：交叉之间倾向于相隔较远，即 Day 015 中以 $I = 1 - c$ 度量的现象。第三，**交叉稳态**（crossover homeostasis）：DSB 的数目在细胞之间波动时，交叉的数目仍相对稳定。Cole 等（2012）发现，小鼠精母细胞中早期重组蛋白 RAD51 与 DMC1 的焦点数在细胞之间差异很大，而标记交叉的 MLH1 焦点数差异很小；他们认为这种稳态调控很可能是为了避免产生非整倍体配子。

干涉使交叉的分布比泊松过程更均匀，同一区间内的多次交叉较少，因此假定无干涉的 Haldane 作图函数会高估由重组率推算的图距。Kosambi（1944）的作图函数在推导中考虑了干涉：

$$r = \frac{1}{2}\tanh(2d) \quad\Longleftrightarrow\quad d = \frac{1}{4}\ln\frac{1 + 2r}{1 - 2r},$$

其中 $d$ 为以摩计的图距。$d$ 很小时两个函数都给出 $r \approx d$；$r$ 较大时，同一 $r$ 对应的 Kosambi 图距小于 Haldane 图距（练习 1）。哪一个函数更合适，取决于所研究物种中干涉的实际强度。

---

## 3 基因转换

### 3.1 机制与证据

在 DSBR 模型中，侵入的单链与模板链配对，形成由两条来自不同同源染色体的单链组成的**异源双链 DNA**（heteroduplex DNA）；若两条同源染色体在此处序列不同，就会出现错配。断裂处被切除的序列按同源染色体的序列重新合成，异源双链中的错配被修复时也可能以对方为模板。两种过程都使一条染色单体上的一段序列被另一条同源染色体的序列非相互地改写，称为**基因转换**（gene conversion），它发生在起始断裂附近的短片段内（Duret & Galtier 2009）。若能回收一次减数分裂的全部四个产物（如真菌的四分子），杂合位点本应呈 2:2 分离，基因转换则使其呈 3:1 或 1:3 分离（练习 2）。

人类的非交叉基因转换片段很短：在三个热点的精子分型研究中，转换片段的平均长度只有几十到几百个碱基（Jeffreys & May 2004）。Williams 等（2015）利用 98 次减数分裂的数据，首次在全基因组范围研究人类的非交叉基因转换；这些事件与 DSB 热点的重叠表明，其中大多数很可能源于减数分裂。

### 3.2 偏向基因转换

若修复对两种碱基没有偏好，基因转换只是随机地改变个别配子，平均而言不改变等位基因频率。但许多真核生物中的基因转换偏向 G 与 C，称为 **GC 偏向基因转换**（GC-biased gene conversion, gBGC）（Duret & Galtier 2009）。Williams 等（2015）发现，在 AT/GC 杂合位点上，人类非交叉基因转换有 68%（区间估计 58%–78%）传递了 GC 等位基因。

一个简单的模型可以说明这种偏向的群体后果。设某位点有 W（A 或 T）与 S（G 或 C）两个等位基因；在杂合子的每次减数分裂中，该位点以概率 $c$ 落入转换片段，转换偏向 S 的概率为 $\pi$。一次转换使四个产物由 2:2 变为 3:1 或 1:3，因此杂合子传递 S 的概率为

$$\frac{1}{2} + c\left[\frac{3}{4}\pi + \frac{1}{4}(1 - \pi) - \frac{1}{2}\right] = \frac{1 + b}{2}, \qquad b = \frac{c\,(2\pi - 1)}{2}.$$

在随机交配的大群体中，设 S 的频率为 $p$、$q = 1 - p$，下一代 $p' = p^{2} + 2pq \cdot \frac{1 + b}{2}$，即

$$\Delta p = b\,p\,q .$$

这与每个 S 等位基因具有选择优势 $b$ 的加性选择形式相同（Day 025）。也就是说，gBGC 不涉及适合度，却能像选择一样推动 GC 等位基因的频率上升。Duret 与 Galtier（2009）认为，gBGC 可以解释哺乳动物基因组中 GC 含量的空间分布，并会促进有害的 AT→GC 突变的分离与固定，从而增加突变负荷。gBGC 对 GC 含量与 dN/dS 检验的影响将在 Day 097 讨论。

### 3.3 基因转换与短距离连锁

转换片段很短，因此它主要打乱相距很近的位点之间的组合。设转换片段在每个碱基处以速率 $g$（每次减数分裂）起始，沿一个方向延伸，长度服从均值为 $L$ 的指数分布，则相距 $x$ 个碱基的两个位点恰有一个落入片段、因而被分开的概率为

$$P_{\mathrm{GC}}(x) = 2gL\left(1 - e^{-x/L}\right),$$

而交叉将它们分开的概率约为 $\rho x$，$\rho$ 为每碱基每次减数分裂的交叉率。$x \ll L$ 时 $P_{\mathrm{GC}} \approx 2gx$，与交叉一样随距离线性增加；$x \gg L$ 时 $P_{\mathrm{GC}}$ 趋于常数 $2gL$。因此，在数百碱基的尺度上基因转换可能比交叉更有效地打破位点间的关联，在长距离上则几乎可以忽略（练习 4）。用 LD 推断重组率时必须考虑这一点（Day 024）。

---

## 4 重组热点与 PRDM9

### 4.1 热点的发现

在精细尺度上，重组事件集中在称为**重组热点**（recombination hotspot）的狭窄区段中（Baudat et al. 2010）。热点可以通过**精子分型**（sperm typing）直接测定（Jeffreys & May 2004），也可以由群体遗传变异中的 LD 模式间接推断。Myers 等（2005）用后一种方法构建了人类基因组的精细重组图，识别出 25,000 多个热点；他们比较人类与黑猩猩后发现，重组景观的精细结构进化极快。基于千碱基与兆碱基尺度上重组行为的差异，他们提出热点是随机产生与消失的特征，而大尺度的重组率受到约束。Myers 等（2008）随后找到一个简并的 13 碱基基序 CCNCCNTNNCCNC，它与至少 40% 的人类热点募集交叉有关。

### 4.2 PRDM9 决定热点位置

2010 年的三篇论文把热点与基因 *PRDM9* 联系起来。PRDM9 是一种具有锌指 DNA 结合域的减数分裂蛋白，并具有组蛋白 H3 第 4 位赖氨酸三甲基转移酶活性（Mihola et al. 2009；Baudat et al. 2010）。Myers 等（2010）发现，上述基序在黑猩猩中不起作用，并在人类谱系中被一种自我毁灭式的驱动逐步清除；多条证据表明，快速进化的锌指蛋白 PRDM9 结合这一基序，其序列变化可能是两个物种热点不同的原因。Baudat 等（2010）给出了三条证据：热点使用不同的两个小鼠品系在 PRDM9 锌指阵列上存在多态；人类 PRDM9 的共有等位基因被预测能识别该基序，体外实验证实了这一结合特异性；人类 PRDM9 锌指的等位变异与全基因组热点使用的个体差异显著相关。同期，Parvanov 等（2010）证明 *Prdm9* 控制着小鼠热点的激活。由此得到的图景是：PRDM9 结合特定的 DNA 序列，把重组的起始定位到基因组的特定位置（Baudat et al. 2010）。

PRDM9 并不是重组本身所必需的。Brick 等（2012）发现，*Prdm9* 敲除小鼠中热点仍然形成，但位置改变：约 44% 的热点位于已注释基因的启动子，而野生型中只有约 3%；作者认为 PRDM9 把重组机器引离启动子等功能元件。缺少 PRDM9 的鸟类提供了自然对照：Singhal 等（2015）在斑胸草雀与长尾草雀中发现，热点富集在功能元件附近，大多为两个物种所共有，其保守性似可延续数千万年。

### 4.3 热点转换悖论

热点的存在本身构成一个进化难题。设某位点有能起始 DSB 的活性等位基因 H 与不能起始的 h。在 H/h 杂合子中，断裂发生在 H 所在的染色单体上，并按同源染色体（h）的序列修复，结果 H 被转换为 h。按 3.2 节的记号，这相当于 $\pi = 0$、$b = -c/2$：h 在传递中占优势。Boulton、Myers 与 Redfield（1997）模拟大群体后发现，活性热点等位基因会迅速被非活性等位基因取代，后者由罕见突变产生，并借助与重组相伴的转换而扩增；已知的重组益处似乎不足以维持热点。这就是**热点转换悖论**（hotspot conversion paradox）：热点会自我毁灭，为什么又普遍存在（练习 3）？

PRDM9 的发现提示了一种解决方式。热点确实在被毁灭，Myers 等（2010）在人类谱系中观察到的正是 PRDM9 结合基序被逐步清除；但 PRDM9 的锌指阵列进化很快，新的等位基因识别新的序列，可以在别处产生新的热点。按照这一图景，热点的位置不断更替，这与人类和黑猩猩热点位置明显不同的观察一致；而在不依赖 PRDM9 的鸟类中，热点位于功能元件附近，长期稳定（Singhal et al. 2015）。

---

## 5 重组率的变异

重组率在多个层次上变异。在基因组内，重组在千碱基尺度上集中于热点，在兆碱基尺度上的变化则受到约束（Myers et al. 2005）。在两性之间，重组率或重组分布的差异称为**雌雄重组差异**（heterochiasmy）。Bhérer 等（2017）汇总了 10 万次以上减数分裂的系谱数据，发现人类女性全基因组的交叉率约为男性的 1.6 倍；在基因组的大部分区域女性的重组率更高，但在端粒附近通常相反；两性的热点大多共享，差异主要在于热点强度而非位置。Sardell 与 Kirkpatrick（2020）综述了多种真核生物的重组景观，发现在许多物种中雄性的重组偏向端粒，雌性的分布则较均匀。在个体之间，PRDM9 等位变异影响热点的使用（Baudat et al. 2010）；在物种之间，依赖 PRDM9 的热点快速更替，不依赖 PRDM9 的热点则可以长期稳定（Myers et al. 2010；Singhal et al. 2015）。

这些变异有直接的进化后果。重组率较低的区域中，位点之间的关联维持更久，选择对连锁中性位点的影响也更大；重组率的异质性因此会影响遗传多样性的分布（Day 053），也是检测选择时必须控制的混杂因素（Day 071）。重组的位置与速率本身也受遗传变异（如 PRDM9 的等位变异）影响，因而可以进化；为什么重组能够维持，将在 Day 055 与 Day 148 讨论。

---

## 6 案例研究：PRDM9 与小鼠杂种不育

**问题** 小鼠某些亚种之间杂交产生的雄性杂种不育。这种不育的遗传基础是什么，它与重组有何关系？

**方法与结果** Mihola 等（2009）把三十年前已被定位的杂种不育基因 *Hst1* 鉴定为 *Prdm9*：将携带"可育"等位基因的细菌人工染色体导入雄性杂种，可以挽救其不育。一年后，*Prdm9* 被证明是热点的决定因子（第 4.2 节）。Davies 等（2016）进一步发现，杂种不育的程度与各 PRDM9 变体在其控制的 DSB 位点上同时结合两条同源染色体（对称结合）的程度密切相关：全基因组的对称结合水平越高，生育力指标越高。作者的解释是，减数分裂驱动造成的亚种特异的 PRDM9 结合位点降解，即第 4.3 节所述的热点侵蚀，会不断增加不对称结合。他们把小鼠 *Prdm9* 中编码锌指阵列的部分替换为人类的对应序列，DSB 热点随之转移到新的位置，雄性杂种的生育力完全恢复。

**意义** 这一案例把本讲的三条线索，即 DSB 的定位、热点的自我毁灭与 PRDM9 的快速进化，联系在一起。它也说明，一个"物种形成基因"的作用可以通过其分子功能得到解释：作者据此认为，由 *Prdm9* 驱动的杂种不育在进化上应是暂时的。杂种不育的一般遗传学理论将在 Day 080 讨论。

---

## 今日学习材料（均可免费获取）

| 类型 | 材料 | 说明 |
|---|---|---|
| 必读 | [OpenStax *Biology 2e* §11.1 The Process of Meiosis](https://openstax.org/books/biology-2e/pages/11-1-the-process-of-meiosis) | 联会复合体、重组结、交换与交叉结，约 15 分钟 |
| 必读 | Coop，*Population and Quantitative Genetics*：[第 3 章 Population Structure and Correlations Among Loci](https://bio.libretexts.org/Bookshelves/Genetics/Population_and_Quantitative_Genetics_(Coop)/03%3A_Population_Structure_and_Correlations_Among_Loci) | 章末关于位点间相关的部分，作为 Day 024 的预习，约 15 分钟 |
| 精读 | Myers et al.（2010）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC3828505) | 人类与黑猩猩的热点差异、基序的清除与 PRDM9 |
| 精读 | Baudat et al.（2010）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC4295902) | PRDM9 决定热点位置的三条证据 |
| 选读 | Boulton, Myers & Redfield（1997）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC21556) | 热点转换悖论的原始表述 |
| 选读 | Williams et al.（2015）：[eLife 开放获取](https://doi.org/10.7554/eLife.04637) | 人类非交叉基因转换与 GC 偏向 |
| 选读 | Bhérer, Campbell & Auton（2017）：[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC5414043) | 人类重组的性别差异 |
| 选读 | Davies et al.（2016）：[牛津大学 ORA 存档](https://ora.ox.ac.uk/objects/uuid:0e9f43c0-7b12-4918-8158-cb4b3747dcf1) | 案例研究原文 |

---

## 思考与练习

1. **（计算）** 三对位点的重组率分别为 $r = 0.10$、$0.25$、$0.40$。(a) 分别用 Haldane 与 Kosambi 作图函数计算图距（cM）。(b) 为什么 Kosambi 图距总是较小，且差别随 $r$ 增大而增大？(c) 若图距为 50 cM，两个函数预测的重组率各是多少？
2. **（计算）** 某真菌杂合位点（W/S）的 1000 个四分子中，940 个呈 2:2 分离，40 个呈 3S:1W，20 个呈 1S:3W（本题数据为假设）。(a) 估计该位点落入转换片段的概率 $c$ 与转换偏向 S 的概率 $\pi$。(b) 计算孢子中 S 的比例，并用正文中的 $b$ 公式验证。(c) 在随机交配的大群体中，若不考虑漂变与选择，S 的频率由 0.1 上升到 0.9 约需多少代？
3. **（计算）** 某热点的活性等位基因 H 在 H/h 杂合子中每次减数分裂被转换为 h 的概率为 $c = 0.02$（本题数据为假设）。(a) 杂合子传递 H 的概率是多少？(b) 忽略漂变与新突变，H 的频率由 0.99 下降到 0.01 约需多少代？若每代 25 年（假设），约合多少年？(c) 这一结果为什么构成悖论？PRDM9 的发现如何提示了解决方式？
4. **（推导与计算）** (a) 按 3.3 节的假设推导 $P_{\mathrm{GC}}(x) = 2gL(1 - e^{-x/L})$。(b) 设 $\rho = 1 \times 10^{-8}$、$g = 2 \times 10^{-8}$（每碱基每次减数分裂）、$L = 300$ bp（本题参数为假设），计算 $x = 100$ bp、1 kb、10 kb 与 100 kb 时基因转换与交叉各自分开两个位点的概率。(c) 这对用 LD 推断重组率意味着什么？
5. **（概念）** 判断并纠正：(a)"重组热点是基因组中固定不变的特征，在近缘物种之间位置相同。"(b)"*Prdm9* 敲除小鼠不再形成重组热点。"(c)"基因转换只改变个别配子，没有群体水平的进化后果。"(d)"人类女性在基因组每一处的重组率都高于男性。"
6. **（文献评论）** 阅读 Myers 等（2010）与 Baudat 等（2010）。两项研究分别用哪些证据把 PRDM9 与热点联系起来？它们各自依赖什么类型的数据？你认为还需要什么证据，才能确认"PRDM9 的快速进化使热点不断更替"这一图景？

<details>
<summary>答案要点</summary>

1. (a) Haldane：11.16、34.66、80.47 cM；Kosambi：10.14、27.47、54.93 cM（代码验算）。(b) 由重组率推算图距时，需要补回因偶数次交叉而不可见的交叉；干涉减少了同一区间内的多次交叉，需要补回的部分就少。$r$ 越大，区间内发生多次交叉的机会越多，两种假设的差别越明显。(c) Haldane：$r \approx 0.316$；Kosambi：$r \approx 0.381$。
2. (a) $c = 60/1000 = 0.06$，$\pi = 40/60 \approx 0.667$。(b) S 的比例 $= (940 \times 2 + 40 \times 3 + 20 \times 1)/4000 = 0.505$；$b = 0.06 \times (2 \times 0.667 - 1)/2 = 0.01$，$(1 + b)/2 = 0.505$，二者一致。(c) $\Delta p = 0.01\,pq$，与选择系数为 0.01 的加性选择相同；按递推式逐代计算约需 440 代（logistic 近似 $2\ln 9/0.01 \approx 439$ 代，代码验算）。
3. (a) $(1 - c)/2 + c/4 = 0.495$，即 $b = -c/2 = -0.01$。(b) 约 920 代（logistic 近似 $2\ln 99/0.01 \approx 919$ 代，代码验算），约 2.3 万年，在进化时间尺度上很短。(c) 在本题的假设下，热点约两万多年就会消亡，那么现存的大量热点需要解释（Boulton et al. 1997）。PRDM9 研究表明，热点确实在被清除（Myers et al. 2010），但 PRDM9 锌指阵列的快速进化不断产生识别新序列的等位基因，从而在别处产生新热点；这一图景预测热点位置在近缘物种之间迅速更替，而在缺少 PRDM9 的物种中保持稳定，二者都有证据支持（Myers et al. 2010；Singhal et al. 2015）。
4. (a) 设位点 A 在 0，B 在 $x$，片段向右延伸。从 A 左侧 $y$ 处起始的片段，长度介于 $y$ 与 $y + x$ 之间时只覆盖 A，概率为 $e^{-y/L} - e^{-(y+x)/L}$，对 $y$ 积分得 $gL(1 - e^{-x/L})$；从 A、B 之间距 B 为 $y$ 处起始、长度超过 $y$ 的片段只覆盖 B，对 $y \in (0, x)$ 积分得 $gL(1 - e^{-x/L})$；从 B 右侧起始的片段两点都不覆盖。两项相加即得结果。片段向左或向右延伸的概率各半时，由对称性结果不变（蒙特卡洛模拟验证）。(b) 基因转换：$3.4\times10^{-6}$、$1.16\times10^{-5}$、$1.2\times10^{-5}$、$1.2\times10^{-5}$；交叉：$10^{-6}$、$10^{-5}$、$10^{-4}$、$10^{-3}$；基因转换所占份额依次约为 77%、54%、11%、1.2%（代码验算）。(c) 在很短的距离上，LD 的衰减快于只考虑交叉时的预期；若忽略基因转换，由短距离 LD 推断的交叉率会偏高，而长距离的 LD 主要反映交叉。
5. (a) 错误。依赖 PRDM9 的热点在人类与黑猩猩之间位置明显不同（Myers et al. 2005；Myers et al. 2010）；但在缺少 PRDM9 的鸟类中，热点可以在两个物种间长期共享（Singhal et al. 2015）。(b) 错误。敲除小鼠中热点仍然形成，但更多地位于基因启动子（约 44%，野生型约 3%）（Brick et al. 2012）。(c) 错误。有偏向的基因转换在群体层面相当于加性选择，可以改变等位基因频率乃至基因组的 GC 含量（Duret & Galtier 2009）；即使无偏，基因转换也会打乱短距离位点之间的组合。(d) 错误。全基因组平均而言女性的交叉率约为男性的 1.6 倍，但在端粒附近通常是男性更高（Bhérer et al. 2017）。
6. Myers 等：群体遗传与比较基因组数据显示，与约 40% 人类热点相关的基序在黑猩猩中不起作用，并在人类谱系中被清除；PRDM9 锌指预测能结合该基序，且快速进化。Baudat 等：小鼠品系间热点使用的差异对应 PRDM9 锌指阵列的多态；共有等位基因与基序的结合得到体外实验证实；人类 PRDM9 等位变异与热点使用相关。前者主要依赖序列与进化分析，后者结合了小鼠遗传学、体外结合实验与人类关联分析。可能的进一步证据：直接比较不同 PRDM9 等位基因的全基因组结合位点与 DSB 图谱；改变锌指阵列后观察热点是否随之移动（Davies et al. 2016 的人源化实验即属此类）；在多个物种中检验结合基序的侵蚀速率是否与预期一致；比较有无 PRDM9 的类群中热点的稳定性。

</details>

---

## 关键术语

| 中文 | English | 释义 |
|---|---|---|
| 双链断裂 | double-strand break (DSB) | DNA 两条链同时断开；减数分裂中由 SPO11 有计划地产生，以启动重组 |
| 双链断裂修复模型 | double-strand break repair (DSBR) model | 断裂末端切除、单链侵入同源染色体，形成双 Holliday 连接后被拆解的重组模型 |
| 双 Holliday 连接 | double Holliday junction (dHJ) | 两条同源 DNA 分子之间含两个四链交叉结构的重组中间体 |
| 非交叉 | non-crossover (NCO) | 两侧序列不发生互换的重组修复结果，常伴有短片段的基因转换 |
| 联会复合体 | synaptonemal complex | 减数分裂前期 I 中沿全长连接同源染色体的蛋白质结构 |
| 交叉结 | chiasma | 同源染色体之间可在显微镜下观察到的连接点，是交换的细胞学表现 |
| 交叉保证 | obligate crossover | 每对同源染色体通常至少发生一次交叉的规律 |
| 交叉稳态 | crossover homeostasis | 双链断裂数目波动时交叉数目仍保持相对稳定的现象 |
| Kosambi 作图函数 | Kosambi map function | 在推导中考虑了干涉的作图函数，$r = \tfrac{1}{2}\tanh(2d)$ |
| 基因转换 | gene conversion | 一条同源染色体上的一段序列被另一条同源染色体的序列非相互地改写 |
| 异源双链 DNA | heteroduplex DNA | 由来自两条同源染色体的单链配对形成、可能含有错配的双链 DNA |
| 重组热点 | recombination hotspot | 重组率远高于周围区域的狭窄基因组区段 |
| 精子分型 | sperm typing | 对精子 DNA 分型，以直接测定某一区段交叉与基因转换频率的方法 |
| 热点转换悖论 | hotspot conversion paradox | 热点等位基因因基因转换在传递中处于劣势、理论上应自我消亡却普遍存在的矛盾 |
| 雌雄重组差异 | heterochiasmy | 两性之间重组率或重组分布的差异 |

---

## 参考文献

- Baudat, F., Buard, J., Grey, C., Fledel-Alon, A., Ober, C., Przeworski, M., Coop, G., & de Massy, B. (2010). PRDM9 is a major determinant of meiotic recombination hotspots in humans and mice. *Science, 327*(5967), 836–840. https://doi.org/10.1126/science.1183439 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC4295902)］
- Bhérer, C., Campbell, C. L., & Auton, A. (2017). Refined genetic maps reveal sexual dimorphism in human meiotic recombination at multiple scales. *Nature Communications, 8*, 14994. https://doi.org/10.1038/ncomms14994 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC5414043)］
- Boulton, A., Myers, R. S., & Redfield, R. J. (1997). The hotspot conversion paradox and the evolution of meiotic recombination. *Proceedings of the National Academy of Sciences of the United States of America, 94*(15), 8058–8063.（DOI 未核实）［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC21556)］
- Brick, K., Smagulova, F., Khil, P., Camerini-Otero, R. D., & Petukhova, G. V. (2012). Genetic recombination is directed away from functional genomic elements in mice. *Nature, 485*(7400), 642–645. https://doi.org/10.1038/nature11089 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC3367396)］
- Cole, F., Kauppi, L., Lange, J., Roig, I., Wang, R., Keeney, S., & Jasin, M. (2012). Homeostatic control of recombination is implemented progressively in mouse meiosis. *Nature Cell Biology, 14*(4), 424–430. https://doi.org/10.1038/ncb2451 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC3319518)］
- Davies, B., Hatton, E., Altemose, N., Hussin, J. G., Pratto, F., Zhang, G., Hinch, A. G., Moralli, D., Biggs, D., Diaz, R., Preece, C., Li, R., Bitoun, E., Brick, K., Green, C. M., Camerini-Otero, R. D., Myers, S. R., & Donnelly, P. (2016). Re-engineering the zinc fingers of PRDM9 reverses hybrid sterility in mice. *Nature, 530*(7589), 171–176. https://doi.org/10.1038/nature16931 ［[牛津大学 ORA 存档](https://ora.ox.ac.uk/objects/uuid:0e9f43c0-7b12-4918-8158-cb4b3747dcf1)］
- Duret, L., & Galtier, N. (2009). Biased gene conversion and the evolution of mammalian genomic landscapes. *Annual Review of Genomics and Human Genetics, 10*, 285–311. https://doi.org/10.1146/annurev-genom-082908-150001
- Jeffreys, A. J., & May, C. A. (2004). Intense and highly localized gene conversion activity in human meiotic crossover hot spots. *Nature Genetics, 36*(2), 151–156.（DOI 未核实）
- Keeney, S., Giroux, C. N., & Kleckner, N. (1997). Meiosis-specific DNA double-strand breaks are catalyzed by Spo11, a member of a widely conserved protein family. *Cell, 88*(3), 375–384. https://doi.org/10.1016/S0092-8674(00)81876-0
- Kosambi, D. D. (1944). The estimation of map distances from recombination values. *Annals of Eugenics, 12*(1), 172–175. https://doi.org/10.1111/j.1469-1809.1943.tb02321.x（部分数据库将出版年记为 1943）
- Mihola, O., Trachtulec, Z., Vlcek, C., Schimenti, J. C., & Forejt, J. (2009). A mouse speciation gene encodes a meiotic histone H3 methyltransferase. *Science, 323*(5912), 373–375. https://doi.org/10.1126/science.1163601
- Myers, S., Bottolo, L., Freeman, C., McVean, G., & Donnelly, P. (2005). A fine-scale map of recombination rates and hotspots across the human genome. *Science, 310*(5746), 321–324. https://doi.org/10.1126/science.1117196
- Myers, S., Bowden, R., Tumian, A., Bontrop, R. E., Freeman, C., MacFie, T. S., McVean, G., & Donnelly, P. (2010). Drive against hotspot motifs in primates implicates the *PRDM9* gene in meiotic recombination. *Science, 327*(5967), 876–879. https://doi.org/10.1126/science.1182363 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC3828505)］
- Myers, S., Freeman, C., Auton, A., Donnelly, P., & McVean, G. (2008). A common sequence motif associated with recombination hot spots and genome instability in humans. *Nature Genetics, 40*(9), 1124–1129. https://doi.org/10.1038/ng.213
- Parvanov, E. D., Petkov, P. M., & Paigen, K. (2010). *Prdm9* controls activation of mammalian recombination hotspots. *Science, 327*(5967), 835. https://doi.org/10.1126/science.1181495
- Sardell, J. M., & Kirkpatrick, M. (2020). Sex differences in the recombination landscape. *The American Naturalist, 195*(2), 361–379. https://doi.org/10.1086/704943 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC7537610)］
- Singhal, S., Leffler, E. M., Sannareddy, K., Turner, I., Venn, O., Hooper, D. M., Strand, A. I., Li, Q., Raney, B., Balakrishnan, C. N., Griffith, S. C., McVean, G., & Przeworski, M. (2015). Stable recombination hotspots in birds. *Science, 350*(6263), 928–932. https://doi.org/10.1126/science.aad0843 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC4864528)］
- Szostak, J. W., Orr-Weaver, T. L., Rothstein, R. J., & Stahl, F. W. (1983). The double-strand-break repair model for recombination. *Cell, 33*(1), 25–35. https://doi.org/10.1016/0092-8674(83)90331-8
- Williams, A. L., Genovese, G., Dyer, T., Altemose, N., Truax, K., Jun, G., Patterson, N., Myers, S. R., Curran, J. E., Duggirala, R., Blangero, J., Reich, D., Przeworski, M., & T2D-GENES Consortium. (2015). Non-crossover gene conversions show strong GC bias and unexpected clustering in humans. *eLife, 4*, e04637. https://doi.org/10.7554/eLife.04637 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC4404656)］

**网络资源**（访问日期 2026-11-20）

- Coop, G. (n.d.). *Population and quantitative genetics*, Chapter 3 Population structure and correlations among loci. LibreTexts. https://bio.libretexts.org/Bookshelves/Genetics/Population_and_Quantitative_Genetics_(Coop)/03%3A_Population_Structure_and_Correlations_Among_Loci
- OpenStax. (n.d.). *Biology 2e*, §11.1 The process of meiosis. https://openstax.org/books/biology-2e/pages/11-1-the-process-of-meiosis

---

**上一讲** [Day 017 · 突变 II：随机性与适合度效应分布](day017-mutation-randomness-dfe.md) ｜ **下一讲** Day 019 · 基因组变异的形式与群体测序数据
