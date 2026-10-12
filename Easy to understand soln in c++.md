## 01. Easy to understand soln in c++.....

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/binary-search-1587115620/1)

### Problem Description

**Task:** Given a sorted array arr[] and an integer k, find the position(0-based indexing) at which k is present in the array using binary search. If k doesn't exist in arr[] return -1.

> **Note:** If multiple occurrences are there, please return the smallest index.

#### Examples

##### Example 1

- **Input:**
```text
arr[] = [1, 2, 3, 4, 5], k = 4
```
- **Output:**
```text
3
```
- **Explanation:** 4 appears at index 3.

##### Example 2

- **Input:**
```text
arr[] = [11, 22, 33, 44, 55], k = 445
```
- **Output:**
```text
-1
```
- **Explanation:** 445 is not present.

##### Example 3

- **Input:**
```text
arr[] = [1, 1, 1, 1, 2], k = 1
```
- **Output:**
```text
0
```
- **Explanation:** 1 appears at index 0.

#### Constraints

- **1.** `1 ≤ arr.size() ≤ 10⁵¹ ≤ arr[i] ≤ 10⁶¹ ≤ k ≤ 10⁶`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(log n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-06-16 20:05:38
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public int firstSearch(int[] arr, int k) {
        // Code Here
         int n = arr.length;
        int low = 0;
        int hi = n-1;
        int idx = -1;
        while(low<=hi){
            int mid = (low+hi)/2;
            if(arr[mid]<k)     low = mid+1;
            else if(arr[mid]>k)    hi = mid-1;
            else{
                idx = mid;
                hi = mid-1; 
            }
        }
        return idx;
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-06-16 19:46:11
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public int firstSearch(int[] arr, int k) {
        // Code Here
        int n = arr.length-1;
        int j = n;
        int i = 0;
        int idx = -1;
        while(i<=j){
            int mid = (i+j)/2;
            if(arr[mid]>k) {j = mid-1;}
            else if(arr[mid]<k){ 
                i = mid+1;}
            else{
                // arr[mid]==k;
                idx = mid;
                j = mid - 1;
            }
        }
        return idx;
    }
}
```

*Generated on: 10/12/2026, 9:24:23 PM*