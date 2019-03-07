# 使用信心博弈机制反制外挂

&emsp;&emsp;如今很多多人对战游戏中都出现各种各样的外挂，虽然游戏公司总是在更新自己的反作弊措施，但是却依然不理想。其原因是受到高利润的影响，制作外挂这个行业，总是能够吸收到一些高技术的人才，所以想通过纯粹的反外挂技术目前是做不到的。

&emsp;&emsp;要通过纯粹的技术手段实现反外挂不可行，那么我们能不能使用一些更加高效的方法来抑制外挂使用者的数量呢？

&emsp;&emsp;要探讨上面这个问题，首先我们需要探讨为何有人使用外挂。使用外挂，是一种违背规则的行为，通过这种行为，使用外挂者往往能够得到一般人通过游戏无法得到的信息和技术，从而使自己获得胜利。并且这种行为，不会违法法律，最大的惩罚，也只不过是把使用外挂的玩家的账号给封禁，如果这个玩家并没有向这个账号中投入金钱，几乎可以说是没有任何惩罚。

&emsp;&emsp;这个现状加剧了使用外挂的行为，没有任何惩罚的现状加剧了使用外挂玩家的嚣张气焰。有人可能说这只是就免费游戏的情况而言，对于买断制游戏，如果使用外挂被封号，那么他们就必须重新购买游戏，所以不会有很多人开挂。可这并不能阻止外挂使用者的数量，拿绝地求生大逃杀作为例子，其需要98元购买游戏，但是开挂的人少了吗，并不少，甚至形成了一个产业链。销售外挂的人往往可能还提供低价的黑号（被盗的号）给购买外挂的玩家，这使得购买游戏的门槛大大降低，最终也不能阻止大量使用外挂的玩家涌入，最终破坏一般玩家的游戏体验。

&emsp;&emsp;最终，我们可以把使用外挂的原因归结于两点：第一是外挂技术在不断的提升，仅凭反外挂技术是不能够检查出全部的使用外挂的情况的，所以总是能够使用外挂；第二是使用外挂的成本低廉，几乎不会受到任何惩罚，所以总是有人敢于使用外挂。

&emsp;&emsp;现在我们可以回答上面的那个问题了，我们既然不能解决第一个产生外挂的原因，那么我们只能从第二点开始入手：提升开挂的代价。有人可能会说：提升开挂的代价？那很明显不现实，如果一个游戏卖998元，那么势必会把很多的玩家拒之门外，因为有很多玩家都是因为这个游戏的价格比较低或者免费而来玩的。但其实提升开挂的代价可远远不止提升购买游戏的价格这一种手段，接下来我将描述如何使用信心博弈机制来对抗外挂。

&emsp;&emsp;信心博弈机制的核心便是信心。信心是什么呢？对于每个玩家来说，我们对其都有一定的信心，相信其不会使用外挂。

&emsp;&emsp;对于一个刚刚创建的账号，我们对其的信心是非常有限的，因为我们对其几乎一无所知。但是我们总是可以知道一些最基本的知识，即其创建账号和游玩的常用IP，对于不同的地区，我们都可以给与这个地区内的玩家某个初始信心值，这个信心值可以从先验的数据中分析出来，我们能够吸收其他游戏的使用外挂的地区分布，从而得到这个先验知识；或者我们也可以从这个游戏现有开挂数据中分析出使用外挂的分布得到这个值，并且随着游戏的持续运营，对其进行更新；当然我们也可以结合以上两者，进行联合分析，也是完全没问题的。

    初始信心=信心值-f（地区开挂占比）或 初始信心=信心值*f（地区开挂占比）（f的值域为(0，1]）

&emsp;&emsp;为什么要让每个地区的初始信心不同呢？这主要是一种先验知识，据我所知，中国玩家的玩家数量在很多当前很热的游戏中都是很多的，可能是因为玩家基数很大，或者是因为中国玩家就是有很多玩家喜欢使用外挂，又或是中国的游戏环境造就了这一点。不过原因不是重点，重点是中国使用外挂的玩家在总的玩家中占比非常大。那么我们不得不降低对于中国地区的玩家是否会使用外挂的信心。当然这里并不是进行任何的地域歧视，仅仅是一个事实，如果东南亚或是美国欧洲的玩家使用外挂的比例也很高，那我们也需要降低这种初始的信心。

