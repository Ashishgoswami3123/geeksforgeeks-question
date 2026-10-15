## 01. Insert at Bottom of Stack

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/insert-an-element-at-the-bottom-of-a-stack/1)

### Problem Description

**Task:** Given a stack st containing n integers and an integer x, insert x at the bottom of the stack.

> **Note:** While displaying the stack, the bottommost element is printed first.

#### Examples

##### Example 1

- **Input:**
```text
st = [4, 3, 2, 1, 8], x = 2
```
- **Output:**
```text
[2, 4, 3, 2, 1, 8]
```
- **Explanation:** After insertion of 2, the final stack will be [2,4,3,2,1,8].

##### Example 2

- **Input:**
```text
st = [5, 3, 1], x = 4
```
- **Output:**
```text
[4, 5, 3, 1]
```
- **Explanation:** After insertion of 4, the final stack will be [4,5,3,1].

#### Constraints

- **1.** `1 ≤ n ≤ 10⁵⁰ ≤ x, elements of stack ≤ 10⁹`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(n)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-15 07:12:19
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public Stack<Integer> insertAtBottom(Stack<Integer> st, int x) {
       if(st.size()==0){
           st.push(x);
           return st;
       }
       int top = st.pop();
       insertAtBottom(st,x);
       st.push(top);
        return st;
    }
}
```

*Generated on: 10/15/2026, 7:12:28 AM*