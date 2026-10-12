## 01. Reverse a Doubly Linked List

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/reverse-a-doubly-linked-list/1)

### Problem Description

**Task:** Given the head of a doubly linked list, reverse the list and return the head of the reversed doubly linked list.

> **Note:** Driver code will print the returned list in both forward and backward directions.

#### Examples

##### Example 1

- **Output:**
```text
5 < - > 4 < - > 33 < - > 4 < - > 5
```
- **Explanation:** After reversing the given doubly linked list the new list will be 5 < - > 4 < - > 3.

##### Example 2

- **Output:**
```text
196 < - > 59 < - > 122 < - > 7575 < - > 122 < - > 59 < - > 196Explanation: After reversing the given doubly linked list the new list will be 196 < - > 59 < - > 122 < - > 75.
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-13 00:43:36
- **Status:** Correct
- **Marks:** 2

```java
/* Structure of Doubly Linked List Node
class Node {
    int data;
    Node next;
    Node prev;

    Node(int data) {
        this.data = data;
        this.next = null;
        this.prev = null;
    }
}
*/
class Solution {
    public Node reverse(Node head) {
        Node p= null;
        Node c = head;
        while(c!=null){
            Node f = c.next;
            c.next = p;
            c.prev = f;
            p = c;
            c = f;
        
        
        }
        
        return p;
    }
}
```

*Generated on: 10/13/2026, 12:43:45 AM*