&emsp;&emsp;有了初始的信心，这只是第一步，其次，我们就需要引入信心上升这个关键的步骤。信心上升，指的是我们对于这个账号的信心提升，这主要是玩家通过某种方式，让我们觉得他开挂的可能性很低。

&emsp;&emsp;那么什么情况下我们认为一个账号是可信的？我接下来会一一列举我的想法，当然可能会有缺漏，希望读者也能有自己的观点或者是创新。

&emsp;&emsp;就拿现在非常火的APEX作为例子，如果我看到一个玩家持有传家宝皮肤（可能评价需要向游戏内充入2000元才能抽到），那么我大可能相信这个玩家不会开挂，为什么呢？是因为一旦他使用外挂被封号，他充入这个账号的所有钱都打水漂了。所以第一个提升信心的便是提升账号价值，这个也是最直接的一种。

&emsp;&emsp;其次就是身份绑定。当然这并不是说一个账号随便绑定一个身份就可信了，这里需要按照身份绑定的严格程度来逐步提高这种信心。如果是简单的绑定一张身份证，那么互联网上似乎到处都能够找到这种信息来绑定。略微严格一点，需要手持身份证的照片来验证本人是否是这个身份信息的主人，那似乎也可以找到代激活来钻空子。我认为只有每次登录的时候都需要验证本人是否是这个账号的主人，例如说每次登录需要刷脸来进行验证，再通过机器学习的方法验证是否是本人在同一个地点进行的登录，一个人最多也就把周围非常熟的身份信息拿来使用，对于陌生人来说，如此频繁的代刷脸，从理论上来说应该是不可行的。只要能够确定一个账号是本人（至少是本人的家属或是非常熟的人）在使用，那么一个人能进行开挂的次数是非常有限的，一旦绑定本人身份信息的账号被封禁，他就很难再次激活一个有身份绑定的账号。在不可能获取大量身份信息的前提下，我们大可相信绑定身份信息的账号使用者不会使用外挂，即使使用了外挂，那么他就很难在此通过这种方式提高我们对其的信心了，保证不会被滥用。因此第二种提升信心的方式便是身份绑定。

&emsp;&emsp;对于身份绑定而已，不同的人能够获取的信心值也是不同的，例如职业玩家就几乎不可能使用自己的身份信息的账号来开挂，因为一旦被检查出使用过外挂，他的职业生涯可以说是结束了，对于一些主播来说也是同理，对于这些名人的身份绑定的账号，提升的信心值肯定是可以比普通的身份信息高的。

&emsp;&emsp;但是身份绑定也并不总是可行，其可能会违反某些国家的法律，那么在这些地区，这种方法是不可以使用的，否则会为游戏公司带来相当大的麻烦。但是在一些并不违法的地区来说，这种方法就能够很有效的确认账号的可信度，而且对那些不是对个人信息太过在意的用户来说，这也是一种很方便而且免费的证明方式。

&emsp;&emsp;对于既不想充值，也不想泄露自身身份信息的玩家来说，就很难提高我们对其不会使用外挂的信心。但是，如果玩家能够为账号提供某种意义上的担保，我们也可以提高对这个账号的信心。例如玩家可以将电脑的闲置时间交付给游戏公司来使用，游戏公司能够使用这个计算资源来提高游戏的质量，也可以用于外挂检查的计算，还可以用来挖数字货币，或者是以计算云的方式租借出去，最终形成的盈利，以游戏内充值的方式返还给玩家，以此提高账号的价值；或者可以有某种向某种担保机构担保这个账号不会有使用外挂的行为，否则将某笔资金赔偿给游戏公司。这种担保形式可以以外部公司的形式，或者以公司内部的形式，在法律允许的前提下来实行，就都是可以的。当然给账户内放入高价值道具（道具可交易的前提下）也是一种意义上的担保行为，即使没有直接向游戏公司进行充值行为，也还是提高了账号的价值，也是一种提高信心的方式。

