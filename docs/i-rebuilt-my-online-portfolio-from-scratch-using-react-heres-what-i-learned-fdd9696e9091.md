# 我用 React 从头开始重建了我的在线作品集——以下是我学到的东西

> 原文：<https://javascript.plainenglish.io/i-rebuilt-my-online-portfolio-from-scratch-using-react-heres-what-i-learned-fdd9696e9091?source=collection_archive---------13----------------------->

![](img/76eefadb720ee3fda0876c6e7aa2e128.png)

Photo by [Andrew Neel](https://unsplash.com/@andrewtneel)

当谈到专业的在线投资组合时，人们很容易认为只有特定类型的人需要有一个。例如，可能有一个摄影师想要一个网站在线展示他们的作品。这是有道理的，因为摄影师通常有一个真实的照片组合展示给世界。然而，时代变了。现在，无论你是谁或做什么，拥有一个在线作品集都是有意义的。根据我的经验，拥有一个在线投资组合是非常有益的。作为一名软件工程师，我刚刚建立了一个新的，定制的来展示我的工作和兴趣。为了构建这个站点，我使用了[React](https://reactjs.org/)+[React Bootstrap](https://react-bootstrap.github.io/)，并使用 [Netlify](http://netlify.com) 部署它。这是一篇关于一般过程和经验教训的文章！

## 为什么要制作在线作品集？

在线作品集是人们用大量细节和创意描述他们的经历和兴趣的完美方式。因此，在线作品集与简历或 Linkedin 个人资料的目的不同，这两者本质上都有可用空间、可接受格式和总体表达自由方面的限制。

制作自己的在线作品集有几种选择。对大多数人来说有意义的一个选择是使用“无代码”网站构建器，如 [Wix](https://www.wix.com/) 或 [Squarespace](https://www.squarespace.com/) ，它们有大量的个人网站模板。一旦建成，你通常可以免费发布这些网站，或者每月支付一点额外的费用来使用特定的域名。另一个选择，我认为非常好，就是使用[概念](https://www.notion.so/)创建一个公共页面。这是另一个无代码和免费的路线，但结果可能会比 Wix 或 Squarespace 看起来更不像网站。然而，这没那么重要。真正重要的是，你在网站中包含的内容简单、清晰，并且符合你希望它达到的目的。

我选择的选项需要做的工作最多，但仍然是免费的，让我对在线投资组合的外观和行为有绝对的自由。也就是说，我从头开始编写我的网站。根据我的具体情况，通过自定义代码来建立一个网站，因为作为一名软件工程师，我想要一个不言自明的在线投资组合。这只是另一个准确展示我的工程技能的机会，而且对我来说是很好的练习。

很多年前，我建立了自己的第一个在线作品集。我使用了普通的 HTML、CSS 和 JavaScript，以及前端工具包引导程序。我在 [Glitch](https://glitch.com/) 中构建了它，这是一个应用创建平台，在那个时候还是相当新的。我相信个人网站在我的项目、我写的文章等方面传达了正确的信息，但在本质上，还有很大的改进空间。当时，我还在学习 web 开发最佳实践。作为一名工程师，从那以后我走过了漫长的道路。不可避免地，是投资组合*重生*的时候了。

## 创建新的投资组合

为了从头开始重建我的在线投资组合，我决定使用 React。React 是一个现代的、流行的 web 库，对可重用性和组件的强调将允许我在幕后很好地组织这个站点。而且有了 [Create React App](https://create-react-app.dev/) ，很容易快速启动一个新的网站进行开发。

为了设计和美观，我使用了 React Bootstrap，一个现代的 CSS 框架。这是专门针对 React 的 Bootstrap 的解释，它主要利用定制组件来轻松创建元素。因此，在使用这个框架时，重点更多地放在了特定的标记名上，而不是所有的属性上。

这个基础本身已经是我旧作品集的一个改进，因为旧网站只使用了普通的网络语言和基本的引导程序。这种原始的方法没有利用任何高级的库或框架，公平地说，今天可用的这些工具中的一些甚至真的不存在，或者在当时并不流行。

## 新方法的好处

随着我继续开发这个网站，我发现了几个好处。帮助我节省了大量开发时间的 React Bootstrap 组件包括容器、行、列、卡片、按钮组、按钮工具栏和按钮。例如，这些组件允许我利用网格系统来展示我已经完成的项目。此外，使用这些组件有助于确保投资组合将是移动友好的。

我简化新站点代码的另一种方法是将我的内容作为 JSON 对象写在一个特定的文件中，然后利用组件中的 JavaScript 映射列出这些对象。我刚刚创建了一个包含 JSON 的 utils 文件，其中包含了我的项目、文章、书籍推荐等信息。，创建类似“get”的函数来返回这些对象，然后导出这些函数供组件访问。这与我的旧网站有很大的不同，我的旧网站实际上是将拷贝和代码混合在一起，并在一个巨大的列表中包含每一项的内容。唷！

映射 JSON 对象的方法有几个好处。首先，它允许我尽可能接近地模拟从数据库而不是在代码本身中访问有关项目、文章等信息的情况。如果将来我想创建一个数据库、管理网站和/或 CMS 集成来提升我的在线投资组合，这种结构将使过渡更加无缝。我使用的“get”函数基本上模仿了简单的 fetch 函数，这就是我包含这些函数的原因(因为乍一看，包含它们似乎很愚蠢)。在 JSX 完成的映射允许我显示这些内容，随着我从事更多的项目、写更多的文章等等，这些内容肯定需要是动态的。事实上，为了给站点添加新的内容，我需要做的就是在 JSON 中添加新的内容。我可以做到这一点，而不需要编辑核心 React 代码，DOM 中呈现的内容会自行处理。

为了给这个站点添加额外的特色，我写了一些自己定制的 CSS 来添加 React Bootstrap。这包括通过使用关键帧在一些容器中添加动画颜色渐变，以及添加大量缩放变换效果。我甚至创建了一个颜色随机函数，用来给一些元素添加内嵌背景样式，这意味着每次访问网站时，网站的颜色都是随机的。尽管存在重复颜色的风险，这可以通过添加更多颜色选项的随机发生器来改善，但这使网站更有趣。所有这些变化都改善了总体用户体验。我甚至把链接按钮做得更加丰富多彩，互动性更强，而非链接按钮是灰色的，互动性更差。

我当然也利用了可重用组件。例如，我这样做是为了我所谓的“媒体”推荐。更具体地说，我推荐一个书单和一个播客列表，放在不同的部分，但是在我的文件夹里，我知道这些部分看起来几乎是一样的。因此，我为所有这些部分创建了一个可重用的组件，并简单地在父(应用程序)级别将内容作为道具传入。这有助于避免大量重复代码！

## 发布作品集

尽管作品集已经完成，并且在我的本地环境下看起来不错，但我需要将它发布给全世界。我考虑的两个选项是 [Github Pages](https://pages.github.com/) 、Netlify 和 [Vercel](https://vercel.com/dashboard) 。这些选项中的每一个都使 React 应用部署成为一种流畅的体验，但我出于个人原因选择了 Netlify。我想获得更多探索网络生活的经验。Netlify 拥有许多好处，这里列出了。我还想要一个相当短的免费域名，我知道 Netlify 能够提供。

Netlify 使得部署静态网站变得非常容易，下面是它如何为我工作的。我创建了一个 Netlify 帐户，将它链接到我的 [Github](https://github.com/) 帐户，然后在 Netlify 中创建了一个新项目。然后，在我的 React 应用程序中，我运行“npm run build”命令来创建一个构建文件夹。该命令将站点的可部署版本放入单个文件夹中。然后，在新 Netlify 项目的 deploy 部分，我简单地用 Finder(我在 mac 上)打开构建文件夹，并将其拖放到 Netlify 中。就这样，网站被部署了。在站点设置下，我编辑了站点名称，使网络域名更接近我想要的名称。

哦，如果你不想每次都用拖放的方式，还有一个简单的方法。您可以在 Github repo 中设置代码，并将该 repo 连接到 Netlify。您可以对其进行设置，以便每次向 repo 提交新代码时，Netlify 都会自动构建和部署这些更改。如果你不想使用你的 CLI 与 Github repo 交互，我推荐使用 Github Desktop 作为 GUI。

然后，新的在线作品集上线了！每当我对我的投资组合进行更改时，我可以只在本地进行，并创建一个新的构建文件夹来拖到 Netlify 中。我自己不需要通过 Github 做任何事情，如果我选择了 Github Pages 路线，事情会有所不同。

## 未来的考虑

我喜欢想办法改进我的投资组合。我的一个想法是加入更多项目证据的视觉效果，尤其是那些不再在网上发布的项目。这种情况的一个示例解决方案是显示不再在 app store 上的应用程序的徽标或屏幕截图。我确信，在未来几年的迭代中，我有许多其他方法可以使投资组合变得更好。我会考虑的。

我希望这能让你深入了解使用 React 构建定制在线投资组合的过程，以及这次经历的主要收获。

非常感谢你的阅读！

*更多内容看* [*说白了. io*](http://plainenglish.io/) *。报名参加我们的* [*免费每周简讯*](http://newsletter.plainenglish.io/) *。在我们的* [*社区*](https://discord.gg/GtDtUAvyhW) *获得独家写作机会和建议。*