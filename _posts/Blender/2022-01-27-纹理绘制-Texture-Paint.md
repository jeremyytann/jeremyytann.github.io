---
title: 纹理绘制 Texture Paint
date: 2022-01-27 17:04:00 +0800
categories: [Notes, Blender]
tags: [Blender]
img_path: /assets/img/Blender/Blender-8
---

若想手动给物体表面材质上色，可以先到**阴影模式（Shading）**里添加一个**图像纹理（Image Texture）**，然后新建一个图像，再到**纹理绘制模式（Texture Paint）**中进行绘制即可。在新建图像中，**宽度（Width）及高度（Height）并非越大越好**。

> 值的大小会间接影响渲染时长，因此根据场景选择适当的宽高度即可。

纹理绘制完毕之后，只需要将该节点的**颜色（Color）**连接到**原理化BSDF（Principled BSDF）**的**基础色（Base Color）**，就可以将纹理贴到物体表面了。

![](after-texture-paint.png){: style="border-radius: 5%"}

以上为**完成纹理绘制的渲染图**。

<br>

![](screenshot.png){: style="border-radius: 5%"}

![](screenshot-1.png){: style="border-radius: 5%"}

以上为**甜甜圈贴上纹理的实际操作界面**，以供参考。
