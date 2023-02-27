# 需要解决的问题

Agents on one side can get matched to several candidates

- Many-one stable matching problem
- Hospitals/Residents problem (HR) and HR with Ties (HRT)

Note: In HR incomplete lists are allowed.

# 匹配原则

- Applicants rank hospitals in order of preference
- Hospitals do likewise with their applicants

# Hospitals / Residents problem (HR)

###  Participants

- A set of n1 residents {r1 , r2 , …, rn1 }
- A set of n2 hospitals {h1 , h2 , …, hn2 }

Each hospital has a **capacity**

### Preferences

- Residents rank acceptable hospitals in strict order of  preference, hospitals do likewise
- We assume that unacceptability is mutual: if h finds r unacceptable then r finds h unacceptable and vice versa

# Resident - oriented GS

##### 例子：

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/Resident%20-%20oriented%20GS.PNG

##### 原理：

**r1选择h2，**

**r2选择h1**

**r3选择h1**

此时，由于h1医院已经满员（两个），不能再选了，

r5，r6不能再选h1医院了，将h5和h6中如果出现了h1，划去

r4选择h2，h2暂时满员，r4之后的r5不能选择h2了，所以将r5中的h2划去，

r5没有匹配的医院

**r6**不能选择h1，可以**选择h2**，因为在h2的Preferences中，r6比r4靠前，且**r4选择h3**

Stable matching: M = {(r1 , h2 ), (r2 , h1 ), (r3 , h1 ), (r4 , h3 ), (r6 , h2 )} 

# Hospital - oriented GS

##### 例子

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/Hospital%20-%20oriented%20GS.PNG

##### 原理

**h1选择r1，r3**

**h2选择r2，r6**

**h3选择r4**，r3，此时，h1和h3都选择r3，但是在r3的Preferences中h1排在前面，所以r3选择h1

Stable matching: M = {(r1 , h1 ), (r2 , h2 ), (r3 , h1 ), (r4 , h3 ), (r6 , h2 )}