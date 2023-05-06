# Trees

## [Trees](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)

- Common Terminology
  - Node - A Tree node is a component which may contain its own values, and references to other nodes
  - Root - The root is the node at the beginning of the tree
  - K - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, `k = 2`.
  - Left - A reference to one child node, in a binary tree
  - Right - A reference to the other child node, in a binary tree
  - Edge - The edge in a tree is the link between a parent and child node
  - Leaf - A leaf is a node that does not have any children
  - Height - The height of a tree is the number of edges from the root to the furthest leaf

- Traversals
  - Traversing a tree allows us to search for a node, print out the contents of a tree, etc.
  - Two categories of traversals for trees:
    - Depth First
      - Prioritizes going through the depth (height) of the tree first
      - Multiple ways to do depth first traversal. Each way has a different order for searching/printing the `root`
        - Pre-order: `root >> left >> right`
          - Means the `root` has to be looked at first
          - When calling `preOrder` for the first time the `root` will be added to the call stack.
          - Then start reading the `preOrder`'s function code from the top to bottom.
          - The `root.value` is output to the console.
          - Then check if the `root` has a `left` node set.
            - If yes: send the `left` node the `preOrder` method recusrively.
            - Process continues until a leaf node is reached.
        - In-order: `left >> root >> right`
        - Post-order: `left >> right >> root`
      - Most common way to traverse through a tree is with recursion.
      - Rely on the *call stack* to navigate back up the tree when reaching the end of a sub-path.
    - Breadth First
      - doodah

---

### Trees Cheat Sheet

#### Introduction

- A tree data structure is a non-linear data structure consisting of nodes connected by edges.
- Trees are used to represent hierarchical relationships between elements, such as organization charts or file systems.

#### Components of a Tree

- Node: A single element of the tree. May contain it's own valies, and references to other nodes.
- Root: The topmost/beginning node of the tree.
- Edge: A connection between two nodes, linking a parent with a child.

#### Other Terminology

- K: A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, `k = 2`.
- Parent: A node that has one or more child nodes.
- Child: A node that is connected to a parent node.
- Leaf: A node with no children.
- Height: The distance between the root node and the deepest node in the tree.
- Left: A reference to one child node, in a binary tree
- Right: A reference to the other child node, in a binary tree

#### Types of Trees

- Binary Tree: A tree in which each node can have at most two children.
- K-ary Tree: A tree with more than two child nodes. `K` is used to refer to the maximum number of children that each Node is able to have.
- Binary Search Tree: A tree where nodes are organized in a manner where
  - all values that are smaller than the root are placed to the left
  - all values that are larger than the root are placed to the right

#### Traversal Methods

- Depth First: Prioritizes going through the depth (height) of the tree first
  - Pre-order traversal: `root >> left >> right`
  - In-order traversal: `left >> root >> right`
  - Post-order traversal: `left >> right >> root`
- Breadth First: traversal iterates through the tree by going through each level of the tree node-by-node.

#### Big O

- Time:
  - Inserting a new node is `O(n)`.
  - Searching for a specific node `O(n)`.
  - The worst case for most operations will involve traversing the entire tree, hence the `O(n)`.
- Space:
  - A node insertion using breadth first insertion will be `O(w)`, where `w` is the largest width of the tree.
- Perfect tree:
  - The maximum width for a perfect binary tree (every non-leadf node has 2 children), is `2^(h-1)`, where `h` is the height of the tree.
  - Height can be calculated as `log n`, where `n` is the number of nodes.
- Binary Search Tree:
  - Time: insertion and search operations is `O(h)`, or `O(height)`
    - If balanced (or perfect): the height of the tree is `log(n)`
  - Space: `O(1)`, because during a search, there is no allocating additional space.
