# Day 012 · 树状思维 I：如何阅读系统发育树

> **部分** 第一部分 概念基础与证据 ｜ **周次** 第 2 周 进化的证据与树状思维 ｜ **发布日期** 2026-11-14 ｜ **建议用时** 约 90 分钟（讲义 35′ · 主读／主看 35′ · 练习 20′）
> **主读** OpenStax *Biology 2e* §20.1–20.2；Yale EEB 122 第 15 讲 *Phylogeny and Systematics*；Gregory（2008）
> **关键词** tree thinking · phylogenetic tree · root · node · branch length · cladogram · phylogram · chronogram · polytomy · sister group · monophyly · paraphyly · polyphyly · node rotation · primitive lineage fallacy

## 学习目标

完成本讲后，应能够：

1. 说明系统发育树表示的是什么，识别根、节点、末端与枝，并区分分支图、系统发育图与时间树；
2. 依据共同祖先的远近判断亲缘关系，正确识别姐妹群，并理解节点旋转不改变树的含义；
3. 区分单系群、并系群与多系群，并能在具体例子中判别；
4. 识别并纠正常见的读树误区：按末端顺序读出"进化阶梯"、把早分支或物种贫乏的谱系视为"原始"、把现生物种当作彼此的祖先；
5. 用树状思维重新表述"人类由黑猩猩进化而来"之类的说法。

---

## 1 系统发育树与树状思维

**系统发育树**（phylogenetic tree）以分支图的形式表示一组生物的进化关系，即谱系分化的历史。系统发育树是关于过去的**假说**：它由形态、分子等数据推断而来，会随新类群的发现与新数据的积累而修订（OpenStax §20.1）。《物种起源》全书唯一的插图就是一幅谱系分歧图（Darwin 1859；Day 002）。

能够正确阅读与运用系统发育树的能力，被 O'Hara 称为**树状思维**（tree thinking）；O'Hara（1997）把它与 Mayr 所说的"群体思维"（population thinking）对照讨论。Baum、Smith 与 Donovan（2005）指出，树状思维并不容易掌握：人们常常误读系统发育树，例如把一棵只表示人与小鼠共享祖先的树，读成"人由小鼠演化而来"。他们主张在各个层次的进化生物学教学中都训练树状思维。Gregory（2008）系统梳理了十种最常见的读树误区。本讲先讲读树的规则（第 2–4 节），再讨论误区（第 5 节）。

树的末端可以是物种，也可以是种群、个体或基因。由一个基因的序列推断出的**基因树**未必与物种树一致，原因将在 Day 046 与 Day 120 讨论。本讲默认末端为物种。

---

## 2 树的构成

### 2.1 根与时间方向

**有根树**（rooted tree）有一个代表全部类群共同祖先谱系的**根**（root），时间从根流向末端；**无根树**（unrooted tree）只表示类群之间的关系，不指明共同祖先的位置（OpenStax §20.1）。为无根树定根，通常需要引入一个已知位于研究类群之外的**外类群**（outgroup）：根被放在外类群与研究类群（内类群）之间。同样数目的物种，有根树比无根树多得多（Day 010 练习 1）。

### 2.2 节点

**内部节点**（internal node）代表一次谱系分化，也可以理解为其所有后裔的**最近共同祖先**（most recent common ancestor, MRCA）所在的祖先群体。若一个节点分出两个以上的谱系，称为**多歧分支**（polytomy）。多歧分支通常表示现有数据尚不能解析这些谱系之间的关系（OpenStax §20.1），少数情况下也可能代表几乎同时发生的多次分化。

许多发表的树在节点旁标有数值，如自展值（bootstrap）或后验概率。它们度量的是数据对该节点所定义的分支的统计支持程度，而不是分化的时间或谱系的"年龄"。支持度低的节点应被视为不确定的关系，读树时不宜据此下结论。这些数值的计算方法见 Day 115–118。

### 2.3 枝与枝长

**枝**（branch）代表谱系随时间的延续。按枝长的含义，常见的树有三类：

