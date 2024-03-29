---
title: Basics of OOP
date: 2022-07-20 14:24:00 +0800
categories: [Notes, Object-Oriented Programming]
tags: [Object-Oriented Programming]
img_path: /assets/img/OOP/OOP-1
---

## **Object-Oriented Programming**

---

Object-Oriented Programming is a programming paradigm that relies on the concept of **classes** and **objects**. It is used to structure a software program into simple, reusable pieces of code blueprints, which are used to create individual instances of objects.



## **Benefits of OOP**

---

- OOP models complex things as **reproducible, simple structures**
- **Reusable**, as OOP objects can be used across programs
- Allows for **class-specific behavior** through **polymorphism**
- **Easier to debug**, classes often contains all the applicable information to them
- **Secure**, protects information through **encapsulation**



## **Concepts of OOP**

---

### **Classes**

A class is **an abstract blueprint** used to create more specific, concrete objects. Classes often represent broad categories that **share attributes**. These classes define what attributes an instance of this type will have, but not the value of those attributes for a specific object.

Classes can also contain functions, called **methods** available only to objects of that type. These functions are defined within the class and perform some action helpful to that specific type of object.

In a nutshell, classes are essentially **user defined data types**. Classes are where we create a blueprint for the structure of methods and attributes. Individual objects are instantiated, or created from this blueprint.



### **Objects**

Objects are **instances of classes** created with specific data.



### **Attributes**

Attributes are the **information that is stored**. Attributes are defined in the Class template. When objects are instantiated, individual objects contain data stored in the Attributes field.

The **state of an object** is defined by the data in the object's attributes field.



### **Methods**

Methods represent behaviors. Methods **perform actions** that might **return information about an object or update an object's data**. The method's code is defined in the class definition.

When individual objects are instantiated, these objects can call the methods defined in the class.



## **Principles of OOP**

---

The four principles of object-oriented programming are **encapsulation, abstraction, inheritance and polymorphism**.



### **Inheritance**

Inheritance allows classes to inherit features of other classes and it **supports reusability**. If basic attributes and behaviors are defined in a parent class, child classes can be created extending the functionality of the parent class, and adding additional attributes and behaviors.

The **benefits of inheritance** are programs can create a generic parent class, and then create more specific child classes as needed. This simplifies overall programming as child classes automatically gain access to functionalities within their parent class.



### **Encapsulation**

Encapsulation means **containing all important information inside an object**, and **only exposing selected information to the outside world**. Attributes and behaviors are defined by code inside the class template.

When an object is instantiated from the class, the data and methods are encapsulated in that object. Encapsulation hides the internal software code implementation inside a class, and hides internal data of inside objects.

Encapsulation requires **defining some fields as private and some as public**.

`Private/Internal Interface` methods and properties, accessible from other methods of the same class.

`Public/External Interface` methods and properties, accessible also from outside the class.

The **benefits of encapsulation** are:

- **Adds security**, as only public methods and attributes are accessible from the outside.
- **Protects against common mistakes**, as only public fields and methods accessible, so developers will not acidentally change something important.
- **Protects IP**, as code is hidden in a class, only public methods are accessible by the outside developers.
- **Supportable**, as most code undergoes updates and improvements.
- **Hides complexity**, as no one can see what's behind the objects.



### **Abstraction**

Abstraction means that the user interacts with only selected attributes and methods of an object. It uses simplified high level tools, to access a complex object.

Abstraction is **using simple classes to represent complexity**. It is an extension of encapsulation. For example, you don't have to know all the details of how the engine works to drive a car.

Abstraction serves an important security role. By only displaying selected pieces of data, and only allowing data to be accessed through classes and modified through methods, data will be protected from exposure.

The **benefits of abstraction** are:

- Simple, high level user interfaces.
- Complex code is hidden.
- **Adds security**, as data is protected from exposure.
- **Easier software maintenance**, as code updates rarely affect the abstraction.



### **Polymorphism**

Polymorphism means **designing objects to share behaviors**. Using inheritance, objects can override shared parent behaviors, with specific child behaviors. Polymorphism allows the same method to execute different behaviors in two ways: **method overriding and method overloading**.

`Method overriding` **Runtime polymorphism** uses method overriding. In method overriding, a child class can provide a **different implementation than its parent class**.

`Method overloading` **Compile Time polymorphism** uses method overloading. Methods or functions may **have the same name**, but a **different number of parameters passed into the method call**. Different results may occur depending on the number of parameters passed in.

The **benefits of polymorphism** are:

- Objects of different types can be passed through the same interface.
- Method overriding and method overloading.



## **References**

---

- <https://www.educative.io/blog/object-oriented-programming>
- <https://www.freecodecamp.org/news/object-oriented-programming-concepts-21bb035f7260/>