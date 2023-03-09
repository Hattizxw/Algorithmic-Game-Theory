# Kiraly’s algorithm

# 条件

When a leader is rejected by all followers in his list, he is given a  second chance

# 算法内容

- For a leader *l*, and for two followers *fi* and *fj* , we say that *l* prefers  *fi* to *fj* if 
  1. either he prefers *fi* in the usual sense 
  2. or he is indifferent between the two, *fj* is engaged and *fi* is free.
- For a follower *f*, and for two leaders *li* and *lj* , we say that *f* prefers  *li* to *lj* if
  1. either she prefers *li* in the usual sense 
  2. or she is indifferent between the two, *li* has a second chance (he is  proposing to the followers in his list for the 2nd time) and *lj* does not  (he is proposing to the followers in his list for the 1st time).

自我理解：当一轮配对之后，存在有leader没有follower，我们给leader第二次机会，此时，对于一些indifferent的follower来说，如果存在二次机会的leader给他发送了请求，他就会改变自己的偏好，先选择二次机会的那个leader

# 例子

l1:( f1 f2 )           f1: ( l1 l2 ) 

l2: f1                   f2: l1 

l3: f3 f4              f3: ( l3 l4 ) 

l4: f3                   f4: l3

首先，

l1向f1提出邀请，f1暂时接受l1，此时，

l2不能向f1提交申请，

l3向f3发出邀请，f3暂时接受l3，

l4不能向f3发送邀请，**此时给l2和l4第二次机会**

l2给f1发出邀请，由于f1是indifferent，所以，他会更改偏好，接受l2，

l1将只能给f2发送邀请，f2接受l1，

l4给f3发送请求，由于f3是indifferent，所以，他会更改偏好，接受l4，

l3只能给f4发送邀请，f4接受f3