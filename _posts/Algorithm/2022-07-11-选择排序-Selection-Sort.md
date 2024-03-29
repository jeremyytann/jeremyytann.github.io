---
title: 选择排序 Selection Sort
date: 2022-07-11 16:04:00 +0800
categories: [Notes, Algorithm]
tags: [Algorithm, Sorting]
img_path: /assets/img/Algorithm/Algorithm-4
katex: true
---

## **选择排序简介**

---

选择排序的基本思想是，在未排序的数列中找到最小或最大的元素，将其存放在数列的起始位置。

接着，再从剩余未排序的元素中继续寻找最小或最大的元素，逐个放到已排序数列的末尾。

以此类推，直到所有元素均排列完毕。



## **选择排序实现**

---

下面以数列 {20,40,30,10,60,50} 为例，演示选择排序的过程。

![](selection-sort.jpeg)

第一趟，i = 0。此时，找到最小值 a[3] = 10，并将其与 a[0] 交换位置，数列变为 {10,40,30,20,60,50}。

第二趟，i = 1。此时，找到最小值 a[3] = 20，并将其与 a[1] 交换位置，数列变为 {10,20,30,40,60,50}。

第三趟，i = 2。此时，找到最小值 a[2] = 30。由于已处在正确位置，因此不做任何处理。

第四趟，i = 3。此时，找到最小值 a[3] = 40。由于已处在正确位置，因此不做任何处理。

第五趟，i = 4。此时，找到最小值 a[5] = 50，并将其与 a[4] 交换位置，数列变为 {10,20,30,40,50,60}。



## **复杂度与稳定性**

---

### **选择排序时间复杂度**

选择排序的时间复杂度是 $O(N^2)$。

假设要被排序的数列中有 N 个数，遍历一趟的时间复杂度为 $O(N)$。

由于算法需要遍历 N-1 次，因此选择排序的时间复杂度为 $O(N^2)$。



### **选择排序稳定性**

使用**数组实现**的选择排序是**不稳定**的，而用**链表实现**的选择排序则是**稳定**的。



## **代码实现**

---

**输入：**arr 为要排序数列，n 为数列的元素个数

``` cpp
void selectionSort(int* arr, int n) {
  int i, j, min, temp;
  
  for (i = 0; i < n; i++) {
    min = i;
    
    for (j = i + 1; j < n; j++) {
      if (arr[j] < arr[min]) {
        min = j;
      }
    }
    
    if (min != i) {
      temp = arr[i];
      arr[i] = arr[min];
      arr[min] = temp;
    }
  }
}
```



## **参考文章**

---

- <https://www.cnblogs.com/skywang12345/p/3597641.html>
- <https://pdai.tech/md/algorithm/alg-sort-x-select.html>

