---
title: Blender 5 — 渲染 Rendering
date: 2022-01-26 03:54:00 +0800
categories: [Notes, Blender]
tags: [Blender]
img_path: /assets/img/Blender/Blender-5
---



### **相机视图 Camera View**

若想快速定位相机，可先在视窗调整到想要的位置。

随后按下组合键Ctrl+Alt+Numpad 0，或是View > Align View > Align Active Camera to View点击即可。 

---

### **渲染引擎 Render Engine**

渲染引擎可以在**渲染属性（Render Properties）**中找到。

#### **Eevee渲染引擎**

渲染效率高，不包含光线追踪。

![](eevee-before-settings.png){: style="border-radius: 5%"}

以上是**Eevee渲染引擎的原始渲染图**，可见由于Eevee渲染引擎不包含光线追踪，因此在实时渲染时会产生不真实的阴影。

为了优化Eevee渲染引擎的阴影渲染效果，可以在**光线物体的数据属性（Object Data Properties）**里，调整**阴影（Shadow）里的偏移数值（Bias）**。同时为了优化**阴影的细腻度**，可到**渲染属性（Render Properties）**中，提高阴影里的**矩形尺寸（Cube Size）**。

![img-description](eevee-after-shadows.png){: style="border-radius: 5%"}

以上是**调整了偏移数值及提高矩形尺寸后的渲染图**。

为了实现较为真实的阴影渲染效果，可以在**渲染属性（Render Properties）**里开启**环境光遮蔽（Ambient Occlusion）**。

![img-description](eevee-after-ao.png){: style="border-radius: 5%"}

以上是**开启环境光遮蔽后的渲染图**。

---

#### **Cycles渲染引擎**

渲染时间长，包含光线追踪。

![](cycle.png){: style="border-radius: 5%"}

以上是**Cycle渲染引擎的原始渲染图**，可见此渲染引擎所渲染出的图效果极佳，但需花费较长的渲染时间。

---

### **Sample采样**

采样次数越高，渲染图中的物体就越清晰。