- **分支图**（cladogram）：只表示分支拓扑，枝长没有意义。除非另有说明，不应把枝长读成经历的时间（OpenStax §20.1）。
- **系统发育图**（phylogram）：枝长与变化量成正比，例如每个位点的替换数，通常附有比例尺。
- **时间树**（chronogram）：枝长与时间成正比。所有现生末端到根的距离相等，这样的树称为**超度量树**（ultrametric tree）。

### 2.4 末端

树的**末端**（tip）是被抽样的类群。对于现生物种组成的树，所有末端都是同时代的，任何一个末端都不是另一个末端的祖先。

### 2.5 同一棵树的不同画法

同一组关系可以画成直角的矩形树、斜线树、环形树，或不定根的放射状树。只要拓扑（以及有意义的枝长）相同，这些图包含的信息完全一样。画法的选择取决于用途：末端很多时环形树更节省空间，强调时间时宜用带时间轴的矩形树。画法也会影响读者的理解，例如过于写实、带叶的"大树"图形就容易引起误读（第 5 节）。

---

## 3 读树：亲缘关系取决于共同祖先的远近

### 3.1 亲缘关系的定义

在树中，A 与 B 的亲缘关系比 A 与 C 更近，当且仅当 A 与 B 的最近共同祖先比 A 与 C 的最近共同祖先更晚（更靠近末端）。判断亲缘关系的方法是沿着枝回溯到节点，而不是看末端在图上是否相邻。由同一个节点分出的两个谱系互为**姐妹群**（sister group）。姐妹群起源于同一次分化，因此一样"古老"（Crisp & Cook 2005），二者都不是对方的祖先（OpenStax §20.1）。

### 3.2 节点旋转

绕任何一个节点旋转其后裔枝，都不改变树所表示的关系（OpenStax §20.1）。因此，末端从左到右的排列顺序没有意义。一棵有 $n$ 个末端的完全分辨有根树有 $n - 1$ 个内部节点，每个节点都可以旋转，所以同一棵树共有 $2^{n-1}$ 种等价的画法（练习 2）。这正是"沿末端顺序读树"是错误的原因：同一棵树可以把任何一个类群画在最右端。

### 3.3 读树示例

以有根树 `((A,(B,C)),(D,E));` 为例，读树可以按以下步骤进行：

1. 找出所有内部节点：(B,C)、(A,(B,C))、(D,E) 与根，共 4 个，对应 $2^{4} = 16$ 种等价画法。
2. 确定姐妹群：B 与 C 互为姐妹群；A 是 (B,C) 的姐妹群；(D,E) 是 (A,B,C) 的姐妹群。
3. 比较亲缘关系：A 与 B 的最近共同祖先是节点 (A,(B,C))，A 与 D 的最近共同祖先是根，因此 A 与 B 的关系比 A 与 D 更近；而 A 与 B、A 与 C 的关系同样近。
4. 判断单系性：{B, C}、{A, B, C}、{D, E} 都是单系群；{A, B} 不是，因为它们最近共同祖先的后裔还包括 C。

注意，第 3 步中 A 与 B、A 与 C 的关系"同样近"，与图中哪一个末端离 A 更近无关。

### 3.4 相似性不等于亲缘关系

在系统发育图中，不同谱系的进化速率可能差别很大。如果一个谱系积累了大量变化，它与自己的姐妹群在总体上可能并不相似，反而与关系较远的类群更相似（练习 3）。因此，亲缘关系不能由总体相似性直接读出，而要依据共有衍征（Day 006）来推断；Day 013 将讨论这一原则在分类中的应用，Day 114 将讨论由速率差异引起的长枝吸引问题。

---

## 4 单系群、并系群与多系群

依据一个类群是否包含其共同祖先的全部后裔，可以把类群分为三类：