&emsp;&emsp;如果一个玩家什么都不想做，也不想充钱，那么他们只能尽可能的提升有效游戏时间来提高这种信心。有效游戏时间指的是玩家活跃的游戏时间，挂机或是通过脚本模拟游戏行为所产生的游戏时间是不被计算在内的。但是这种信心说实话十分脆弱，需要大量的时间积累才能够形成。例如说1000小时以上，才可能接近一个普通身份绑定的水平，想达到这个时间水平其实是非常困难的。因此还有一种集体信心的方式给这类玩家使用，集体信心便是一群人共同担保这些人不会使用外挂，一但有一名成员使用外挂被发现，那么全员都会收到惩罚，因为连坐的机制，使得一个人只有可能和完全能够相信的人，例如亲人或是很熟的朋友，来形成一个集体。集体信心可以使得使用外挂的代价变高，并且能有效的汇集信心，从而来提升我们对于这个集体内所有玩家的信心。因此在使用集体信心的情况下，在集体内的玩家达到一定数量之后，集体内的玩家即使是只积累有效游戏时间，就能够很快的提升个人和集体的信心。如果集体内部玩家怀疑集体内部存在使用外挂的行为，可以举报这种行为，以免除连坐的惩罚，同时玩家的信心值高于某个值的时候，也可以选择退出集体，一旦退出，就不能再加入任何集体，以防止高信心玩家来拉高某些集体的信心，玩完之后再退出这种规避惩罚的行为出现。

&emsp;&emsp;以上便是信心提升机制的内容，可以总结为以下几条公式：

    玩家总信心 = max( m(玩家充值金额+账号价值+账号为游戏公司提供计算的时间所带来的价值+账号的担保价值) + t(玩家游戏时间) + id(账号身份绑定程度) , c(账号绑定集体的总信心值，集体玩家数量) )  （随某个时间间隔更新）

    m(x) = 信心贡献随金额总量的增长公式
    t(x) = 信心贡献随时间的增长公式
    id(x) = 信心贡献随身份绑定程度的增长公式
    c(x) = 集体信心 / a(集体玩家数量)
    a(x) = 随x上升而上升的值，但值域应为[1,x)

    if( 玩家总信心>c(x) ) 玩家可以退出集体

&emsp;&emsp;有了信心提升机制，那么也要有对应的信心下降机制，因为对于任何一个信心很高的账号，我们依然不排除使用该账号的玩家有使用外挂的可能。对于信心的下降，也有两种我认为的评价的方式。

&emsp;&emsp;首先便是非常常用的举报机制，可以说任何一个有意愿反外挂的游戏公司都会给游戏加入这个功能。但是有效程度也飘忽不定。但对于再好的举报系统一般来说，举报作弊玩家最快也要1天以上才有可能被封号，响应时间很长。而且，往往还有很多误举报，例如游戏技术比较弱的玩家被技术比较强的打败，弱的玩家因此就举报厉害的玩家。这些都是使得常规的举报系统不那么好用的原因。但是一个玩家被举报了，那么我们当然可以降低他的信心值，因为我们认为他有可能开挂了，这一点，是可以肯定的。

&emsp;&emsp;其次是数据异常检测系统或是任何能够检测异常行为的系统。这些系统都能够检测玩家的异常数据或是行为，但是不能够100%的确认玩家是否使用外挂。如果这个系统能够100%检查使用外挂的行为，那么就没有必要用在信心博弈机制上了，直接封了那个账号就可以了，就变成了常规的反外挂机制。不过，出现任何异常我们也都可以认为玩家有可能使用外挂，降低信心值合情合理。

&emsp;&emsp;那为什么需要这些仅仅是有可能检测出使用外挂的系统呢？那是因为100%检查出外挂的系统运行速度很慢，因为需要严格的比对任何有可能出现外挂的数据，这也是常规的反外挂机制运行很慢的原因之一。然而，如果我们利用这些并不是100%完美的系统或者机制，我们可以评价一个账号存在有使用外挂的嫌疑，从而降低其信心评分，并且响应时间会很快。

&emsp;&emsp;另外，信心下降机制计算的值是玩家当前信心，其存在老化机制来避免长期游玩所带来的信心持续下降的问题，老化的参数是不固定的，随着异常出现的分布来进行计算，对于同等举报总量的前提下，使得短期出现大量的举报的情况（使用外挂的几率大，理应老化速度慢）和长时间少量举报的情况（使用外挂几率小，理应老化速度快）的老化速度不一样。

