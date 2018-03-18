---
layout: post
title: 你知道矿工在挖什么吗——小白学比特币之三
date: 2018-3-06
categories: blog
tags: [比特币,区块链]
---


> **本文目录**
> - 1\. 什么是挖矿
> - 2\. 什么是矿工
> - 3\. 挖矿四步骤
> - --  3.1. 验证交易
> - --  3.2. 把交易加入区块
> -  -- 3.3. 验证区块
> -  -- 3.4. 把区块加入主链

# 1. 什么是挖矿

比特币系统中，挖矿主要有两个目的:
> 1. Mining nodes validate all transactions by reference to bitcoin's consensus rule. Therefore, mining provides security for bitcoin transactions by rejecting invalid or malformed transactions.  (From *Mastering Bitcoin*)

第一个目的是，挖矿根据比特币共识来验证所有交易。因此，挖矿通过拒绝非法或者异常的交易来为比特币交易提供**安全保障**。

> 2. Mining creates new bitcoin in each block, almost like a central bank printing new money. The amount of bitcoin created per block is limited and diminishes with time , following a fixed issuance schedule. (From *Mastering Bitcoin*)

第二个目的是，挖矿会在每个区块里**产生新的比特币**，就像中央银行印钱一样。每个区块所能产生的比特币是有限的，并且会随着时间递减。

总的来说，挖矿行为主要是为整个比特币系统提供安全保障，并且产生新的比特币。

挖矿，其实是一种比喻的说法。比特币的总量是2100万枚，是限量供应。就像其他稀有金属一样（比如黄金），总量有限，每开采一点，可使用量也会变少。

#2. 矿工
之前提到过，比特币是一个点对点的电子现金系统。这里的“点”就是节点(node)，所谓节点就是指运行了比特币软件的计算机。每个人都可以成为一个节点，只要你在计算机上安装了比特币软件，然后你的计算机就会自动在网络上传播比特币交易。有些节点会把交易加入到区块，放到区块链上，这样的节点就是**挖矿节点(**mining node)，也就是我们通常所说的矿工(miner)。当然，也可以用矿工来代指维护挖矿节点的人。

# 3. 挖矿四步骤
比特币挖矿有四个步骤：
> 1. 验证交易
> 2. 把已验证交易加入区块
> 3. 验证区块
> 4. 把已验证区块加到链上

## 3.1 验证交易
任何比特币节点接收到一笔比特币交易后第一件事就是验证这笔交易。有一个标准清单来验证一笔交易是否合法有效，这个清单里所包含的检查条目有十几条，就不一一翻译了，可以在这个网址上看到详细条目https://github.com/bitcoinbook/bitcoinbook/blob/develop/ch10.asciidoc

## 3.2 把已验证交易加入区块

被验证过的交易会放在记忆池里 (memory  pool) 或者交易池(transaction pool)里。矿工会构建一个新的空区块，并从记忆池里收集一些交易放入到这个区块中。那么这个新的区块包含什么东西呢？总的来说，每个区块里包含的信息如下：
> - coinbase交易
> - 已验证交易若干
> - 交易费用
> - 区块头（Block Header）

### 3.2.1 Coinbase交易
coinbase交易，每个区块里的第一笔交易就叫做**coinbase交易**(coinbase transaction)，这笔交易里只包含了一个输入（Input）, 叫做coinbase，**用来创建新比特币**。实际上，coinbase只是一个"空白"输入("blank" input)。

