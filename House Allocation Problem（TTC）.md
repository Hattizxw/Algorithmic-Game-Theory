# 条件

- A model for allocation of indivisible goods.
- A set of *n* agents, each owns a unique house and a strict preference ordering over all *n* houses
- The objective is to reallocate the houses among the agents to improve the agents’ utility.

# Top Trading Cycle mechanism (**TTC**)

### **In each round:**

- Each agent points to her most preferred house (possibly her own house); each house points back to its owner
- This creates a directed graph; in this graph, identify cycles
  - Finite: cycle must exist
  - Strict preferences: each agent is in at most one cycle
- Assign each agent in a cycle to the house she is pointing at and remove her from the mechanism with her assigned house
- If all houses are assigned or all agents are assigned or all preference lists are empty, stop.

### 例子

a1: h3>h2>h1

a2: h1>h4>h2

a3: h1>h4>h3

a4: h3>h4

### 过程

a1指向自己最喜欢的房子h3，

h3指向自己的主人a3，

a3指向最近最喜欢的房子h1，

h1指向自己的主人a1，

这样子，他们四个就变成了一个cycle

所以：

- a1 is matched to h3
- a3 is matched to h1

对于a2来说，她最喜欢的房子是h1，已经被分配给了别人，他只能选择h4，

h4指向自己的主人a4，

a4指向自己最喜欢的房子h3，但是h3已经被分配给了别人，他只能指向h4，

这样，他们四个并不能形成一个闭合的cycle，

所以a2不能选择h4，a2只能选择h2，

h2指向自己的主人a2，这样他们俩可以形成一个闭合的cycle

- a2 is matched to h2

同理a4也是，他和自己的房子h4形成一个闭合的cycle

- a4 is matched to h4

##### 结果

- a1 is matched to h3
- a3 is matched to h1
- a4 is matched to h4
- a2 is matched to h2

这样做每个人最坏的情况也是得到自己的房子，不会有更坏的结果





