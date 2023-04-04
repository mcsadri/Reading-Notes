# Implementation: Linked Lists

## Resources

### [Big O: Analysis of Algorithm Efficiency](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/big_oh.html) (Up through the section titled “Linear Complexity Growth”)

### [Linked Lists](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html)

#### Terminology

- *Linked List* - A data structure that contains nodes that links/points to the next node in the list.
- *Singly* - `Singly` refers to the number of references the node has. A `Singly` linked list means that there is only one reference, and the reference points to the `Next` node in a linked list.
- *Doubly* - `Doubly` refers to there being two (double) references within the node. A `Doubly` linked list means that there is a reference to both the `Next` and `Previous` node.
- *Node* - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.
- *Next* - Each node contains a property called `Next`. This property contains the reference to the next node.
- *Head* - The `Head` is a reference of type `Node` to the first node in a linked list.
- *Current* - The `Current` is a reference of type `Node` to the node that is currently being looked at. When traversing, you create a new `Current` variable at the `Head` to guarantee you are starting from the beginning of the linked list.

#### Traversal

The best way to approach a traversal is through the use of a `while()` loop. This allows us to continually check that the `Next` node in the list is not null. If we accidentally end up trying to traverse on a node that is `null`, a `NullReferenceException` gets thrown and our program will crash/end.

When traversing through a linked list, the `Current` variable will tell us where exactly in the linked list we are and will allow us to move/traverse forward until we hit the end.

### [What’s a Linked List, Anyway pt1](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d)

### [What’s a Linked List, Anyway pt2](https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996)
