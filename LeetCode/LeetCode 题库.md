# LeetCode ——题解

<!-- TOC -->

- [LeetCode ——题解](#leetcode-题解)
    - [103.二叉树的锯齿形层序遍历](#103二叉树的锯齿形层序遍历)
        - [思路：二叉树的层序遍历 / 队列 Queue 换成栈 Stack](#思路二叉树的层序遍历--队列-queue-换成栈-stack)
        - [解法](#解法)

<!-- /TOC -->


<!-- TOC -->
- **根据解题方法和思路分类**
    - 『数据类型』
        - 『数组』
            
        - 『矩阵/二维数组』
            
        - 『字符串』
            
        - 『字符流』
        - 『队列/堆栈』
            - [103.二叉树的锯齿形层序遍历](#103二叉树的锯齿形层序遍历)
        - 『链表』
            
        - 『树』
            - [103.二叉树的锯齿形层序遍历](#103二叉树的锯齿形层序遍历)
        - 『哈希表』
           
    - 『算法』
        - 『位运算』
        - 『二分查找』
            
        - 『双/多指针』
            
        - 『双层循环』
            
        - 『排序算法』 
        - 『递归』
           
        - 『动态规划』
           
        - 『数学』
            
        - 『二叉树遍历』
            - [103.二叉树的锯齿形层序遍历](#103二叉树的锯齿形层序遍历)
        - 『回溯法』   
           
            

<!-- /TOC -->


<br><br><br><br><br><br>

## 103.二叉树的锯齿形层序遍历
**给定一个二叉树，返回其节点值的锯齿形层序遍历。（即先从左往右，再从右往左进行下一层遍历，以此类推，层与层之间交替进行）。**<br>
例如：
给定二叉树 [3,9,20,null,null,15,7],
```
    3
   / \
  9  20
    /  \
   15   7
```
返回锯齿形层序遍历如下：
```
[
  [3],
  [20,9],
  [15,7]
]
```
### 思路：二叉树的层序遍历 / 队列 Queue 换成栈 Stack
1. 边界处理。
2. 建立两个堆栈，stack1 用于存放奇数层的节点，stack2 用于存放偶数层的节点；
3. 当两个堆栈不全为空的时候，进循环：
* 每次循环创建一个 list，用于存入 lists 作为结果；
* 当 stack1 不为空时，进入奇数层 stack1 取出、偶数层 stack2 存入处理。此时每次从 stack1 取出一个节点 node 存入 list，同时在 stack2 存入不为空的左、右节点（因为出栈时反向）；
* 当 stack2 不为空时，进入偶数层 stack2 取出、奇数层 stack1 存入处理。此时每次从 stack2 取出一个节点 node 存入 list，同时在 stack1 存入不为空的右、左节点（因为出栈时反向）；
* 每次处理完一个堆栈，存入一次 lists。
4. 当两堆栈都为空，返回结果即可。

### 解法
```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public List<List<Integer>> zigzagLevelOrder(TreeNode root) {
        List<List<Integer>> lists = new ArrayList<>();
        if(root == null) return lists;
        Stack<TreeNode> stack1 = new Stack<>();
        Stack<TreeNode> stack2 = new Stack<>();
        stack1.push(root);
        while(!stack1.isEmpty() || !stack2.isEmpty()){
            List<Integer> list = new ArrayList<>();
            if(!stack1.isEmpty()){
                while(!stack1.isEmpty()){
                    TreeNode node = stack1.pop();
                    list.add(node.val);
                    if(node.left != null)  stack2.push(node.left);
                    if(node.right != null) stack2.push(node.right);   
                }
            }else{
                while(!stack2.isEmpty()){
                    TreeNode node = stack2.pop();
                    list.add(node.val);
                    if(node.right != null) stack1.push(node.right);   
                    if(node.left != null)  stack1.push(node.left);
                }
            }
            lists.add(list);
        }
        return lists;
    }
}
```
<br><br>

