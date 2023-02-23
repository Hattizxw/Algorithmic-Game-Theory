# Stable Matching with Incomplete Lists(SMI)

### 定义

> An agent prefers to remain unmatched than to get matched to an  unacceptable partner. (代理人宁愿保持不匹配，也不愿与不可接受的合作伙伴。)
>

### 匹配结果如下图所示

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/stable%20match.PNG

# Stable Matching with Ties（SMT）

### 定义

> Agents may be indifferent among several candidates 

### 匹配结果如下图所示

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/stable%20match1.PNG

# Leader-optimal matching

**Leader-optimal matching**: a stable matching in which each leader  receives his best achievable partner. 

**Follower-optimal matching**: a stable matching in which each follower  receives her best achievable partner.

# Conflict of interests

**Leader-pessimal matching**: a stable matching in which each  leader receives his worst achievable partner. 

**Follower-pessimal matching**: a stable matching in which each  follower receives her worst achievable partner.

# Dominant-strategy truthfulness

### **Gale-Shapley不是DS truthful**

- When the leader-oriented version of Gale-Shapley algorithm is  executed, all leaders find it in their best interest to be truthful.
- Some followers, however, may benefit from misreporting their  preferences.
-  因为，对于follower来说，他只是从向他发送propose的leader中选择更好的（并不一定是第一个），并不能从它的preferences中选择。
  - 对于每个leader来说，阐述他真实的preference是最优选择