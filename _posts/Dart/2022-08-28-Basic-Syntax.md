---
title: Basic Syntax
date: 2022-08-28 16:35:00 +0800
categories: [Notes, Dart]
tags: [Dart]
img_path: /assets/img/Dart
---

## **Classes and Methods**

---

`Class`

A class is **an abstract blueprint** used to create more specific, concrete objects.

`Object`

Objects are **instances of classes** created with specific data.

``` dart
class Person {
  void sayHi() {
    print('Hi');
  }
}

void call() {
  final person = Person();
  person.sayHi();
}
```



## **Conditional Property Access**

---

In order to guard access to a property or method of an object that might be null.

`?.` Add a question mark before the dot.

``` dart
List<String>? names = ['Jeremy'];
List<String>? nulls = null;

print(names?.length ?? 0);	// prints 1
print(nulls?.length ?? 0);	// prints 0
```



## **Constructors**

---

`Constructor` is **a member function of a class** that has the same name as the class name. It **helps to initialize the object of a class**.

`Factory Constructors` can **return instances** that are **not of the same class**.

``` dart
class Person {
  final String name;

  // constructor
  Person(this.name);

  // factory constructor
  factory Person.createHuman() {
    return Person('Default');
  }
  
  void printName() {
    print(name);
  }
}

void call() {
  final person = Person.createHuman();
  person.printName();
}
```



## **Operators**

---

### **Custom Operators**

We can define custom operators on your own classes.

`Overriding the == operator`

``` dart
class Person {
  final String name;

  // constructor
  Person(this.name);

  @override
  // covariant force class to ignore type of parameters defined in super class
  bool operator ==(covariant Person other) => other.name == name;

  @override
  // hashCode is the identifier for instances of the class
  int get hashCode => name.hashCode;
}

void call() {
  final person1 = Person('John');
  final person2 = Person('John');
  print(person1 == person2);	// prints true
}
```



### Null Aware Operators

Null aware operators are used to add null aware objects. They are listed below:

`?` Add a question mark after the data type to make it nullable.

``` dart
String? name = null;
```



`??` is used to find the first non-null value.

``` dart
String? value1 = null;
String? value2 = 'A';
String? value3 = 'B';

print(value1 ?? value3 ?? value2);	// prints B
print(value2 ?? value1 ?? value3);	// prints A
```



`??=` is used to assign value to a variable only if the variable is currently null.

``` dart
int? number = null;
number ??= 5;
print(number);	// prints 5

number ??= 10;
print(number);	// still prints 5
```