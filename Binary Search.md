## 01. Binary Search

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/who-will-win-1587115621/1)

### Problem Description

**Task:** Given an array arr[], sorted in ascending order and an integer k. Return true if k is present in the array, otherwise, false.Examples:Input: arr[] = [1, 2, 3, 4, 6], k = 6

#### Examples

##### Example 1

- **Output:**
```text
false1 ≤ arr[i] ≤ 10⁶
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(log n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-06-16 19:27:52
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public boolean binarySearch(int[] arr, int k) {
        // code here
        int n = arr.length;
        int low =0;
        int hi = n-1;
        while(low<=hi){
           int  mid = (hi+low)/2;
            if(arr[mid]==k) return true;
            else if (arr[mid]<k)    low = mid+1;
            else if(arr[mid]>k)     hi = mid -1;
            
            
        }
        return false;
        
    }
}
```

*Generated on: 10/12/2026, 9:25:04 PM*