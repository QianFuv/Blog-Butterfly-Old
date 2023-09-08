---
abbrlink: 5b5c4441
categories: []
date: '2023-09-08T15:45:39.330899+08:00'
tags: []
title: C4 Model介绍
updated: 2023-9-8T16:24:48.284+8:0
---
# C4 Model - C4模型

> 请向建筑行业的专业人士询问如何通过视觉手段传达建筑物的结构，你会得到场地平面图、楼层平面图、立面图、剖面图和详细图纸。相比之下，如果要求软件开发者使用图表来传达软件系统的架构，则很可能会得到一堆混乱不清的方框和线条……符号不统一（颜色编码、形状、线型等）、命名模糊、关系未标注、术语普遍化以及缺失技术选择和抽象混杂等问题。作为一个行业，我们确实有统一建模语言（UML）、ArchiMate和SysML，但问这些是否提供了有效的软件架构沟通方式往往是无关紧要的，因为许多团队已经放弃它们而转向更简单的“盒子和线条”图表。放弃这些建模语言是一回事，但或许在追求敏捷性的过程中，许多软件开发团队失去了视觉沟通能力。

# 简介

## 什么是C4模型？

- 一组抽象的分层，包括软件系统（systems）、容器（containers）、组件（components）和代码（code）。
- 一组分层图表，包括系统上下文（context）、容器（containers）、组件（components）和代码（code）。
- 与符号和工具无关

C4模型被创建出来是为了帮助软件开发团队描述和沟通软件架构，无论是在前期设计会议中还是在回顾现有代码库时。它可以以与使用Google地图缩放感兴趣的区域相同的方式，在不同层次的细节上创建您代码的地图。

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
