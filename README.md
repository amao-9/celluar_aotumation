# celluar_aotumation
Python实现元胞自动机
## 元胞自动机介绍
- 细胞自动机（英语：Cellular automaton），又称格状自动机、元胞自动机，是一种离散模型，在可计算性理论、数学及理论生物学都有相关研究。它是由无限个有规律、坚硬的方格组成，每格均处于一种有限状态。整个格网可以是任何有限维的。同时也是离散的。每格于t时的态由t-1时的一集有限格（这集叫那格的邻域）的态决定。每一格的“邻居”都是已被固定的。（一格可以是自己的邻居。）每次演进时，每格均遵从同一规矩一齐演进。

就形式而言，细胞自动机有三个特征：

- 平行计算（parallel computation）：每一个细胞个体都同时同步的改变
- 局部的（local）：细胞的状态变化只受周遭细胞的影响。
- 一致性的（homogeneous）：所有细胞均受同样的规则所支配
## 规则
- 当前细胞为存活状态时，当周围的存活细胞低于2个时（不包含2个），该细胞变成死亡状态。（模拟生命数量稀少）
- 当前细胞为存活状态时，当周围有2个或3个存活细胞时，该细胞保持原样。
- 当前细胞为存活状态时，当周围有超过3个存活细胞时，该细胞变成死亡状态。（模拟生命数量过多）
- 当前细胞为死亡状态时，当周围有3个存活细胞时，该细胞变成存活状态。（模拟繁殖）

## 实现方法
- 利用pygame库，将视窗划分为x*x的网格，每个网格形成一个“元胞自动机格”，每格维护自己的状态，每次tick只绘制变化了的单元
