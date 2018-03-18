---
layout: post
title: 谁说区块链上数据不可篡改？——小白学比特币之五
date: 2018-3-17
categories: blog
tags: [比特币,区块链]
description: 区块链数据其实可篡改
---

本文为作者原创，已做[press.one数字签名](https://press.one/file/v?s=a1ac80c24fb3ca6e6118797d62c8e4937bef8fb8878cbf60baa589ae345a8539b92f2343a30d8060603b0c29fdcb93efbc46486b0f3beb11c5c095ddf3dfd74f0&h=281ceeb89ef781ede44ded261cd81b11c9d8d1e2ffbade1b328052c2d29567da&a=dd1bb42228bee252f306bc2529d1d887482cb23a&f=P1&v=2)。

本文为小白学习比特币基本概念系列之四，若有理解不当或者叙述不够简单明了详尽之处，恳请指出、留言讨论。

***
# 01. 什么是共识攻击？
众所周知，比特币系统里的交易有一个很大的特点，就是**不可篡改**性（数据不可篡改）。在比特币网络，每一笔交易，被验证过后就永远的被记录在链里，而且是所有人共同见证。

比特币网络里的节点在验证交易或区块时是遵循一定的规则，这个规则是被绝大多数矿工都接受、认可，大部分人都同意按照这样的规则来出比特币网络里的交易、维护比特币网络运行。被大多数人都认可的一套规则，在比特币系统里（也包括其他区块链）被称为共识(consesnsus)。

共识事关重大，小到情侣处对象，大到星球之间往来，若是无法达成共识，或者说有人故意对已达成的共识进行攻击，想要撕毁“合约”，曾经说过的山盟海誓都不算数——情侣分手；老板许下的江山没你的份——员工离职；说好一起玩耍的欧盟面对“叛徒”——英国脱欧、星球之间种族互相歧视——相互毁灭……后果可想而知。

一套共识被所有人都认可这是最佳理想状况，实际情况是，不会是所有人都认可，而是被大部分人认可。当超过一半以上的人不认可这套共识时或者故意想破坏这套共识时，这个系统就岌岌可危了。

反映在比特币网络中，只要某个矿工团体所拥有的算力在全比特币网络里占比超过50%，那么这个矿工团体就拥有了对比特币网络共识发起攻击、并且会成功的能力，因此也可以把共识攻击称之为51%攻击（51% Attack）。简单来说就是一个团体或人有能力做假账了。

比特币官网上对于51%攻击的定义是：
> The ability of someone controlling a majority of network hash rate to revise transaction history and prevent new transactions from confirming.  —— [比特币官网](https://bitcoin.org/en/glossary/51-percent-attack)

一个人（团体）有能力控制大部分的比特币网络哈希算力，这样他就可以修改交易历史，以及禁止新的交易被确认。**这种行为就是意图篡改区块链上的数据**。打个比方，比如现在在全球范围内有100台计算机在参与比特币网络的记账，以及维护比特币系统的正常运行。而其中有51台计算机是属于某个人的，那么只要这个人愿意，他就可以调配这51台计算机，协调运作，对比特币网络系统进行攻击——说直白点，就是可以篡改数据、做假账了。如果51台计算机或者更多计算机的账本上都没有某笔交易记录话，那么剩下的计算机会选择相信少数还是多数呢？

在《精通比特币》一书里，提到过矿工在比特币系统中扮演着[保护比特币网络、发行比特币的角色](xxx)，所以比特币系统里的这套共识也有赖于大部分矿工诚实的、并非出自一己之私利的共同维护:
> The consensus mechanism depends on having a majority of the miners acting honestly out of self-interest. ——《精通比特币》


在比特币网络里，共识通常会通过以下两种方式来攻击：
> - 双重支付 (Double-spend Attack)
> - 否认服务 (Denial-of-Service) , DoS攻击

# 02. 双重支付攻击
什么是双重支付攻击呢？双重支付攻击就是攻击者可以通过分叉的方式将之前已被确认过的区块变成无效区块，把它排挤到“备用”链上:
> A double-spend attack is where the attacker cause previously confirmed blocks to be invalidated by forking below them and re-converging on an alternate chain.  —— From 《精通比特币》

双重支付攻击可以下两种方式发生：
> - 在一笔交易被确认之前发起
> - 或者依靠自己的算力“撤销”那些区块 (就像word上的撤销动作)

关于双重支付攻击具体是如何运作的，可以看之前的文章[一笔钱花两次: 双重支付——小白学比特币之四](https://www.jianshu.com/p/59aaa2cb44d9)。

# 03. 否认服务（DoS攻击）
攻击共识的另外一种行为就是，否认服务(Denial-of-Service)，DoS:
> Sending lots of data to a node may make it so busy it cannot process normal Bitcoin transactions.  —— From [Denial-of-service attack@Bitcoin wikipedia](https://en.bitcoin.it/wiki/Weaknesses#Denial_of_Service_.28DoS.29_attacks)

给单个节点发送大量数据（小额交易），让这个节点无法瘫痪，暂时无法处理交易，或者处理交易异常缓慢。这个时候攻击者就有机可趁。有点类似于一大群人蜂拥到一个商店，堵在门口，那么其他客户就没有办法进去买东西了。

> An attacker with a majority of the mining power can simply ignore specific transactions. If they are included in a block minded b another miner, the attacker can deliberately fork and remine that block, again excluding the specific transactions. —— From 《精通比特币》

拥有大部分算力的矿工节点，能轻易“忽视”特定交易，如果这些交易放在了一个被验证过的区块里，那么攻击者就故意的分叉出一个区块，然后自己重新再挖一次，通过这个动作把之前的交易删掉。这样的行为能导致针对一个或多个地址持续的DoS攻击。

实际上，一个矿工或者矿工团体如果没有51%算力，比如只有30%的算力，也可以对比特币系统进行攻击。只是在攻击成功的概率上有所不同。拥有51%算力，如果发起攻击，则大概率会成功(almost guaranteed to succeed)。
> Security research groups have used statistical modeling to claim that various types of consensus attacks are possible with as little as 30% of the hashing power.  ——From 《精通比特币》

# 04. 小结
51%算力攻击可以让算力拥有者排除或者修改交易数据，但是这样的攻击行为也是有限的，矿工能做到的攻击是：
- 撤销在矿工控制下矿工自己发送的交易（这个可以导致双重交易）
- 阻止一些或者所有的交易获得确认
- 阻止一些或者其他所有矿工挖有效区块

攻击者不能做到的是：
- 在没有和其他矿工合作的前提下，无法撤销其他人的交易
- 无法完全地阻止交易被发送
- 无法修改每个区块能够发行的比特币数量
- 无法凭空造币
- 无法向自己发送不属于他的币

(以上翻译自[Bitcoin Wiki](https://en.bitcoin.it/wiki/Weaknesses#Attacker_has_a_lot_of_computing_power))

总结一下，比特币系统依赖于共识，如果有人出于各种原因想搞破坏，就会对比特币系统发起攻击。当他所拥有的算力超过50%时，他就具备了成功攻击的能力，这个也被称为51%攻击。一般来说，5攻分为两种，一个是双重支付攻击，一种是DOS攻击。

矿工有没有必要这么做呢？这是又涉及到成本的问题，因为拥有了51%以上算力的矿工，必然是投入了大量的金钱，这要看他发起攻击对于他有什么好处？这是另外一个话题了……

作为比特币收发者的个人，注意一笔交易要至少6个确认数才能算是安全(确认数越多，修改难度越大）。**共识靠大家，安全你我他**。

下一篇将会谈到的基本概念是硬分叉和软分叉。

***
# 参考文献
[1] Mastering Bitcoin 第二版 https://github.com/bitcoinbook/bitcoinbook


# ChangLog
- 20180317 创建及发布anattaguo.github.io
