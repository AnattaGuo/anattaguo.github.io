---
layout: post
title: 比特币如何交易及记账——小白学比特币之二
date: 2018-3-06
categories: blog
tags: [比特币,区块链]
---

在[小白学比特币1](/_posts/2018-02-14-learning-bitcoin-overview.md) 中， 提到比特币不仅是一个**电子现金**（系统），也是一个公开的账本，这账本上记录了每笔交易的信息。用比特币交易，其实就跟我们用人民币或者美元交易买卖东西一样。作者给比特币交易行为的定义是：

> In simple terms, a transaction tells the network that the owner of some bitcoin **value** has authorized the transfer of that **value** to another owner. The new owner can now spend the bitcoin by creating another transaction that authorizes transfer to another owner, and so on , in a chain of ownership. （简单来说，一笔转账告诉网络，这些比特币的所有者授权将这些比特币转给另外一个所有者。新的所有者可以通过创建一笔新的交易，授权转账给其他所有者，来花费这比特币，以此类推。）

那么，在比特币系统里，是以什么样的形式将这些交易记录下来的呢？

# 01. 比特币的记账方法
## 1.1 复式记账
跟传统记账一样，在比特币系统中也对交易采用复式记账的方法 (double-entry bookkeeping ledger)，直白点翻译就是双入口记账。复式记账，简单理解就是以下两点:

