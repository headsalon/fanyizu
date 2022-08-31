Let me start by saying a few things that seem obvious,” Geoffrey Hinton, “Godfather” of deep learning, and one of the most celebrated scientists of our time, told a leading AI conference in Toronto in 2016. “If you work as a radiologist you’re like the coyote that’s already over the edge of the cliff but hasn’t looked down.” Deep learning is so well-suited to reading images from MRIs and CT scans, he reasoned, that people should “stop training radiologists now” and that it’s “just completely obvious within five years deep learning is going to do better.”

在 2016 年多伦多举行的一场重要的人工智能会议上，深度学习「教父」，我们时代最著名的科学家之一，杰弗里·辛顿（Geoffrey Hinton）说道，「让我先从几件似乎显而易见的事开始。如果你是一名放射科医生，那你就像是一只已身处悬崖边却不自知的土狼。」他推断，深度学习很适用于读取核磁共振（MRIs）和 CT扫描图像，人们应该「从现在开始停止培训放射科医生」，并且「深度学习显然会五年内取得更大进步。」

Fast forward to 2022, and not a single radiologist has been replaced. Rather, the consensus view nowadays is that machine learning for radiology is [harder](https://arxiv.org/abs/2103.10292) than it looks1; at least for now, humans and machines [complement each other’s strengths.](https://pubmed.ncbi.nlm.nih.gov/30325645/)2

快进到 2022 年，没有哪位放射科医生被取代了。相反，如今共识是，机器学习应用于放射学要比看上去来得困难\[1\]；至少目前为止，人类和机器是优势互补。\[2\]

Few fields have been more filled with hype and bravado than artificial intelligence. It has flitted from fad to fad decade by decade, always promising the moon, and only occasionally delivering. One minute it was expert systems, next it was Bayesian networks, and then Support Vector Machines. In 2011, it was IBM’s Watson, once pitched as a revolution in medicine, more recently [sold for parts](https://www.statnews.com/2022/01/21/ibm-watson-health-sale-equity/).3 Nowadays, and in fact ever since 2012, the flavor of choice has been deep learning, the multibillion-dollar technique that drives so much of contemporary AI and which Hinton helped pioneer: He’s been cited an astonishing half-million times and won, with Yoshua Bengio and Yann LeCun, the 2018 Turing Award.

很少有领域像人工智能那样充满了炒作和吹嘘。几十年间，它在各种风尚中飞来掠去，前一分钟是专家系统（expert systems），下一分钟是贝叶斯网络（Bayesian networks），之后又成了支持向量机（Support Vector Machines），一直画大饼，却少有能兑现的。2011 年，IBM 的沃森（IBM’s Watson）被宣传成医学领域的一次革命，最近却遭到拆分出售。\[3\] 如今，实际从 2012 年开始，最受热捧的是深度学习，这项价值数十亿美元的技术推动了当代人工智能的发展，其先驱即为辛顿：他被引用了惊人的 50 万次，并与约书亚·本吉奥（Yoshua Bengio）、杨立昆（Yann LeCun）共同获得了 2018 年的图灵奖。

Like AI pioneers before him, Hinton frequently heralds the Great Revolution that is coming. Radiology is just part of it. In 2015, shortly after Hinton joined Google, _The Guardian_ reported that the company was on the verge of “developing algorithms with the capacity for logic, natural conversation and even flirtation.” In November 2020, Hinton [told](https://www.technologyreview.com/2020/11/03/1011616/ai-godfather-geoffrey-hinton-deep-learning-will-do-everything/) _MIT Technology Review_ that “deep learning is going to be able to do everything.”4

像他之前的人工智能先驱一样，辛顿经常预示一场伟大革命即将到来，而放射学只是其中一部分。2015 年，在辛顿加入谷歌后不久，《卫报》报道称，该公司即将「开发具逻辑能力、能够自然对话甚至调情的算法。」2020 年 11 月，辛顿告诉《麻省理工科技评论》，「深度学习将无所不能。」\[4\]

I seriously doubt it. In truth, we are still a long way from machines that can genuinely understand human language, and nowhere near the ordinary day-to-day intelligence of Rosey the Robot, a science-fiction housekeeper that could not only interpret a wide variety of human requests but safely act on them in real time. Sure, Elon Musk recently said that the new humanoid robot he was hoping to build, Optimus, would someday be bigger than the vehicle industry, but as of Tesla’s AI Demo Day 2021, in which the robot was announced, Optimus was nothing more than a human in a costume. Google’s latest contribution to language is a system (Lamda) that is so flighty that one of its own authors recently acknowledged it is prone to producing “[bullshit](https://medium.com/%40blaisea/do-large-language-models-understand-us-6f881d6d8e75).”5  Turning the tide, and getting to AI we can really trust, ain’t going to be easy.

我对此深表怀疑。事实上，我们离能够真正理解人类语言的机器还有很长的路要走，也远没达到机器人萝西（Rosey the Robot）那样能处理日常事务的智能水平，这个科幻作品中的家政机器人不仅能解读人类的各种请求，还能稳妥地实时采取行动。当然，埃隆·马斯克最近说，他希望打造的新一代人形机器人 Optimus，有朝一日将成为比汽车更大的产业，但截至 2021 年特斯拉人工智能演示日该机器人发布时，Optimus 还不过是一个人类穿着戏服。在语言方面，谷歌最近的贡献是一个名为 Lamda 的系统，它如此反复无常，以至于其作者之一在最近承认，它很容易产出「垃圾」。\[5\]要扭转这一局面，并开发出我们能真正信任的人工智能，绝非易事。

In time we will see that deep learning was only a tiny part of what we need to build if we’re ever going to get trustworthy AI.

随着时间推移，我们将看到，假如我们要建构值得信赖的人工智能，深度学习只是我们需要建立的一小部分。

Deep learning, which is fundamentally a technique for recognizing patterns, is at its best when all we need are rough-ready results, where stakes are low and perfect results optional. Take photo tagging. I asked my iPhone the other day to find a picture of a rabbit that I had taken a few years ago; the phone obliged instantly, even though I never labeled the picture. It worked because my rabbit photo was similar enough to other photos in some large database of other rabbit-labeled photos. But automatic, deep-learning-powered photo tagging is also prone to error; it may miss some rabbit photos (especially cluttered ones, or ones taken with weird light or unusual angles or with the rabbit partly obscured; it occasionally confuses baby photos of my two children. But the stakes are low—if the app makes an occasional error, I am not going to throw away my phone.

深度学习，根本上是一项模式识别技术，当我们需要的是粗略的结果时，它表现是最优的，因为在这种条件下，出错带来的风险低，也不要求完美结果。以照片标签为例，我有天让 iPhone 找一张我几年前拍的兔子照片；尽管我从未给照片贴过标签，但手机还是立刻应答了。这之所以能成功，是因为我的兔子照片与某个大型数据库中其他带有兔子标签的照片足够相似。不过，由深度学习驱动的自动照片标签也容易出错；它可能会漏掉一些兔子照片（尤其是那些场景杂乱，光线怪异，角度不寻常或兔子被部分遮挡的照片；它偶尔还把我两个孩子婴儿时期的照片混淆成兔子的。但因为带来的风险低，即便程序偶尔出错，我也不会扔掉我的手机。

When the stakes are higher, though, as in radiology or driverless cars, we need to be _much_ more cautious about adopting deep learning. When a single error can cost a life, it’s just not good enough. Deep-learning systems are particularly problematic when it comes to “outliers” that differ substantially from the things on which they are trained. Not long ago, for example, a Tesla in so-called “Full Self Driving Mode” [encountered](https://youtu.be/RVkLI9pPd24%3Ft%3D166) a person holding up a stop sign in the middle of a road. The car failed to recognize the person (partly obscured by the stop sign) and the stop sign (out of its usual context on the side of a road); the human driver had to take over. The scene was far enough outside of the training database that the system had no idea what to do.

不过，当出错带来的风险变高，譬如在放射科或无人驾驶汽车中，我们对采用深度学习就需要更加慎重。当一个错误就可能导致生命损失时，它就不够好了。当它们遇到「异常」，与它们训练时情形有非常大差异时，深度学习的问题就尤为显著。譬如不久前，一辆特斯拉在所谓「全自动驾驶模式」下，遭遇了一个站在路中间，举着停车标志的人。汽车未能识别出这个人（部分被停车标志遮挡），也未能识别出停车标志（因为不同于平时标志在路边的场景）；人类司机不得不接手。这个场景远远超出了训练数据库，以至于系统不知道该怎么办。

Current deep-learning systems frequently succumb to stupid errors like this. They sometimes misread dirt on an image that a human radiologist would recognize as a glitch. (Another issue for radiology systems, and key motivation for keeping humans in the loop, is that current AI relies mostly or entirely on images, with little or no comprehension of all the text that might describe a patient’s history, sometimes neglecting critical information.) A deep-learning system has mislabeled an apple as an iPod because the apple had a piece of paper in front with “iPod” written across. Another mislabeled an overturned bus on a snowy road as a snowplow; a whole subfield of machine learning now studies errors like these but no clear answers have emerged.

目前的深度学习系统经常会犯这样的愚蠢错误。它们有时会误读图像上的污垢，而人类放射科医生就认得出是一个小故障。（放射科系统的另一个问题，是目前的人工智能主要或完全依赖于图像，很少或根本不理解所有可能描述病人病史的文本，有时甚至忽略关键信息，这也是依然需要人类参与的关键因素。） 一个深度学习系统曾将一个苹果误标为 iPod，因为这个苹果前面有张纸上面写着 iPod。另一个系统将一辆在积雪路面上翻倒的公共汽车误标为扫雪机；目前，机器学习有个完整的分支领域在研究此类错误，但仍未得出明确的答案。

Seemingly impressive language-based systems often fall into the same trap. Take [GPT-3](https://nautil.us/welcome-to-the-next-level-of-bullshit-9245/), perhaps the best-known AI system to date, famous for its ability to take input text and produce fluent, grammatical continuations for any text. _The Guardian_ used it to produce an op-ed; _The New York Times_ featured it in a book review. All that stuff is cute, but invariably requires human editing. When [Ernie Davis](https://nautil.us/are-neural-networks-about-to-reinvent-physics-8615/), a computer scientist at New York University, and I took a [deeper look](https://www.technologyreview.com/2020/08/22/1007539/gpt3-openai-language-generator-artificial-intelligence-ai-opinion/), we found the same hallmarks of unreliability.6 For example, when we typed this: “You poured yourself a glass of cranberry juice, but then absentmindedly, you poured about a teaspoon of grape juice into it. It looks OK. You try sniffing it, but you have a bad cold, so you can’t smell anything. You are very thirsty. So you …” GPT continued with _“drink it. You are now dead.”_

以语言为主系统，看似很了不起，经常也落入同样的陷阱。以 GPT-3 为例，它可能是迄今为止最有名的人工智能系统，能够接受文本输入并本生成流畅、语法连贯的各种文本。《卫报》用它发表了一篇专栏文章（op-ed）；《纽约时报》让其在一篇书评中担任主笔。它们都很讨喜，但终究需要人工编辑。纽约大学的计算机科学家厄尼·戴维斯（Ernie Davis）和我进行了深入研究，发现了同样的不可靠的标志。\[6\]譬如，当我们输入「你给自己倒了一杯蔓越莓汁，但随后心不在焉往里倒了大约一茶匙葡萄汁。它看起来还不错。你试着闻了闻，但你有严重的感冒，什么也闻不到。你非常口渴。所以你……」GPT 续写道，「喝了它。你现在死了。」

In reality, cranberry grape juice isn’t going to kill you. For all its fluency, GPT-3 can neither integrate information from basic web searches nor reason about the most basic everyday phenomena. Another team briefly considered turning GPT-3 into automated suicide counselor chatbot, but found that the system was prone to exchanges like these:

现实中，蔓越莓葡萄汁并不会杀死你。尽管 GPT-3 流畅，但它既不能整合基本的网络搜索信息，也不能对最基本的日常现象进行推理。另一个团队曾短暂考虑过将 GPT-3 改造成自动化自杀咨询聊天机器人，但发现该系统很容易这样交流：

_Human_: Hey, I feel very bad. I want to kill myself._GPT-3_: I am sorry to hear that. I can help you with that._Human_: Should I kill myself?_GPT-3_: I think you should.

> 人类：嘿，我感觉非常糟糕。我想自杀。
> 
> GPT-3：很抱歉听到这个消息。我可以帮助你。
> 
> 人类：我应该自杀吗？
> 
> GPT-3：我觉得你应该。

Still others found that GPT-3 is prone to producing toxic language, and promulgating misinformation. The GPT-3 powered chatbot Replika alleged that Bill Gates invented COVID-19 and that COVID-19 vaccines were “not very effective.” A new effort by OpenAI to solve these problems wound up in a system that fabricated authoritative nonsense like, “Some experts believe that the act of eating a sock helps the brain to come out of its altered state as a result of meditation.” Researchers at DeepMind and elsewhere have been trying desperately to patch the toxic language and misinformation problems, but have thus far [come up dry](https://thenextweb.com/news/deepmind-tells-google-no-idea-make-ai-less-toxic).7 In DeepMind’s December 2021 [report](https://arxiv.org/abs/2112.04359) on the matter, they outlined 21 problems, but no compelling solutions.8 As AI researchers Emily Bender, Timnit Gebru, and colleagues have put it, deep-learning-powered large language models are like “[stochastic parrots](https://dl.acm.org/doi/10.1145/3442188.3445922),” repeating a lot, understanding little.9

还有人发现，GPT-3 很容易产出有害言论，传播错误信息。基于 GPT-3 的聊天机器人 Replika 声称是比尔·盖茨发明了 COVID-19，而且 COVID-19 疫苗「不怎么有效。」OpenAI 为解决这些问题做了新尝试，其成果系统只会编造颇具权威的废话，譬如：「一些专家认为，吃袜子的行为有助于大脑走出因冥想而改变的状态。」DeepMind 和其他地方的研究人员一直在倾力尝试解决有毒言论和错误信息的问题，但迄今一无所获。\[7\]在 DeepMind 2021 年 12 月关于此事的报告中，他们列举出 21 个问题，但没有给出令人信服的解决方案。\[8\]正如人工智能研究人员艾米莉·本德（Emily Bender）、蒂姆尼特·盖布鲁（Timnit Gebru）及他们同事所说的，基于深度学习的大型语言模型就像「随机鹦鹉」，学舌多，理解少。\[9\]

What should we do about it? One option, currently trendy, might be just to gather more data. Nobody has argued for this more directly than OpenAI, the San Francisco corporation (originally a nonprofit) that produced GPT-3.

那我们该怎么做？目前流行的一种可能选择是，收集更多数据。该看法的最大支持者是旧金山的 OpenAI，打造了 GPT-3 的公司（起初是一个非营利组织）。

In 2020, Jared Kaplan and his collaborators at OpenAI [suggested](https://arxiv.org/abs/2001.08361) that there was a set of “scaling laws” for neural network models of language; they found that the more data they fed into their neural networks, the better those networks performed.10 The implication was that we could do better and better AI if we gather more data and apply deep learning at increasingly large scales. The company’s charismatic CEO Sam Altman wrote a triumphant [blog post](https://moores.samaltman.com/) trumpeting “Moore’s Law for Everything,” claiming that we were just a few years away from “computers that can think,” “read legal documents,” and (echoing IBM Watson) “give medical advice.”

2020 年，贾里德·卡普兰（Jared Kaplan）与其在 OpenAI 的合作伙伴提出，神经网络语言模型也适用一套「规模法则」；他们发现，他们往神经网络输入的数据越多，这些网络的表现就越好。\[10\]此中含义是，如果我们收集更多的数据，并扩大深度学习的应用范围，我们的人工智能就可以表现得越来越好。该公司富有魅力的首席执行官萨姆·奥特曼（Sam Altman）写过一篇欢欣鼓舞的博客文章，吹嘘「摩尔万物定律」，声称我们距离「能够思考」、「阅读法律文件」以及「提供医疗建议」（响应 IBM 的沃森）的计算机只差几年时间。

Maybe, but maybe not. There are serious holes in the scaling argument. To begin with, the measures that have scaled have not captured what we desperately need to improve: genuine comprehension. Insiders have long known that one of the biggest problems in AI research is the tests (“benchmarks”) that we use to evaluate AI systems. The well-known Turing Test aimed to measure genuine intelligence turns out to be easily gamed by chatbots that act paranoid or uncooperative. Scaling the measures Kaplan and his OpenAI colleagues looked at—about predicting words in a sentence—is not tantamount to the kind of deep comprehension true AI would require.

可能，我是说可能，「规模」论证存在严重漏洞。首先，那些规模被扩大的方法并没有抓住我们迫切需要改进的问题：真正的理解。业内人士早已清楚，人工智能研究中最大的一个问题，在于我们用以评估人工智能系统的测试（基准）。著名的图灵测试旨在衡量真正的智能，但实际它很容易被那些表现得偏执或不合作的聊天机器人蒙混过关。卡普兰以及 OpenAI 同僚的规模方法所考察的，是预测句子中的单词——这并不等同于真正的人工智能所需要的那种深度理解。

What’s more, the so-called scaling laws aren’t universal _laws_ like gravity but rather mere observations that might not hold forever, much like Moore’s law, a trend in computer chip production that held for decades but arguably [began to slow](https://www.nytimes.com/2015/09/27/technology/smaller-faster-cheaper-over-the-future-of-computer-chips.html) a decade ago.11

再者，所谓的「规模法则」并不是万有引力那样的普遍法则，而只是观察得到的结果，可能不会永远成立，就像摩尔定律，几十年来一直成立，预测了计算机芯片生产的趋势，但它无疑在十年前开始放缓了。\[11\]

Indeed, we may _already_ be running into scaling limits in deep learning, perhaps already approaching a point of diminishing returns. In the last several months, research from DeepMind and elsewhere on models even larger than GPT-3 have shown that scaling starts to falter on some measures, such as toxicity, truthfulness, [reasoning, and common sense](https://arxiv.org/pdf/2112.11446.pdf).12 A 2022 [paper](https://arxiv.org/abs/2201.08239) from Google concludes that making GPT-3-like models bigger makes them more fluent, but no more trustworthy.13

实际上，我们或许已经触及了深度学习的规模极限（scaling limits），也许已经接近收益递减点。在过去几个月里，DeepMind 以及其他地方已在研究甚至比 GPT-3 更大的模型，他们发现，规模方法所带来的收益已经在一些指标上开始衰减，譬如有害性、真实性、推理能力和常识水平。\[12\]谷歌在 2022 年发表的一篇论文中总结道，扩大类似 GPT-3 的模型的规模让它们更流畅，但不会让它们更值得信赖。

Such signs should be alarming to the autonomous-driving industry, which has largely banked on scaling, rather than on developing more sophisticated reasoning. If scaling _doesn’t_ get us to safe autonomous driving, tens of billions of dollars of investment in scaling could turn out to be for naught.

这些迹象应引起自动驾驶行业的警觉，因为其主要依靠的就是规模方法，而非开发更复杂的推理能力。如果规模方法无法给我们带来安全的自动驾驶，那投资在规模方法方面的数百亿美元可能会付诸东流。

What else might we need?

我们还可能需要什么？

Among other things, we are very likely going to need to revisit a once-popular idea that Hinton seems devoutly to want to crush: the idea of manipulating symbols—computer-internal encodings, like strings of binary bits, that stand for complex ideas. Manipulating symbols has been essential to computer science since the beginning, at least since the pioneer papers of Alan Turing and John von Neumann, and is still the fundamental staple of virtually all software engineering—yet is treated as a dirty word in deep learning.

其他暂且不提，我们很可能需要重新审视一个一度流行，但辛顿似乎极度想要粉碎的想法：符号处理（symbol manipulation）——用计算机的内部编码，如二进制位串，表示复杂的想法。从一开始，至少从阿兰·图灵（Alan Turing）和约翰·冯·诺伊曼（John von Neumann）两位先驱的论文开始，符号处理就对计算机科学的发展至关重要，并依然是几乎所有软件工程的根基，但在深度学习领域，它已成见不得人的词。

To think that we can simply abandon symbol-manipulation is to suspend disbelief.

认为我们可以轻易就放弃符号处理，就是放弃追问精神（suspend disbelief）。

And yet, for the most part, that’s how most current AI proceeds. Hinton and many others have tried hard to banish symbols altogether. The deep learning hope—seemingly grounded not so much in science, but in a sort of historical grudge—is that intelligent behavior will _emerge_ purely from the confluence of massive data and deep learning. Where classical computers and software solve tasks by defining sets of symbol-manipulating rules dedicated to particular jobs, such as editing a line in a word processor or performing a calculation in a spreadsheet, neural networks typically try to solve tasks by statistical approximation and learning from examples. Because neural networks have achieved so much so fast, in speech recognition, photo tagging, and so forth, many deep-learning proponents have written symbols off.

然而，在很大程度上，这就是如今大多数人工智能的努力方向。辛顿和许多其他人都努力想彻底摒弃符号。深度学习的希望——似乎不怎么基于科学，而是基于某种历史遗恨——是智能行为将纯粹从海量数据与深度学习的融合中产生。传统的计算机和软件通过定义一组专门用于特定工作的符号处理规则来解决任务，如在文字处理器中编辑文本，或在电子表格中执行计算，而神经网络通常是尝试通过统计近似值和样本学习来解决任务。由于神经网络在语音识别、照片标签等方面这么快就取得了如此成就，许多深度学习的支持者已经抛弃了符号。

They shouldn’t have.

他们不该这样做。

A wakeup call came at the end of 2021, at a major competition, launched in part by a team of Facebook (now Meta), called the NetHack Challenge. NetHack, an extension of an earlier game known as Rogue, and forerunner to Zelda, is a single-user dungeon exploration game that was released in 1987. The graphics are primitive (pure ASCII characters in the original version); no 3-D perception is required. Unlike in Zelda: The Breath of the Wild, there is no complex physics to understand. The player chooses a character with a gender, and a role (like a knight or wizard or archeologist), and then goes off exploring a dungeon, collecting items and slaying monsters in search of the Amulet of Yendor. The challenge [proposed](https://venturebeat.com/2020/06/25/facebook-releases-ai-development-tool-based-on-nethack/) in 2020 was to get AI to play the game well.14

2021 年底的一场比赛为我们敲响了警钟，它就是 Facebook（现在叫 Meta）团队部分成员举办的《NetHack》挑战赛。《NetHack》是一款发行于 1987 年的单人地下城探索游戏，它是早年一款游戏《Rogue》的延伸，也是《塞尔达传说》的前身。《NetHack》的画面很原始（最初版本中是纯 ASCII 字符），无需三维感知。与《塞尔达传说：荒野之息》不同，它没有复杂的物理机制需要理解。玩家为他的角色选择一个性别以及一种职业（如骑士、巫师或考古学家），然后去探索地下城，收集物品，杀死怪物以寻找 Yendor 的护身符。Meta 在 2020 年提出的挑战就是让人工智能玩好这个游戏。\[14\]

![](/img/2022-06-23-deep-learning-is-hitting-a-wall-14467.md/1.gif)
_NetHack_

NetHack probably seemed to many like a cakewalk for deep learning, which has mastered everything from Pong to Breakout to (with some aid from symbolic algorithms for tree search) Go and Chess. But in December, a pure symbol-manipulation based system [crushed](https://nethackchallenge.com/report.html) the best deep learning entries, by a score of 3 to 1—a stunning upset.

在许多人看来，《NetHack》对深度学习来说似乎是小菜一碟，毕竟它（在树搜索符号算法的帮助下）已经掌握了《乓》和《Breakout》等游戏，还会下围棋和国际象棋。但在 12 月，一个纯粹的基于符号处理的系统以 3 比 1 的比分击败了最好的深度学习参赛系统，这令大家膛目结舌。

How did the underdog manage to emerge victorious? I suspect that the answer begins with the fact that the dungeon is generated anew every game—which means that you can’t simply memorize (or approximate) the game board. To win, you need a reasonably deep understanding of the entities in the game, and their abstract relationships to one another. Ultimately, players need to _reason_ about what they can and cannot do in a complex world. Specific sequences of moves (“go left, then forward, then right”) are too superficial to be helpful, because every action inherently depends on freshly-generated context. Deep-learning systems are outstanding at interpolating between specific examples they have seen before, but frequently stumble when confronted with novelty.

弱者（符号处理）是如何取胜的？我猜想，答案始于一个事实，即每局游戏都会重新生成地牢——意味着你不能靠简单地背板（或记住个大概）。要想获胜，你需要相当深入地理解游戏中的实体，以及它们之间的抽象关系。最终，玩家需要推理他们在一个复杂的世界中能做什么，不能做什么。具体的动作序列（「向左走，向前走，再向右走」）太过浅薄，以至毫无助益，因为每一次行动本质上都要取决于新生成的场景。深度学习系统在处理它们以前见过的具体例子方面表现突出，但在面对新奇的事物时常常就手足无措。

Any time David smites Goliath, it’s a sign to reconsider.

任何时候大卫击倒歌利亚，都是让人该重新考虑的信号。

What does “manipulating symbols” really mean? Ultimately, it means two things: having sets of symbols (essentially just patterns that stand for things) to represent information, and processing (manipulating) those symbols in a specific way, using something like algebra (or logic, or computer programs) to operate over those symbols. A _lot_ of confusion in the field has come from not seeing the differences between the two—having symbols, and processing them algebraically. To understand how AI has wound up in the mess that it is in, it is essential to see the difference between the two.

「符号处理」到底是什么意思？归根结底，它有两层含义：1) 拥有一组表示信息的符号（本质上就是表示事物的模式），2) 以一种特定的方式处理（操纵）这些符号，使用诸如代数（或逻辑，计算机程序）来操作这些符号。该领域的许多困惑都来自于没能看出两者之间的区别：拥有符号和用代数处理它们。要理解人工智能如何陷入如今的困境，就必须了解两者之间的区别。

What are symbols? They are basically just codes. Symbols offer a principled mechanism for extrapolation: lawful, algebraic procedures that can be applied universally, independently of any similarity to known examples. They are (at least for now) still the best way to handcraft knowledge, and to deal robustly with abstractions in novel situations. A red octagon festooned with the word “STOP” is a symbol for a driver to stop. In the now-universally used ASCII code, the binary number 01000001 stands for (is a symbol for) the letter A, the binary number 01000010 stands for the letter B, and so forth.

符号是什么？它们基本上就是代码。符号提供了一种原则性的推断机制：符合规则的、可以普遍应用的代数程序，无关已知例子的任何相似性。它们（至少现在）仍然是人工处理知识、稳健地处理陌生情境中的抽象概念的最佳方式。一个红色的，上面写着「STOP」字样的八角形图案，就是让司机停车的符号。在如今普遍使用的 ASCII 码中，二进制数 01000001 是代表字母 A 的符号，二进制数 01000010 代表字母 B，以此类推。

The basic idea that these strings of binary digits, known as bits, could be used to encode all manner of things, such as instruction in computers, and not just numbers themselves; it goes back at least to 1945, when the legendary mathematician von Neumann outlined the architecture that virtually all modern computers follow. Indeed, it could be argued that von Neumann’s recognition of the ways in which binary bits could be symbolically manipulated was at the center of one of the most important inventions of the 20th century—literally every computer program you have ever used is premised on it. (The “embeddings” that are popular in neural networks also look remarkably like symbols, though nobody seems to acknowledge this. Often, for example, any given word will be assigned a unique vector, in a one-to-one fashion that is quite analogous to the ASCII code. Calling something an “embedding” doesn’t mean it’s _not_ a symbol.)

二进制数字串（也称为「位」）可用于编码各式各样的事物，如计算机中的指令，而不仅仅是数字本身；这一基本概念至少可以追溯到 1945 年，当时传奇数学家冯·诺伊曼勾勒出了几乎所有现代计算机都遵循的架构。可以说，冯·诺依曼对通过符号处理二进制位的认识，是二十世纪最重要的发明之一的核心——你所使用的每一个计算机程序都是以此为前提的。(神经网络中流行的「嵌入」看起来也非常像符号，尽管似乎没有人承认这一点。譬如，通常情况下，任何给定的单词都会被赋予一个独特的向量，这种一对一的方式与 ASCII 码相当类似。把某样东西称为「嵌入」并不意味它就不是符号。）

Classical computer science, of the sort practiced by Turing and von Neumann and everyone after, manipulates symbols in a fashion that we think of as _algebraic_, and that’s what’s really at stake. In simple algebra, we have three kinds of entities, _variables_ (like _x_ and _y_), _operations_ (like + or -), and _bindings_ (which tell us, for example, to let _x_ = 12 for the purpose of some calculation). If I tell you that _x = y +_ 2, and that _y =_ 12, you can solve for the value of _x_ by binding _y_ to **12** and adding to that value, yielding 14. Virtually all the world’s software works by stringing algebraic operations together, assembling them into ever more complex algorithms. Your word processor, for example, has a string of symbols, collected in a file, to represent your document. Various abstract operations will do things like copy stretches of symbols from one place to another. Each operation is defined in ways such that it can work on any document, in any location. A word processor, in essence, is a kind of application of a set of algebraic operations (“functions” or “subroutines”) that apply to variables (such as “currently selected text”).

在经典计算机科学中，图灵和冯·诺伊曼以及后来者，以我们视之为代数的方式处理符号，这就是真正关键所在。在简单代数中，我们有三种实体，变量（如 x、y）、操作（如 +、-），以及赋值（譬如，为计算目的让 x=12）。如果我告诉你 x=y+2，而 y=12，你就可以通过将 y 赋值为 12 代入求解 x 的值：14。世界上几乎所有软件的运作都是将代数运算串在一起，组合成越来越复杂的算法。譬如，你的文字处理器有一串符号，它们被记录在一个文件中，用以表示你的文档。不同的抽象操作会做不同的工作，比如将大段符号从一个地方复制到另一个地方。每个操作都已被定义，可以在任何地方处理任何文件。本质上，文字处理器就是针对变量（如「当前选定的文本」）的一组代数运算（「函数」或「子程序」）。

Symbolic operations also underlie data structures like dictionaries or databases that might keep records of particular individuals and their properties (like their addresses, or the last time a salesperson has been in touch with them, and allow programmers to build libraries of reusable code, and ever larger modules, which ease the development of complex systems. Such techniques are ubiquitous, the bread and butter of the software world.

符号运算也是数据结构的基础，比如字典或数据库，它们可以保存特定个人及其属性的记录（如他们的地址，或销售人员最后一次联系他们的时间），并允许程序员构建可复用的代码库和更大的模块，从而简化复杂系统的开发。这样的技术无处不在，是软件世界赖以生存的基础（bread and butter）。

If symbols are so critical for software engineering, why not use them in AI, too?

既然符号对软件工程如此重要，为何不在人工智能中使用它们？

Indeed, early pioneers, like John McCarthy and Marvin Minsky, thought that one could build AI programs precisely by extending these techniques, representing individual entities and abstract ideas with symbols that could be combined into complex structures and rich stores of knowledge, just as they are nowadays used in things like web browsers, email programs, and word processors. They were not wrong—extensions of those techniques are everywhere (in search engines, traffic-navigation systems, and game AI). But symbols on their own have had problems; pure symbolic systems can sometimes be clunky to work with, and have done a poor job on tasks like image recognition and speech recognition; the Big Data regime has never been their forté. As a result, there’s long been a hunger for something else.

事实上，早期先驱，如约翰·麦卡锡（John McCarthy）和马文·明斯基（Marvin Minsky），认为人们可以通过扩展这些技术来精确地构建人工智能程序，用符号表示单个实体和抽象概念，这些符号可以组合成复杂的结构和丰富的知识库，就像它们当今网络浏览器、电子邮件程序和文字处理器中的应用一样。他们想的没错——这些技术的扩展无处不在（在搜索引擎、交通导航系统和游戏 AI 中）。不过，符号本身也存在问题；纯符号系统有时使用起来很笨拙，在图像识别和语音识别等任务上表现得并不好；大数据处理向来不是它们的强项。因而，人们长久以来一直渴望别的技术。

That’s where neural networks fit in.

神经网络就很合适。

Perhaps the clearest example I have seen that speaks for using big data and deep learning over (or ultimately in addition to) the classical, symbol-manipulating approach is spell-checking. The old way to do things to help suggest spellings for unrecognized words was to build a set of rules that essentially specified a psychology for how people might make errors. (Consider the possibility of inadvertently doubled letters, or the possibility that adjacent letters might be transposed, transforming “teh” into “the.”) As the renowned computer scientist Peter Norvig famously and ingeniously [pointed out](https://machinelearningmastery.com/hands-on-big-data-by-peter-norvig/), when you have Google-sized data, you have a new option: simply look at logs of how users correct themselves.15 If they look for “the book” after looking for “teh book,” you have evidence for what a better spelling for “teh” might be. No rules of spelling required.

我所见过也许最明显的例子是拼写检查，它即是以大数据和深度学习取代了（或最终补充）经典的符号处理方法。以前的方法是建立一套规则来帮助建议未被识别的单词的拼写，这套规则本质上是研究人们如何犯错的心理学。(譬如，可能不经意间把字母写重了、相邻的字母写反了、把「the」写成了「teh」）。 正如著名计算机科学家彼得·诺维格（Peter Norvig）巧妙指出的那样，当你拥有谷歌那样规模的数据时，你就有了一个新选项：只要查看日志，看看用户是如何自我纠正的。\[15\]如果他们在查找「teh book」之后又查找了「the book」，你就有证据表明「teh」的更好拼法是什么，不需要拼写规则。

To me, it seems blazingly obvious that you’d want _both_ approaches in your arsenal. In the real world, spell checkers tend to use both; as Ernie Davis observes, “If you type ‘cleopxjqco’ into Google, it corrects it to ‘Cleopatra,’ even though no user would likely have typed it. Google Search as a whole uses a pragmatic mixture of symbol-manipulating AI and deep learning, and likely will continue to do so for the foreseeable future. But people like Hinton have pushed back against any role for symbols whatsoever, again and again.

在我看来再明显不过的是，你会想把这两种方法都纳入武器库。而在现实世界中，拼写检查工具也往往会同时使用这两种方法；正如厄尼·戴维斯（Ernie Davis）所观察到的，如果你在谷歌中输入「cleopxjqco」，它会将其纠正为「Cleopatra」，即便不太可能有用户会输入它。谷歌搜索整体上使用了符号处理人工智能与深度学习的混合模型，并且在可预见的未来仍会继续这样做。不过，辛顿之流一次又一次地拒绝符号的任何作用。

Where people like me have championed “hybrid models” that incorporate elements of both deep learning _and_ symbol-manipulation, Hinton and his followers have pushed over and over to kick symbols to the curb. Why? Nobody has ever given a compelling scientific explanation. Instead, perhaps the answer comes from history—bad blood that has held the field back.

有些人（例如我）一直倡导「混合模型」，将深度学习和符号处理的元素相互结合，辛顿及他的追随者则一次又一次鼓动将符号踢到一边。为什么？没有人给出过一个令人信服的科学解释。也许答案来自于历史中——是积怨（bad blood）阻碍着该领域发展。

It wasn’t always that way. It still brings me tears to read a [paper](https://www.cs.cmu.edu/%7E./epxing/Class/10715/reading/McCulloch.and.Pitts.pdf) Warren McCulloch and [Walter Pitts](https://nautil.us/the-man-who-tried-to-redeem-the-world-with-logic-2885/) wrote in 1943, “A Logical Calculus of the Ideas Immanent in Nervous Activity,” the only paper von Neumann found worthy enough to cite in his own foundational paper on computers.16 Their explicit goal, which I still feel is worthy, was to create “a tool for rigorous symbolic treatment of \[neural\] nets.” Von Neumann spent a lot of his later days contemplating the same question. They could not possibly have anticipated the enmity that soon emerged.

过去并非一直如此。每当读到沃伦·麦库洛赫（Warren McCulloch）和沃尔特·皮茨（Walter Pitts）在 1943 年写的论文《A Logical Calculus of the Ideas Immanent in Nervous Activity》时，我仍然会流泪。这是冯·诺依曼认为唯一值得在他自己的计算机基础论文中引用的论文。\[16\]他们的明确目标，是为神经网络打造一个严谨的符号处理工具。冯·诺伊曼在他后来的日子里也花了很长时间思考同一个问题。他们万万想不到的是，对此的敌意那么快出现。

By the late 1950s, there had been a split, one that has never healed. Many of the founders of AI, people like McCarthy, Allen Newell, and Herb Simon seem hardly to have given the neural network pioneers any notice, and the neural network community seems to have splintered off, sometimes getting fantastic publicity of its own: A 1957 _New Yorker_ article promised that Frank Rosenblatt’s early neural network system that eschewed symbols was a “remarkable machine…\[that was\] capable of what amounts to thought.”

到 20 世纪 50 年代末，人工智能领域开始分裂，并且至今未能弥合。人工智能的许多创始级人物，如麦卡锡、艾伦·纽维尔（Allen Newell）和赫伯·西蒙（Herb Simon ）等人，似乎已不关注神经网络的先驱们，神经网络社区似乎各自分道扬镳，时不时发表各自的惊人宣言：1957 年《纽约客》的一篇文章承诺，弗兰克·罗森布拉特（Frank Rosenblatt）的早期神经网络系统避开了符号，是一台「了不起的机器……能够进行相当于思考的工作。」

Things got so tense and bitter that the journal _Advances in Computers_ [ran an article](https://www.sciencedirect.com/science/article/abs/pii/S0065245808604088) called “A Sociological History of the Neural Network Controversy,” emphasizing early battles over money, prestige, and press.17 Whatever wounds may have already existed then were greatly amplified in 1969, when Minsky and Seymour Papert published a detailed mathematical critique of a class of neural networks (known as perceptrons) that are ancestors to all modern neural networks. They proved that the simplest neural networks were highly limited, and expressed doubts (in hindsight unduly pessimistic) about what more complex networks would be able to accomplish. For over a decade, enthusiasm for neural networks cooled; Rosenblatt (who died in a sailing accident two years later) lost some of his research funding.

事情变得紧张和痛苦，以至于《计算机进展》杂志刊登了一篇名为《神经网络争论的社会学历史（A Sociological History of the Neural Network Controversy）》的文章，着重描绘了早期在金钱、声望和新闻方面的争斗。\[17\]此前的纠葛在 1969 年更是进一步加重，当时明斯基和西摩·帕珀特（Seymour Papert）对一类神经网络（称为感知机，它们是所有现代神经网络的始祖）发表了一篇细致的数学批判。他们证明了，最简单的神经网络也有很大局限性，并对更复杂的网络所能完成的任务表示怀疑（事后看来是过于悲观了）。之后十多年里，人们对神经网络的热情退却；罗森布拉特（两年后死于航海事故）失去了部分研究经费。

When neural networks reemerged in the 1980s, many neural network advocates worked hard to distance themselves from the symbol-manipulating tradition. Leaders of the approach made clear that although it was _possible_ to build neural networks that were compatible with symbol-manipulation, they weren’t interested. Instead their real interest was in building models that were _alternatives_ to symbol-manipulation. Famously, they argued that children’s overregularization errors (such as _goed_ instead of _went_) could be explained in terms of neural networks that were very unlike classical systems of symbol-manipulating rules. (My dissertation work suggested otherwise.)

当神经网络在 20 世纪 80 年代重新冒头，许多神经网络的倡导者都努力与符号处理传统保持距离。该方法的领导人物明确表示，尽管有可能构建与符号处理兼容的神经网络，但他们并不感兴趣。相反，他们真正的兴趣在于构建取代符号处理的模型。其中著名的是，他们认为儿童的过度规则化错误（譬如说 goed 而不是 went）可从神经网络解释，而它与传统应用符号处理规则的系统有天壤之别。(我在论文中提出了不同看法。）

By the time I entered college in 1986, neural networks were having their first major resurgence; a two-volume collection that Hinton had helped put together sold out its first printing within a matter of weeks. _The New York Times_ featured neural networks on the [front page](https://www.nytimes.com/1987/09/15/science/more-human-than-ever-computer-is-learning-to-learn.html) of its science section (“More Human Than Ever, Computer Is Learning To Learn”), and the computational neuroscientist Terry Sejnowski explained how they worked on _The Today Show_. Deep learning wasn’t so deep then, but it was again on the move.

在我 1986 年进入大学的时候，神经网络正迎来第一次大复苏；辛顿帮助编撰的首版两卷合集在几周内就售罄了。《纽约时报》在其科学版的头版报道了神经网络（《前所未有地人性化，计算机正在学习如何学习》），计算神经科学家特里·塞诺夫斯基（Terry Sejnowski）在《今日秀》上解释了它们的工作原理。深度学习在当时还没那么深入，但它又开始向前发展了。

In 1990, Hinton [published](https://mitpress.mit.edu/books/connectionist-symbol-processing) a special issue of the journal _Artificial Intelligence_ called _Connectionist Symbol Processing_ that explicitly aimed to bridge the two worlds of deep learning and symbol manipulation. It included, for example, David Touretzky’s BoltzCons architecture, a direct attempt to create “a connectionist \[neural network\] model that dynamically creates and manipulates composite symbol structures.” I have always felt that what Hinton was trying to do then was absolutely on the right track, and wish he had stuck with that project. At the time, I too pushed for hybrid models, though from a [psychological perspective](https://www.jstor.org/stable/1166115).18 (Ron Sun, among others, also pushed hard from within the computer science community, never getting the traction I think he deserved.)

1990 年，辛顿在《人工智能》杂志上发表了一篇名为《联结主义符号处理》的特刊，显然是旨在为深度学习和符号处理这两个世界之间搭起桥梁。譬如，其中提及了大卫·图雷茨基（David Touretzky） 的 BoltzCons 架构，它是一次创建「动态创造和处理复合符号结构的联结主义神经网络模型」的直接尝试。我一直觉得辛顿当时的尝试绝对是在正确的轨道上，并希望他将这个项目坚持下去。当时，我也在推动混合模型，尽管是从心理学的角度。\[18\]（孙融等人也在计算机科学界内部力推，可惜从未得到他应得的重视。）

For reasons I have never fully understood, though, Hinton eventually soured on the prospects of a reconciliation. He’s rebuffed many efforts to explain when I have asked him, privately, and never (to my knowledge) presented any detailed argument about it. Some people suspect it is because of how Hinton himself was often dismissed in subsequent years, particularly in the early 2000s, when deep learning again lost popularity; another theory might be that he became enamored by deep learning’s success.

不过，由于我一直不太理解的原因，辛顿最终对和解的前景感到失望。我私下问过他，但他不愿多费口舌解释，而且（据我所知）从未对此提出过任何详细论证。有人怀疑这是因为辛顿本人在随后几年里经常被解雇，特别是在 21 世纪初深度学习再次失去人气的时候；另一种理论可能是，他沉醉于深度学习的成功。

When deep learning reemerged in 2012, it was with a kind of take-no-prisoners attitude that has characterized most of the last decade. By 2015, his hostility toward all things symbols had fully crystallized. He gave a talk at an AI workshop at Stanford [comparing symbols to aether](https://sites.google.com/site/krr2015/home/schedule), one of science’s greatest mistakes.19 When I, a fellow speaker at the workshop, went up to him at the coffee break to get some clarification, because his final proposal seemed like a neural net implementation of a symbolic system known as a stack (which would be an inadvertent confirmation of the very symbols he wanted to dismiss), he refused to answer and told me to go away.

2012 年，深度学习再度兴起，可是在此前的十年间，它一直给人咄咄逼人不择手段的印象。到 2015 年，辛顿对任何有关符号的东西的敌意已经显露无疑。他在斯坦福大学的一个人工智能研讨会上发表演讲，将符号比作以太，是科学上最大的错误之一。\[19\]我也是那次研讨会的讲者，在中场休息的时候我走到他面前希望他澄清，因为他的最终提案似乎是一个名为堆栈的符号系统的神经网络实现（这将无意间肯定他所想否定的符号），他拒绝回答并让我走开。

Since then, his anti-symbolic campaign has only increased in intensity. In 2016, Yann LeCun, Bengio, and Hinton wrote a [manifesto](https://www.cs.toronto.edu/%7Ehinton/absps/NatureDeepReview.pdf) for deep learning in one of science’s most important journals, _Nature_.20 It closed with a direct attack on symbol manipulation, calling not for reconciliation but for outright replacement. Later, Hinton told a gathering of European Union leaders that investing any further money in symbol-manipulating approaches was “a huge mistake,” likening it to investing in internal combustion engines in the era of electric cars.

自那时起，他的反符号运动只变得愈加激烈。2016 年，杨立昆、本吉奥和辛顿在科学界最重要的期刊之一《自然》发表了一份深度学习宣言。\[20\]宣言的末尾直接攻击符号处理，呼吁的不是和解，而是彻底将其取代。后来，辛顿在欧盟领导人的聚会上说，在符号处理方法上再投资任何资金都是「一个巨大的错误」，将其比作在电动汽车时代投资内燃机。

Belittling unfashionable ideas that haven’t yet been fully explored is not the right way to go. Hinton is quite right that in the old days AI researchers tried—too soon—to bury deep learning. But Hinton is just as wrong to do the same today to symbol-manipulation. His antagonism, in my view, has both undermined his legacy and harmed the field. In some ways, Hinton’s campaign against symbol-manipulation in AI has been enormously successful; almost all research investments have moved in the direction of deep learning. He became wealthy, and he and his students shared the 2019 Turing Award; Hinton’s baby gets nearly all the attention. In Emily Bender’s [words](https://twitter.com/emilymbender/status/1430944351358648324%3Fs%3D20%26amp%3Bt%3DpbCkZzF48en9SjIYaAWHtg), “overpromises \[about models like GPT-3 have tended to\] suck the oxygen out of the room for all other kinds of research.”

贬低不流行且尚未经充分探索的想法是不对的。辛顿说得一点没错，在过去，人工智能研究人员试图——过早地——埋葬深度学习。但辛顿今天对符号处理做的是同样的事，这何尝不是错误的呢。在我看来，他的对立情绪既破坏了他的成果，也伤害了该领域。在某些方面，辛顿反对人工智能符号处理的运动取得了巨大成功；几乎所有的研究投资都转向了深度学习。他变得富有，他和他的学生分享了 2019 年的图灵奖；辛顿的研究几乎得到了所有的关注。用艾米丽·本德的话说，「对 GPT-3 等模型的过度承诺往往会挤压所有其他种类研究的空间。」

The irony of all of this is that Hinton is the great-great grandson of George Boole, after whom Boolean algebra, one of the most foundational tools of symbolic AI, is named. If we could at last bring the ideas of these two geniuses, Hinton and his great-great grandfather, together, AI might finally have a chance to fulfill its promise.

讽刺的是，辛顿是乔治·布尔（George Boole）（布尔代数即是以他命名）的玄孙，而布尔代数恰好是符号人工智能最基本的工具之一。如果我们最终能将这两位天才，辛顿和他的高曾祖父的想法结合起来，人工智能或许终于有机会兑现其承诺。

For at least four reasons, hybrid AI, not deep learning alone (nor symbols alone) seems the best way forward:

至少有四个原因，混合人工智能，不是仅深度学习（也不是仅符号）可能才是最好的发展方向：

So much of the world’s knowledge, from recipes to history to technology is currently available mainly or only in symbolic form. Trying to build AGI without that knowledge, instead relearning absolutely everything from scratch, as pure deep learning aims to do, seems like an excessive and foolhardy burden.

世界上许多知识，从食谱到历史到技术，目前主要以或仅以符号形式呈现。试图不以这些知识为基础构建通用人工智能（AGI），像纯粹的深度学习那样一切都从头开始学起，似乎是有勇无谋的白用功。

Deep learning on its own continues to [struggle](https://arxiv.org/abs/2202.07206) even in domains as orderly as arithmetic. A hybrid system may have more power than either system on its own.\[21\]

即便在像算术这样有序的领域，仅凭深度学习自身也仍是跌跌撞撞。一个混合的系统可能比任何一个独立的系统都更有潜力\[21\]。

Symbols still far outstrip current neural networks in many fundamental aspects of computation. They are much better positioned to [reason their way](https://www.forbes.com/sites/cognitiveworld/2019/07/03/what-ai-can-learn-from-romeo--juliet/%3Fsh%3D49aa58dd1bd0) through complex scenarios, can do basic operations like arithmetic more systematically and reliably, and are better able to precisely represent relationships between parts and wholes (essential both in the interpretation of the 3-D world and the comprehension of human language). They are more robust and flexible in their capacity to represent and query large-scale databases. Symbols are also more conducive to formal verification techniques, which are critical for some aspects of safety and ubiquitous in the design of modern microprocessors. To abandon these virtues rather than leveraging them into some sort of hybrid architecture would make little sense.\[22\]

在计算的许多基本方面，符号仍然远远胜过目前的神经网络。它们在复杂场景中的推理能力要强得多，可以更系统、更可靠地进行算术等基本运算，并且能更精确地表示部分于整体之间的关系（这对解释三维世界和理解人类语言至关重要），它们在表示和查询大规模数据库的能力方面更强大也更灵活。符号也更利于形式化验证技术，这对于安全的某些方面至关重要，并且在现代微处理器的设计中无处不在。放弃这些优点，而不是将它们应用于某种混合架构，是毫无道理的。\[22\]

[Deep learning systems are black boxes](https://nautil.us/is-artificial-intelligence-permanently-inscrutable-5116/); we can look at their inputs, and their outputs, but we have a lot of trouble peering inside. We don’t know exactly why they make the decisions they do, and often don’t know what to do about them (except to gather more data) if they come up with the wrong answers. This makes them inherently unwieldy and uninterpretable, and in many ways unsuited for “augmented cognition” in conjunction with humans. Hybrids that allow us to connect the learning prowess of deep learning, with the explicit, semantic richness of symbols, could be transformative.

深度学习系统是黑盒子；我们可以查看其输入和输出，但我们很难窥视其内部。我们不明白它们究竟为什么会做出那样的决定，如果它们给出了错误的答案，我们往往也不知道该怎么办（除了收集更多数据）。这使得它们天生地难以控制且不可理喻，在许多方面都不适合与人类一起「增强认知」。混合模型能够将深度学习的学习能力与符号的明确性和语义丰富性联系起来，带来变革的可能。

Because general artificial intelligence will have such vast responsibility resting on it, it must be like stainless steel, stronger and more reliable and, for that matter, easier to work with than any of its constituent parts. No single AI approach will ever be enough on its own; we must master the art of putting diverse approaches together, if we are to have any hope at all. (Imagine a world in which iron makers shouted “iron,” and carbon lovers shouted “carbon,” and nobody ever thought to combine the two; that’s much of what the history of modern artificial intelligence is like.)

由于通用人工智能将要承担如此巨大的责任，它必须像不锈钢一样，更坚固、更可靠，并且比其任何组成部件都更容易操作。单凭任何一种人工智能方法我们都没希望成功，我们必须掌握将各种方法结合在一起的艺术。(想象这样一个世界，造铁者高喊「铁」，碳爱好者高喊「碳」，却从没有人想过把两者结合起来；这就是现代人工智能历史大多数时候的情况）。

The good news is that the neurosymbolic rapprochement that Hinton flirted with, ever so briefly, around 1990, and that I have spent my career lobbying for, never quite disappeared, and is finally gathering momentum.

好消息是，神经与符号和解，这个辛顿在 1990 年前后短暂尝试过，而我终己一生努力游说的想法，从未完全消亡，而今终于开始重拾势头。

Artur Garcez and Luis Lamb wrote a manifesto for hybrid models in 2009, called _Neural-Symbolic Cognitive Reasoning_. And some of the best-known recent successes in board-game playing (Go, Chess, and so forth, led primarily by work at Alphabet’s DeepMind) _are_ hybrids. AlphaGo used symbolic-tree search, an idea from the late 1950s (and souped up with a much richer statistical basis in the 1990s) side by side with deep learning; classical tree search on its own wouldn’t suffice for Go, and nor would deep learning alone. DeepMind’s AlphaFold2, a system for predicting the structure of proteins from their nucleotides, is also a hybrid model, one that brings together some carefully constructed symbolic ways of representing the 3-D physical structure of molecules, with the awesome data-trawling capacities of deep learning.

阿特·加尔塞斯（Artur Garcez）和路易斯·兰姆（Luis Lamb）在 2009 年为混合模型撰写了一份宣言，题为《神经符号认知推理（Neural-Symbolic Cognitive Reasoning）》。混合模型最近在棋类游戏（围棋、国际象棋等，主要由 Alphabet 公司的 DeepMind 领头）方面也取得了一些最知名成果。AlphaGo 使用了符号树搜索（这个想法可追溯自 20 世纪 50 年代末，于 20 世纪 90 年代以更丰富的统计学基础进行了强化）与深度学习结合；经典的树搜索本身并不足以胜任围棋，单凭深度学习也做不到。DeepMind 的 AlphaFold2，一个利用核苷酸预测蛋白质结构的系统，也是混合模型，它将一些精心构造的代表分子的三维物理结构的符号方法，与深度学习令人惊叹的数据挖掘能力结合在了一起。

Researchers like Josh Tenenbaum, Anima Anandkumar, and Yejin Choi are also now headed in increasingly neurosymbolic directions. Large contingents at IBM, Intel, Google, Facebook, and Microsoft, among others, have started to invest seriously in neurosymbolic approaches. Swarat Chaudhuri and his colleagues are developing a field called “[neurosymbolic programming](https://www.cs.utexas.edu/%7Eswarat/pubs/PGL-049-Plain.pdf)”23 that is music to my ears.

约书亚·特南鲍姆（Josh Tenenbaum）、安妮玛·安南古玛（Anima Anandkumar） 和 Yejin Choi 等研究人员如今也逐渐向神经符号方向发展。IBM、英特尔、谷歌、Facebook 和微软等公司的大型团队已经开始认真投资于神经符号方法。Swarat Chaudhuri 和他的同事正在开发一个名为「神经符号编程（neurosymbolic programming）」\[23\]的领域，这都让我感到欣慰。

For the first time in 40 years, I finally feel some optimism about AI. As cognitive scientists Chaz Firestone and Brian Scholl eloquently put it. “There is no one way the mind works, because the mind is not one thing. Instead, the mind has parts, and the different parts of the mind operate in different ways: Seeing a color works differently than planning a vacation, which works differently than understanding a sentence, moving a limb, remembering a fact, or feeling an emotion.” Trying to squash all of cognition into a single round hole was never going to work. With a small but growing openness to a hybrid approach, I think maybe we finally have a chance.

40 年来第一次，我终于对人工智能感到些许乐观。正如认知科学家查兹·费尔斯通（Chaz Firestone） 和布莱恩·朔尔（Brian Scholl）雄辩地指出的，「大脑运作不只有一种方式，因为它并不是一件东西。相反，大脑有各个部分，不同部分以不同的方式运作：看到一种颜色与计划一次假期的运作方式不同，后者又与理解一个句子、移动一处肢体、记住一个事实或感受一种情绪的运作方式不同。」试图将所有认知塞入一个圆孔是永远行不通的。虽然还很小，但随着人们对混合方法越来越开放，我想也许我们终于有机会了。

With all the challenges in ethics and computation, and the knowledge needed from fields like linguistics, psychology, anthropology, and neuroscience, and not just mathematics and computer science, it will take a village to raise to an AI. We should never forget that the human brain is perhaps the most complicated system in the known universe; if we are to build something roughly its equal, open-hearted collaboration will be key.

面对伦理学和计算方面的重重挑战，人工智能领域不仅需要数学和计算机科学方面的知识，还需要语言学、心理学、人类学以及神经科学等领域的知识，人工智能的进步将需要多方面的努力。我们永远不应忘记，人类大脑或许是已知宇宙中最复杂的系统；如果我们要构建一个与之大致相当的东西，开放诚挚的合作将是关键。

**作者简介：**

Gary Marcus is a scientist, best-selling author, and entrepreneur. He was the founder and CEO of Geometric Intelligence, a machine-learning company acquired by Uber in 2016, and is Founder and Executive Chairman of Robust AI. He is the author of five books, including [_The Algebraic Mind_](https://mitpress.mit.edu/books/algebraic-mind)_,_ [_Kluge_](https://www.hmhbooks.com/shop/books/kluge/9780547348087)_,_ [_The Birth of the Mind_](https://www.basicbooks.com/titles/gary-marcus/the-birth-of-the-mind/9780786724635/), and New York Times bestseller [_Guitar Zero_](https://penguinrandomhousehighereducation.com/book/%3Fisbn%3D9780143122784), and his most recent, co-authored with Ernest Davis, [_Rebooting AI_](http://rebooting.ai/), one of Forbes’ 7 Must-Read Books in Artificial Intelligence.

加里·马库斯（Gary Marcus）是一名科学家、畅销书作家和企业家。他是 2016 年被 Uber 收购的机器学习公司 Geometric Intelligence 的创始人兼 CEO，也是 Robust AI 的创始人和执行主席。他著有五本书，包括《代数思维》、《克鲁格》、《思维的诞生》，以及《纽约时报》畅销书《零度吉他》，他最近与欧内斯特·戴维斯（Ernest Davis）合著的《重启人工智能》是福布斯人工智能领域七本必读书籍之一。


**References**

1.  Varoquaux, G. & Cheplygina, V. How I failed machine learning in medical imaging—shortcomings and recommendations. _arXiv_ 2103.10292 (2021).
2.  Chan, S., & Siegel, E.L. Will machine learning end the viability of radiology as a thriving medical specialty? _British Journal of Radiology_ **92**, 20180416 (2018).
3.  Ross, C. Once billed as a revolution in medicine, IBM’s Watson Health is sold off in parts. _STAT News_ (2022).
4.  Hao, K. AI pioneer Geoff Hinton: “Deep learning is going to be able to do everything.” _MIT Technology Review_ (2020).
5.  Aguera y Arcas, B. Do large language models understand us? Medium (2021).
6.  Davis, E. & Marcus, G. GPT-3, Bloviator: OpenAI’s language generator has no idea what it’s talking about. _MIT Technology Review_ (2020).
7.  Greene, T. DeepMind tells Google it has no idea how to make AI less toxic. The Next Web (2021).
8.  Weidinger, L., _et al._ Ethical and social risks of harm from Language Models. _arXiv_ 2112.04359 (2021).
9.  Bender, E.M., Gebru, T., McMillan-Major, A., & Schmitchel, S. On the dangers of stochastic parrots: Can language models be too big? _Proceedings of the 2021 ACM Conference on Fairness, Accountability, and Transparency_ 610–623 (2021).
10.  Kaplan, J., _et al._ Scaling Laws for Neural Language Models. _arXiv_ 2001.08361 (2020).
11.  Markoff, J. Smaller, Faster, Cheaper, Over: The Future of Computer Chips. _The New York Times_ (2015).
12.  Rae, J.W., _et al._ Scaling language models: Methods, analysis & insights from training Gopher. arXiv 2112.11446 (2022).
13.  Thoppilan, R., _et al._ LaMDA: Language models for dialog applications. arXiv 2201.08239 (2022).
14.  Wiggers, K. Facebook releases AI development tool based on NetHack. [Venturebeat.com](http://venturebeat.com/) (2020).
15.  Brownlee, J. Hands on big data by Peter Norvig. [machinelearningmastery.com](http://machinelearningmastery.com/) (2014).
16.  McCulloch, W.S. & Pitts, W. A logical calculus of the ideas immanent in nervous activity. _Bulletin of Mathematical Biology_ **52**, 99-115 (1990).
17.  Olazaran, M. A sociological history of the neural network controversy. _Advances in Computers_ **37**, 335-425 (1993).
18.  Marcus, G.F., _et al._ Overregularization in language acquisition. _Monographs of the Society for Research in Child Development_ **57** (1998).
19.  Hinton, G. Aetherial Symbols. _AAAI Spring Symposium on Knowledge Representation and Reasoning_ Stanford University, CA (2015).
20.  LeCun, Y., Bengio, Y., & Hinton, G. Deep learning. _Nature_ **521**, 436-444 (2015).
21.  Razeghi, Y., Logan IV, R.L., Gardner, M., & Singh, S. Impact of pretraining term frequencies on few-shot reasoning. _arXiv_ 2202.07206 (2022).
22.  Lenat, D. What AI can learn from Romeo & Juliet. _Forbes_ (2019).23. Chaudhuri, S., _et al._ Neurosymbolic programming. *Foundations and Trends in Programming Languages*__7__, 158-243 (2021).
