# Binary Tree Level Order Traversal (easy)

1.  Intuition
    1.  "level-by-level traversal" BFS. (c.f. root-to-leaf uses DFS)
    2.  What is BFS? We can traverse a tree in a level-be-level order.  
    3.  Use a Queue to store nodes of a level before going to the next level. 
    4.  The space complexity is O(w) where 'w' is the maximum number of nodes on any level
    5.  The time complexity is O(n) since we may have to visit all the nodes.