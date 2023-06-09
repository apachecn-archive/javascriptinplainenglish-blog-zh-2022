# 软件开发在过去 10 年中是如何被破坏的

> 原文：<https://javascript.plainenglish.io/how-software-development-has-been-disrupted-in-the-last-10-years-b31de946a736?source=collection_archive---------10----------------------->

## 为了更快地开发软件，你必须用不同的方式

![](img/f1e390f869a67c77f30421987de308d8.png)

[Daniel K Cheung](https://unsplash.com/@danielkcheung)

> 人生苦短，没时间去造没人想要的东西。菲尔·麦金尼

[写代码很简单，但创建软件却复杂而艰难](https://itnext.io/unrecognized-simplicity-of-writing-code-and-the-underestimated-complexity-of-creating-software-cdf6c20ca68e)。多年来，软件开发的规则一直在调整、更新和变化。

技术变了，但是软件开发的过程保持不变。出现了技术中断、流程变化和思维方式的改变。

# 贝宝、彼得·泰尔和打破规则

我在读《T4:逆势而上:彼得·泰尔和硅谷对权力的追求》，彼得·泰尔鼓励公司打破现有的商业规则，以实现更快的增长。

如果你打破了规则，你就可以增长——用你的方式实现极端增长，成为垄断。彼得·泰尔喜欢说，一旦你成为垄断者，竞争就是失败者的事情。当你处于垄断地位时，你不必浪费时间和精力与竞争对手斗争，或者降低价格，增加新功能来跟上。

贝宝就像一家银行，例如，他们让你可以用信用卡支付物品并把钱存入你的账户。银行是有规定的，PayPal 懒得注册银行，因为它不想因为遵守规则而变慢。

贝宝没有遵循银行用于欺诈和身份证明的规则。它没有尽力阻止人们将钱用于非法目的。

要开一家银行，你需要证明你的身份，这是为了减少欺诈，不允许人们使用假的或偷来的身份。

PayPal 采取了快速增长、打破规则、事后道歉的方式。PayPal 希望增长黑客，这使他们做以下事情:

*   没有身份证明来创建 PayPal 帐户
*   很少检查他们把钱花在了什么地方
*   先支付 20 美元加入 PayPal，然后支付 10 美元加入

这导致了不可思议的增长，PayPal 闪电般地超越了它的竞争对手(他们遵守游戏规则)，从传统银行那里抢走了客户。

当竞争对手抱怨时，PayPal 道歉，继续做，继续成长。

PayPay 获得了巨大的增长，但也有很多欺诈行为，人们用偷来的信用卡上传资金。PayPal 将不得不为欺诈使用支付信用卡。早些年，贝宝因欺诈损失了数百万英镑。

这似乎是一个可行的策略，但当时贝宝烧钱，没有明确的赚钱计划。该计划是成为一个垄断，然后提高价格。成为垄断者意味着贝宝将击败竞争对手，当他们提价时，将没有好的选择。

不能保证成功，快速增长的前期支出是一个巨大的风险，一个巨大的回报场景。

不遵守规则让 PayPal 得以快速发展。软件开发的规则是什么，你能打破或弯曲它们以获得更快的开发吗？

# **软件开发规则**

我对软件开发的信念是质量是捷径，捷径花费你更多的时间，而不是你现在获得的时间。[质量是创建软件并将其投入生产的最快方式](https://itnext.io/software-development-is-misunderstood-quality-is-fastest-way-to-get-code-into-production-f1f5a0792c69)。

下面是软件开发的高级步骤。

1.  需求由客户定义，由 BA/顾问和开发团队提炼
2.  开发人员编写代码，创建定制，从而创建软件。
3.  开发人员测试/单元测试
4.  将软件部署到测试环境
5.  测试软件(手动测试或自动测试)—反馈/回到步骤 1
6.  向用户展示/演示软件—反馈/回到第 1 步的更改
7.  将软件部署到用户环境(UAT) —用户测试—反馈/更改回到步骤 1
8.  培训用户、文档。
9.  将软件部署到生产中。旧软件关闭了。
10.  软件被维护，错误被修复，更新版本通过开发生命周期进入生产。

显然有一个更详细的观点，软件的目标是创建高质量的软件，并为维护而构建。

每一行代码都必须维护，代码质量越低，产生的技术债务就越多。技术债务/低质量代码使得所有与代码的交互更加困难，耗时更长。

创建软件更加详细，但是对于本文，我们将坚持上面的高级规则。

# **软件开发规则是如何被打破、改进或破坏的？**

什么样的变化改进或扰乱了软件开发？

下面是软件开发被破坏的一些方式的列表。

# **DevOps、ALM 和自动化**

当我使用术语 DevOps 时，我指的是 ALM、自动化和 DevOps。

当软件开发遇到困难时，开发人员不会去做。当从开发环境向测试/UAT 环境部署变更是手工的和困难的时候，这种情况并不经常发生。

不经常部署和保持环境同步的后果是:

*   测试人员测试的软件不同于开发或生产软件
*   用户看不到最新的软件或变化
*   用户没有测试最新的软件

如果环境是同步的，那么测试每个环境就像测试相同的软件。

DevOps 通过自动化构建、发布、测试和其他枯燥的手工任务打破了这一限制。

*   允许开发人员查看他的最新代码是否可以编译
*   每夜构建
*   开发团队从源代码部署代码
*   为代码库运行自动化测试，以查看是否有任何损坏
*   允许在数小时内恢复环境
*   有助于提高部署的速度和准确性
*   它有助于消除软件开发的无聊感。

DevOps、ALM 和自动化提高了软件构建的质量，并增加了客户对开发团队的信心。

对于大型项目，DevOps、ALM 和自动化对软件开发产生了持久的影响。我无法想象没有它做一个大型软件项目，这将是一项艰苦的工作。

# **近海**

这不会改变或扰乱软件开发过程，但会扰乱价格。软件开发人员很贵，因为软件是一门技能，作为软件开发人员需要练习才能提高。

降低成本的一个方法是将软件开发人员安置在工资较低的国家。海上开发可以降低 60%到 70%的成本。

远程工作能力的增加使得离岸工作变得更加容易，并且能够创造一种更加协作的工作方式。

# 结构

我低估了框架有多强大，直到我转到一个不使用它们的项目。我是一名 Java 开发人员，我们使用了一个叫做 Spring 的框架。

我参与了一个项目，在那里他们创建了自己的框架。我不得不学习自己的个人框架，并维护、修复和更新框架中的错误。

框架创建了一个标准的开发方法，你不需要在管道上工作。框架构建得很好，使用配置而不是代码来改变它的工作方式。

框架很流行，这意味着很容易找到有框架经验的开发人员。如果他们没有经验，网上会有很多信息和教程可以学习。

# 敏捷

敏捷成为最热门的项目方法，客户从不知道什么是敏捷变成了要求敏捷的项目。

有些人认为敏捷已经消失了，但是[敏捷死亡的谣言被夸大了](https://itnext.io/agile-isnt-dead-and-it-can-t-be-killed-64d4ceba9e50)。

以前的软件项目方法是瀑布项目。花了几个月的时间试图预先确定所有的需求。然后在发布到生产之前构建整个系统。

敏捷将软件分成更小的块，称为特性/用户故事。它将在 sprint 结束时将软件发布到产品中。理论上，客户可以在开始开发新软件几周后获得投资回报。

敏捷缩短了软件开发和即时变更的反馈循环。它让 scrum 团队中的业务专家作为产品所有者参与进来，一旦开发人员创建了软件，他们就有权决定和修改软件。

我喜欢敏捷项目过程的诚实和快速反馈。敏捷并不适合所有项目，它需要深入的业务知识和果断的产品所有者，敏捷才能成功。

实际上，不可能将功能分解成更小的块来发布到生产中。许多客户不喜欢在每个冲刺阶段(2 或 4 周)发布产品。

我现在在项目中看到的是瀑布和敏捷的混合——wagi le 或 Scrumfall。前期需求收集和整体设计到位。开发是以敏捷的方式完成的，包括冲刺、回放和其他敏捷仪式。这允许多个开发团队同时工作，并且客户可以得到快速的反馈。

缺失的需求和不正确的软件可以被快速地改变，确保软件永远不会离需求太远。

首先设计一个具有较小功能的系统会产生技术债务和低效的设计。一个特征接一个特征的软件设计不能创建整个系统的有效设计。

# **云**

过去在公司服务器上运行的软件和用户需要在他们的计算机上安装胖客户端(应用程序)。

互联网的技术进步以及数据中心和服务(谷歌、亚马逊/AWS、微软/Azure)的发展使得软件可以在安装了应用程序的云中运行。

这使得软件开发更加容易，而不必在计算机上安装应用程序和管理版本。客户很快开始要求服务来摆脱维护和升级他们自己的服务器的负担。

互联网速度的提高和支持互联网的移动应用的爆炸式增长。

它没有改变软件开发过程，但它改变了软件的使用和消费方式。

# **快捷键**

这是牛仔开发，它可以在小项目上工作。这是走捷径的艺术，不是单元测试，没有 DevOps。

它发展很快，走捷径，希望技术债不要追上来拖你的后腿。在开发人员很少的小项目中，开发人员可以理解整个解决方案。

这使得公司在培训软件开发人员方面的投资不会减少，因为他们不需要了解软件开发的所有方面。这些公司在培训、工资上花费更少，并移除所有不创造代码的活动。

主要是小公司和较小的软件项目。我在一些这样的公司工作过，我不喜欢这样，因为我想写更好质量的代码。

这种方法在大型/企业项目中是失败的，因为技术债务会吞没项目并使它们变慢。

# **开源**

开源软件是开放给所有开发者使用的代码库。代码由志愿开发人员构建和维护。

开源代码曾经不被看好，而且由于增加了风险，它被禁止使用。

开源已经赢得了信任，并被视为创建使用现有开源功能的软件的有效方法。

越多的开发者创建开源库，所有的开发者就越能从中受益。

# **低码**

低代码理论认为软件开发需要昂贵的熟练开发人员来创建和维护代码。打破这个规则的一个方法是创建低代码开发工具，允许开发人员不用写代码就能创建软件。可重用的组件和工作流、集成和 GUI 界面允许开发人员无需代码即可创建软件。

理论上，低级代码可以更快、更容易地用初级开发人员创建软件。消除学习如何编写代码的需要降低了复杂性，提高了开发速度和易于维护。开发人员的成本会更低，因为非开发人员(公民开发人员)。

低代码开发可以更快、更省钱地创建软件(由于使用初级/公民开发者)。软件被部署到减少其他代码的云服务中。

初级/市民开发者写的几千个 app 会产生维护问题吗？

软件开发的技巧需要的不仅仅是一个好的工具，它需要一个熟练的软件开发人员。

# **机器学习/人工智能**

机器学习不会扰乱软件的创作，相反，它会扰乱用户支持软件所需的时间。

人工智能/机器学习自动化了像用聊天机器人回答问题这样的任务。AI 可以自动接收电子邮件，对其进行分类，并自动将其分配给正确的团队。

它可以阅读文档，将电话翻译成文本等。

# 其他人

*   虚拟机—使开发机器和服务器易于创建、重置
*   kubernetes——一个完整的环境

# **软件开发中什么不会变**

思考软件开发，我不确定将来规则会如何被打破，如何被打乱。

我不认为软件开发不能自动化——这是一个有未知最终目标的创造性过程。开发的大部分是解决制造什么，而不是制造什么。当软件基于独特的业务时，我看不到自动化软件的方法。

创建软件的成本在未来不会降低太多，因为创建软件不是一项商品业务。创建软件是一个基于个人素质的创造性过程。

[为什么软件开发中的廉价选项成本更高？](https://blog.devgenius.io/why-the-cheap-option-in-software-development-cost-more-dfce7f32c728)

软件项目的一半是发现软件应该做什么以及如何工作。组织具有不同技能的人群，共同决定软件应该如何工作，需要有技能的人。

[领导和资深开发者是软件项目成败的主要原因](https://medium.com/geekculture/leadership-and-senior-developers-are-the-main-reasons-for-success-or-failure-of-software-projects-7855d41fb66e)。

高级角色是成功软件项目的关键。当我看到一个进展顺利的项目，高层的人都不错。当我到达时

即使你能自动创建软件，你也不能自动理解一个复杂的业务是如何运作的。在这个行业工作的人不明白这一切是如何运作的。

*更多内容看* [***说白了。报名参加我们的***](http://plainenglish.io/) **[***免费周报***](http://newsletter.plainenglish.io/) *。在我们的* [***社区获得独家访问写作机会和建议***](https://discord.gg/GtDtUAvyhW) *。***