- **单系群**（monophyletic group），又称**分支**（clade）：一个祖先及其全部后裔；分支必须包含一个分支点的全部后裔（OpenStax §20.2）。由定义可知，在有根树上，剪断通向某个节点的那根枝，就能把一个单系群与树的其余部分分开。
- **并系群**（paraphyletic group）：一个祖先及其部分而非全部后裔。传统意义上的"爬行动物"不包括鸟类，而鸟类与被包括在内的动物拥有共同祖先，因此是并系群（Digital Atlas of Ancient Life, n.d.）。
- **多系群**（polyphyletic group）：成员来自不同的谱系，类群不包含其成员的最近共同祖先（Georgia Institute of Technology, n.d.）；这类类群通常是依据趋同的相似性归并起来的。

在树上还可以追溯性状的起源。若某个性状只出现在一个单系群中，最简单的解释是它在该分支的祖先中出现过一次，并被全部后裔继承，即同源（Day 006）；若具有该性状的类群分散在树的不同位置，则可能需要假定多次独立起源（趋同），或一次起源加若干次丢失。选择所需变化次数最少的解释，就是最大简约原则（OpenStax §20.2；方法见 Day 114）。按这种性状视角，一个由趋同性状定义、其共同祖先并不具有该性状的类群，通常被称为多系群。

只有单系群反映了完整的谱系历史。并系群与多系群在日常语言中仍很常用，但不能当作进化单元来使用。Day 009–010 讨论的平胸鸟提供了一个例子：Harshman 等（2008）发现能飞的䳍类位于平胸鸟内部，平胸鸟因此不构成单系群（练习 5）。分类是否只应承认单系群，将在 Day 013 讨论。

---

## 5 常见的读树误区

**表 1 常见读树误区及其纠正**

| 误区 | 例子 | 正确的理解 |
|---|---|---|
| 沿末端顺序读树 | 由末端从左到右的排列读出关系或"进化顺序" | 末端顺序可以任意旋转，亲缘关系只取决于节点 |
| 把某一类群当作"主干" | 把人类所在的谱系画成主线，其他类群都是旁枝 | 树没有主干，每个末端谱系从根到现在经历的时间相同 |
| 把共同祖先想象成某个现生类群 | 认为两个现生类群的共同祖先很像其中一方 | 共同祖先是已灭绝的群体，其性状需要独立推断 |
| 原始谱系谬误 | 把物种贫乏、"最早分出"的谱系当作祖先或"原始" | 姐妹群一样古老；"原始"与"衍生"只适用于性状，不适用于整个生物 |
| 把现生物种当作彼此的祖先 | "人类由黑猩猩进化而来" | 人与黑猩猩是姐妹谱系，源于一个已灭绝的共同祖先 |

表 1 中的前三条见于 Gregory（2008）。其中最严重的是**原始谱系谬误**（primitive lineage fallacy）：把物种贫乏、看似"早分支"或位于"基部"（basal）的谱系视为祖先（Omland et al. 2008）。Crisp 与 Cook（2005）指出，这类误读源于没有区分现生的后裔与早已灭绝的祖先。早分支谱系的现生代表经历了与其姐妹群同样长的进化时间，完全可能有大量自身的衍生性状；"祖征"与"衍征"只适用于具体的性状状态，用来描述整个生物没有意义。祖先的性状只能通过统计模型推断，而且需要化石、发育与功能形态等独立信息的支持。教材中常用的"基部类群"（basal taxon）一词（OpenStax §20.1），使用时应注意它只描述分支位置，而不意味着"原始"。

另一类误区与时间有关。例如，把直立树最左侧（或横置树最下方）的末端读成"最早出现"或"最古老"的类群（见 *Understanding Evolution* 的 The Tree Room）。这些误区的共同根源，是把分支的树读成了线性的阶梯，也就是 Day 002 讨论的"自然阶梯"观念的残余。Omland 等（2008）因此强调，系统发育树表示的是现生物种作为亲属的关系，而不是祖先与后裔的序列。

Understanding Evolution 的读树资源还建议，作图时使用直角的树形、附上时间轴，并把人类等容易被视为"高等"的类群放在树的中部而非边缘。这些建议说明，树的画法本身会影响读者的理解。

---

## 今日学习材料（均可免费获取）

