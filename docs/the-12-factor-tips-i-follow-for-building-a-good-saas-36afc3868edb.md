# 我遵循的建设好 SaaS 的 12 个因素

> 原文：<https://javascript.plainenglish.io/the-12-factor-tips-i-follow-for-building-a-good-saas-36afc3868edb?source=collection_archive---------9----------------------->

## 以及我对每个因素的一些看法。

![](img/04bc25ee3a170639560d4b2fffb470d8.png)

Photo by [Wonderlane](https://unsplash.com/@wonderlane?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com?utm_source=medium&utm_medium=referral)

2010 年，我第一次着手建造 SaaS。作为程序员，我的第一份也是最重要的工作之一。从那以后，这成了我最喜欢的项目类型。我为客户做过 SaaS 的项目，甚至在其他不完全是 SaaS 的项目中也做过，它们是网络应用，和 SaaS 有很多相似之处。

如果你刚进入这个 web 编程的世界，却不知道一个合适的方法可以遵循，那你就要倒霉了。

## **1。代码库**

代码库必须是独一无二的，并且可以从中执行许多部署。因此，这里的规则是明确的:如果你有一个以上的代码库，你没有一个 web 应用程序，而是一个分布式系统，每个库都必须遵循 12 个因素。

## **在实践中**

在 Node.js 项目中，我认为这是 Git 上每个 web 应用程序的单一存储库。目前，有很多关于 mono repo 的讨论，我们在同一个存储库中有几个 web 应用程序。不过，同样的规则也适用于分布式系统，因为在实践中，您必须独立地部署每个 monorepo 项目。所以，它们是独立的网络应用。

## **2。依赖性**

这个因素意味着应用程序拥有的所有依赖项必须配置为与应用程序本身一起安装。永远不要相信您将要部署它的环境已经全局安装了任何库。

## **在实践中**

在 Node.js 项目中，所有开发和生产依赖项都必须在 package.json 中正确引用，即使是那些最终可能会全局安装在服务器上的依赖项，如 TypeScript。

## **3。设置**

这个因素表明，您的所有应用程序设置可能因环境而异(开发、HTML、测试、生产等。)必须在环境级别进行配置，并且不应该在代码中进行硬编码。

## **在实践中**

在 Node.js 中，我们通过使用通过 dotenv 或 dotenv-safe 等模块加载的环境变量来实现这一点。

## **4。支持服务**

这个因素表明，您的应用程序需要的所有支持服务，从 MySQL 等数据库到 RabbitMQ 中的队列，通过 SMTP Gateway 和您自己公司的 web API，都应该被视为 web 应用程序外部的资源。

## **在实践中**

如上所述，这通常包括在每个服务的环境变量中配置凭证和 URL，即使所讨论的服务是由您创作或管理的。让你的 web 应用程序与它们保持松散耦合，这样将来做改变就容易多了。

## **5。编译、交付、执行**

“构建、发布和运行”因素指的是极限编程中经常引用的持续集成、持续交付和持续部署的概念。

## **在实践中**

我看到许多公司通过配置和使用 DevOps 工具(如 Jenkins、CircleCI、Bamboo 和 BitRise)来实现这一点，这些工具插入到他们的 Git 存储库中，当开发人员努力掌握测试、构建时，新版本就会生成，新版本会运行许多次新测试，并投入生产。

组装这种完全自动化的 CI/CD 流水线，并且仍然有信心在生产中不会出现任何问题，这不是一项简单的任务，但我在我经历过的一些公司中看到了这种情况。

## **6。流程**

12 因素应用程序在一个或多个彼此不共享数据的无状态进程中运行。当有多个进程时，每个进程都是独立的，不知道其他进程的存在，任何需要持久化的数据都存储在数据库中。

## **在实践中**

如果你的 web 应用有一个 RESTful 后端，你将遵循这个规则，因为这个架构也是无状态的。同样，假设您正在使用节点集群或 PM2 上传应用程序中的几个流程。在这种情况下，您也将满足这个要求，因为事件循环将被分叉，并且您将拥有并行运行的进程，即使在 Node.js 的情况下也是如此。

## **7。端口绑定**

这个因素意味着你的 web 应用必须是独立的。也就是说，它不依赖于像 Apache 或 IIS 这样的 web 服务器来运行，并且可以通过本地端口来访问它以响应 HTTP 请求。你能使用一个 shell 命令来上传你的应用程序，而不把它托管在 web 服务器上吗？然后注意这个因素！

在 Node.js 中，这非常简单，因为这是该技术最基本的原则之一，对吗？

## **8。竞赛**

这个因素是对因素 6 的加强，因为在 web 应用程序中处理并发性的最佳方式是拥有隔离的、独立的进程，这些进程既可以纵向扩展(将更多资源放在同一服务器上)，也可以横向扩展。我在因素 6 中给出的技巧同样适用于这里。

## **9。一次性**

12 因素应用程序可以随时关闭和重新启动，不会给用户体验带来重大负担和损失。

为了实现这一点，您应该关注快速启动和关闭，这允许任何挂起的进程在应用程序关闭之前完成处理。即使在崩溃导致你的网络应用程序意外关闭的情况下，它也应该在再次启动后从停止的地方恢复。

## **在实践中**

例如，可以通过 RabbitMQ 和 AWS SQS 这样的队列在 Node.js 中获得这种行为。您从队列中取出一条消息，只在处理完成后提交它。所以，如果不是因为某些原因，重启应用程序会从队列中再次拾起。

## 10。开发和生产之间的奇偶校验

简而言之，尽可能保持所有环境的平等。我见过的一些最灾难性的部署都是不同背景的错，所以我们在部署前做的所有测试都是无用的，因为最终的环境是不一样的。

## **在实践中**

目前，解决这一问题的一种普遍技术是通过使用 Docker 容器，我们在本地和其他环境中运行将在生产中使用的相同映像，只是配置不同。另一种常见的技术是使用类似 Sequelize 的 ORM 进行迁移，这将很容易保证数据库的奇偶校验。

## **11。日志**

这个因素通常不适用，但应该适用。它说您的日志应该是应用程序中有序事件的流，并且这个流应该被定向到 stdout(标准输出，通常是控制台屏幕)。您想要的任何其他格式必须由环境管理，在您的流中插入一些文件、日志收集器等。

## **在实践中**

因此，在 Node.js 应用程序中，您不应该明确地告诉您的日志要保存到一个文件中，甚至不应该有代码来管理这个日志文件，而是应该允许这个标准的日志输出被一些将处理它们的外部服务捕获。

## **12。管理流程**

最终，您将需要创建管理脚本来调整数据库、将数据导入应用程序、将旧数据处理成新格式，等等。

这些管理脚本，即使只使用一次，也必须遵循 12 个因素中的几个，如#1、#2、#3、#4、#10 和#11。

Node.js 等技术受益于 REPL 工具，无需上传应用程序即可运行管理脚本。不过，在必要的时候，遵循第 7 个因素，这样脚本就是一个自包含的应用程序，不需要特定于 web 的服务器来运行它。

*更多内容请看*[***plain English . io***](https://plainenglish.io/)*。报名参加我们的* [***免费周报***](http://newsletter.plainenglish.io/) *。关注我们关于*[***Twitter***](https://twitter.com/inPlainEngHQ)[***LinkedIn***](https://www.linkedin.com/company/inplainenglish/)*[***YouTube***](https://www.youtube.com/channel/UCtipWUghju290NWcn8jhyAw)*[***不和***](https://discord.gg/GtDtUAvyhW) *。***