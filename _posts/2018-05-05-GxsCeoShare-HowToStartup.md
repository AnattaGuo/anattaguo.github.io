---
layout: post
title: 创业从业必看：区块链应用和公有链的底层逻辑——公信宝CEO黄敏强分享之二
date: 2018-05-05
categories: blog
tags: [区块链]
description:
---
本文是公信宝CEO黄敏强在一块听听上分享的听课笔记，课程一个分为三个部分，第一部分是讲[《普通人如何搭上区块链这辆快车》](https://anattaguo.github.io/blog/2018/04/21/GxsCeoShare-HowToEnter/)，点击标题即可查看文章内容。

《创业从业必看：区块链应用和公有链的底层逻辑》是分享的第二部分，这一部分分为三节：
- 关键选择：到底是做公链还是做公链上的应用？
- 认知升级：从互联网思维升级到区块链思维
- 马上行动：如何跨界入行区块链，上车的最佳姿势


# 1. 关键选择：到底是做公链还是做公链上的应用？

## 1.1 什么是公链？
公链是一条独立运行，人人可以参与交易和记账的区块链。公有链有以下几个特点：
- 独立运行：有自己的区块链，自己出块、打包、运行。也就是有自己的一条跑道。    

- 人人参与记账和交易：这个是指人人都可以发送交易、进行记账。如果你成为矿工和见证人节点，就有权参与到连上所有交易活动。

- 账本公开：链上每一条交易、消息的广播都是全网广播。每一个人都可以通过区块浏览器都可以去查询某个交易ID对应的交易消息体，每个区块下面有多少交易，每个账户下面有多少数字货币资产以及账户的转账历史，这些都无法隐藏。

-  节点分散：不是所有节点都控制在开发者、团队或者某一个人手里，公链要求节点足够分散，这样不容易造成[51%攻击](https://anattaguo.github.io/blog/2018/03/17/learning-bitcoin-consensus-attack/)。如果超过半数节点控制在一个人手里，容易造成51%攻击，造成[双花](https://anattaguo.github.io/blog/2018/03/14/learning-bitcoin-double-spending/)等一系列问题。如果做公链就一定要去做开发者社区并且开发者要足够多；让更多人成为矿工或见证人，这样可以确保权利分散，节点分散其实就是权利分散。为什么说节点分散就是权利的分散呢？因为作为矿工或者见证人，他们都有打包、交易、记账、广播消息等一系列权限。作为这条链上的贡献者，他会有相应的区块奖励和交易手续费奖励，他是这个链上有权限的人。如果链上有权限的人太集中的话，那么他的权利就会太大。如果一条公链的节点足够分散，权利会分散，相应地，这个公链会更强大。

- 开源：所有开源都要在github上提交代码。下载代码必须可以运行。例如比特币，是一条典型公链，是1.0时代公链。公链是一条独立运行，人人都可以参与记账和交易的区块链。

当然除了公链之外，区块链还有联盟链和私有链。**联盟链**，只有许可之后，才可以在这个链上发起交易和参与记账、而且记账节点比较少，甚至是比较集中。而**私有链**更加封闭，作为某一个领域或某一个企业（内部）使用的链；或者是编程爱好者把开源代码拉下来，单独修改了参数、端口、缩写，把它变成一条独立运行的私有链。


## 1.2 什么是智能合约型公链
智能合约型公链除了以上提到的公链的几个特点之外，它还具有可编程可运行计算能力的公链。也就是说1.0时代的公链只能在公链上硬编码，其他用户开发者不可以在已经运行的链上添加新的代码和合约。无法在在运行的时候写一个代码让他智能运行、实时计算。

1.0 时代公链只能是硬编码，而智能合约在已经运行的链上，可以随时添加代码和计算逻辑，这个就是只能合约。

智能合约一般都有代码即法律(code is law)这样的规则，你可以发起写一个合约，合约里面约定了，在什么时候、在什么规则下，执行什么样的程序。If是什么，else是什么，它把规则写得非常清楚；或者说关于什么时候自我销毁，什么时候转账给别人，什么时候执行下一个合约的执行或者销毁都已经编在链上，写在智能合约里面。这个合约地址就可以提供给别人用，别人以这个规则去参考和运行。另外，这个合约的代码也是开源的，大家相信这个合约、它是公开透明并且合理合规，所以大家会按照这个合约去做交易转账和执行。

比如，两个人签订一个合同，当公司估值达到多少的时候，一个人的股份就会被回收，以什么价格来回收。现在会通过线下签合同的形式去做这件事，靠人的制度来进行约束，如果这个人不承认，就只能打官司。这样的场景，可以发起一个智能合约，把它写在已经运行的公链上，估值到多少，自动转让多少个token。你已经认同这个合约，没有人可以停掉它，没有人可以阻止它，它会按照既定的规则走下去，所以这个就叫智能合约。

现在典型的智能合约就是以太坊公链，它也是公链的2.0时代。以及公信宝，公信宝也是一个智能合约型公链。公信宝为什么要自己做公链。一开始想做公民信用数据，由公民自己来管理。想做数据经济，让自己成为数据的主人，让数据产生它的价值，如果没有自己可控制的公链，没有自己可以扩展的公链，那其实想做这些东西很难实现。所以公信宝从开始开发时，就要设定自己要做一条公链，公链出来之后，再搭建公链上的应用。

## 1.3 什么是公链上的应用
基于某个公链上开发的、专注解决某类场景需求的程序，也叫dApper（去中心化应用），典型的dApp应用有以太猫。

## 1.4 如何选择
如何选择，是做公链，还是做公链上应用？公链好比你在做一个操作系统，如安卓，IOS操作系统。应用就好比操作系统里的某一个应用，例如苹果里面的淘宝。相对来说，做公链的天花板更高，门槛也高。也就是说，做公链要有主链的开发能力，推广能力，运营能力。这些都非常重要，推广的难处在于，节点至少要分散，需要推广到全球去。做公链，还需要吸引开发者，建立开发者社区，此外也需要跟其他公链去竞争。

做应用天花板相对较低，而且如果你的应用做得足够好，有可能超过公链本身的影响力。比如，安卓里面facebook这样的应用，有可能Facebook本身的想象力比安卓还高。门槛低的意思是开发者不要去搭建主链，不需要有主链的开发能力。只需要有应用的开发能力，应用所使用到的开发语言比较简单，规则明确，流程简单，所以开发门槛低。推广简单是指，你】只需要推广给你的用户即可，不需要推广给开发者，推广给全球的社区。它推广的是你的C端用户。还有一个好处，就是它的民众影响力大。比如，布洛克城影响力超过公信宝影响力。

**总结：根据自己的优劣势，去选择一个在区块链上的工作方向，不管是做公链还是做应用，都是在合作重构一个未来的信用社会。**

# 2. 做公链：如何设计有竞争力的公链

## 2.1 做公链成功的关键点
 推广足够多的节点，让网络足够健壮，让权力足够分散，让矿工足够多。这是推广。另外要建立强大的社区，社区有投资者社区、用户社区，更重要是开发者社区。吸引更多的开发者到你的链上做开发，还要提供非常好的开发环境来吸引开发者。

 为什么说要提供更好的开发环境呢？因为接下来公链会越来越多，会处于一个公链百家争鸣、百花齐放的时代。实际上我们不需要那么多公链，因为开发者资源有限。如何吸引到那么多开发者到你链上来开发，这就是公链与公链的竞争。能够有竞争力的公链才能吸引到开发者，就好比手机操作系统，一开始有很多手机操作系统，现在只剩下两个主流的，IOS和安卓。那么对于区块链来说，推广比较好的节点和社区有EOS和ETH。

## 2.2 现在的公链都是怎么设计的
现有的公链，智能合约可调用的权限和资源非常少，它只能根据链上的账户体系、支付体系还有账本。也就是我有个钱包账户，钱包里有钱我可以支付，然后钱包以及链上有一些资源，只能调用这些东西去开发一个纯数学计算的应用，因为资源太有限了，所以只能用这种数学的语言，程序逻辑去做纯数学的计算。智能合约是一个沙盒，它是一个封闭的黑箱子，它不能调用外部网络，只能调用链上的网络，是一个运行在链上的虚拟机。所以在这样有限的资源里，能够做出的内容就比较多，能够做出来的应用就比较窄。现在因为智能合约性能受限，公链开发主要在拓展性能和共识机制，让TPS更高，性能更强，让共识机制更安全等，链上有限的开发。但是这样对开发者来说，做不出什么东西来。因为以前的公链的最大应用是发个TOKEN，做个ICO，这已经是很好的应用了，养猫已经到了极限了，但还是把链给堵死了。

如果开发者开发出来的应用非常有限的话，那么区块链如何去影响我们每一个人，如何走进我们的生活？如何改变我的生活？所以需要更进一步扩展。

## 2.3 下一代公链如何升华
下一代公链需要在开发者流量上去支持，在开发者可调用的资源数据上去支持。比如说，在以太坊上开发应用，你开发完后，以太坊是不会给你带流量的，你需要单独去推广应用，这就是没有流量支持。以及在智能合约里，只能调用有限资源，不能访问外部网络，你就无法调用这个用户背后的数据，跟他有关的身份数据是没有办法调用的。所以，下一代公链应该在流量在用户数据上做出更多的支持。

为什么是流量呢？因为当你需要开发者在你链上开发的时候，开发者开发出来，他没有足够多的费用跟精力去做它的推广，如果你的公链平台自带流量，那么开发者做出的应用在低成本的时候就获得大量用户的关注及使用，他可以很轻松的让自己的应用盈利或者抽佣，这样对开发者的要求就会比较低，也许就是一个纯技术的团队，可能是一个人或者两三个人。就可以做出一个很有意思的应用，这就很好玩。

数据上支持指的是，如果每个用它的用户，这个用户数字身份背后有一系列的如兴趣爱好、学历教育、工作、支付、消费习惯都有关的标签的话，我们就会大概知道他是一个什么样的人。如果我们已经大概知道他是一个什么样的人的话，那么我们就可以开发出非常丰富、落地于民生的应用。如果要让区块链普及到大众，让大众可以举例什么是区块链，这一步就会非常重要，你一定要做出跟我们每个人生活有关的应用。

**总结：区块链，特别是公链，将会是未来社会中最重要的基础设施，下一代公链一定能够成为未来信用社会的基石。**

# 3. 做应用：“古典互联网”如何跨界开发区块链应用
## 3.1 做区块链应用成功的关键点
发现需求和痛点**   

你做的应用痛点要很痛，需求要很强。这是至关重要的一点，这是门槛。如果你做的应用大家用不用都无所谓，就没有必要去做了。因为你没有办法吸引用户。发现用户痛点和需求后，要做出让用户有很好体验、交互、UI等等这些，吸引我们用户去使用。

一定要有合理的TOKEN使用场景，应用必须要有TOKEN的使用和产出奖励及消耗，数字货币的经济模型讲究币的产出，币是怎么出来的，币是怎么奖励的，币是怎么消耗使用的。

## 3.2 和区块链结合的应用怎么设计？
*交易历史记录不可篡改*，这个特性非常重要。一个交易只要你记上去就不可篡改。那么这个特性如何设计到应用里呢？比如可以设计一个社交场景，约会，你们约会的记录、评价都会在链上了。如果对于一个人的评价是不好的评价的话，在链上是改不掉的。又比如说，一个人在链上发起了一个信用贷款，贷款一个比特币，约定一个礼拜后还一个比特币，并且要支付10%左右的一个利息。如果一个礼拜后，这个人没有还款，利息也没有付，那么贷款应用方就会在链上给他记上“逾期”或者“黑名单”，这样的记录是无法删除的。在过去中心化的世界里，一个人是可以付费删除或者走后门删除，但是在区块链世界里不可以删除。

除了这个特点之外，区块链其他特点非对称加密、共识机制、密码学、智能合约等等基础知识，如果不是做技术的人不一定要去了解这些。因为要设计应用，这是至关重要。其他一系列的基础知识是为账本做出努力。

*智能合约构建一个信任场景*。交易历史记录的账本不可篡改，账本是真是的，那么如果你的应用不是去中心化，是中心化的，那么也就是说产生这个账本交易的数据的源头都有可能造假的情况下，如何确保最终记账是真实的？所以智能合约在这里起的作用，是在智能合约里面，是去中心化的，那么应用产生的所有数据跟记录也都是真实的，最终你产生的账本也都是真实的，这就是完全去中心化的，也就是完全真实。有些场景，用区块链来做追踪溯源，比如说做食品溯源，养鸡、养鸭，这种源头就是人为控制的，源头就是中心化世界的，你把它记录到链上，你的账本就不会真实。这是个伪需求。

（P.S. 区块链在溯源上使用的难度，关键在于产品在上链之前的鉴真，如果项目方在源头上的控制和鉴定是中心化，有很大权力，那区块链后续的流转数据即使不可篡改，其追求的溯源价值可能也无法达到。如果在源头的控制上就能做到去中心化和高度客观性，区块链的对于后续环节的记录也就有了意义。）

*TOKEN合理的经济模型*， TOKEN要有产出奖励和消耗。那应用设计的时候一定要把这个经济模型设计到你的应用里去。一个人如果做好事、对链有意义、对应用有价值的事情，发放奖励给这个人。想要去体验更多的功能，比如去使用一些很重要的功能（付费），就需要消费TOKEN，例如竞猜、打赏、下注、抵押...这样就会使用TOKEN。没有TOKEN大家就会没有诚信的去做事情。有TOKEN在，大家就会很谨慎的做事情。所以TOKEN在消耗和使用的时候就一定要有合理的使用场景。比如，竞猜，分有脑竞猜和无脑竞猜，明天市场牛熊，如果明天涨是什么样的规则，跌的是什么样的规则，如果写在智能合约里面，执行就非常简单，输了就会有自动转账的记录。这个交易记录、合约事实、执行规则都会在链上有账本有记录。这就是一个典型的智能合约。


## 3.3 今后的区块链应用开发需要怎么样提升
一定要做出体验像互联网产品一样的区块链应用，就是让人们记得住、经常用，让区块链技术真正为社会产生价值，实现信用社会这样一个伟大的愿景。这样的愿景用过去的公链无法达到，因为过去的过去的公链跟我们每个人都没有关系，因为做出来的应用没法跟我们没有关系。所以一定要有跟人有关的标签，例如身份验证、数据。

**总结：未来将区块链技术变得伟大的，一定是它的应用，因为应用一旦普及就会对社会公众产生巨大影响，普及也会非常快，操作系统如此，互联网如此，区块链将来也会如此。**

最后，其实，在区块链领域里面，你还有其他事情可以做，比如说你可以做区块链媒体、区块链展会、区块链峰会、数字货币交易所、咨询、成立一个创业工坊、咖啡馆，不一定要去做公链或应用。只要跟区块链沾边的都可以做，这些都不需要区块链技能或区块链行业从业背景都可以做。

# ChangeLog
- 20180505 create