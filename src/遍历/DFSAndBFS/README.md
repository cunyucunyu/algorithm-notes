# DFS/BFS

- 网格位置方向模板
- DFS

## 网格位置方向模板

使用深度优先遍历（bfs）或者官广度优先遍历（bfs）时对于表格位置方向定位可以使用一个二维数组来表示。
```java
public static final int[][] DIRECTIONS={{0, 1}, {0, -1}, {1, 0}, {-1, 0}};
```
## DFS(depth first search)模板

**在递归中，如果层级过深，很可能保存过多的临时变量，导致栈溢出。大部分的递归转非递归，都可以通过栈来进行实现。**

- 非递归DFS
```java
public List<TreeNode> dfs(TreeNode root){
    List<TreeNode> res=new ArrayList<>();
    Stack<TreeNode> stack=new Stack<>();
    stack.add(root);
    while(!stack.empty()){
        TreeNode node=stack.peek();
        res.add(node);
        stack.pop();
        if(node.right!=null){
            stack.push(node.right);
        }
        if(node.left!=null){
            stack.push(ndoe.left);
        }
    }
    return res;
}
```








