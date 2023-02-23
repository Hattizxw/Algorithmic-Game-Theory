对于拍卖来说，如何拍卖两个人（卖家和买家）都获利最多

**通过设计机制，提高最大化收入**

## 单物品拍卖

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/auction.PNG

## **密封价格拍卖（**Sealed-Bid Auctions**）**

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/auction1.PNG

## **第一价格拍卖**(First-Price Auctions)

在第一价格拍卖(First-Price Auctions)中，获胜的竞拍者需要支付的价格就是其报价，这也是现实中很常见的一种拍卖方式。

## 第二价格拍卖(Second-Price Auctions)

也即维克里拍卖(Vickrey auctions)  也是dominant-strategy truthful

在这种拍卖中，报价最高者支付第二高的报价得到拍卖的物品。

接下来，作者用两个命题及其证明说明了维克里拍卖的两个重要性质。

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/auction2.PNG

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/auction3.PNG

#### 为什么说vickrey是dominant-strategy truthful

truthful：大家都会出自己心中真实的对商品的估值。因为最终如果是i拍卖到商品（他的价格为最高），他并不是支付他所需出的价格，而是第二个人出的价格。

dominant- strategy：因为他出这个价格是最好的选择（可以拿到这个商品）

### **第二价格拍卖是理想的拍卖**

原因：满足了三个良好的性质

(1) 它是DSIC的；

(2) 它是社会福利最大化的；

(3) 它可以在多项式时间(实际上是线性时间)内实施。

**第(1)个性质中**的DSIC是占优策略激励相容。它使竞拍者的报价变得简单易行，也使拍卖设计者能够更容易地推测拍卖结果

**第(2)个性质中**

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/auction4.PNG

**第(3)个性质中**则是指完成拍卖结果计算所需要的时间随着拍卖参与者的增加线性增加，即可以在很短时间内运行出结果，从而保证实施效率。

## **经典案例：关键字搜索拍卖**

> 搜索引擎的搜索结果页面上一般有两类内容：一类是根据PageRank等算法得到的与搜索关键字相关的源生链接，另一类则是通过付费呈现出来的广告链接。每次我们在搜索引擎上搜索关键字时，搜索引擎在背后都实时地运行着一场拍卖，来决定哪些广告商的链接被显示出来、以怎样的次序排列、以及要付多少钱。这样的关键字搜索拍卖创造了巨大的利润，在2006年，这一块的利润占据了谷歌总利润的98%。

https://algorithmic-game-1316943030.cos.ap-nanjing.myqcloud.com/auction5.PNG