---
title: Advanced Dart
date: 2022-08-30 12:45:00 +0800
categories: [Notes, Dart]
tags: [Dart]
img_path: /assets/img/Dart
---

## **Async & Await**

---

The **async** and **await** keywords provide a declarative way to define asynchronous functions and use their results.



### **Async**

Async functions **always return a promise**. 

To define an async function, **add async before the function body.**

`Asynchronous Task` is a task that whose **results are not returned immediately**.



### **Await**

Await expressions make promise-returning functions behave as though they are synchronous by **suspending execution until the returned promise is fulfilled or rejected**.

`Await` keyword is only valid inside async functions.



##  **Extensions**

---

Extensions allow **adding logic to existing classes**.

``` dart
class Person {
  final String firstName;
  final String lastName;
	
  // constructor
  Person(this.firstName, this.lastName);
}

extension FullName on Person {
  String get fullName => '$firstName $lastName';
}

void call() {
  final person = Person('Noname', 'Unknown');
  print(person.fullName);	// prints Noname Unknown
}
```



## **Future**

---

Future is **a class type for the data to be returned in the future**.

``` dart
Future<int> multipleTwo(int number) {
  return Future.delayed(const Duration(seconds: 3), () {
    return number * 2;
  });
}

// async marks this function as asynchronous,
// can be used to wait for the result of another function
void call() async {
  // await can be used to wait for the result of another function
  final result = await multipleTwo(2);
  print(result); // prints 4 after 3 seconds
  
  // another way to write the above code
  multipleTwo(10).then((value) => print(value));
}
```



## **Generator**

---

Generators in Dart allows the user to **produce a sequence of value easily**.



### **Synchronous Generator**

The synchronous generator **returns an iterable object** that can be accessed sequentially.

To implement synchronous generator function, mark the function body as **sync***, and **use yield statements to deliver values**.

``` dart
Iterable<int> getNums() sync* {
  yield 1;
  yield 2;
  yield 3;
}

void call() {
  for (final value in getNums()) {
    print(value);	// prints 1, 2, 3
  }
}
```



### **Asynchronous Generator**

The asynchronous generator **returns a stream object**. A stream provides a way to receive a sequence of events.

To implement an asynchronous generator function, mark the function body as **async***, and **use yield statements to deliver values**.

``` dart
Stream<Iterable<int>> getNums() async* {
  yield [1, 2, 3];
  yield [4, 5, 6];
  yield [7, 8, 9];
}

void call() async {
  await for (final value in getNums()) {
    print(value);	// prints 1, 2, 3
  }
}
```



## **Stream**

---

Streams **provide an asynchronous sequence of data**.

``` dart
Stream<String> printTest() {
  return Stream.periodic(const Duration(seconds: 1), (value) {
    return 'Test';
  });
}

void call() async {
  await for (final value in printTest()) {
    print(value); // print Test every second
  }
}
```



## **References**

---

- https://dart.dev/codelabs/async-await
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function
- https://www.geeksforgeeks.org/generators-in-dart/