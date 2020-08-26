# Binary tree 分治回溯

##### [124.Binary Tree Maximum Path Sum](https://leetcode.com/submissions/detail/383424572/)
```java
    // res[0] - MaxSinglePathSum
    // res[1] - MaxPathSum
    
    // 左右最长single path sum + root
    resMaxPair[1] = Math.max(leftMaxPair[0], 0) + Math.max(rightMaxPair[0], 0) + root.val
```

        [687. Longest Univalue Path](https://leetcode.com/submissions/detail/383351782/)
        ```java
            // res[0] - MaxSinglePathSum
            // res[1] - MaxPathSum

            if (root.left != null && root.left.val == root.val) 
                leftLongestSinglePath = leftLongestPair[0] + 1;
        ```

        [543. Diameter of Binary Tree](https://leetcode.com/submissions/detail/383417408/)
        ```java
            // res[0] - MaxSinglePathSum
            // res[1] - MaxPathSum

            if (root.left != null)
                leftLongestSinglePath = leftLongestPair[0] + 1;
        ```

##### [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/submissions/detail/383535536/)
```java
    // != null 意味着有一个target node
    if (leftRes != null && rightRes != null)
        return root;
    
    if (leftRes != null)
        return leftRes;
```

##### [98. Validate Binary Search Tree](https://leetcode.com/submissions/detail/383578242/)
```java
    public Result(boolean isValid, int max, int min)
    {
        this.isValid = isValid;
        this.max = max;
        this.min = min;
    }
    
    if (leftRes.max >= root.val || rightRes.min <= root.val)
        res.isValid = false;
```

##### [101. Symmetric Tree](https://leetcode.com/submissions/detail/386480852/)
```java
    boolean isLeftSymmetric = helper(root1.left, root2.right);
    boolean isRightSymmetric = helper(root1.right, root2.left);
```
