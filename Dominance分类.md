# Strict Dominance

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/Strict%20Dominance.PNG

无论对方选什么（出什么策略），自己选择的这个数（策略）都是最获利的

# Weak Dominance

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/Weak%20Dominance.PNG

无论对方选什么（出什么策略），自己选择的这个数（策略）至少和对方某一个策略相比是获利的，其他和对方策略获利情况相等。

eg：

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/Weak%20Dominance1.PNG

此图中，对于player 1来说，B相对于A来说是一个Weak Dominance

因为，B的值，（2，2，3）大于等于A的值（1，2，0）

# Very Weak Dominance

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/Very%20Weak%20Dominance.PNG

无论对方选什么（出什么策略），自己选择的这个数（策略）至少都是和对方获利情况相等。

> In all cases above we say that s ′ i is a strictly (resp. weakly; very weakly) dominated strategy.
>
> A strategy is strictly (resp. weakly; very weakly) dominant for an agent if it strictly (resp. weakly; very weakly) dominates any other strategy for that agent.

如果一个策略严格地（相对较弱；非常弱）支配一个代理的任何其他策略，则该策略对该代理是严格（相对较弱）支配的。

# Dominant-Strategy

占优策略是[博弈论](https://baike.baidu.com/item/博弈论/81545?fromModule=lemma_inlink)（game theory）中的[专业术语](https://baike.baidu.com/item/专业术语/10203750?fromModule=lemma_inlink)，所谓的占优策略就是指无论竞争对手如何反应都属于本企业最佳选择的竞争策略。显然，在公司的商务竞争过程中，具有占优策略的一方无疑拥有明显的优势，处于竞争中的主动地位。占优策略有时是显而易见的

### 定义

> 每一个博弈中的企业通常都拥有不止一个[竞争策略](https://baike.baidu.com/item/竞争策略?fromModule=lemma_inlink)，其所有策略的集合构成了该企业的策略集。在企业各自的策略集中，**如果存在一个与其他[竞争对手](https://baike.baidu.com/item/竞争对手?fromModule=lemma_inlink)可能采取的策略无关的最优选择，则称其为占优策略(**Dominant Strategy)，与之相对的其他策略则为**劣势策略**。占优策略是[博弈论](https://baike.baidu.com/item/博弈论?fromModule=lemma_inlink)（game theory）中的专业术语，**所谓的占优策略就是指无论竞争对手如何反应都属于本企业最佳选择的[竞争策略](https://baike.baidu.com/item/竞争策略?fromModule=lemma_inlink)**。显然，在公司的商务竞争过程中，具有占优策略的一方无疑拥有明显的优势，处于竞争中的主动地位。占优策略有时是显而易见的

### 两项原则

**原则1：如果一个[博弈](https://baike.baidu.com/item/博弈?fromModule=lemma_inlink)参与者拥有一个占优策略，则应该使用之。**

我们用一个广告例子来说明这个原则。两家公司， A和B，在考虑是否通过广告促销。它们的利润额将依赖于那一家公司做广告，或者两家公司都做广告，或者两家公司都不做广告。这些可能性和相应的利润额被总结在旁边的矩阵里（如图1所示）。

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/Dominant-Strategy.PNG

观察：

对A，无论B怎么做，做广告都是最优的。所以做广告是A的占优策略。

对B，无论A怎么做，做广告也都是最优的。所以做广告也是B的占优策略。

结论：两家厂商都应该做广告

**原则2：在[纳什均衡](https://baike.baidu.com/item/纳什均衡?fromModule=lemma_inlink)时，对于给定其他参与者的行为，每个参与者的行为都应该是最优。**

我们用一个稍加变化的广告[博弈](https://baike.baidu.com/item/博弈?fromModule=lemma_inlink)的例子来说明这个原则。A没有占优策略，如果B做广告，A的最佳对策是做广告；如果B不做广告，A的最佳对策还是做广告。对B来说，做广告是占优策略。

总体分析：

应用原则1，B应该做广告。然后应用原则2，A应该采用他对B做广告的最佳对策，所以A也应该做广告。因此，在纳什均衡时，A和B都做广告。

# an equilibrium in dominant strategies.

A strategy profile (s1, . . . ,sn) in which every si is a dominant strategy for agent i is called an equilibrium in dominant strategies.

# Dominant-strategy truthfulness

### 定义

A direct mechanism is dominant-strategy truthful if, for every agent i, telling the truth (i.e. revealing the true valuation) maximises i’s utility, no matter what strategy the other players pick.

### Vickrey auction is dominant-strategy truthful

**证据：**

Assume that the other bidders bid in some arbitrary way. We show that i maximises her utility by bidding truthfully. We break the proof into two cases:

1. By bidding honestly, i wins the auction. 
2. By bidding honestly, i loses the auction.

**Case 1: By bidding honestly, i wins**

- If i submitted a higher bid, she would still win and pay the same amount 
- If i submitted a lower bid, she would either still win and pay the same amount… or lose and get utility zero.

**Case 2: By bidding honestly, i loses**

- If i submitted a lower bid, she would still lose and pay nothing
- If i submitted a higher bid, she would either lose and still pay nothing… or win and pay more than her valuation.

### Dominant-strategy truthfulness满足这两个假设就成立

1. Every participant in the mechanism has a dominant strategy, no matter what her private valuation is （每个参加者都有自己的占优策略）
2. This dominant strategy is direct revelation, where the participant truthfully reports all of its private information to the mechanism.（每个参与者说的都必须是真实的）

### Characterization of DS Truthful Mechanisms

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/Characterization%20of%20DS%20Truthful%20Mechanisms.PNG