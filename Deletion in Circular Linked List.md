## 01. Deletion in Circular Linked List

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/deletion-and-reverse-in-linked-list/1)

### Problem Description

**Task:** Given the head of a circular linked list and an integer key, delete the first occurrence of the node containing key, if it exists. Return the head of the modified circular linked list.

#### Examples

##### Example 1

- **Input:**
```text
key = 8Output: 1 - > 7 - > 10Explanation: After deleting 8 from the given circular linked list, it has elements as 1, 7, 10.
```

##### Example 2

- **Input:**
```text
key = 8Output: 2 - > 5 - > 7 - > 10
```
- **Explanation:** After deleting 8 from the given circular linked list, it has elements as 2, 5, 7, 10.

#### Constraints

- **1.** `1 ≤ number of nodes ≤ 10⁵⁰ ≤ node - > data, key ≤ 10⁵`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-12 21:49:38
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
    Node deleteNode(Node head, int key) {
       Node temp = head;
       while(temp.next!=head){
           temp = temp.next;
          
       }
        if(head.data==key){
            head = head.next;
            temp.next = head;
            return head;
        }
        Node m = head;
        Node n = head.next;
        while(n!=head){
            if(n.data==key){
                m.next = n.next;
                break;
            }
           n = n.next;
           m = m.next;
        }
        temp.next = head;
        return head;
    }
}
```

*Generated on: 10/12/2026, 9:49:50 PM*