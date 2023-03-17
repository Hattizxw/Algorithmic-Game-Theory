# Defined by a Simultaneous Eating procedure

Agents simultaneously “eat” their most preferred items at a uniform speed, moving onto their next most preferred item whenever an item is fully eaten

# 例子

参与者的preference：

小明：红豆，薯条，饺子

小美：红豆，饺子，薯条

小红：薯条，红豆，饺子

### 第一步

小明，小美每人吃0.5的红豆，

小红吃0.5的薯条，

此时红豆吃完， 小明和小红开始分别吃薯条和饺子

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/RSD1.PNG

### 第二步

小明和小红每个人在吃0.25的薯条，此时薯条也吃完了，

小美吃了0.25的饺子，

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/RSD2.PNG

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/RSD3.PNG

### 第三步

小明和小红也开始吃饺子，第三轮每人再吃0.25的饺子

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/RSD4.PNG

### 结果

|      | 红豆 | 薯条 | 饺子 |
| :--: | :--: | :--: | :--: |
| 小明 | 0.5  | 0.25 | 0.25 |
| 小美 | 0.5  |  0   | 0.5  |
| 小红 |  0   | 0.75 | 0.25 |

# 例题

1：b>a>c

2:  a>b>c        

3:  a>c>b

结果：

|      |  a   |  b   |  c   |
| :--: | :--: | :--: | :--: |
|  1   |  0   | 3/4  | 1/4  |
|  2   | 1/2  | 1/4  | 1/4  |
|  3   | 1/2  |  0   | 1/2  |

# 不是 truthfulness

例子：

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/PSM.PNG