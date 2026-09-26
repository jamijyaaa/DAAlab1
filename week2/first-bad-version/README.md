# First Bad Version

## 1. Problem

The task is to find the first bad version.

If one version is bad, all versions after it are also bad. We need to find the first bad version with as few checks as possible.

## 2. Approach

I used binary search.

I check the middle version using `isBadVersion()`.

If the version is bad, I search in the left part. If it is good, I search in the right part.

When only one version is left, it is the first bad version.

## 3. Time Complexity

**Time Complexity: O(log n)**

The search area is divided by half after each check.

## 4. Space Complexity

**Space Complexity: O(1)**

I only use a few variables, so no extra memory is needed.

## 5. Reflection / Improvement

A simple solution would be to check all versions one by one. This would take O(n) time.

Binary search is more efficient because it reduces the number of API calls to O(log n).
