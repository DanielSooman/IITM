<img width="1104" height="233" alt="image" src="https://github.com/user-attachments/assets/6e86d7d5-f126-4cca-bb9f-de612441ee0d" />



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
def mergeSortedList(head1,head2):
    
    l = []
    t1 = head1
    t2 = head2
    
    
    while t1:
        l.append(t1.data)
        t1 = t1.next
        
        
    while t2:
        l.append(t2.data)
        
        t2 = t2.next
        
        
    l.sort()
    
    
    head3 = Node(l[0])
    
    t3 = head3
    
    for i in range(1,len(l)):
        t3.next = Node(l[i])
        t3 = t3.next
        
    return head3
```

---

### **3. [cite_start]PYQ: Remove Duplicates from Sorted List** [cite: 8]
[cite_start]Another common basic operation identified in the trends[cite: 8].

```python
def removeDuplicate(head):
    
    curr = head
    
    while curr and curr.next:
        if curr.data == curr.next.data:
            curr.next = curr.next.next
            
        else:
            curr = curr.next
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








# BST


<img width="709" height="586" alt="image" src="https://github.com/user-attachments/assets/a5d558af-18d8-45c2-80af-1e6b52753081" />
```
class Node:
    def __init__(self,data):
        self.left = None
        self.data = data
        self.right = None
def insert_element(root,k):


    if root is None:
        return Node(k)


    if k < root.data:
        if root.left is None:
            root.left = Node(k)
        else:
            insert_element(root.left, k)
            
    elif k > root.data:
        if root.right is None:
            root.right = Node(k)
        else:
            insert_element(root.right, k)
    

```
