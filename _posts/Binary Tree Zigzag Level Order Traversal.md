---
layout: post
title: 103. Binary Tree Zigzag Level Order Traversal
---

```
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
from collections import deque





# left_to_right 
class Solution:
    def zigzagLevelOrder(self, root: TreeNode) -> List[List[int]]:
        result = []
        
        # edge case always check if root is empty
        if root is None:
            return result
        
        queue = deque()
        queue.append(root)

        left_to_right = True
        
        while queue:
            current_level = len(queue)
            current_result = deque()
            
            
            for _ in range(current_level):
                node = queue.popleft()
                if left_to_right:
                    current_result.append(node.val)
                else:
                    current_result.appendleft(node.val)
                    
                
                if node.left is not None:
                    queue.append(node.left)
                
                if node.right is not None:
                    queue.append(node.right)
                    
            left_to_right = not left_to_right 
            result.append(list(current_result))
            
        return result
```