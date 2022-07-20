---
title: OOP 2 — Object Copying
date: 2022-07-20 16:05:00 +0800
categories: [Notes, Object-Oriented Programming]
tags: [Object-Oriented Programming]
img_path: /assets/img/OOP/OOP-2
---

In object-oriented programming, object copying is creating a copy of an existing object, a unit of data in object-oriented programming.



## **Methods of copying**

---

There are different strategies for making a copy of an object, referred to as **shallow copy** and **deep copy**.



![](Object-copying.jpeg)



### **Shallow copy**

Shallow copy **stores the references of objects to the original memory address**. It stores the copy of the original object and points the references to the objects. So, it **reflects changes** made to the new or copied object in the original object.

Shallow copy is **simple, fast and efficient**.



### **Deep copy**

Deep copy **stores copies of the object's value**. It stores the copy of the original object and recursively copies the objects as well. So, it **does not reflect changes** made to the new or copied object in the original object.

Deep copy is **comparatively slower and has a cost associated with it**.



## **References**

---

- <https://www.quora.com/What-is-the-difference-between-a-shallow-copy-and-a-deep-copy-in-Java>
- <https://www.baeldung.com/cs/deep-vs-shallow-copy>

