---
abbrlink: 5b5c4441
categories: []
date: '2023-09-08T15:45:39.330899+08:00'
tags: []
title: C4 Model介绍
updated: 2023-9-10T17:28:51.801+8:0
---
# C4 Model - C4模型

> 这篇文章的一些内容需要科学上网才可以浏览，但是没有梯子也不影响整体的阅读和理解。

> 请向建筑行业的专业人士询问如何通过视觉手段传达建筑物的结构，你会得到场地平面图、楼层平面图、立面图、剖面图和详细图纸。相比之下，如果要求软件开发者使用图表来传达软件系统的架构，则很可能会得到一堆混乱不清的方框和线条……符号不统一（颜色编码、形状、线型等）、命名模糊、关系未标注、术语普遍化以及缺失技术选择和抽象混杂等问题。作为一个行业，我们确实有统一建模语言（UML）、ArchiMate和SysML，但问这些是否提供了有效的软件架构沟通方式往往是无关紧要的，因为许多团队已经放弃它们而转向更简单的“盒子和线条”图表。放弃这些建模语言是一回事，但或许在追求敏捷性的过程中，许多软件开发团队失去了视觉沟通能力。

# 简介

## 什么是C4模型？

- 一组抽象的分层，包括软件系统（systems）、容器（containers）、组件（components）和代码（code）。
- 一组分层图表，包括系统上下文（context）、容器（containers）、组件（components）和代码（code）。
- 与符号和工具无关

C4模型是一种“先抽象后具体”的软件架构图表方法，基于反映软件架构师和开发人员思考和构建软件的抽象。少量的抽象和图表类型使得C4模型易于学习和使用。请注意，您不需要使用所有四个层次的图表；只需使用那些增加价值的——系统上下文和容器图表对许多软件开发团队已经足够了。

C4模型被创建出来是为了帮助软件开发团队描述和沟通软件架构，无论是在前期设计会议中还是在回顾现有代码库时。它可以以与使用Google地图缩放感兴趣的区域相同的方式，在不同层次的细节上创建您代码的地图。

可以通过下面的**小组件**体验↓

<!DOCTYPE html>

<html>
<head>
    <title>Embedded Diagram</title>
</head>
<body>
    <iframe id="myEmbeddedDiagram" src="https://structurizr.com/embed/36141?diagram=SystemContext&diagramSelector=true&iframe=myEmbeddedDiagram" width="100%" marginwidth="0" marginheight="0" frameborder="0" scrolling="no" allowfullscreen="true"></iframe>
    <script type="text/javascript" src="https://static.structurizr.com/js/structurizr-embed.js"></script>
</body>
</html>

## 视频介绍

<div style="position: relative; padding-bottom: 56.25%; /* 16:9比例的占位符 */">
  <iframe
    src="https://www.youtube-nocookie.com/embed/x2-rSnhpw0g?si=FOFb0uq9xRC1K4_Z"
    title="YouTube video player"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    allowfullscreen
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
  ></iframe>
</div>

## C4模型的优势和作用在哪里？

