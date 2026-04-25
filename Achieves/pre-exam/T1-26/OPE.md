# LinkedList

### **Common Node Definition**
For all Linked List problems, we assume the following standard class definition:
```python
class ListNode:
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next
```

---

### **1. [cite_start]Predicted Question: Reverse in Groups of K** [cite: 13]
[cite_start]This focuses on advanced pointer manipulation[cite: 15].

```python
def reverse_k_group(head, k):
    # Check if there are at least k nodes left
    curr = head
    for _ in range(k):
        if not curr: return head
        curr = curr.next
    
    # Reverse k nodes
    prev, curr = None, head
    for _ in range(k):
        nxt = curr.next
        curr.next = prev
        prev = curr
        curr = nxt
    
    # Recurse for the remaining list
    head.next = reverse_k_group(curr, k)
    return prev
```

---

### **2. [cite_start]PYQ: Merge Two Sorted Lists** [cite: 8]
[cite_start]A frequently recurring topic in previous exams[cite: 8].

```python
def mergeTwoLists(l1, l2):
    dummy = ListNode()
    tail = dummy
    
    while l1 and l2:
        if l1.val < l2.val:
            tail.next = l1
            l1 = l1.next
        else:
            tail.next = l2
            l2 = l2.next
        tail = tail.next
    
    # Attach remaining nodes
    tail.next = l1 or l2
    return dummy.next
```

---

### **3. [cite_start]PYQ: Remove Duplicates from Sorted List** [cite: 8]
[cite_start]Another common basic operation identified in the trends[cite: 8].

```python
def deleteDuplicates(head):
    curr = head
    while curr and curr.next:
        if curr.val == curr.next.val:
            # Skip the next node
            curr.next = curr.next.next
        else:
            # Move to next unique node
            curr = curr.next
    return head
```

---

### **4. [cite_start]PYQ: Basic Operations (Insert at End & Delete First)** [cite: 8]
[cite_start]These represent the most fundamental operations found in the PYQs[cite: 8, 14].

**Insert at End:**
```python
def insertAtEnd(head, val):
    new_node = ListNode(val)
    if not head:
        return new_node
    curr = head
    while curr.next:
        curr = curr.next
    curr.next = new_node
    return head
```

**Delete First:**
```python
def deleteFirst(head):
    if not head:
        return None
    return head.next
```
