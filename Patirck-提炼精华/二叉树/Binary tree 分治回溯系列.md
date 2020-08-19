# Binary tree 分治回溯
##### [124.Binary Tree Maximum Path Sum](https://leetcode.com/problems/binary-tree-maximum-path-sum/)
##### [543. Diameter of Binary Tree](https://leetcode.com/problems/diameter-of-binary-tree/)
##### [687. Longest Univalue Path](https://leetcode.com/problems/longest-univalue-path/)
#  
# 
# 
#### [Longest Path](https://leetcode.com/submissions/detail/383417408/)
```java
    int leftLongestSinglePath = 0;
    
    if (root.left != null)
    {
        leftLongestSinglePath = leftLongestPair[0] + 1;
    }
```

#### [Path Sum](https://leetcode.com/submissions/detail/383424572/)
```java
    Math.max(Math.max(leftMaxPair[0], rightMaxPair[0]), 0) + root.val;
    
    Math.max(leftMaxPair[0], 0) + Math.max(rightMaxPair[0], 0) + root.val
```