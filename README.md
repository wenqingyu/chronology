## Story Point Approach

为了量化技术团队的开发迭代能力，方便团队效率优化，我们引入了敏捷开发里的一些重要概念，比如说 **Story Point，**关于Story Point的概念[**请看这里**](https://agilefaq.wordpress.com/2007/11/13/what-is-a-story-point/)。Story Point 被用作量化技术开发迭代能力的一个基础量度，但是一个完整优秀的技术团队除了有不错的基础的开发迭代能力以外，还应该具备对技术框架优化，新技术拓展，开发流程标准化以及效率优化等方面的考量。

对个人而言，Story Point也用来测量技术团队成员的能力和实际发挥效率，因此，仔细的设计Story Point的衡量方式会非常重要，因为错误，有偏差的会直接影响到团队成员的积极性和方向性。

### 测量维度

* 复杂度（Complexity）
* 工作时长（Work Time）
* 风险（Risk）

#### 工时（Effort）

我们先从最简单的开始，工时自然就是就是花费在该任务上的付出 **Effort**（主要是时间成本 **Time** **Effort**），但是脱离复杂度和风险（依赖性和失败概率）的考虑，工时本身是不全面且具有误导性的。比如：**“女人10月怀胎，是没有办法实现十个女人一个月生孩子“。**所以这里的工时是指 该任务**复杂度** 对应的 **最佳开发人员匹配**下的平均预估工作时长， 估计中还要充分考虑一些风险性问题（依赖性，需求变更，失败概率等）。即便如此，工时还是不能等价于**Story Point。**

随着任务的复杂度升高，对开发人员的能力，经验要求也会随之提高，如果开发人员缺乏对应任务的经验，就会需要额外的研究和分析工时，所以当我们定义一个任务的工时（Effort）的时候，就引入了一个 **复杂度（这个会在稍后阐述）** 与 **开发人员能力 **匹配度的概念：

即：**最佳匹配工时（Best Matching Effort）：** **Complexity Level &lt;---&gt; \(Capability/Experience Level\). **

**EX**: 对于一些刚刚开始运行的技术团队来说，后端新项目的数据库结构以及业务逻辑的设计，会是极重要并且非常烧脑的工作，这样的任务会被评估为**复杂度：高，对应复杂度系数 = 3。**这样的任务，通常最适合让团队里**经验丰富，能力较强**的后端架构师来主导设计，这样才能达到**能力，经验的最佳匹配**，使开发性能最大化，因此这里的**最佳匹配开发人员平均开发工时**就是这些高级架构师做这个任务的平均时长，我们假设是 **10** 个工时。

即：**Story Point = Task Complexity（该任务的复杂度）3 x Best Matching Effort（最佳匹配工时）10 = 30**

#### 

#### 复杂度（Complexity）

然而，复杂度本身量化也是个非常困难的问题，于是我们引入了两个Agile里面常用的概念，从这两个方向入手来考虑：

* 复杂度粒度（细分程度）

* 相对复杂度递进常量 ß。

**复杂度粒度：**我们往往会将不同的任务按照不同的复杂程度来划分，就像电商会将产品按照不同的产品类别来划分，然而，产品细分的颗粒程度也需要平衡，分得过于细腻，提高管理维护成本；反之分的过于粗略，体现不出差别，划分效果不明显。以我们目前的团队任务为例，我们暂时只分为三个等级：简单，中等，复杂，以防止因为过度划分，而浪费不必要的时间。待将后项目整体扩大，任务类别细化程度更高，再逐步细化复杂度粒度即可。当然，这里的参数，常量，划分方式都是尝试性的定义，对于不同的团队，项目，要根据实际情况条件和经验来确定。

**相对复杂度：**举个例子，将团队中涉及到的任务分为：简单，中等，复杂三个难度等级，找到团队里最基础，最简单的工作类型设为复杂度 = 1，比如：翻译StringID校对，调整基础的CSS样式等，视每个团队的实际情况而定。对应的，中等类型的复杂度 = 1 + 1 x 32% = 1 x 132%（稍后会解释 ß = 32%这个数值的确定思路），以此类推，复杂类型的复杂度 = 1 + \(132%\) ^ 2 = 174%。

至此，**Story Point **就可以根据 **Complexity x 最佳匹配开发人员平均开发工时 **得出**.**

| 示例任务 | 任务复杂度 | 最佳匹配工时 | Story Point |
| :--- | :--- | :--- | :--- |
| 新架构设计 | 复杂（1.74） | 13 | 23 |
| API开发 | 中等（1.32） | 5 | 7 |
| 基础CSS样式调整 | 基础（1） | 7 | 7 |



**斐波那契数列：理想状态下，Story Point 的分布，**相较于使用 \(1, 2, 3, 4, 5, 6, 7 . . .\) 的线性增长方式来估计，斐波那契数列（1, 2, 3, 5, 8, 13, 21）这样的方式更加有效，因为随着任务越大，point的数量越大，对于任务估计的误差也就越大，比如 1 和 2 分的 story point的任务有明显差别，但是 7 和 8 分的任务你几乎看不出任何差别。

