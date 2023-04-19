# [Stacks and Queues](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)

## Cheat Sheet

### Stacks

- Definition: A **stack** is a linear data structure that follows the FILO/LIFO principle. This means that:
  - FILO: the first item added in the stack will be the last item popped out of the stack.
  - LIFO: the last item added to the stack will be the first item popped out of the stack.

- Operations
  - `push(item)`: Add an item to the top of the stack.
  - `pop()`: Remove the top item from the stack and return it.
  - `peek()`: Return the top item from the stack without removing it.
  - `is_empty()`: Check if the stack is empty.
  - `size()`: Return the number of items in the stack.

- Use Cases
  - Undo/Redo functionality in text editors.
  - Function call stack in programming languages.
  - Balancing symbols (parentheses, brackets, etc.) in code.

### Queues

- Definition: A **queue** is a linear data structure that follows the FIFO/LILO principle. This means that:
  - FIFO: the first item in the queue will be the first item out of the queue.
  - LILO: the last item in the queue will be the last item out of the queue.

- Operations
  - `enqueue(item)`: Add an item to the back of the queue.
  - `dequeue()`: Remove the front item from the queue and return it.
  - `peek()`: Return the front item from the queue without removing it.
  - `is_empty()`: Check if the queue is empty.
  - `size()`: Return the number of items in the queue.

- Use Cases
  - Managing incoming requests in web servers.
  - Printing jobs in a printer.
  - Breadth-First Search algorithm in graphs.