&emsp;&emsp;当然，信心下降机制如果只作用于被信心下降的玩家，是不可行的。因为这样这个系统非常可能会被滥用，例如有些玩家可能每局都把所有对手举报一次，这会给整个系统带来及其大的干扰。为了反制这种行为，我们可以引入两种机制，一种是反作用机制：如果发现不正常的举报行为，对于玩家来说，会反作用于自己的信心上，适当的下降其自身的信心值，对于数据检测系统，那么则是一种需要调整的信号，因为这证明了这个系统产生了不正常的结果。另外一种机制是：我们可以对每个账户或是系统的信心下降操作进行加权处理，对于每次高水平的举报或检测（例如最后这个玩家被发现确实使用了外挂，或者是收到大量的举报），我们就适当加大其权重，而对于错误的举报或检测（只有很少的举报），我们则适当降低他的权重，最终使得正常使用信心下降机制的玩家或是系统有正常或者稍高的权重，而对于滥用或是有异常的数据检测系统，其结果权重是很低的，产生不了什么影响。

&emsp;&emsp;以上便是信心下降机制的内容，公式（不包含防滥用机制，因为加上会比较复杂）如下：

    玩家当前信心 = 玩家总信心 （初始化）

    玩家当前信心 = 玩家本周期信心 = 上周期计算的玩家当前信心 * a(上周期信心，总信心，异常评价值) - r(本周期举报次数) - e(本周期出现数据异常或行为异常的次数) （初始化后按周期计算）

    a(上次信心，总信心，异常评价值) = 上次信心惩罚的老化计算公式，最小为上次信心值，最大为总信心值，随着异常评价值来改变老化的速率

    r(本周期举报次数) = 信心下降值随本周期举报次数上升的公式
    e(本周期出现数据异常或行为异常的次数) = 信心下降值随本周期出现数据异常或行为异常的次数上升的公式

&emsp;&emsp;我们通过以上两种机制，一种信心上升机制计算玩家总信心值，一种信心下降计算玩家当前信心值，最终我们可以得到一个账号当前没有使用外挂的可信度。从而我们可以进入信心博弈机制的核心功能：负信心代偿机制。

&emsp;&emsp;对于一个信心为负的账号，我们不得不怀疑其有重大的使用外挂的嫌疑，并且信心值越小，使用外挂的嫌疑越大。因此我们必须让这些账号的玩家付出某种代价，作为“惩罚”；对于普通的正信心账号，这个机制没有任何影响，因此对于普通的玩家，其受到误举报而进入负信心的状态的可能性非常低，所以往往只有厉害的玩家才需要提升自己的总信心值以防误举报的影响。这也是为什么这个机制叫做信心博弈机制，一个玩家总是希望自己不被认为使用了外挂，但是有些机制总是认为这些玩家有可能使用了外挂，两者相互博弈，总是想向别人证明自己是对的，那么双方都需要给出足够的证据，证明自己的正确性，如果玩家的证明多，那我们大可相信玩家，如果信心下降机制给出的证据多，那我们就不得不怀疑这个玩家是否有使用外挂的嫌疑了。

&emsp;&emsp;那么对于这些负信心的玩家，他们需要付出什么代价呢。首先由于他们并不是一定使用了外挂，可能只是技术比较厉害，所以我们不能直接给与过于严厉的惩罚，比如封号。但我们总需要减少这类玩家的游戏时间，对于不同的游戏，我们可以使用不同的惩罚机制：例如对于需要匹配的游戏，我们可以对这类玩家进行延长匹配时间的惩罚，或是我们可以将这些玩家按负信心度进行匹配，将有使用外挂嫌疑的玩家匹配到一起。对于其余类型的游戏，我们大可降低这些玩家的游戏体验，例如增大延迟，或是降低响应时间来进行“软惩罚”。对于负信心值过高的账号，我们可以暂时对账号进行短时间的冻结，但是时间不宜过长。对于有排位机制的游戏，这种负信心也往往也以表示为一种叫做炸鱼的行为，即一名比较厉害的玩家通过某种不合适的行为（例如故意输掉比赛或是玩小号），到达比比玩家正常水平低很多的段位，这种行为也是有必要进行惩罚的，负信心代偿完全可以兼容这种情况。最后总结为公式如下：

    玩家游戏时间或体验 = 正常游戏时间或体验                                    (信心值>=0)
    玩家游戏时间或体验 = 正常游戏时间或体验 - f(0-玩家的负信心值)  (信心值<0)

    f(0-玩家的负信心值) = 惩罚随信心值的降低而增长的公式

    if( 玩家游戏时间或体验 < 0 )   冻结账号

