```java
public List<Integer> postorderTraversal(TreeNode root) 
{
	List<Integer> res = new ArrayList<>();
	Deque<TreeNode> stack = new ArrayDeque<>();
	
	TreeNode stackTop = null;
	TreeNode lastVisited = null;
	
	while (root != null || !stack.isEmpty())
	{
	    // 1.root 有左子树，继续向下，直到没有
	    if (root != null)
	    {
    		stack.push(root);
    		root = root.left;
    		continue;
	    }  
	    
	    stackTop = stack.peek();
	    
	    // 2.栈顶元素 有右子树 && 右子树没访问过
	    if (stackTop.right != null && stackTop.right != lastVisited)
	    {
		    root = stackTop.right;
	    }
	    // 3. 栈顶元素 没右子树 || 右子树访问过了
	    else 
	    {
    		res.add(stackTop.val);
    		lastVisited = stackTop;
    		stack.pop();
	    }
	}
	
	return res;
}
```
