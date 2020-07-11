---
layout: post
title:  Binary Tree Level Order Traversal (easy)
---
Solution 1. We can use the library’s sort function. Time complexity will be O(nlogn)

Solution 2. Two pass solution. 

1.  Count the numbers of 0s, 1s, and 2s.
2.  After counting, put all 0s first, then 1s and 2s in the array.

Solution 3. 

​	Intuition

1.  three colors
    1.  0: low. left. the rightmost boundary of zeros
    2.  1: i. The current element under the consideration
    3.  2: high. right. the leftmost boundary of twos