&emsp;&emsp;对比常规的机制来说，信心博弈采用一种比较柔性的惩罚措施，对比起直接使用封号的措施，往往能够得到更加快速的响应，因为对于一次错误的封号，所带来的舆论风波往往大于少封一个使用外挂的玩家，所以在这种硬性的惩罚措施实施之前，都必须进行极其严格的审查，因此时效性很差。但是如果使用程度较低的惩罚机制，则可以快速的对于每次信心下降的情况做出响应，可以低延迟的对有嫌疑的玩家进行“处罚”，这才是这个机制的优越之处。对于使用外挂嫌疑越大的玩家，我们通过降低其游戏体验和游戏时间，最终使得其和正常玩家一起游玩的游戏时间下降，并通过降低其游戏体验来制衡其使用外挂的效果，最终将正常玩家的游戏体验提高到一个合理的水平，而且反馈能非常及时。即使刚性的处罚的速度能够提升到和柔性处罚相似的速度，柔性的处罚也有其自身的优势，因为一个玩家如果因为使用外挂被封号，那么他大可用5分钟创建一个新的账号，继续游玩。但是对于柔性的处罚来说，他可能需要5分钟来匹配下一局游戏，然而他并不知道是由于他已经被检测到有很大可能使用外挂了，往往还认为是正常的匹配时间延长了，或是网络出现了波动。我们总是能够“悄悄的”使使用外挂的玩家体验变差，或者直白一点，就是恶心他们。而这种处罚措施在他们看来往往并不直接挂钩于自己的作弊行为，他们便会依然使用这个账号进行游玩，那么处罚措施便能够长时间的作用于这些玩家，所以其比一般的反外挂机制变得更加有效。

&emsp;&emsp;但是这并不是说这个系统就能完全的取代传统的外挂检测系统，我们依然需要对100%确认有使用外挂的机制来进行最严厉的处罚，即封号。不然仅凭借信心博弈机制，是无法对开挂者做出真正的惩罚的，只能进行“软惩罚”，玩家即使账号价值再高，也能肆无忌惮的使用外挂，因为无论如何都不会被封号，那么提升信心就会变得非常廉价，使得信心上升机制完全作废。因此提高传统的反外挂技术依然很有必要。信心博弈和传统的外挂检测系统并不是相互排斥的，反而是互利共赢的。因为信心博弈依赖传统的外挂检测来打击真正的使用外挂的行为，而传统的外挂检测系统则可以利用账号的信心估量其需要对其进行检查的严格程度，使得对于使用外挂可能性高（即信心值低）的账号，我们可以以一种非常严格的机制（耗时长但是非常有效且精准的机制）去检查，这样能够非常迅速的打击篡改数据这类暴力修改游戏程序内容（包括游戏内容本身和游戏内存数据）的外挂。

&emsp;&emsp;不过，即使信心博弈机制是一种很有效的防治外挂的机制，也很容易受到舆论导向的攻击，因为对于玩家来说，“明目张胆”的降低他们的游戏时间和游戏体验，是一种不可被接受的行为。即使这个玩家有有90%的可能性是使用过外挂的，在舆论上也很容易被人利用来攻击游戏公司。所以，我们也无需将这种机制告诉所有的玩家，我们完全可以将这种机制隐藏在普通的反外挂机制后。玩家完全不知道其匹配时间增长或是游戏体验下降是出于什么原因。会将其归咎于游戏公司的玩家肯定不多，这样才能够安全的上线这个系统。而且隐藏这个系统的存在，才能够有效的长时间处罚有作弊行为嫌疑的玩家，使信心博弈机制能够发挥其最大的作用。

&emsp;&emsp;最后进行一下总结，使用信心博弈机制来反制外挂是一种可行的方法，最简单的概括一下就是通过概率来估算一个玩家使用外挂的可能性，最终决定其游玩质量的高低，使得使用外挂嫌疑高的玩家的游玩时间减少，并且水平下降，从而使得正常游戏的玩家遇到使用外挂的玩家概率降低，或是有更大的概率击败使用外挂的玩家，最终使得大部分的玩家的游戏体验总是能在一个正常的水平，最终能够很有效的减少外挂对于一个游戏的影响。
    

注：
1.本文完全由本人编写，由于水平比较低（只是一个普通的大学生），并且没有系统的学习过反外挂的技术，所以可能使用了别人的观点但是并不知道出处，所以如果有这种情况，请指出。

2.本文的公式完成度很低，主要是这些公式需要一些外挂的数据来进行分析，究竟使用怎样的函数是适合的，还有递增递减速率的问题，这是需要定量的，而不是仅仅定性即可，如果有好的想法，请赐教。
