---
title: UML Class Diagram
date: 2022-07-23 18:55:00 +0800
categories: [Notes, Object-Oriented Programming]
tags: [Object-Oriented Programming, UML]
img_path: /assets/img/OOP/UML
---

## **UML Class Notation**

---

A class represents a concept that encapsulates state (attributes) and behavior (operations). Each **attribute has a type** and each **operation has a signature**.

The **class name is the only mandatory information**.



### **Class Name**

- The name of the class appears in the **first partition**.



### **Class Attributes**

- Attributes are shown in the **second partition**.
- The attribute type is shown after the colon.
- Attributes map onto member variables (data members) in code.



### **Class Operations (Methods)**

- Operations are shown in the **third partition**. They are **services the class provides**.
- The return type of a method is shown after the colon at the end of the method signature.
- The return type of method parameters is shown after the colon following the parameter name. Operations map onto class methods in code.



### **Class Visibility**

`+` **public** attributes or operations

`-` **private** attributes or operations

`#` **protected** attributes or operations



### **Parameter Directionality**

`in` passed to the method by the caller

`inout` passed to the method by the caller, and possibly modified by the method and is passed back

`out` not set by the caller but is modified by the method, and is passed back out



## **Relationships between classes**

---

### **Inheritance / Generalization**

A generalization is a taxonomic relationship between a more general classifier and a more specific classifier. Each instance of the specific classifier is also an indirect instance of the general classifier. Thus, the specific classifier inherits the features of the more general classifier.

<img src="Inheritance.drawio.png" style="zoom:90%;" />

The relationship is **displayed as a solid line with a hollow arrowhead** that points from the child element to the parent element.

- It represents an **"is-a" relationship**.
- An abstract class name is shown in italics.
- **SubClass1** and **SubClass2** are **specializations of SuperClass**.



### **Association**

Associations are **relationships between classes** in a UML Class Diagram. 

<img src="Association.drawio.png" style="zoom:90%;" />

The relationship is **displayed as a solid line between classes**.

`Simply Association`

It is a **structural link** between two peer classes.

- There is an **association between Class1 and Class2**.

`Cardinality`

Cardinality is expressed in terms of:

- one-to-one
- one-to-many
- many-to-many



### **Aggregation**

Aggregation is **a special type of association**. 

<img src="Aggregation.drawio.png" style="zoom:90%;" />

The relationship is **displayed as a solid line with an unfilled diamond at the association end**, which is connected to the class that represents the aggregate.

- It represents a **"part of" relationship**.
- **Class2 is part of Class1**, many instances of Class2 can be associated with Class1.
- Objects of two classes **have separate lifetimes**.



### **Composition**

Composition is **a special type of aggregation** where **parts are destroyed when the whole is destroyed**. 

<img src="Composition.drawio.png" style="zoom:90%;" />

The relationship is **displayed as a solid line with a filled diamond at the association end**, which is connected to the class that represents the whole or composite.

- Objects of two classes **live and die together**.
- Class2 **cannot stand by itself**.



### **Dependency**

Dependency is **a special type of association** where **an object of one class might use an object of another class in the code of a method**. If the object is not stored in any field, then this is modeled as a dependency relationship. 

<img src="Dependency.drawio.png" style="zoom:90%;" />

The relationship is **displayed as a dashed line with an open arrow**.

- Exists between two classes if changes to the definition of one may cause changes to the other.
- **Class1 depends on Class2**.



### **Realization**

Realization is a relationship between the blueprint class and the object containing its respective implementation level details. This object is said to realize the blueprint class. In other words, it is the **relationship between the interface and the implementing class**. 

<img src="Realization.drawio.png" style="zoom:90%;" />

The relationship is **displayed as a dashed line with a hollow arrowhead** that points from the class element to the interface element.



## **References**

---

- <https://www.visual-paradigm.com/guide/uml-unified-modeling-language/uml-class-diagram-tutorial/>
- <https://blog.csdn.net/weixin_44691608/article/details/117972671>