| 类型 | 材料 | 说明 |
|---|---|---|
| 必读 | [OpenStax *Biology 2e* §20.1 Organizing Life on Earth](https://openstax.org/books/biology-2e/pages/20-1-organizing-life-on-earth) | 系统发育树的基本术语与读法，约 15 分钟 |
| 必读 | [OpenStax *Biology 2e* §20.2 Determining Evolutionary Relationships](https://openstax.org/books/biology-2e/pages/20-2-determining-evolutionary-relationships) | 同源与同功、分支与简约法，约 15 分钟 |
| 必看 | [Yale EEB 122](https://oyc.yale.edu/ecology-and-evolutionary-biology/eeb-122) 第 15 讲 *Phylogeny and Systematics* | 分子系统学的发现与建树的基本思路，附讲稿 |
| 精读 | Gregory（2008）：[开放获取全文](https://doi.org/10.1007/s12052-008-0035-x) | 十种常见读树误区，建议完整阅读 |
| 选读 | *Understanding Evolution*：[The Tree Room](https://evolution.berkeley.edu/the-tree-room/) | 读树入门与[常见误区](https://evolution.berkeley.edu/the-tree-room/tree-misinterpretations) |

---

## 思考与练习

1. **（读树）** 有根树 T 的 Newick 表示为 `((((A,B),C),(D,E)),(F,G));`。(a) C 的姐妹群是什么？(b) C 与 A 更近，还是与 D 更近？为什么？(c) 下列类群中哪些是单系群：{A, B, C}、{C, D, E}、{D, E, F, G}、{F, G}、{A, B, C, D, E}？(d) T 有多少个内部节点？同一棵树有多少种等价的画法？
2. **（旋转与计数）** 判断下列树中哪些与 T1 = `((A,B),(C,(D,E)));` 表示相同的关系：T2 = `(((E,D),C),(B,A));`，T3 = `((A,C),(B,(D,E)));`，T4 = `(((D,E),C),(A,B));`。并计算 $n = 5$、$10$、$20$ 个末端的完全分辨有根树各有多少种等价画法。
3. **（枝长）** (a) 系统发育图 `((A:0.50,B:0.05):0.10,C:0.15);` 中枝长以每位点替换数计。计算 A–B、B–C、A–C 之间沿树的路径长度（patristic distance）。B 的姐妹群是谁？B 在总体上与谁更"相似"？如何解释二者的差异？(b) 时间树 `((A:10,B:10):30,(C:25,D:25):15);` 中枝长以百万年计。验证它是超度量树，并求 A 与 B、A 与 C、C 与 D 分别在多久以前拥有最近共同祖先。
4. **（纠正误读）** 用树状思维改写下列说法，并指出各自对应表 1 中的哪种误区：(a) "人类由黑猩猩进化而来。"(b) "单孔类是其余现生哺乳动物的姐妹群，所以鸭嘴兽是原始的哺乳动物，保留了哺乳动物祖先的全部特征。"(c) "这棵树的最右端是人类，说明人类是进化的顶点。"(d) "物种最少的那一支是最古老的类群。"
5. **（类群判别）** (a) 按本讲的定义，不包括鸟类的"爬行动物"为什么是并系群？(b) 根据 Harshman 等（2008）的结果，䳍类位于平胸鸟内部。若只按成员组成来判断，不包括䳍类的"平胸鸟"属于哪一类群？(c) Harshman 等把平胸鸟称为"多系"。结合平胸鸟赖以定义的性状（不能飞行）的起源，解释这一用法。由此看，并系与多系的区分依赖于什么？
6. **（文献评论）** Baum 等（2005）主张在各个层次的生物学教学中训练树状思维，Omland 等（2008）则强调树状思维对"全部生物学"的意义。举两个例子，说明在进化生物学以外的研究中，读树错误可能导致错误的结论。

<details>
<summary>答案要点</summary>

1. (a) (A,B)。(b) 与 A 更近：C 与 A 的最近共同祖先是节点 ((A,B),C)，比 C 与 D 的最近共同祖先（节点 (((A,B),C),(D,E))）更晚，与图中末端的位置无关。(c) {A, B, C}、{F, G}、{A, B, C, D, E} 是单系群；{C, D, E} 与 {D, E, F, G} 不是（代码验算）。(d) 7 个末端、6 个内部节点，共 $2^{6} = 64$ 种等价画法。
2. T2 与 T4 与 T1 相同，只是若干节点被旋转；T3 不同，因为它把 A 与 C 归为姐妹群。$n = 5$、$10$、$20$ 时，等价画法分别为 16、512 与 524,288 种。
3. (a) A–B = 0.55，B–C = 0.30，A–C = 0.75。B 的姐妹群是 A，但 B 与 C 之间的路径更短，即在总体上更相似。原因是 A 所在的谱系进化速率很快、积累了大量变化，使 A 与 B 变得不相似；亲缘关系由共同祖先决定，而不是由总体相似性决定。这种速率差异若不加处理，还可能误导建树（长枝吸引，Day 114）。(b) 四个末端到根的距离都是 40，故为超度量树。A 与 B 的最近共同祖先在 1000 万年前，A 与 C 在 4000 万年前（即根），C 与 D 在 2500 万年前。
4. (a) 人与黑猩猩是姐妹谱系，源于一个已灭绝的共同祖先，两者自分化以来都在进化（把现生物种当作祖先）。(b) 即使单孔类确是其余现生哺乳动物（兽类）的姐妹群，两个谱系自分化以来也经历了同样长的时间；鸭嘴兽可能保留了某些祖征，也必然具有许多自身的衍征，"原始"只能针对具体性状而言（原始谱系谬误）。(c) 末端顺序可以任意旋转，任何类群都可以被画在最右端；树没有"顶点"（沿末端顺序读树、把某一类群当作主干）。(d) 姐妹群一样古老，物种数的多少反映的是物种形成与灭绝速率的差异，而不是起源的早晚（原始谱系谬误）。
5. (a) 爬行动物的最近共同祖先的后裔包括鸟类，把鸟类排除在外，就只包含了部分后裔。(b) 若平胸鸟与䳍类合起来构成一个单系群（古颚类），去掉其中的一个单系亚群（䳍类）后，剩下的成员只包含共同祖先的部分后裔，按成员组成判断是并系群。(c) 不能飞行在平胸鸟中至少独立出现了三次，其最近共同祖先很可能能够飞行；若以"不能飞行"来定义这个类群，它就是依据趋同性状归并的、不包含具有该性状的共同祖先的类群，因此被称为多系。可见，并系与多系的区分取决于我们是只看成员组成，还是同时考虑定义类群的性状在祖先中是否存在；Day 013 将继续讨论这一问题。
6. 示例：(1) 比较基因组学中，把"早分支"的现生物种当作祖先状态的代表，可能把该物种自身的衍生性状误认为祖先性状（Crisp & Cook 2005；Omland et al. 2008）；(2) 在病原体传播研究中，把序列相似性直接读成传播关系，或把末端的排列顺序读成传播的先后，都会得出错误的传播路线；(3) 在保护生物学中，把物种贫乏的谱系误认为"活化石"或"原始"，会影响对进化独特性的评估。

</details>

---

## 关键术语

| 中文 | English | 释义 |
|---|---|---|
| 树状思维 | tree thinking | 依据系统发育关系理解生物多样性与性状演化的思维方式 |
| 系统发育树 | phylogenetic tree | 表示一组生物谱系分化历史的分支图，是关于过去的假说 |
| 有根树 | rooted tree | 指明全部类群共同祖先所在位置、具有时间方向的树 |
| 无根树 | unrooted tree | 只表示类群之间的关系、不指明共同祖先位置的树 |
| 外类群 | outgroup | 已知位于研究类群之外、用于为树定根的类群 |
| 内部节点 | internal node | 树中代表一次谱系分化的点，对应其后裔的最近共同祖先 |
| 最近共同祖先 | most recent common ancestor (MRCA) | 一组类群的所有共同祖先中最晚的那一个 |
| 多歧分支 | polytomy | 一个节点分出两个以上谱系，通常表示关系尚未解析 |
| 分支图 | cladogram | 只表示分支拓扑、枝长没有意义的树 |
| 系统发育图 | phylogram | 枝长与变化量成正比的树 |
| 时间树 | chronogram | 枝长与时间成正比的树 |
| 超度量树 | ultrametric tree | 所有末端到根的距离相等的树 |
| 姐妹群 | sister group | 由同一个节点分出的两个谱系 |
| 节点旋转 | node rotation | 绕节点交换后裔枝的左右位置，不改变树所表示的关系 |
| 单系群（分支） | monophyletic group (clade) | 一个祖先及其全部后裔 |
| 并系群 | paraphyletic group | 一个祖先及其部分而非全部后裔 |
| 多系群 | polyphyletic group | 成员来自不同谱系、不包含其最近共同祖先的类群 |
| 原始谱系谬误 | primitive lineage fallacy | 把物种贫乏、早分支的谱系视为祖先或"原始"的错误 |

---

## 参考文献

- Baum, D. A., Smith, S. D., & Donovan, S. S. S. (2005). The tree-thinking challenge. *Science, 310*(5750), 979–980. https://doi.org/10.1126/science.1117727
- Crisp, M. D., & Cook, L. G. (2005). Do early branching lineages signify ancestral traits? *Trends in Ecology & Evolution, 20*(3), 122–128. https://doi.org/10.1016/j.tree.2004.11.010
- Darwin, C. (1859). *On the origin of species by means of natural selection, or the preservation of favoured races in the struggle for life*. John Murray. ［[Project Gutenberg](https://www.gutenberg.org/ebooks/22764)］
- Gregory, T. R. (2008). Understanding evolutionary trees. *Evolution: Education and Outreach, 1*, 121–137. https://doi.org/10.1007/s12052-008-0035-x ［开放获取］
- Harshman, J., Braun, E. L., Braun, M. J., Huddleston, C. J., Bowie, R. C. K., Chojnowski, J. L., Hackett, S. J., Han, K.-L., Kimball, R. T., Marks, B. D., Miglia, K. J., Moore, W. S., Reddy, S., Sheldon, F. H., Steadman, D. W., Steppan, S. J., Witt, C. C., & Yuri, T. (2008). Phylogenomic evidence for multiple losses of flight in ratite birds. *Proceedings of the National Academy of Sciences of the United States of America, 105*(36), 13462–13467. https://doi.org/10.1073/pnas.0803242105 ［[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC2533212)］
- O'Hara, R. J. (1997). Population thinking and tree thinking in systematics. *Zoologica Scripta, 26*(4), 323–329.（DOI 未核实）
- Omland, K. E., Cook, L. G., & Crisp, M. D. (2008). Tree thinking for all biology: The problem with reading phylogenies as ladders of progress. *BioEssays, 30*(9), 854–867. https://doi.org/10.1002/bies.20794

**网络资源**（访问日期 2026-11-14）

- Digital Atlas of Ancient Life. (n.d.). *Phylogenetic trees and classification*. https://www.digitalatlasofancientlife.org/learn/systematics/phylogenetics/trees-classification/
- Georgia Institute of Technology. (n.d.). *Phylogenetic trees*. Biological Principles. https://bioprinciples.biosci.gatech.edu/module-1-evolution/phylogenetic-trees
- OpenStax. (n.d.). *Biology 2e*, §20.1 Organizing life on Earth. https://openstax.org/books/biology-2e/pages/20-1-organizing-life-on-earth
- OpenStax. (n.d.). *Biology 2e*, §20.2 Determining evolutionary relationships. https://openstax.org/books/biology-2e/pages/20-2-determining-evolutionary-relationships
- Stearns, S. C. (2009). *EEB 122: Principles of evolution, ecology and behavior* [Video lectures]. Open Yale Courses. https://oyc.yale.edu/ecology-and-evolutionary-biology/eeb-122
- University of California Museum of Paleontology. (n.d.). *The tree room*. Understanding Evolution. https://evolution.berkeley.edu/the-tree-room/

---

**上一讲** [Day 011 · 正在发生的进化：直接观测](day011-evolution-in-action.md) ｜ **下一讲** Day 013 · 树状思维 II：系统分类与命名
