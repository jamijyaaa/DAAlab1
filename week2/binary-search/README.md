# Kth Largest Element in a Stream

## 1. Problem

The task is to find the kth largest number after adding new numbers to the stream.

For example, if `k = 3`, we need to return the 3rd largest number after each `add()`.

## 2. Approach

I used a `PriorityQueue` (min-heap).

When a new number is added, I put it into the heap. If there are more than `k` numbers, I remove the smallest one.

This way, the heap always keeps the `k` largest numbers. The smallest number in the heap is the kth largest number, so I return it using `peek()`.

## 3. Time Complexity

**Time Complexity: O(log k)**

Adding and removing an element from the heap takes `O(log k)` time. The heap contains at most `k` elements.

## 4. Space Complexity

**Space Complexity: O(k)**

The heap stores only `k` elements, so the amount of extra memory depends on `k`.

## 5. Reflection / Improvement

A simpler solution would be to store all numbers and sort them every time. However, that would be slower.

Using `PriorityQueue` is more efficient because I only keep the `k` largest elements.
