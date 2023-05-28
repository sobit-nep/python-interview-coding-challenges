**data_structures.md**

## Data Structure Coding Challenges

In this file, we will explore some coding challenges related to data structures in Python.

### Challenge 1: Implement a Stack using a List

Write a Python class `Stack` that implements a stack data structure using a list. The class should have methods for pushing an element onto the stack (`push`), popping the top element from the stack (`pop`), and checking if the stack is empty (`is_empty`).

```python
class Stack:
    def __init__(self):
        self.stack = []
        
    def push(self, element):
        self.stack.append(element)
        
    def pop(self):
        if not self.is_empty():
            return self.stack.pop()
        else:
            raise Exception("Stack is empty")
            
    def is_empty(self):
        return len(self.stack) == 0
```

### Challenge 2: Simulate a Binary Search Tree

Write a Python class `Node` that represents a node in a binary search tree. The class should have methods for inserting a value into the tree (`insert`), searching for a value in the tree (`search`), and printing the tree in inorder traversal (`print_inorder`).

```python
class Node:
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None
        
    def insert(self, value):
        if value < self.value:
            if self.left is None:
                self.left = Node(value)
            else:
                self.left.insert(value)
        else:
            if self.right is None:
                self.right = Node(value)
            else:
                self.right.insert(value)
                
    def search(self, value):
        if value == self.value:
            return True
        elif value < self.value:
            if self.left is None:
                return False
            else:
                return self.left.search(value)
        else:
            if self.right is None:
                return False
            else:
                return self.right.search(value)
                
    def print_inorder(self):
        if self.left:
            self.left.print_inorder()
        print(self.value, end=" ")
        if self.right:
            self.right.print_inorder()
```

### Challenge 3: Reverse a Linked List

Write a Python class `LinkedList` that represents a linked list. The class should have methods for adding a node to the list (`add_node`), reversing the list (`reverse`), and printing the list (`print_list`).

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
        
class LinkedList:
    def __init__(self):
        self.head = None
        
    def add_node(self, data):
        new_node = Node(data)
        if self.head is None:
            self.head = new_node
        else:
            current = self.head
            while current.next:
                current = current.next
            current.next = new_node
            
    def reverse(self):
        prev = None
        current = self.head
        while current:
            next_node = current.next
            current.next = prev
            prev = current
            current = next_node
        self.head = prev
        
    def print_list(self):
        current = self.head
        while current:
            print(current.data, end=" ")
            current = current.next
```

### Challenge 4: Implement a Hash Table

Write a Python class `HashTable` that implements a hash table data structure. The class should have methods for adding a key-value pair to the hash table (`add_pair`), retrieving the value associated with a key (`get_value`), and removing a key-value pair from the hash table (`remove_pair`).

```python
class HashTable:
    def __init__(self):
        self.size = 10
        self.table = [[] for _ in range(self.size)]
        
    def _hash_function(self, key):
        return hash(key) % self.size
    
    def add_pair(self, key, value):
        index = self._hash_function(key)
        bucket = self.table[index]
        for i, (k, v) in enumerate(bucket):
            if k == key:
                bucket[i] = (key, value)
                return
        bucket.append((key, value))
        
    def get_value(self, key):
        index = self._hash_function(key)
        bucket = self.table[index]
        for k, v in bucket:
            if k == key:
                return v
        raise KeyError("Key not found")
        
    def remove_pair(self, key):
        index = self._hash_function(key)
        bucket = self.table[index]
        for i, (k, v) in enumerate(bucket):
            if k == key:
                del bucket[i]
                return
        raise KeyError("Key not found")
```

### Challenge 5: Implement a Queue using a List

Write a Python class `Queue` that implements a queue data structure using a list. The class should have methods for adding an element to the queue (`enqueue`), removing the first element from the queue (`dequeue`), and checking if the queue is empty (`is_empty`).

```python
class Queue:
    def __init__(self):
        self.queue = []
        
    def enqueue(self, element):
        self.queue.append(element)
        
    def dequeue(self):
        if not self.is_empty():
            return self.queue.pop(0)
        else:
            raise Exception("Queue is empty")
            
    def is_empty(self):
        return len(self.queue) == 0
```

You can add more challenges and solutions to this file, or create separate Markdown files for different categories of coding challenges.