> - 每一笔交易都要在至少两个账户上进行记录。
> - 每一笔debit必须有一笔credit与之相匹配。(每单笔交易转账及所有交易转账总和都需要遵守基本会计等式 **资产(Assets) = 负债 (Liabiliteis) + 所有者权益 (Equity)**)
![复式记账](http://upload-images.jianshu.io/upload_images/147665-639780ddce338b35.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

**每一笔交易都要至少在两个账户上进行记录**，在会计记账中有三个基本账户也就是资产账户、负债账户以及所有者权益账户，跟会计等式**资产(Assets) = 负债 (Liabiliteis) + 所有者权益 (Equity)**是一一对应的。那么单独每个账户又是以怎么样的方式呈现出来的呢？方法是每个账户都需要记录这个账户的debits和credits（见上图）：
 - debits，借出给其他账户，记在账户左边。
 - credits，从其他账户借入，记在账户右边。

## 1.2 比特币的复式记账
说完复式记账，再回到《Mastering Bitcoin》(精通比特币) ，在书中，作者给出的记账例子如下面那张截图；一笔交易中可以包含多个Input和output。这里的Input和output如何理解呢？

> Each transaction contains one or more "inputs", which are like debits against a bitcoin account. On the other side of the transaction, there are one or more "outputs", which are like credits added to a bitcoin account. （每笔交易都包含一个或多个“输入”，就像存入比特币在比特币账户里。同样的，每笔交易也都包含一个或多个“输出”，就像在一个比特币账户增加一笔贷款。）
![比特币复式记账](http://upload-images.jianshu.io/upload_images/147665-8e49d33d3b8fc99c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

总结一下：
> In summary, transactions move value from transaction inputs to transaction outputs. 交易是将价值从Input移到output。

通过作者这句话，**可以看到比特币系统其实执行的是价值交易。更进一步地，可以理解为价值的输入和输出。**

# 02.交易链（Transaction Chains）

上笔交易和下笔交易之间会形成一个“无形的链”：
> The transactions form a chain, where the inputs from the latest transaction correspond to outputs from previous transctions. (这些交易会形成一个“链”，这个“链”上的input来自上一笔交易里相应的output,而这output又来自更早的一笔交易)。

作者用一张图形象的说明了什么是“交易链”。
- 在第一个笔交易中，Joe转给Alice 0.1005BTC, 在output这一边，有Alice地址里的0.1BTC以及0.005BTC的转账费用，加起来等于左边input的0.1005BTC。
- 在第二笔交易中，Alice转给Bob  0.0150BTC，output这一边里Bob钱包里的0.015BTC，加上Alice钱包里的0.0845BTC，再加上转账费用0.0005BTC等于左边input Alice钱包里的总额0.1BTC。
![比特币交易链](http://upload-images.jianshu.io/upload_images/147665-14c567c61b1fea3a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

对于同一个地址而言，上一笔交易中的output将会作为下一笔交易的输入，这样就形成了一个交易链。

![比特币交易链](http://upload-images.jianshu.io/upload_images/147665-9b1454d8ccc1e3d5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


# 03\. 找零[^2]
[^2]: https://en.bitcoin.it/wiki/Change

 在上面的交易截图中，我们可以看到这几笔交易里有**spent**、**unspent**和**change**。**change**为找零地址，为什么会有找零地址呢？

> This is beacuse transaction inputs, like currency notes, cannot be divided. (这是因为交易输入就和纸币一样，不可以被分割）

比特币系统中的找零概念和平时用现金交易的找零概念是一样的，如果你要买一个1块钱的包子，但是你身上只有一张20块钱的纸币，这个时候就需要包子铺老板找给你19元零钱。

| Inputs | Outputs |
| :------- | ----: |
| 20元 | 1 元 (给包子铺老板) |
|      | 10 元 (unspent) |
|      | 5元 (unspent) |
|      | 1元 (unspent) |
|      | 1元 (unspent) |
|      | 1元 (unspent) |
|      | 1元 (unspent) |

在比特币系统中，每一个input就相当于一定面值的纸币。如果一笔交易中只包含一个Input，为20个BTC，当这个地址向其他地址支付1个BTC时候，就需要对方找还19个BTC。不同的是，比特币不像纸币那样只有几种面值固定的纸币，比特币系统可以随时创建“新面值”。

| Inputs | Outputs |
| :------- | ----: |
| 20BTC-被销毁| 1BTC (spent) |
|      | 19BTC (新创建的面值，找还给你) |

出于保护隐私的考虑，找零地址没必要跟原先的付款地址一样，通常钱包会生成一个新的找零地址。

在真实应用中，并不会在找零地址旁边标注**change**的字样，如下图显示(截图来自blockchain.info上的某笔交易)，
![交易详情](http://upload-images.jianshu.io/upload_images/147665-db5707bd5b2314d2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

# 04. 比特币也有面值: UTXO

比特币系统可以随时创建“新面值”来用于找零，而且这“零钱”可以用于下次交易。在每个输出(output)记录里，可消费的比特币数量会被标记成**unspent**，这样的输出有一个专门的名字叫做**Unspent Transaction Outputs**(UTXO)。可以把unspent的输出理解为面值不同的、可用于下次消费的纸币，就好像10元面值纸币、100元面值纸币那样。

# 05. 比特币里没有币：真实比特币长什么样

在前文，我们展示了一笔交易在浏览其中长什么样子。下图就是上图中第二笔交易（Alice付给Bob 0.0150个BTC）在[浏览器中的展示](https://blockchain.info/tx/0627052b6f28912f2703066a912ea577f2ce4da4caa5a5fbd8a57286c345c2f2)， 其交易号为`0627052b6f28912f2703066a912ea577f2ce4da4caa5a5fbd8a57286c345c2f2` :

![交易`0627052b6f28912f2703066a912ea577f2ce4da4caa5a5fbd8a57286c345c2f2`](http://upload-images.jianshu.io/upload_images/147665-e0074486509c4322.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


但是，我们在页面上看到的这些地址、输入、输出等，在比特币的系统中脱掉“外衣”后，全都长另外一幅样子：

![脱掉华丽外衣的比特币交易](http://upload-images.jianshu.io/upload_images/147665-70847cc9f40db9be.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


这个可以简单的理解为面对不同对象时，说不同的语言：一种是对人说的语言，就是我们在网页上看到的那个样子；一种是对机器说的语言，就是用计算机编解码后的样子。

通过计算机把比特币交易信息解码后，可以看到比特币其实就是一串代码：
> **In bitcoin, there are no coins, no senders, no recipients, no balances, no accounts, and no addresses. All those things are constructed at a higher level for the benefit of the user, to make things easier to understand.** 在比特币里，没有币，没有发送者，没有收据，没有余额，没有账户，没有地址。这些东西呈现成这样是为了让用户更便于理解。

# 06. 再看交易输入和输出

让我们以本文开头截图中的第二笔交易，也就是交易号为`0627052b6f28912f2703066a912ea577f2ce4da4caa5a5fbd8a57286c345c2f2`的交易为例，看看在复式记账、网页前端及在比特币系统中这笔交易的呈现形式——

![比特币的三套衣服](http://upload-images.jianshu.io/upload_images/147665-2d34d144f9b38e25.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


# 07. 交易费
就像在银行转账需要手续费一样，在比特币系统中的每笔交易也需要手续费。**比特币系统中的手续费不是按照每笔交易所包含的币数量来计算**，通过上面几个章节的分析，可以知道比特币及系统中交易，其实是一串串代码。**比特币系统中的手续费是根据交易在网络上所占大小（以千字节为单位）来计算。** 把每笔交易想象成一个txt文本就好理解了，如果一笔交易所含字节多，所需手续费相应也会高。在待确认的交易中，矿工会优先选择处理手续费高的交易。
> Transaction fees are calculated based on the size of the transaction in kilobytes, not the value of the transaction in bitcoin.

在https://bitcoinfees.earn.com/#fees 这个网上可以查到整个比特币系统的交易费费情况，在http://bitcoinfees.21.co/api/v1/fees/recommended页面下可以查到当前最佳交易费用为多少。

当然，如果使用手机钱包客户端，一般会自动推荐合适的交易费用。

# 参考文献
- [1] Mastering Bitcoin 第二版 https://github.com/bitcoinbook/bitcoinbook
- [2] http://learnmeabitcoin.com
- [3] https://www.myaccountingcourse.com/accounting-basics/double-entry-accounting
***
# ChangeLog
- 20180318 发布至github，合并交易（上）及（下）
- 20180316 标题更改为“小白学比特币”， 增加参考文献
- 20180314 修改标题
- 20180228 首次公开发布
