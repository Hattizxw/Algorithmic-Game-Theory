# Stable Roommates problem (SR)

- Participants
  - 2n students or agents
- Preferences
  - Each agent has strict preferences over all other (2n-1)  agents
- Matching
  - A set of n disjoint pairs of agents
- Stable Matching
  - A matching M with no blocking pair

eg

A: **C** B D 

B: **D** C A 

C: B **A** D 

D: A C **B**

# Irving’s Algorithm

Irving’s algorithm runs in O(n^2 ) time and works in two phases

- **Phase 1**: similar to GS algorithm for the Stable Matching  problem
- **Phase 2**: elimination of “rotations”

### Semiengagement

如果x向y提出邀请，说明，x Semiengagement y，此时y并不需要接收x的邀请，它依然可以选择它偏好靠前的

### 例题

• A: C > D > B > F > E  

• B: F > E > D > A > C 

• C: B > D > E > A > F 

• D: E > B > C > F > A 

• E: C > A > B > D > F 

• F: E > A > C > D > B

##### 符号规定如下图

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/Irving%E2%80%99s%20Algorithm1.PNG

x的符号（X有一个 bottom  bar）意味着，x处于semiengaged状态，也就是说**x向y提出了邀请**

y的符号（y有一个top bar）意味着，**y被x提出了邀请**

##### Phase 1

###### 说明

1. A向c提出proposes，所以c有一个top bar；

   在c哪一行，需要给A画一个 bottom  bar（说明C被A提出了proposes）;

   需要将C行中A后面的F划去，因为即使C被F proposes，他因为已经有A了，所以不可能选择F;

   也需要将F行中的C划去

2. B向F提出proposes，所以F有一个top bar；

   在F哪一行，需要给B画一个bottom  bar（说明F被B提出了proposes）

3. C向B提出proposes，所以B有一个top bar；

   在B哪一行，需要给C画一个bottom  bar（说明B被C提出了proposes）

4. D向E提出proposes，所以E有一个top bar；

   在E哪一行，需要给D画一个bottom  bar（说明E被D提出了proposes）

   需要将E行中D后面的F划去，因为即使E被F proposes，他因为已经有D了，所以不可能选择F

   也需要将F行中的E划去

5. E向C提出proposes，所以C有一个top bar；

   在C哪一行，需要给E画一个bottom  bar（说明C被E提出了proposes）

   需要将C行中E后面的A也划去，则A行中的C也应该被划去，A需要重新向其他agent提出proposes

6. A向D提出proposes，所以D有一个top bar；

   在D哪一行，需要给A画一个bottom  bar（说明D被A提出了proposes）

7. F向A提出proposes，所以A有一个top bar；

   在A哪一行，需要给F画一个bottom  bar（说明A被F提出了proposes）

   同理需要将A行中的E划去，E行中的A划去

###### 这样做的原因是

例如A，当他向C提出proposes之后，A就not free，但是对于C来说，他还是free还可以接收其他agent的proposes，

但是，我们此时看C行，它已经有A这个选项，不可能再选F了，所以（C,F）应该被删除

###### 如下图所示

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/Irving%E2%80%99s%20Algorithm2.PNG

##### 一阶段结束之后得到

A： D B F  

B：F E D A C 

C： B D E  

D： E B C F A 

E： C B D  

F： A D B

##### Phase 2

###### Exposed Rotation说明

A： D **<font color="#dd0g0g">B</font>** F  

B：F E D A **<font color="#o000dd">C</font>** 

C： B **<font color="#dd0g0g">D</font>** E  

D： E B C F **<font color="#o000dd">A</font>** 

E： C B D  

F： A D B

用Exposed Rotatio表示为

|   P:    |  A   |  C   |  A   | Last entry   |
| :-----: | :--: | :--: | :--: | ------------ |
| **q：** |  B   |  D   |      | second entry |

ABCD关系如图所示：

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/Irving%E2%80%99s%20Algorithm3.PNG

解释：

找A的第二个选择B（写于A的正下方），再找B的最后一个选项为C（C开启另一列）；

再找C的最后一个选项D（写在C的正下方），再找D的最后一个选项A（C开启另一列）

停止

从这个表格中，我们可以得出

**D will reject A!** 

**and B will reject C!**

因为对于B和D来说，不会接收位于他们偏好的最后一个选项

###### 一轮Exposed Rotation之后，如图所示

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/Irving%E2%80%99s%20Algorithm4.PNG

• A: B > F  

• B: F > E > D > A  

• C: D > E  

• D: E > B > C > F  

• E: C > B > D 

 • F: A > D > B

###### 二轮Exposed Rotation之后

• A: F  

• B: E > D  

• C: D > E  

• D: B > C > F  

• E: C > B  

• F: A > D

###### 三轮Exposed Rotation之后

• A: F  

• B: E > D  

• C: D > E  

• D: B > C  

• E: C > B  

• F: A

###### 四轮Exposed Rotation之后

• A: F  

• B: D  

• C: E  

• D: B  

• E: C  

• F: A

###### 得到最终答案

• A: B > D > **F** > C > E 

• B: D > **E** > F > A > C 

• C: **D** > E > F > A > B 

• D: F > **C** > A > E > B 

• E: F > C > D > **B** > A 

• F: **A** > B > D > C > E