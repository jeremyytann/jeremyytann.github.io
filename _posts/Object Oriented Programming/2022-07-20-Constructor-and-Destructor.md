---
title: Constructor and Destructor
date: 2022-07-20 17:36:00 +0800
categories: [Notes, Object-Oriented Programming]
tags: [Object-Oriented Programming]
img_path: /assets/img/OOP/OOP-3
---

## **Constructor**

---

A constructor is **a member function of a class** that has the same name as the class name. It **helps to initialize the object of a class**.

It can either accept the arguments or not. It is **used to allocate the memory to an object of the class**. It is **called whenever an instance of the class is created**. It can be defined manually with arguments or without arguments.

There **can be many constructors in a class**. It **can be overloaded with differing parameters**.



## **Destructor**

---

Like a constructor, destructor is also a member function of a class that has the same name as the class name, but it is **preceded by a tilde(~) operator** in C++. It **helps to deallocate the memory of an object**.

It is **called while the object of the class is freed or deleted**. In a class, there is always a single destructor without any parameters. So, it **cannot be overloaded**. 

It is always **called in the reverse order of the constructor**. If a class is inherited by another class and both the classes have a destructor, then the destructor of the child class is called first, followed by the destructor of the parent or base class.



## **Implementation**

---

### **Code**

``` cpp
class Object {
public:
    string name;

    // constructor
    Object(string name) {
        this->name = name;
        cout << name << " constructor called." << endl;
    }

    // destructor
    ~Object() {
        cout << name << " destructor called." << endl;
    }
};

int main() {
    Object one("one");  // constructor called

    while (true) {
        Object two("two");  // constructor called
        break;
    }   // destructor called for two
}   // destructor called for one
```

### **Output**

``` cpp
one constructor called.
two constructor called.
two destructor called.
one destructor called.
```



## **References**

---

- <https://www.geeksforgeeks.org/difference-between-constructor-and-destructor-in-c/>
- <https://en.wikipedia.org/wiki/Constructor_(object-oriented_programming)>
- <https://en.wikipedia.org/wiki/Destructor_(computer_programming)>