C4模型是一种**易于学习、开发人员友好**的软件架构图表方法。良好的软件架构图表有助于在软件开发/产品团队内外进行沟通，**高效地**引入新员工，进行架构审查/评估，风险识别（例如[风险暴露](https://riskstorming.com/)），威胁建模等。

# 抽象定义

> 为了创建您代码的这些地图，我们首先需要一个共同的抽象集来创建一种普遍语言，以便描述软件系统的静态结构。软件系统由一个或多个容器（应用程序和数据存储）组成，每个容器包含一个或多个组件，而这些组件又由一个或多个代码元素（类、接口、对象、函数等）实现。人们可能会使用我们构建的软件系统。

![Abstractions](https://vip2.loli.io/2023/09/10/RO1rxBmflX9A4ZN.png)

## Person - 人

人代表着你的软件系统中的一个人类用户（例如演员、角色、虚拟人物等）。

## Software System - 软件系统

软件系统是最高层次的抽象，描述了为其用户提供价值的东西，无论他们是否为人类。这包括您正在建模的软件系统以及您的软件系统所依赖（或反之）的其他软件系统。在许多情况下，一个软件系统由单个软件开发团队“拥有”。

## Container - 容器

**不是 Docker！**在 C4 模型中，容器代表一个**应用程序**或**数据存储**。容器是需要运行才能使整个软件系统正常工作的东西。实际上，容器就像：

- **服务器端Web应用程序**：在Apache Tomcat上运行的Java EE Web应用程序，运行在Microsoft IIS上的ASP.NET MVC应用程序，在WEBrick上运行的Ruby on Rails应用程序，Node.js应用程序等。
- **客户端Web应用程序**：使用Angular、Backbone.JS、jQuery等在Web浏览器中运行的JavaScript应用程序。
- **客户端桌面应用程序**：使用WPF编写的Windows桌面应用程序，使用Objective-C编写的OS X桌面应用程序，使用JavaFX编写的跨平台桌面应用程序等。
- **移动App**：苹果iOS App、Android App、微软Windows Phone App等。
- **服务器端控制台应用程式**：独立（例如“public static void main”） 应该有一个批处理过程等。
- **无服务器函数**：单个无服务器函数（例如Amazon Lambda、Azure Function等）。
- **数据库**：关系型数据库管理系统中的模式或数据库，文档存储库，图形数据库等，如MySQL、Microsoft SQL Server、Oracle Database、MongoDB  ，Riak, Cassandra, Neo4j 等。
- **Blob或内容存储库**：Blob存储库（例如Amazon S3, Microsoft Azure Blob Storage 等）或内容交付网络(例如Akamai, Amazon CloudFront 等) 。
- **文件系统**：完整本地文件系统或较大网络文件系统(例如SAN,NAS 等) 的一部分. •Shell脚本: 单个Bash Shell脚本等。
- **还有很多**......

容器本质上是一个上下文或边界，用于执行某些代码或存储数据。每个容器都是一个可独立部署/运行的东西或运行时环境，通常（但并非总是）在自己的进程空间中运行。因此，容器之间的通信通常采用进程间通信形式。

## Component - 组件

“组件”这个词在软件开发行业中是一个非常重载的术语，但在这个上下文中，“组件”是指一组相关功能，封装在一个明确定义的接口后面。如果你使用像Java或C#这样的语言，最简单的想法就是将组件视为实现类集合，在接口后面。如何打包这些组件（例如每个JAR文件、DLL、共享库等）是一个独立且正交的问题。

需要注意的重要一点是容器内所有组件通常都在同一个进程空间中执行。**在C4模型中，组件不是可分别部署的单位。**

# 四层模型

## System Context diagram - 系统上下文图

![A System Context diagram](https://vip2.loli.io/2023/09/10/TEpWsNC9neJ7ZS4.png)

![Diagram key](https://vip2.loli.io/2023/09/10/LBa26tnHvYFWs3d.png)

系统上下文图是绘制和记录软件系统的良好起点，它让你能够退后一步看到整体情况。绘制一个图表，将您的系统作为中心盒子，并围绕其用户以及与之交互的其他系统。在这里详细信息并不重要，因为这是您放大查看系统全貌的视角。焦点应该放在人员（演员、角色、人物等）和软件系统上，而不是技术、协议和其他低级别细节。这种类型的图表可以向非技术人员展示。

- **范围**：单个软件系统。
- **主要元素**：在范围内的软件系统。
- **支持元素**：与在范围内的软件系统直接连接的人员（例如用户、演员、角色或虚拟人物）和软件系统（外部依赖项）。通常这些其他软件系统位于您自己的软件系统之外的范围或边界，您不需要对它们负责或拥有所有权。
- **目标受众**：所有人，包括技术和非技术人员，在软件开发团队内外。
- **推荐给大多数团队使用**：是。

## Container diagram - 容器图

![A Container diagram](https://vip2.loli.io/2023/09/10/CNm3wTLKUt5SzuQ.png)

![Diagram key](https://vip2.loli.io/2023/09/10/nbZfOXcWxIKlv9z.png)

一旦您了解了系统如何适应整个IT环境，下一个非常有用的步骤是使用容器图缩小到系统边界。 "容器"类似于服务器端Web应用程序、单页应用程序、桌面应用程序、移动应用程序、数据库模式、文件系统等。基本上，容器是可分别运行/部署的单位（例如独立的进程空间），它执行代码或存储数据。容器图显示软件架构的高级形状以及如何在其中分配责任。它还显示主要技术选择以及容器之间如何通信。这是一个简单且高度关注技术的图表，对软件开发人员和支持/运营人员都很有用。

- **范围**：单个软件系统。
- **主要元素**：在范围内的软件系统中的容器。
- **支持元素**：直接连接到容器的人员和软件系统。
- **目标受众**：软件开发团队内外的技术人员，包括软件架构师、开发人员和运营/支持工作人员。
- **推荐给大多数团队使用**：是。
- **备注**：此图表未涉及集群、负载均衡器、复制、故障转移等内容，因为这些内容可能会因不同环境（如生产、暂存或开发）而异。这些信息最好通过一个或多个部署图来捕获。

## Component diagram - 组件图

![A Component diagram](https://vip2.loli.io/2023/09/10/5aOKpHunw3XDWiA.png)

![Diagram key](https://vip2.loli.io/2023/09/10/UwR8Q4zmXdqPjJE.png)

接下来，您可以放大并进一步分解每个容器，以识别主要的结构建筑块及其相互作用。组件图显示了一个容器由多个“组件”组成，每个组件是什么、它们的职责以及技术/实现细节。

- 范围：单个容器。
- 主要元素：在范围内的容器中的组件。
- 支持元素：软件系统内的容器（以及直接连接到组件的人员和软件系统）。
- 目标受众：软件架构师和开发人员。
- 推荐给大多数团队吗？不，只有当您觉得它们增加了价值，并考虑自动化其创建以进行长期文档记录时才创建组件图。

## Code diagram - 代码图表

![A UML class diagram](https://vip2.loli.io/2023/09/10/xq8OJamup7CtfM2.png)

最后，您可以放大每个组件，展示它如何作为代码实现；使用UML类图、实体关系图或类似的工具。这是一个可选的细节层次，并且通常可以从IDE等工具中按需提供。理想情况下，该图应该使用工具（例如IDE或UML建模工具）自动生成，并且您应该考虑仅显示那些属性和方法，以便讲述您想要讲述的故事。除了最重要或最复杂的组件外，不建议使用此级别的详细信息。

- 范围：单个组件。
- 主要元素：在所涉及的组件内的代码元素（例如类、接口、对象、函数、数据库表等）。
- 目标受众：软件架构师和开发人员。
- 推荐给大多数团队使用吗？不推荐，特别是对于长期存档文件而言，因为大多数集成开发环境可以按需生成此级别的详细信息。
