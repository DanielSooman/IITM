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


Here's clean, exam-ready code for all requested variations:

---

### Node Class (use this everywhere)
```python
class Node:
    def __init__(self, data=None):
        self.data = data
        self.next = None
```

---

### Variation 1 — Insert at Beginning
```python
def insert_at_start(head, data):
    new_node = Node(data)
    new_node.next = head      # point new node to current head
    head = new_node           # new node becomes the new head
    return head

# Example usage:
# head → [3,5,7]  →  after insert_at_start(head, 1)  →  [1,3,5,7]
```

---

### Variation 2 — Insert at Position
```python
def insert_at_position(head, data, pos):
    new_node = Node(data)

    if pos == 0:                        # insert at beginning
        new_node.next = head
        return new_node

    curr = head
    for i in range(pos - 1):           # walk to node just BEFORE pos
        if curr is None:
            return head                 # pos out of range, do nothing
        curr = curr.next

    new_node.next = curr.next           # new node points to next
    curr.next = new_node                # previous node points to new node
    return head

# Example:
# [1,3,7,9], data=5, pos=2  →  [1,3,5,7,9]
```

---

### Variation 5 — Search / Find
```python
def search(head, key):
    curr = head
    index = 0

    while curr is not None:
        if curr.data == key:
            return index            # found, return index
        curr = curr.next
        index += 1

    return -1                       # not found

# Example:
# [1,3,5,7,9], key=5  →  2
# [1,3,5,7,9], key=4  →  -1
```

---

### Variation 7 — Print in Reverse (without reversing)
```python
# METHOD 1: Using recursion (cleanest for exam)
def print_reverse(head):
    if head is None:
        return
    print_reverse(head.next)       # go to end first
    print(head.data, end=" ")      # print while returning back

# METHOD 2: Using a stack
def print_reverse_stack(head):
    stack = []
    curr = head

    while curr is not None:        # push all nodes onto stack
        stack.append(curr.data)
        curr = curr.next

    while stack:                   # pop = reverse order
        print(stack.pop(), end=" ")

# Example:
# [1,3,5,7,9]  →  9 7 5 3 1
```

---

### Variation 6 — Reverse a Linked List ⭐
```python
def reverse_list(head):
    prev = None
    curr = head

    while curr is not None:
        next_node = curr.next      # save next
        curr.next = prev           # reverse the pointer
        prev = curr                # move prev forward
        curr = next_node           # move curr forward

    return prev                    # prev is now the new head

# Dry run on [1,3,5]:
# Step 1: prev=None,  curr=1  →  1→None,  prev=1,  curr=3
# Step 2: prev=1,     curr=3  →  3→1,     prev=3,  curr=5
# Step 3: prev=3,     curr=5  →  5→3,     prev=5,  curr=None
# return prev = 5   →  [5,3,1] ✓
```

---

### Variation 9 — Find Middle Element ⭐
```python
def find_middle(head):
    slow = head
    fast = head

    while fast is not None and fast.next is not None:
        slow = slow.next           # moves 1 step
        fast = fast.next.next      # moves 2 steps

    return slow.data               # slow is at middle when fast reaches end

# Dry run on [1,2,3,4,5]:
# slow=1, fast=1
# slow=2, fast=3
# slow=3, fast=5
# fast.next is None → stop → return slow.data = 3 ✓

# For even length [1,2,3,4]:
# slow=1,fast=1 → slow=2,fast=3 → slow=3,fast=None → stop → return 3
# (returns upper middle for even length)
```

---

### Variation 8 — Find Length
```python
# METHOD 1: Iterative
def length(head):
    count = 0
    curr = head

    while curr is not None:
        count += 1
        curr = curr.next

    return count

# METHOD 2: Recursive (bonus)
def length_recursive(head):
    if head is None:
        return 0
    return 1 + length_recursive(head.next)

# Example:
# [1,3,5,7,9]  →  5
```

---

### Variation 13 — Intersection of Two Lists
```python
def intersection(head1, head2):
    # Store all values of list2 in a set for O(1) lookup
    values = set()
    curr = head2

    while curr is not None:
        values.add(curr.data)
        curr = curr.next

    # Build result list with common values
    result_head = None
    result_tail = None
    curr = head1

    while curr is not None:
        if curr.data in values:              # common element found
            new_node = Node(curr.data)
            if result_head is None:          # first common element
                result_head = new_node
                result_tail = new_node
            else:
                result_tail.next = new_node  # append to result
                result_tail = new_node
        curr = curr.next

    return result_head

# Example:
# [1,3,5,7] and [3,6,7,9]  →  [3,7]
```

---

### Variation 15 — Sum of Linked List
```python
# METHOD 1: Iterative
def list_sum(head):
    total = 0
    curr = head

    while curr is not None:
        total += curr.data
        curr = curr.next

    return total

# METHOD 2: Recursive (bonus)
def list_sum_recursive(head):
    if head is None:
        return 0
    return head.data + list_sum_recursive(head.next)

# Example:
# [1,3,5,7,9]  →  25
```

---

## 📌 Exam Pattern Reminder

| Question asks | What to return |
|--------------|----------------|
| "return the head" | `return head` / `return new_node` |
| "should not return anything" | just modify `curr.next` in-place |
| "return the value/data" | `return curr.data` not the node |
| "return -1 if not found" | always add the `-1` case |

> Always check whether the function returns a **node reference** or **data value** — PYQs have both styles and mixing them up costs marks.





# BST


<img width="709" height="586" alt="image" src="https://github.com/user-attachments/assets/a5d558af-18d8-45c2-80af-1e6b52753081" />


```python
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
