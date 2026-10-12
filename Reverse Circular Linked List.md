## 01. Reverse Circular Linked List

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/reverse-the-circular-linked-list/1)

### Problem Description

**Task:** Given a circular linked list, reverse the linked list by changing the links between its nodes. Return the head of the reversed circular linked list. The returned list must remain circular after reversal. Nodes may contain duplicate values.

#### Examples

##### Example 1

- **Input:**
```text
head[] = [1, 7, 8, 10]Output: 10 - > 8 - > 7 - > 1Explanation: After reversing the given circular linked list, we'll get 10 - > 8 - > 7 - > 1.
```

##### Example 2

- **Input:**
```text
head[] = [2, 5, 7, 8, 10]Output: 10 - > 8 - > 7 - > 5 - > 2
```
- **Explanation:** After reversing the given circular linked list, we'll receive 10 - > 8 - > 7 - > 5 - > 2.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-10-12 21:15:34
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public Node reverseCircular(Node head) {
       Node temp = head;
       while(temp.next!=head){
           temp = temp.next;
       }
       temp.next = null;
       Node p = null;
       Node c = head;
       while(c!=null){
           Node f = c.next;
           c.next = p;
           p = c;
            c = f;
          
       }
       head.next = temp;
       return temp;
       
        
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-10-12 21:15:21
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
    public Node reverseCircular(Node head) {
       Node temp = head;
       while(temp.next!=head){
           temp = temp.next;
       }
       temp.next = null;
       Node p = null;
       Node c = head;
       while(c!=null){
           Node f = c.next;
           c.next = p;
           p = c;
            c = f;
          
       }
       head.next = temp;
       return temp;
       
        
    }
}
```

*Generated on: 10/12/2026, 9:22:01 PM*