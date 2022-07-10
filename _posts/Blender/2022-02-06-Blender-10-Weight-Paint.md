---
title: Blender 10 — 权重绘制 Weight Paint
date: 2022-02-06 18:23:00 +0800
categories: [Notes, Blender]
tags: [Blender]
img_path: /assets/img/Blender/Blender-10
---

权重绘制（Weight Paint），是在物体表面上绘制权重，权重图中的**颜色由蓝到红分别表示着0到1之间的值**。这里使用绘制权重的原因是为了让甜甜圈表面上的彩色糖只出现在我们想让它出现的位置，而不是到处都是彩色糖。

在进入权重绘制（Weight Paint）模式后，可以根据需求对**权重（Weight）、半径（Radius）以及强度（Strength）**的调整，在物体表面进行权重绘制。

![](weight-paint.png){: style="border-radius: 5%"}

以上是**我所绘制的权重图**，以供参考。

<br>

绘制完权重后，若想要在实现以上说的让甜甜圈表面上的彩色糖只出现在我们想让它出现的位置，则需要将绘制好的权重图输入到彩色糖的分布上。因此我们需要在**几何节点（Geometry Nodes）**中的**组输入（Group Input）**节点中加入一个输入群组以输入我们的权重图。

在节点界面中按下**n键**可以显示节点的各个信息，在节点群组中加入一个输入群组，并将其**类型（Type）设定浮点（Float）**，这是因为我们的权重图是由0到1的浮点数组成的。

加入此输入群组后，可以到Blender界面右边的**属性栏（Properties）中的修改器属性（Modifier Properties）里**，为刚加入的输入群组设定为我们的权重图。随后将其连接到**分布点于面上（Distributed Points on Faces）节点的密度系数(Density Factor）**中，这样此节点就会根据我们所绘制的权重图，在物体的表面上生成对应的点。

![](before-weight-paint.png){: style="border-radius: 5%"}

以上是**绘制权重图之前甜甜圈的渲染图**。

<br>

![](after-weight-paint.png){: style="border-radius: 5%"}

以上是**绘制权重图，并输入到节点之后甜甜圈的渲染图**，可见甜甜圈表面上的彩色糖是根据先前绘制好的权重图分布的。

<br>

![](final-weight-paint.png){: style="border-radius: 5%"}

以上是**完成输入权重图后的实际操作界面**，可供参考。
