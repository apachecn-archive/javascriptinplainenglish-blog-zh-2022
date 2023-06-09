# 平庸的开发人员容易相信的谎言会毁掉他们的职业生涯

> 原文：<https://javascript.plainenglish.io/popular-lies-mediocre-developers-fall-for-that-destroy-their-career-6addbf887a2?source=collection_archive---------0----------------------->

## 你应该忽略的有害编程技巧

![](img/8ef12a377f3c30834dda086cb950bd5e.png)

Photo by [Andrea Piacquadio](https://www.pexels.com/@olly?utm_content=attributionCopyText&utm_medium=referral&utm_source=pexels) from [Pexels](https://www.pexels.com/photo/man-in-white-crew-neck-shirt-wearing-silver-framed-aviator-sunglasses-3780011/?utm_content=attributionCopyText&utm_medium=referral&utm_source=pexels)

没有一个开发者愿意被称为平庸。

每个人都喜欢被称为专家。

但在编程中，有一些流行的谎言往往会助长平庸。

这里有四个流行的谎言，这些谎言会毁了开发者的职业生涯。如果你相信以下任何一个谎言。是时候停止相信他们了。

# 1.“不断学习新事物”是 BS 的建议

建议程序员不断学习新语言或新技术。

他们被告知要跟上科技的发展。他们被告知要更加努力，理解新的概念。他们被要求阅读不同的时事通讯或博客，以了解技术领域的新事物。

但是只有通过学习新的东西，你才能成长为一个开发者。作为一名开发人员，要真正成长，你还需要了解现有的系统。

作为开发人员，我们必须问自己，为什么现有的系统是以一种特殊的方式实现的。我们需要深入挖掘，找出为什么以前的开发者选择了一个特定的设计模式。

## 一个更好理解的例子

假设您开始使用已经使用了很长时间的代码库。代码作者不再为同一个组织工作。

当你试图阅读代码时，你发现它很乱。你想从头开始重写整个代码库。

显而易见，任何开发者的反应都和你的反应一样。开发人员从一开始就有重写未知代码库的倾向。尤其是当他们使用任何新的语言和框架时。

在那种情况下，你首先需要理解上下文。你应该问一些问题，比如为什么选择一种特定的设计模式或语言。

一旦你理解了上下文。只有到那时，您才应该考虑对代码库进行更改。

# 2.以后再解决心态

当在“做得正确”和“做得快”之间做出选择时，是平庸的开发人员。他们在任何情况下都选择快速行动。

他们对自己说:

> "我会在下一次迭代中修复所有的小错误，让代码更具可读性."

在下一次迭代中发生的是，他们被一组新的问题所包围。这些新问题有一种紧迫感。这使得他们没有时间来解决早期的问题。

早期的问题没有解决。它们不断堆积。这就是所谓的技术债务。

短期来看，技术债务可能是有利的，但长期来看，它可能是毁灭性的。

写聪明的代码，不使用透露目的的变量名，不写容易发音的名字在短期内是有益的。这些可以让你快速完成编码。

例如，如果您使用此变量名:

```
let d; 
```

创建此变量是为了表示自创建以来的天数。使用这种类型的变量名，可以快速编码。

但是你必须记住，给一个代码库包含聪明代码的应用程序添加新特性是很困难的。

重构代码库变得更加困难。

在上面的例子中，如果你使用了一个变量名来揭示你创建它的意图。

```
let daysSinceCreation;
```

将来当你调试你的代码时，它会像魔法一样工作。

久而久之，这些小事积少成多。

## 你该怎么办？

这不像你应该总是避免“做得快”。

作为开发人员，有时我们别无选择，只能快速编码并交付。在这些情况下，我们承担了大量技术债务。

在那种情况下，作为开发人员，您需要尽快收回成本，还清技术债务。

# 3.不要打碎东西

平庸的开发人员不断告诉自己:

> “我不允许打碎任何东西。如果我破坏了代码库中的任何东西，我就会被解雇。”

这使得他们的工作很无聊，也不那么有趣。他们害怕承担哪怕是很小的风险。在对一行代码进行修改之前，他们会一直考虑可能出错的地方。

一旦他们做出重大改变。

他们开始祈祷，因为他们不希望任何不相关的功能被打破。

如果您做了一些更改，并且任何不相关的功能中断。这意味着整个系统需要修复。如果不对代码库进行必要的修改，代码的整体质量会下降。

当你试图做出必要的改变时，有些东西会坏掉。但是没有人关心你在改变的时候破坏了什么。如果你现在折射代码，你队友以后的日子就好过了。

如有必要，进行一些设计更改并简化代码。

移除项目不需要的所有代码。

检查角落情况。

## 不要害怕做出这些改变。

必要时清理代码库以说服管理层。去说服他们。告诉他们为什么这些变化从长远来看很重要。

以改善代码库的整体健康状况。

你会打碎一些东西。完全没问题。这是过程的一部分。

# 4.没有考虑代码的所有用例

每个用例都很重要。

简单地让你的代码为一些用例工作从长远来看是行不通的。

作为开发人员，您需要考虑代码的所有用例。

## 让我们举个例子来理解这一点:

假设您为一个包编写了代码，该包将公开提供给其他开发人员使用。

包裹名称是 authenticate_shipping_address。

您编写了这样一个验证邮政编码函数:

```
function authenticatePostalCode(givenCode){ return /^[0-9]{5}(?:-[0-9]{4})?$/.test(givenCode);}
```

在上面的函数中，我们使用了一个正则表达式来检查邮政编码。

如果您不理解正则表达式，并且您是第一次阅读它，不要担心。只是觉得上面的函数有助于验证邮政编码。

## 你的包裹如何成为他人的噩梦

在世界的另一边。

有一个叫鲍勃的程序员。Bob 参与了一个项目，他需要验证用户的邮政编码。

用户将来自不同的国家。

Bob 了解了一个名为:

```
authenticate_shipping_address
```

甚至没有检查代码。他用了这个包，认为它可以检查任何地方的邮政编码。

但几天后，用户开始抱怨该应用程序不验证他们的邮政编码。由于这个错误，该组织损失了数百万美元的业务。

鲍勃因为这个错误受到了上层管理人员的斥责。

后来，当他检查代码时，他发现这个包裹只验证了美国邮政编码。包裹内的代码没有验证英国邮政编码，如“SWIWONY”。

谁犯了错误。这绝对不是鲍勃的错。编写软件包的程序员应该已经考虑了所有的用例。

如果包作者考虑了所有用例，而不是命名包:

```
authenticate_shipping_address 
```

包的名称应该是:

```
US_shipping_address_authentication
```

这会让鲍勃保住他的工作。

当你写代码的时候，考虑每一个用例；否则，构建您的代码的程序员可能会陷入不必要的麻烦。

# 摘要

1.  不要只是不断学习新的东西。
2.  修正它以后的心态。
3.  在做改变的时候打破一些东西是可以的。
4.  考虑你的代码的所有用例。

[点击这里](https://codertoentrepreneurs.substack.com/)加入一个由热爱编程和技术的人组成的社区。喜欢在媒体上阅读？[购买会员资格](https://sanjay-priyadarshi.medium.com/membership)获得全部权限。

[](https://sanjay-priyadarshi.medium.com/membership) [## 通过我的推荐链接加入 Medium-Sanjay Priyadarshi

### 作为一个媒体会员，你的会员费的一部分会给你阅读的作家，你可以完全接触到每一个故事…

sanjay-priyadarshi.medium.com](https://sanjay-priyadarshi.medium.com/membership) 

*更多内容看* [***说白了就是***](https://plainenglish.io/) *。报名参加我们的* [***免费周报***](http://newsletter.plainenglish.io/) *。关注我们关于*[***Twitter***](https://twitter.com/inPlainEngHQ)*和*[***LinkedIn***](https://www.linkedin.com/company/inplainenglish/)*。加入我们的* [***社区***](https://discord.gg/GtDtUAvyhW) *。*