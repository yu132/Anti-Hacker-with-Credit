# 使用信心机制反制外挂
```
    在如今，很多多人对战游戏中都出现外挂，但是却很难反制外挂。

    对于如何进行外挂的防治，当前有很多技术都能检测出外挂，但是外挂也能有更好的技术来躲过这种监管，两者的技术总是相互促进的，因此外挂不总是能够被检测出来。

    对于当今游戏开挂现象频繁的今天，是什么使得大家都选择开挂来玩游戏，而不是选择正常的玩游戏呢？这个问题大概也就是一种心态问题，大部分人都觉得开挂很爽，外挂也往往很少被封，而且不会有什么很大的惩罚，也不像卖挂一样属于违法行为。对于免费游戏，就更是如此，因为就算被发现了，重新建一个号就完了。

    那么，如果将这些外挂选手和一般玩家匹配在一起，那么势必会造成一般玩家游戏体验极差，退游的人数量激增，游戏热度下降，然后游戏完蛋。所以对于一个多人对战网游来说，反外挂肯定是很重要的工作之一，但是，正如之前所说的，反外挂技术不可能总是超过外挂技术的，所以我们不从反外挂技术来进行反外挂。

    对于每个玩家，其游戏账号的价值也是不固定的，一些老玩家或者土豪总是向账户里充钱，不局限于购买道具，或者是皮肤。由于当今道具影响平衡相当严重，受很多玩家诟病，现在游戏大多都是倾向于向只有皮肤的平衡游戏发展。但是对于外挂玩家，他们一般不向游戏充钱，因为一旦封号，一般的游戏公司都是将账号的所有功能冻结，那么游戏账号内的所有投入都会化为乌有。所以外挂玩家一般都不会充钱，即使充钱，那么拿来开挂的账号和充过钱的账号肯定是分开使用的。

    那么我们是不是可以将充过钱的玩家匹配在一起，没充钱的玩家匹配在一起呢？这当然是一种有效降低付费玩家遇到外挂几率的很有效的方法，可是对于免费玩家来说，那就是一场灾难。免费玩家人群往往比付费玩家稳定性低，遇到更多的外挂很有可能会使得免费玩家快速流失，缺失新鲜血液的游戏总是很容易凉掉。而且也有一个问题，那么就是如何衡量付费的多少？如果付1元就能够和付1w的玩家匹在一起，那么对于开挂本身的成本来说1元也微不足道，如果要阶梯式分段匹配，那么对于低付费玩家来说，游戏环境并不会比免费玩家好到哪里去，对于高消费玩家来说，匹配时长会大大增加，因为高付费的玩家非常少。很明显，仅仅通过是否充钱来判断对于一个玩家的信任程度往往很难达到一个理想的标准。

    所以我们在此引入信心机制，这种机制包括上面的内容，但是也引入了新的东西，来使得信心机制有能力来反外挂。

    玩家总是通过账户来进行游戏的，我们对于一个匿名玩家，我们总是只能将其正在游玩的账户的信心等同于对其本身的信心，因为游戏公司并不是国家机构，不可能有玩家的所有信息，而且很有可能玩家对于游戏公司来说，身份是完全隐藏的。对于身份完全明了的情况，反外挂似乎就变得简单了起来，因为一个玩家这辈子似乎只有一次开挂的机会，如果一旦被封号，那么这个身份就不再可用，那么对于开挂的代价来说就很高昂。但是身份并不总是真实的，如之前的CSGO国服，需要支付宝绑定才能够激活账号，但是淘宝上依然有很多卖这种账号的商家，其贩卖的肯定不是自己的身份。所以身份信息也并不总是可信。

    想要抵制外挂，我们如果能在对一个账号实现完美的实名制的前提下（不仅注册需要验证身份，每次登陆时也需要验证，并且验证机制非常严格，例如需要手持身份证，并且每次登录需要刷脸，一旦发现使用外挂，就封禁这个身份），大可相信使用这个账号的玩家是不会开挂的，因为这种验证频率，对于陌生人来说是不可接受的，但是对于一个普通的玩家，其使用自己的身份，在游戏公司不出卖自己的信息的前提下，换取一个能够免除外挂的游戏环境，对于并不是那么在意自己身份信息的玩家，似乎是一种很合理的解决方案，但是这也仅仅在某些地区适合。在有些国家，这种验证方法可能并不合法，那么就不是那么可行了。

    另一种提高账户信心的方式便是增大账户的价值，对于一个高价值账户来说，开挂的代价是非常大的，如果开一次挂被发现，便会损失几w，那么对于任何一个开挂的玩家来说应该都是不可接受的。增大账户的价值之一的方法是给这个账户付费，例如购买游戏内物品。对于一个游戏时长很高的账号（活跃时长，需要有效的排除挂机行为），也可以认为其价值很高。当然也还有其他的方式（免费），例如使用家用主机提供算力（可以用于反外挂（提高服务器算力），或是挖矿），从而提高账户加载。或是通过某种担保，保证不会开挂，否则一定数额的资金将会被冻结，当不玩这个游戏时，可以随意提出。以上方式都可以增大账户的价值，从而提高信心。

    还有一种方式是集体信心，对于既不愿意提供自己身份，也不愿意提供资金的玩家，也并不总是希望开挂的玩家，但是仅使用以上两种判断方法很容易就认为他们可能开挂。为这种玩家，提出集体信心的方式，即一群玩家将他们账号的总价值作为担保，以提升对于他们的总信心的一种方法，由于信心是共享的，证明他们对于彼此是十分信任的，相互相信其余的人不会开挂，这种方式，一般是通过邀请的模式运行的，一个人只会通过邀请最相信的人进入。为什么必须要十分相信的人才能进入呢？集体信心是一种集体担保模式，一人开挂，全员连坐。当然，也为这种集体信心提供逃逸模式，当某个账号的信心程度高于某个值的时候，可以选择从集体中脱离，以免除连坐的惩罚。

    通过了解账户的信心程度，我们便可以知道一个账号开挂的可能性，但是这并不代表所有低信心的账户都是开挂者，由于技术相互增强的情况总是存在，于是反外挂技术不总是能够检查到外挂的存在，因此纯粹基于反外挂技术是不靠谱的，这也是这篇文章出现的原因。那么我们要如何利用信心机制来使开挂者的游戏体验变差的呢？

    在此之前，我们还有一个必需品，那就是举报系统，对于开挂不明显影响其余玩家游戏性的游戏，那么信心机制可能就并不靠谱了，但是对于影响严重的游戏，就会工作的很好。为什么呢？因为对于这些影响游戏体验的开挂玩家，普通玩家通常是深恶痛绝的，对于很多举报并没有奖励的游戏，例如绝地求生大逃杀，或是CSGO，都有很多玩家会去查看DEMO，或是被打死后查看击杀者的视角，来观察对方是否开挂。

    信心机制的另一个核心就是举报系统，这个系统提供了一种什么功能呢？当然就是一个账号是否开挂的可能性，对于一个账号，这局游戏里面所有查看他视角的玩家都觉得他是挂，那么这个账号十有八九就是挂；但是对于一个天天游戏20局，但是没有一个人觉得他是挂的账号，开挂的可能性就很低。

    当然可能有人会有疑问？仅仅靠举报系统不久够了吗，举报多的就封了不就行了？答案肯定是不行的啊，举报同样也只是说明一个账号的开挂的可能性，一个高玩，很有可能被玩的菜的玩家举报，但是这并不能证明这个高玩就开挂了。

    我们从举报系统中提取出我们所需要的那个部分，即信心下降机制。信心下降机制除了玩家的举报，还可以有不是100%准确的数据检测，或是其他的检查用户行为是否可疑的程序。信心机制和信心下降机制两者相互博弈，最终决定一个玩家是否需要付出代价。

    对于一个玩的普通的玩家，这两种机制对于他们来说并没有什么影响，因为缺少信心下降的驱动，使得其信心总是维持在一定的水平，我们总是认为其是可信的。对于一个高玩，其很容易受到信心下降的惩罚，因为技术高也很有可能被举报，对于这种玩家，我们就需要考虑其信心，如果其有足够的信心证明其可信，那么我们就选择相信这个玩家，如果不够，那么我们就给与这个玩家适当的处罚。对于开挂的玩家，其信心无论高低，总是会受到足够的信心下降惩罚，使得其最终会被惩罚到。

    由于我们对于玩家的惩罚是不基于完全正确的判断的，有可能会出现错误，那么给与这个账户封禁的惩罚是不合理的。但是又不得不让这些玩家减少和正常玩家匹配到一起的概率，我有两种解决方式，一种是暴力匹配，将这些玩家按照其负信心度进行匹配，使得外挂玩家更有可能和外挂玩家匹配到一起。一种是延长匹配时间（timecash 时间现金，从 hashcash 中得到灵感，都是需要付出时间的代价），可能普通玩家1分钟就能完成匹配，然后游戏20分钟，但是这些不被信任的玩家往往需要长达10分钟的匹配，这极大程度上减少外挂玩家的匹配次数，降低外挂玩家的游戏体验。当然这两种方式也可以结合使用。

    当然信心下降不是持久的，是会有老化机制的，一个玩家打出神经操作的时候往往被认为是挂，但是这种操作并不总是能够被打出来，而且往往出现十分偶然，可能我们对于爆发式的信心下降需要给这个玩家处罚，但是随着其游玩时间的增加，这种处罚会慢慢的降低。

    信心机制的主要作用就是如上所描述的一样，一种基于开挂概率来对玩家进行“处罚”的一种防治措施，并不能完全阻止外挂的出现，但是其也可以给反外挂技术提供帮助，对于信心下降严重的玩家，我们总是需要严格检查其游戏的数据，更好的集中的排查有嫌疑的玩家，也是其功能之一。
    
    ```
