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
