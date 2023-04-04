# Prep: Data Structures and Algorithms

## Video

- [Basic Recursion](https://www.youtube.com/watch?v=vPEJSJMg4jY)
  - Resursion requires:
    - base/best case
    - recursive case

- [Data Structures in 15 Minutes](https://www.youtube.com/watch?v=sVxBVvlnJsM)
  - 5 most important types of data structures:
    - linked list
    - array
    - hash table
    - stack & queue
    - graphs & trees

- [Big O Explained](https://www.youtube.com/watch?v=v4cd1O4zkGw)
  - 4 important rules to know with the Big O:
    - if you have two different steps in your algorithm, you add up those steps
      - if you have a first step that takes O of A time and a second step that takes O of B you would add up those run times and you get O of A plus B

      ```pseudo
      function doodah():
        do_step_1()     // O(a)
        do_step_2()     // O(b)
                        // O(a+b)
      ```

    - drop constants
      - You do not describe things as O of 2n or O of 3n because you're just looking for how things scale roughly. Is it a linear relationship, is it a quadratic relationship, so you always drop constants.
    - if you have different inputs you're usually going to use different variables to represent them
      - we have two arrays and we're walking through them to figure out the number of elements in common between the two arrays
        - incorrect: O(N^2)
        - correct: O(a * b)
          - a = len of array a, b = len of array b
      - drop non-dominant terms
        - `¯\_(ツ)_/¯`

## Reading

[Basic Data Structures](https://towardsdatascience.com/8-common-data-structures-every-programmer-must-know-171acf6a1a42)

- Data Structures are a specialized means of organizing and storing data in computers in such a way that we can perform operations on the stored data more efficiently.
- Arrays:
  - An array is a structure of fixed-size, which can hold items of the same data type.
  - Arrays are indexed, meaning that random access is possible.
- Linked Lists:
  - A linked list is a sequential structure that consists of a sequence of items in linear order which are linked to each other.
  - you have to access data sequentially and random access is not possible.
- Stacks:
  - A stack is a LIFO (Last In First Out — the element placed at last can be accessed at first) structure which can be commonly found in many programming languages.
  - This structure is named as “stack” because it resembles a real-world stack — a stack of plates.
- Queues:
  - A queue is a FIFO (First In First Out — the element placed at first can be accessed at first) structure which can be commonly found in many programming languages.
  - This structure is named as “queue” because it resembles a real-world queue — people waiting in a queue.
- Hash Tables:
  - A Hash Table is a data structure that stores values which have keys associated with each of them.
  - Supports lookup efficiently if we know the key associated with the value. Hence it is very efficient in inserting and searching, irrespective of the size of the data.
- Trees:
  - A tree is a hierarchical structure where data is organized hierarchically and are linked together.
  - This structure is different from a linked list whereas, in a linked list, items are linked in a linear order.
  - Some examples are binary search tree, B tree, treap, red-black tree, splay tree, AVL tree and n-ary tree.
- Heaps:
  - A Heap is a special case of a binary tree where the parent nodes are compared to their children with their values and are arranged accordingly.
  - Min Heap — the key of the parent is less than or equal to those of its children. This is called the min-heap property. The root will contain the minimum value of the heap.
  - Max Heap — the key of the parent is greater than or equal to those of its children. This is called the max-heap property. The root will contain the maximum value of the heap.
- Graphs:
  - A graph consists of a finite set of vertices or nodes and a set of edges connecting these vertices.
  - The order of a graph is the number of vertices in the graph. The size of a graph is the number of edges in the graph.
  - Two nodes are said to be adjacent if they are connected to each other by the same edge.

**[BIG O CHEATSHEET](https://www.bigocheatsheet.com/)**

[Why Big O](https://triplebyte.com/blog/why-you-should-learn-big-o-and-stop-hacking-your-way-through-algorithms)

- Big-O is the name of the notation used to describe how efficient an algorithm is.
  - O = the “Order” of magnitude (Pop, pop!) of operations.
- Efficiency is the entire point
- Missing the Point Makes Learning Harder
- Getting the Point Also Prevents Mistakes: understanding the point of Big-O (and algorithms in general) will seriously help you avoid mistakes in interviews.

## Discussion Questions

- What is 1 of the more important things you should consider when deciding which data structure is best suited to solve a particular problem?
  - "Some data structures are linear. This means the items are arranged in sequential order. Others are non-linear and should be used when the relationships between items is important. The most widely-used data structures include arrays, stacks, queues, records, trees, graphs, linked lists, and hash tables. There are many factors involved in choosing a data structure to use. *However, memory use, performance, and ease of use are the most important*." [Linode.com](https://www.linode.com/docs/guides/data-structure/)
- How can we ensure that we’ll avoid an infinite recursive call stack?
  - use a base case to validate progression
