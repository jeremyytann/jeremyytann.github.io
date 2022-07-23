---
title: 几何节点 Geometry Nodes
date: 2022-01-27 17:41:00 +0800
categories: [Notes, Blender]
tags: [Blender]
img_path: /assets/img/Blender/Blender-9
---

和**阴影模式（Shading）**一样，**几何节点（Geometry Nodes）**里的**节点（Nodes）**的执行顺序也是**由左到右**的。

### **节点 Node**

这里仅记录我学习过程中有使用到的节点，会随着自己学习使用到的慢慢添加。

<br>

**分布点与面上（Distributed Points on Faces）**— 此节点可在一个面上生成多个点，供其他节点使用。这里使用此节点生成多个点，供之后放置彩色糖的节点使用。

**欧拉旋转（Rotate Euler）**— 此节点可实现物体的旋转。这里使用此节点配合**随机值（Random Value）**节点，随机旋转节点的角度，让每个彩色糖都有不同的放置角度。

**实例化于点上（Instance on Points）**— 此节点可将输入所提供的物体放置到点上。这里将弄好的Cylinder物体输入到此节点的**实例（Instance）**上，让节点将Cylinder物体作为彩色糖实例化于**分布点与面上（Distributed Points on Faces）**节点生成的点上。

**合并几何（Join Geometry）** — 此节点可合并几何节点。

**随机值（Random Value）**— 此节点可生成随机值，供其他节点使用。



<br>

![](final-blender-9.png){: style="border-radius: 5%"}

以上为**完成添加彩色糖物体的渲染图**。

<br>

![](after-adding-nodes.png){: style="border-radius: 5%"}

以上为**甜甜圈添加彩色糖物体**的实际操作界面。
