---
title: Model-View-Controller Pattern
date: 2022-07-23 15:32:00 +0800
categories: [Notes, Software Architecture]
tags: [Software Architecture]
---

## **Model-View-Controller (MVC)**

---

The Model-View-Controller (MVC) is an architectural pattern that **separates an application into three main logical components**: the model, the view, and the controller. Each of these components are **built to handle specific development aspects of an application**.



### **Model**

Model is the **central component of the pattern**. It is the application's dynamic data structure, independent of the user interface. It is connected to the database, **directly manages the data, logic and rules of the application**. Adding or retrieving data is done in the model component.



### **View**

**Data representation** is done by the view component. It **generates the user interface for the user**.

Views are created by the data which is collected by the model component but these data are not taken directly but through the controller. So, the **view only speaks to the controller**.



### **Controller**

Controller is the component that **enables the interconnection between the views and the model**. It **responds to the user input** and **performs interactions on the data model objects**.

The controller does not have to worry about handling data logic, **it just tells the model what to do**. After receiving data from the model, it **processes them and sends all the information to the view**, and **explains how to represent it to the user**.



## **Advantages of MVC**

---

- MVC architecture will **separate the user interface from business logic**.
- Components are **reusable**, and **easy to maintain**.
- **Different components** of the application in MVC can be **independently deployed and maintained**.



## **Disadvantages of MVC**

---

- The **complexity is high**.
- It is **not suitable for small applications**.
- The **inefficiency of data access** in view.



## **References**

- <https://towardsdatascience.com/everything-you-need-to-know-about-mvc-architecture-3c827930b4c1>
- <https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller>
