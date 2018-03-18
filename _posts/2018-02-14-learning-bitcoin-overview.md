---
layout: post
title: 比特币概览——小白学比特币之一
date: 2018-3-06
categories: blog
tags: [比特币,区块链]
---

 [*Mastering Bitcoin*](https://github.com/bitcoinbook/bitcoinbook/releases/tag/Edition1Print1) 第一版是2016年3月份出版； [*Mastering Bitcoin*](https://github.com/bitcoinbook/bitcoinbook) 第二版是2017年7月出版。本系列精读笔记将基于第二版，笔记的内容是根据自己理解来排序，不是严格按照原书目录来排序。

> 本文目录
> 01. 本书作者
> 02. 比特币简史
> 03. 简单来说比特币是什么？
> 04. 获得你的第一个比特币
> 05. 存储比特币

# 01. 本书作者Andreas M. Antonopoulos
*Mastering Bitcoin* 的作者是Andreas M. Antonopoulos（1972~），希腊裔英国人。Andreas毕业于伦敦大学学院，他所学的专业是计算机科学和数据通信及分布式系统。简单来说，Andreas的经历如下：

- 从20世纪90年代开始，Andreas开始给开源及开放式网络商业做咨询相关工作，曾在咨询公司Nemertes Research任职七年之久（2003~2011）。
- 2012年，Andreas迷恋上比特币，开始在各个会议上介绍比特币，并担任与比特币相关的创业公司的顾问，同时也发表比特币相关的文章。
- 2014年，Andreas担任[比特币基金](https://bitcoinfoundation.org/)反贫困委员会主管。
- 2014年1月~2014年9月，出任 [Blockchain.info](https://blockchain.info/) 首席安全官。
- 2016年3月出版 [*Mastering Bitcoin*(第一版)](https://github.com/bitcoinbook/bitcoinbook/releases/tag/Edition1Print1) 一书。

除了*Mastering Bitcoin* 一书外，关于Andreas的资源还有：
- [Andreas M. Antonopoulos个人网站](https://antonopoulos.com/)
- Andreas主持的podcast节目 [*Let's Talk Bitcoin*
](https://letstalkbitcoin.com/blog/category/episodes) (现在已经出到335集了)
- [Andeas 的 YouTube 视频](https://youtube.com/aantonop) (有300多条视频)
- [*The Internet of Money* 系列书](https://www.amazon.com/gp/bookseries/B075VG4NTN)
- [*Mastering Ethereum*](https://www.amazon.com/Mastering-Ethereum-Building-Smart-Contracts/dp/1491971940)，将会于2018年第四季度出版。

*Mastering Bitcoin* 作者Andreas 是比特币及区块链的布道者，他留下的资源真的可以用**HUGE**来形容，重点还都是公开免费的。

#02. 比特币诞生简史
- 2008年，一个叫做中本聪的人写了一篇文章，名为《比特币：一个点对点电子现金系统》，这篇文章标志着比特币的诞生。中本聪发明比特币结合了好几项当时先进的创新发明，其中最为关键的创新是使用一个分布式的的计算机系统（被称为"Proof-of-Work"算法，一般翻译为工作量算法，我觉得翻译为劳动证明算法是不是更利于理解？），这种算法每十分钟就带领一次全球性的“竞选”，允许去中心化的网络对于一笔交易达成共识。
- 2009年，基于中本聪发布的文章，还有其他程序员对中本聪论文的更新。POW(mining)的实现为比特币提供了安全可靠的不断增长的算力保障。
- 2011年，中本聪从公众视野消失。
后面比特币价格的大起大跌，新闻媒体都有报道，这里就不一一赘述了。

# 03. 比特币是什么？
- Bitcoin is a collection of concepts and technologies that form the basis of a digital money ecosystem (比特币它集合了一系列概念和科技，并在此基础上形成的一个数字现金经济系统。)
- Bitcoin is a distributed, peer-to-peer system(比特币是一个分布式的，点对点的系统。)

那么比特币由谁来生产发行呢？
> Bitcoin are created through a process called "mining", which involves competing to find solutions to a mathematical problem while processing bitcoin transactions. (在进行比特币交易记账的时候，比特币通过一个被称作为“挖矿”的过程被创造出来，这个**挖矿**的过程涉及了竞争解决数学题目。)

那么也就是说挖矿过程里面包含了两个要点：一个就是处理比特币**交易**，一个就是**竞争去解数学题目**。

简单来说，**比特币主要由以下四个方面组成**：
- A decentralized peer-to-peer network (the bitcoin protocol) 一个去中心化的点对点网络(比特币协议)  
- A public transaction ledger (the blockchain) 一个公开的交易账本(区块链）
- A set of rules for independent transaction validation and currency issuance (consensus rules) 独立转账验证和货币发行的一系列规则，也就是共识。
- A mechanism for reaching global decentralized consensus on the valid blockchain (Proof-of-Work algorithm) 在有效的区块链上达到全球去中心共识的一套机制。

说到中心化和分布式，那么一定有相对的中心化。那么到底什么是中心化，什么去中心化和分布式网络呢？我在google上找了一张图，可以让自己对于这几个概念有更清晰的理解。至于去中心化和分布式的优点会在以后的读书笔记中做进一步的解释。

![types of network](http://upload-images.jianshu.io/upload_images/147665-ce03fb8af0f408c7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


#04. 获得你的第一个比特币
如何购买比特币呢，一般来说有几下几种方式
- 私人购买：找你的朋友直接购买，如果你朋友中有人持有比特币，你可以找他直接购买，这是最不复杂的一种方式。
- 如果你没有朋友或者认识的人持有比特币，那么你也可以通过线上找私人购买（恩，就是类似于广告墙一类的网站，现在全球最大的比特币场外交易网站是[localbitcoins.com](https://localbitcoins.com/)，上面可以找到全世界各个地方的买家和卖家。能够使用软妹币直接购买比特币的网站是[OTCBTC.com](https://otcbtc.com/referrals/MENGJUNKWO)。
- 出售自己的服务或者产品来获得比特币，例如说如果你觉得自己的文章写得不错，可以要求读者用比特币给你打赏。
- 用比特币ATM机。如果你出境旅行，除了购买奢侈品外，还可以考虑购买一些比特币。可以通过这个网站
 [Coin ATM Radar](https://coinatmradar.com/) 来查询ATM都分布在世界的哪些地方。（注明：截止2018年2月14日，全世界一共有2237台比特币ATM机，分布在63个国家。网站上显示上海就有一台，有机会我要实地考察一下这台ATM。具体地址在上海市，徐汇区，零陵路899号, 6层，608）
- 使用交易所购买。

很多刚开始听说比特币的人以为比特币要一个起买，就惊叹说“太贵了，买不起”。其实这是一个误区，换言之，**你不必一次性购买一个比特币，而是0.1，0.01个或是0.001个。**最小购买单位，是小数点后八位数。 这里推荐对比特币有兴趣，想要尝试购买并且是第一次购买的人，先购买价值500或者1000元人民币的比特币，把整个流程走通。

关于各个交易所及场外的注册买卖过程网上有许多教程，有兴趣的可以自己上网搜。

# 05. 存储比特币
通常我们会选择一个牛皮或者其他材质的钱包来存放手头上的人民币。比特币跟纸币一样也需要一个钱包来存放。一般来说存放比特币的钱包包括以下几种：

- 桌面钱包
- 手机钱包
- 网页钱包
- 硬件钱包
- 纸钱包
- 全节点钱包
- 轻量级钱包
- 第三方API客户端

书中用了Alice的手机钱包作为例子，显示给大家看比特币钱包长什么样。这里我截图了blockchain.info做的手机钱包展示看比特币钱包长什么样。

这张截图是我将手里比特币转给别人的界面：
> - **自** (From)是指我们要从哪个地址转出（好比支付宝付款时你要选择是从银行卡付款还是花呗付款）
> - **至** (To), 是指我们转账对象的**比特币地址**（好比支付宝付款时，你要填写他人的支付宝账号）。或者可以通过截图右上方的扫描对方地址二维码的形式输入转账账号。
> - **BTC**/**CNY**, 输入你的转账数量，系统自动换算这笔转账值多少钱软妹币。
> - **手续费**, 每一笔转账都需要付手续费，手续费的高低代表转账速度的快慢。
![给别人转比特币界面](http://upload-images.jianshu.io/upload_images/147665-e7c10232ab98aeb4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


这张截图是我发起收款的界面：
> - 图中二维码下方那**一串数字**就是自己的比特币地址
> - **二维码**就是比特币地址生成的二维码，他人可通过扫描这张二维码给你付款。
> 在BTC后面输入别人需要付给你的比特币的数量，右边的“CNY”就会自动换算出比特币的现价人民币是多少。
![比特币请求他人付款界面](http://upload-images.jianshu.io/upload_images/147665-5b8f001b65e73ec4.jpeg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

我们可以把比特币钱包地址理解为个人邮箱地址（或者支付宝账号），每个人可以拥有多个邮箱地址，例如韩梅梅可以有hanmeimeiwork@gmail.com, hanmeimeifamily@gmail.com, hanmeimeiwriter@gmail.com ... 跟邮箱地址一样，每个人也可以通过钱包生成多个比特币钱包地址，例如我通过blockchain.info客户端生成了多个钱包地址：

![每个人可以生成多个比特币钱包(地址)](http://upload-images.jianshu.io/upload_images/147665-8b4e14aa9cf4e3ae.jpeg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


**重要！**在扫描二维码或者粘贴复制地址时，一定要检查地址是否正确，以防被他人钓鱼更换。
**重要！**钱包密码、每个钱包地址的私钥(private key)是特别、特别、特别、特别、特别重要的。千万不要通过手机记事本，邮箱、网盘等形式保存记录这些密码——这就相当于把你家保险柜钥匙给了小偷。关于如何备份密码，有搜索能力的人可以自行上网搜索。
***

# ChangLog
- 20180318 发布至github
- -20180306 首发于简书
