# YRMH-IGYT 原理

- Fix a priority order of the agents

- Let the agent with the top priority receive her first-choice room, the 

  second agent receive her top choice among the remaining goods and so 

  on, until someone requests the room of an existing tenant.

- If the existing tenant whose room is requested has already received a 

  room, then proceed the assignment to the next agent. *Otherwise, insert* 

  *the existing tenant at the top of the priority order and proceed with the* 

  *procedure.*

- If at any step a cycle forms, the cycle is formed by existing tenants (*a*1,..,*a**k*) where *a*1 points to the house of agent *a*2, who points to the house of *a*3, and so on. In such a case assign these houses by letting them exchange, and then proceed with the algorithm.

# 例子

### 题目如图片所示：

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/YRMH-IGYT.PNG

Priority order>：a13, a15, a11, a14, a12, a16, a10, a1, a2, a3, a4, a5, a6, a7, a8, a9

### 解题过程

##### 第一步：

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/TRMH-IGYT1.PNG

按照优先级，a13先选择房子，根据a13的偏好，他倾向于h6，

但是h6现在属于a6

我们需要将a6的优先顺序提到最前面，（因为只有a6获得了他更喜欢的房子，他才会放弃h6，将h6给a13）

根据a6的偏好列表，我们发现他喜欢他自己的房子，所以

**a6还是匹配h6**

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/YRMH-IGYT2.PNG

a13只能选择他第二喜欢的房子了，他第二个喜欢的是h13

此时h13并没有主人，所以我们把h13分配给a13

##### 第二步：

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/YRMH-IGYT3.PNG

a15同理，a15喜欢h1，

但是h1此时有主人（a1）

我们需要将a1的优先权提前到a15之前，

a1喜欢h15（没有被分配给任何人）

所以**a1得到h15，**

**a15得到h1**

##### 第三步：

a11喜欢h2，

h2房子的主人a2喜欢h3，

h3房子的主人a3喜欢自己的房子h3

所以**a3依然分配的是h3**

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/YRMH-IGYT4.PNG

此时，需要看a2偏好列表的第二个选项（h4）

h4的主人a4喜欢h2

此时，a2，h2，a4，h4形成了cycle，

所以**a2分配h4，a4分配h2**

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/YRMH-IGYT5.PNG

但是此时**a11**无法得到h2，只能根据他的喜好列表得到**h16**

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/YRMH-IGYT6.PNG

##### 其他的以此类推

# 属性

- 我们可以把YRMH-IGYT看作是GaleiTTC的变体，其中所有空的房屋（以及最初的所有者已经被分配的房屋）都指向最高优先的代理，而不是房屋的所有者。所以我们有时也称这个机制为TTC。
- The YRMH-IGYT mechanism is Pareto efficient, strategyproof, and makes no existing tenant worse off