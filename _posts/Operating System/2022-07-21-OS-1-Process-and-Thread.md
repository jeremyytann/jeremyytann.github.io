---
title: OS 1 — Process and Thread
date: 2022-07-21 15:45:00 +0800
categories: [Notes, Operating System]
tags: [Operating System]
---

## **Process**

---

A process is an **instance of a computer program in execution state** along with **all the necessary information required** for its proper execution, like program counter, CPU registers, its activation state, memory security and management information etc. 

A process can create other processes which are known as **Child Processes**.

The process **takes more time to terminate** and it is **isolated**, means it **does not share the memory with any other process**.



### **States of Process**

`New`, `Ready`, `Running`, `Waiting`, `Terminated`, and `Suspended`



## Thread

---

A thread is a **lightweight and efficient process** that can be **managed independently by a scheduler**. A process can contain multiple threads. The idea is to achieve **parallelism** by dividing a process into multiple threads.

The thread **takes less time to terminate** as compared to the process but A thread **shares information** like data segment, code segment, files etc. **with its peer threads** while it contains its own registers, stack, counter etc.



### **Types of Thread**

`User Level Thread`

- User threads are **implemented by users**.
- Operating System **does not recognize** user level threads.
- Implementation of User threads is **easy**.
- **Context switch time is less**, and **requires no hardware support**.
- If one **user level thread performs blocking operation**, then **entire process will be blocked**.
- User level threads can be **created and managed more quickly**.
- **Any operating system can support** user level threads.

`Kernel Level Thread`

- Kernel threads are **implemented by Operating System**.
- Kernel threads are **recognized** by Operating System.
- Implementation of Kenel thread is **complicated**.
- **Context switch time is more**, and **hardware support is needed**.
- If one **kernel thread perform blocking operation**, then **another thread can continue execution**.
- Kernel level threads **take more time to create and manage**.
- Kernel level threads are **operating system-specific**.



### **States of Thread**

`Running`, `Ready`, and `Blocked`



## **Advantages of Thread over Process**

---

`Responsiveness`

If the process is divided into multiple threads, if **one thread completes its execution**, then its **output can be immediately returned**.

`Faster context switch`

**Context switch time between threads is lower** compared to process context switch as **threads are lighter than processes**.

`Effective utilization of multiprocessor system`

If we have multiple threads in a single process, then we can **schedule multiple threads on multiple processes**. This will **make process execution faster**.

`Resource sharing`

Resources like code, data, and files can be **shared among all threads within a process**.

`Communication`

Communication between multiple threads is easier, as the **threads shares common address space**. While in process, we have to follow some specific communication technique for communication between two process.

`Enhanced throughput of the system`

If a process is divided into multiple threads, and each thread function is considered as one job, then the **number of jobs completed per unit of time is increase**, thus increasing the throughput of the system.



## **References**

- <https://www.geeksforgeeks.org/difference-between-process-and-thread/>
- <https://www.tutorialspoint.com/difference-between-process-and-thread>
- <https://www.geeksforgeeks.org/thread-in-operating-system/>
- <https://www.geeksforgeeks.org/difference-between-user-level-thread-and-kernel-level-thread/>