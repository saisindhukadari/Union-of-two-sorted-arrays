# Union of Two Sorted Arrays 

## Problem Statement

Given two **sorted arrays** `arr1` and `arr2` of sizes `n` and `m`, print the **union** of the two arrays.

The **union** contains all elements from both arrays in sorted order. If an element is present in both arrays, it is printed only once for that occurrence where both pointers meet.

---

## Approach

This solution uses the **Two Pointer Technique**.

* Initialize two pointers:

  * `i` for `arr1`
  * `j` for `arr2`
* Compare the current elements of both arrays:

  * If `arr1[i] < arr2[j]`, print `arr1[i]` and move `i`.
  * If `arr1[i] > arr2[j]`, print `arr2[j]` and move `j`.
  * If both elements are equal, print one of them and move both pointers.
* After one array is completely traversed, print the remaining elements of the other array.

---

## Algorithm

1. Read `n` and `m`.
2. Read the elements of both sorted arrays.
3. Set `i = 0` and `j = 0`.
4. Compare elements using two pointers.
5. Print the smaller element and move the corresponding pointer.
6. If both elements are equal, print once and move both pointers.
7. Print the remaining elements from either array.
8. End.

---

## Example

### Input

```text
5 5
1 2 3 4 5
2 3 4 4 5
```

### Output

```text
1 2 3 4 4 5
```

---

## Time Complexity

* **O(n + m)**

Each element is visited at most once.

---

## Space Complexity

* **O(1)**

No extra data structure is used apart from the input arrays.

---

## Concepts Used

* Arrays
* Two Pointer Technique
* Sorting
* Linear Traversal

---

## Note

This implementation assumes the input arrays are already sorted.

It **does not remove duplicate values within the same array**. For example, if `arr2` contains duplicate `4`s, both may appear in the output. To produce a mathematical union (only distinct elements), additional duplicate-checking logic is required.