每个新区块所产生的比特币数量是每21万个区块后(大约四年）自动减半的，下面这张图就是每21万个区块后，每个区块可以产生的新比特币数量。
![比特币产量图，source： http://www.lothar.com/presentations/bitcoin-brownbag/master.html
](http://upload-images.jianshu.io/upload_images/147665-2688d2b97a2dc6c5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 3.2.2 区块头(Block Header)
区块头主要是用来识别一个区块，其实就像是一堆元数据(metadata)，相当于iPhone手机里的“关于本机“信息。区块头包含的数据如下图所示：
![区块头结构](http://upload-images.jianshu.io/upload_images/147665-ec0a37dac1ce9744.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- Version，版本， 指这个协议版本，也就是比特币软件版本。
- Previous Block Hash， 上一个区块哈希值。
- Merkle Root，默克尔树。用默克尔树这种方法将这个区块里的所有交易ID(TXIDs)进行配对后，进行哈希SHA256运算后，会产生一个特定的值。
- Timestamp, 时间戳，当前时间，相当于创建这个区块时的时间点。
- Bits，用来存储当前系统的target用的，是难度值(Target)的简化版，系统将target变成bits存放在当前区块里。当一个区块头的数据哈希SHA256运算后得出的值，要小于或者等于这个target。
![Bits转成Target, source: http://learnmeabitcoin.com/glossary/bits](https://upload-images.jianshu.io/upload_images/147665-807d57878e12790e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- Nonce, 是一个需要去“猜”的数字, 用这个数字来和区块头里的其他数据进行哈希运算（也就是猜数字）。从0开始猜，如果0不对，就1，1不对，就2，这样递增下去。直到这个数字返回一个区块哈希值小于目标难度值(target nBits)。

矿工要“猜”的数字**NONCE**。
矿工要“猜”的数字**NONCE**。
矿工要“猜”的数字**NONCE**。

用一个简单的不等式来表示就是：
> Hash Function H(Nonce+一个区块里其他数据）= Block Hash ≤ 当前Target

![猜Nonce失败；source: http://learnmeabitcoin.com/glossary/nonce](https://upload-images.jianshu.io/upload_images/147665-248e67cc812f16fd.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

Nonce和这个区块里的其他数据经过哈希运算后，得到一个值，这个值要小于等于target nBits。在这样的情况下，这位矿工在这个10分钟的竞赛中获得了胜利。同时，他需要把这个得到答案的区块传给其他节点，接下来需要其他节点对这个区块进行验证，这样，他就可以获得新的比特币以及交易费用。
![猜Nonce成功，WIN! Source: http://learnmeabitcoin.com/glossary/nonce](https://upload-images.jianshu.io/upload_images/147665-2cc809cf2c16ef84.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


根据以上的描述，一个区块包含的主要信息就如下图所示：
![比特币区块结构图 Source http://www.righto.com/2014/02/bitcoin-mining-hard-way-algorithms.html
](http://upload-images.jianshu.io/upload_images/147665-d066ec6bfe044537.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

在网页前端里显示如下，https://blockchain.info/block-height/286819
![区块信息](https://upload-images.jianshu.io/upload_images/147665-47daa47df54d4cdc.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


### 3.2.3 验证区块
既然一位矿工声称自己是第一个解出难题的人，那么其他矿工需要对他的答案进行验证。那么，跟验证交易一样，验证区块也需要符合一些列的标准，通过验证后才能成为有效区块放到网络上，这些验证标准是：
> - The block data structure is syntactically valid 区块数据结构语法有效
> - The block header hash is less than the target (enforces the Proof-of-Work) 区块头的哈希值小于目标难度值
> - The block timestamp is less than two hours in the future (allowing for errors) 区块的时间戳小于未来两小时
> - The block size is within acceptable limits 区块的大小是在限定范围内（比特币每个区块大小限制在1MB以内）
> - The first transaction  (and only the first) is a coinbase transaction （第一笔交易是coinbase交易）
> - All transactions within the block are valid using the transaction checklist discussed in "verification of Transactions" （这个区块里的所有交易都是合法有效的）

### 3.2.4 把区块加入到主链接上
当一个节点收到一个新的已被验证过的区块后，这个节点会看一下这个区块的上一个区块哈希值，看看它的“爹”是谁，然后把这个区块的“爹”找到，把这个区块接到它“爹”后面，这样一个区块就被正式的纳入到区块链主链上(main chain)了，一个有效的链才算成功的“长高”了。

# 参考文献
[1] Mastering Bitcoin 第二版 https://github.com/bitcoinbook/bitcoinbook
[2] http://learnmeabitcoin.com/glossary/nonce
[3] https://www.coindesk.com/information/how-bitcoin-mining-works/
***
# ChangeLog
- 2018-0318 发布至github
- 20180317 更新3.2.4 把区块加入到主链接上内容
- 20180316 修改标题为“小白学比特币”，增加参考文献
- 20180315 修改关于coinbase交易描述
- 20180314 修改标题
- 20180310 修改对于Bits的解释；增加关于Nonce截图；增加网页前端区块信息截图
- 20180307 首次发布
