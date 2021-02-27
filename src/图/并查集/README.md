# 并查集

## 并查集路径压缩模板

```java
class UnionFind{
    int[] parent;
    public UnionFind(int n){
        parent=new int[n];
        for(int i=0;i<n;i++){
            parent[i]=i;
        }
    }
    
    public void union(index1,index2){
        parent[find(index1)]=find(index2);
    }
    
    public int find(int index){
        if(parent[index]!=index){
            parent[index]=find(parent[index]);
        }
        return parent[index];
    }
}
```

## 并查集题目练习

- [LeetCode：947移除最多的同行或通列石头（Most Stones Removed with Sam Row or Column）](https://leetcode-cn.com/problems/most-stones-removed-with-same-row-or-column/)
- [LeetCode：721账户合并（Accounts Merge）](https://leetcode-cn.com/problems/accounts-merge/)
- [LeetCode：803打砖块（Bricks Falling When Hit）](https://leetcode-cn.com/problems/bricks-falling-when-hit/)



