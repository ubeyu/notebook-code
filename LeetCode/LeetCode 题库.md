# LeetCode ——题解

<!-- TOC -->

- [LeetCode ——题解](#leetcode-题解)
    - [103.二叉树的锯齿形层序遍历](#103二叉树的锯齿形层序遍历)
        - [思路：二叉树的层序遍历 / 队列 Queue 换成栈 Stack](#思路二叉树的层序遍历--队列-queue-换成栈-stack)
        - [解法](#解法)
    - [123. 买卖股票的最佳时机 III](#123-买卖股票的最佳时机-iii)
        - [思路：动态规划](#思路动态规划)
        - [解法](#解法-1)
    - [135.分发糖果](#135分发糖果)
        - [思路1：两次遍历：设定左规则和右规则，选取最大值](#思路1两次遍历设定左规则和右规则选取最大值)
        - [解法](#解法-2)
    - [189. 旋转数组](#189-旋转数组)
        - [思路1：循环](#思路1循环)
        - [解法](#解法-3)
    - [387.字符串中的第一个唯一字符](#387字符串中的第一个唯一字符)
        - [思路1：类动态规划？适合输出结果字符。](#思路1类动态规划适合输出结果字符)
        - [解法](#解法-4)
        - [思路2：类动态规划？适合输出结果索引。](#思路2类动态规划适合输出结果索引)
        - [解法](#解法-5)
    - [455. 分发饼干](#455-分发饼干)
        - [思路1：双指针？贪心算法](#思路1双指针贪心算法)
        - [解法](#解法-6)
    - [547. 省份数量](#547-省份数量)
        - [思路1：深度优先搜索](#思路1深度优先搜索)
        - [解法](#解法-7)
    - [1018. 可被 5 整除的二进制前缀](#1018-可被-5-整除的二进制前缀)
        - [思路1：数学（注意 int 溢出）](#思路1数学注意-int-溢出)
        - [解法](#解法-8)

<!-- /TOC -->


<!-- TOC -->
- **根据解题方法和思路分类**
    - 『数据类型』
        - 『数组』
            - [189. 旋转数组](#189-旋转数组)
            - [455. 分发饼干](#455-分发饼干)
        - 『矩阵/二维数组』
        - 『字符串』
            - [387.字符串中的第一个唯一字符](#387字符串中的第一个唯一字符)
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
            - [455. 分发饼干](#455-分发饼干)
        - 『双层循环』
            - [135.分发糖果](#135分发糖果)
        - 『排序算法』 
        - 『递归』
        - 『动态规划』
           - [123. 买卖股票的最佳时机 III](#123-买卖股票的最佳时机-iii)
           - [387.字符串中的第一个唯一字符](#387字符串中的第一个唯一字符)
        - 『数学』
            - [135.分发糖果](#135分发糖果)
        - 『二叉树遍历』
            - [103.二叉树的锯齿形层序遍历](#103二叉树的锯齿形层序遍历)
        - 『回溯法』  
        - 『贪心算法』    
           - [455. 分发饼干](#455-分发饼干)
            

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


## 123. 买卖股票的最佳时机 III
**给定一个数组，它的第 i 个元素是一支给定的股票在第 i 天的价格。设计一个算法来计算你所能获取的最大利润。你最多可以完成两笔交易。注意：你不能同时参与多笔交易（你必须在再次购买前出售掉之前的股票）。**<br>
示例 1:
```
输入：prices = [3,3,5,0,0,3,1,4]
输出：6
解释：在第 4 天（股票价格 = 0）的时候买入，在第 6 天（股票价格 = 3）的时候卖出，这笔交易所能获得利润 = 3-0 = 3 。
     随后，在第 7 天（股票价格 = 1）的时候买入，在第 8 天 （股票价格 = 4）的时候卖出，这笔交易所能获得利润 = 4-1 = 3 。
```
### 思路：动态规划
```
/**
对于任意一天考虑四个变量:
    fstBuy: 在该天第一次买入股票可获得的最大收益 
    fstSell: 在该天第一次卖出股票可获得的最大收益
    secBuy: 在该天第二次买入股票可获得的最大收益
    secSell: 在该天第二次卖出股票可获得的最大收益
分别对四个变量进行相应的更新, 最后secSell就是最大
收益值(secSell >= fstSell)
**/
```


### 解法
```java
class Solution {
    public int maxProfit(int[] prices) {
        int firBuy = Integer.MIN_VALUE, firSel = 0;
        int secBuy = Integer.MIN_VALUE, secSel = 0;
        for(int i=0;i<prices.length;i++){
            //第一次买入的最大收益
            //第一次卖出的最大收益
            //第二次买入的最大收益
            //第二次卖出的最大收益
            firBuy = Math.max(firBuy, - prices[i]);              //即当前位置及以前最小的价值点
            firSel = Math.max(firSel, firBuy + prices[i]);       //即当前位置及以前一次买卖的最大值
            secBuy = Math.max(secBuy, firSel - prices[i]);       //即当前位置及以前第二次买入最小的价值点
            secSel = Math.max(secSel, secBuy + prices[i]);       //即当前位置及以前第二次卖出最小的价值点
        }
        return secSel;
    }
}
```
<br><br>



## 135.分发糖果
**老师想给孩子们分发糖果，有 N 个孩子站成了一条直线，老师会根据每个孩子的表现，预先给他们评分。**<br>
你需要按照以下要求，帮助老师给这些孩子分发糖果：
* 每个孩子至少分配到 1 个糖果。
* 评分更高的孩子必须比他两侧的邻位孩子获得更多的糖果。

那么这样下来，老师至少需要准备多少颗糖果呢？
示例：
```
输入：[1,0,2]
输出：5
解释：你可以分别给这三个孩子分发 2、1、2 颗糖果。
```

### 思路1：两次遍历：设定左规则和右规则，选取最大值
我们可以将「相邻的孩子中，评分高的孩子必须获得更多的糖果」这句话拆分为两个规则，分别处理。

* 左规则：当 ratings[i−1]<ratings[i] 时，i 号学生的糖果数量将比 i−1 号孩子的糖果数量多。

* 右规则：当 ratings[i]>ratings[i+1] 时，i 号学生的糖果数量将比 i+1 号孩子的糖果数量多。

我们遍历该数组两次，处理出每一个学生分别满足左规则或右规则时，最少需要被分得的糖果数量。每个人最终分得的糖果数量即为这两个数量的最大值。

### 解法
```java
class Solution {
    public int candy(int[] ratings) {
        int n = ratings.length;
        int[] left = new int[n];
        int[] right = new int[n];
        for (int i = 0; i < n; i++) {
            if(i > 0 && ratings[i] > ratings[i-1]) {
                left[i] = left[i-1] + 1;
            }else{
                left[i] = 1;
            }
        }
        int ans = 0;
        for (int i = n-1; i >= 0; i--) {
            if(i < n-1 && ratings[i] > ratings[i+1]) {
                right[i] = right[i+1] + 1;
            }else{
                right[i] = 1;
            }
            ans = ans + Math.max(right[i],left[i]);
        }
        return ans;
    }
}
```
<br><br>

## 189. 旋转数组
**给定一个数组，将数组中的元素向右移动 k 个位置，其中 k 是非负数。**<br>

示例：
```
输入: [1,2,3,4,5,6,7] 和 k = 3
输出: [5,6,7,1,2,3,4]
解释:
向右旋转 1 步: [7,1,2,3,4,5,6]
向右旋转 2 步: [6,7,1,2,3,4,5]
向右旋转 3 步: [5,6,7,1,2,3,4]
```

### 思路1：循环
1. 边界条件；
2. 先把最后 k 个要挪到前面去的元素生成一个长度为 k 的新数组；
3. 从后往前循环 nums，根据索引位置做不同处理：
    * 若索引 i 大于等于 k，nums[i] = nums[i-k]；
    * 若索引 i 小于 k（前 k 个元素）， nums[i] = tmp[i]。
4. 循环结束，返回即可。

### 解法
```java
class Solution {
    public void rotate(int[] nums, int k) {
        if(nums == null || nums.length == 0 || nums.length == 1 || k == 0) return;
        k = k % nums.length;
        int[] tmp = new int[k];
        for(int i=nums.length-k;i<nums.length;i++){
            tmp[i-nums.length+k] = nums[i];
        }
        for(int i=nums.length-1;i>=0;i--){
            if(i<k) nums[i] = tmp[i];
            else{
                nums[i] = nums[i-k];
            }
        }
        return;
    }
}
```
<br><br>

## 387.字符串中的第一个唯一字符
**给定一个字符串，找到它的第一个不重复的字符，并返回它的索引。如果不存在，则返回 -1。**<br>
例如：
```
s = "leetcode"
返回 0

s = "loveleetcode"
返回 2
```

### 思路1：类动态规划？适合输出结果字符。
1. 边界处理。
2. dp[]用于记录每个字符出现的状态：
* -1表示出现大于1次；
* 0表示未出现；
* 其他表示出现一次字符的出现顺序。
3. 循环用于对每个字符状态进行赋值；
4. 循环从dp[]中获取最早出现的一次字符ansC；
5. 循环从s中根据字符ansC找到其索引，即为结果ans。

### 解法
```java
class Solution {
    public int firstUniqChar(String s) {
        if(s == null || s.length() == 0) return -1; //边界条件
        int index = 1;  //设置索引，用于每次判断出现一次字符时赋值并加一
        int dp[] = new int[26];  //用于记录每个字符出现的状态：-1表示出现大于1次；0表示未出现；其他表示出现一次字符的出现顺序
        int ans = -1;  //记录最终索引
        //循环用于对每个字符状态进行赋值
        for(int i=0;i<s.length();i++){
            if(dp[s.charAt(i)-'a'] == 0){
                dp[s.charAt(i)-'a'] = index;
                index ++;
            }else{
                dp[s.charAt(i)-'a'] = -1;
            }
        }
        //用于从dp[]中获取最早出现的一次字符ansC
        char ansC = '#';
        int cul = Integer.MAX_VALUE;
        for(int i=0;i<26;i++){
            if(dp[i]!=-1 && dp[i]!=0 && dp[i]<cul){
                cul = dp[i];
                ansC = (char) (i+'a');
            }
        }
        //用于从s中根据字符ansC找到其索引，即为结果ans
        for(int i=0;i<s.length();i++){
            if(s.charAt(i) == ansC){
                ans = i;
                break;
            }
        }
        //返回结果
        return ans;
    }
}
```
### 思路2：类动态规划？适合输出结果索引。
1. 边界处理。
2. dp[]用于记录每个字符出现的状态：
* 0表示未出现；
* 其他表示出现字符的出现次数。
3. 循环从s和dp[]中得到最先出现的字符坐标。
### 解法
```java
class Solution {
    public int firstUniqChar(String s) {
        if(s == null || s.length() == 0) return -1; //边界条件
        int dp[] = new int[26];
        int ans = -1;
        for(int i=0;i<s.length();i++){
            dp[s.charAt(i)-'a']++;
        }
        for(int i=0;i<s.length();i++){
            if(dp[s.charAt(i)-'a']==1){
                ans = i;
                break;
            }
        }
        return ans;
    }
}
}
```
<br><br>

## 455. 分发饼干
**假设你是一位很棒的家长，想要给你的孩子们一些小饼干。但是，每个孩子最多只能给一块饼干。对每个孩子 i，都有一个胃口值 g[i]，这是能让孩子们满足胃口的饼干的最小尺寸；并且每块饼干 j，都有一个尺寸 s[j] 。如果 s[j] >= g[i]，我们可以将这个饼干 j 分配给孩子 i ，这个孩子会得到满足。你的目标是尽可能满足越多数量的孩子，并输出这个最大数值。**<br>
示例：
```
输入: g = [1,2,3], s = [1,1]
输出: 1
解释: 
你有三个孩子和两块小饼干，3个孩子的胃口值分别是：1,2,3。
虽然你有两块小饼干，由于他们的尺寸都是1，你只能让胃口值是1的孩子满足。
所以你应该输出1。
```

### 思路1：双指针？贪心算法
1. 边界处理；
2. 数组排序；
3. 设置结果记录变量maxChi、左右指针l、r;
4. 当l和r同时满足小于数组长度时，进入while循环：
    * 如果当前**l对应的孩子胃口值**小于等于**饼干值**，则可以将其给孩子，同时maxChi++、l++，r++；
    * 如果当前**l对应的孩子胃口值**大于**饼干值**，则不能将其给任何孩子，同时需要r++。
5. 循环退出，说明已经无饼干或无孩子，直接输出此时结果即可。

### 解法
```java
class Solution {
    public int findContentChildren(int[] g, int[] s) {
        if(g.length == 0 || s.length == 0) return 0;
        Arrays.sort(g);
        Arrays.sort(s);
        int maxChi = 0;
        int l = 0, r = 0;
        while(l < g.length && r < s.length){
            if(g[l] <= s[r]){
                maxChi++;
                l++;
                r++;
            }else{
                r++;
            }
        }
        return maxChi;
    }
}
```
<br><br>

## 547. 省份数量
**有 n 个城市，其中一些彼此相连，另一些没有相连。如果城市 a 与城市 b 直接相连，且城市 b 与城市 c 直接相连，那么城市 a 与城市 c 间接相连。省份 是一组直接或间接相连的城市，组内不含其他没有相连的城市。给你一个 n x n 的矩阵 isConnected ，其中 isConnected[i][j] = 1 表示第 i 个城市和第 j 个城市直接相连，而 isConnected[i][j] = 0 表示二者直接相连。返回矩阵中省份的数量。**<br>

示例：
```
输入：isConnected = [[1,1,0],[1,1,0],[0,0,1]]
输出：2
```
```
输入：isConnected = [[1,0,0],[0,1,0],[0,0,1]]
输出：3
```

### 思路1：深度优先搜索
1. 建立状态记录，表示是否查询过当前城市，如果该城市尚未被访问过，则从该城市开始深度优先搜索；
2. 循环判断 state，若为 true 则 结果加一；
3. 进 dfs ，通过矩阵 isConnected 得到与该城市直接相连的城市有哪些，这些城市和该城市属于同一个连通分量，然后对这些城市继续深度优先搜索，直到同一个连通分量的所有城市都被访问到，即可得到一个省份。
4. 遍历完全部城市以后，即可得到连通分量的总数，即省份的总数。

### 解法
```java
class Solution {
    public int findCircleNum(int[][] isConnected) {
        boolean[] state = new boolean[isConnected.length];
        int count = 0;
        for(int i=0;i<isConnected.length;i++){
            if(!state[i]){
                dfs(isConnected,state,i);
                count++;
            }
        }
        return count;
    }
    private void dfs(int[][] isConnected,boolean[] state,int i){
        for(int j=0;j<isConnected[i].length;j++){
            if(!state[j] && isConnected[i][j] == 1){
                state[j] = true;
                dfs(isConnected,state,j);
            }
        }
    }
}
```
<br><br>

## 1018. 可被 5 整除的二进制前缀
**给定由若干 0 和 1 组成的数组 A。我们定义 N_i：从 A[0] 到 A[i] 的第 i 个子数组被解释为一个二进制数（从最高有效位到最低有效位）。返回布尔值列表 answer，只有当 N_i 可以被 5 整除时，答案 answer[i] 为 true，否则为 false。**<br>

示例1：
```
输入：[0,1,1]
输出：[true,false,false]
解释：
输入数字为 0, 01, 011；也就是十进制中的 0, 1, 3 。只有第一个数可以被 5 整除，因此 answer[0] 为真。
```


### 思路1：数学（注意 int 溢出）
1. 边界条件；
2. for 循环对每一个元素利用 2X + A[i] 计算：
    * 若用方法 1 ，则累加过多时 int 会溢出，造成结果错误；
    * 若用方法 2 ，在每次计算后都对结果进行除去 5 取余即可，不会出现溢出的情况。
3. 每次取余的结果为 0 ，则添加 true 进去，否则添加 false；
4. 输出结果即可。
### 解法
```java
class Solution {
    public List<Boolean> prefixesDivBy5(int[] A) {
        List<Boolean> answer = new ArrayList<>();
        if(A.length == 0)   return answer;
        int getValue = 0;
        for(int i=0;i<A.length;i++){
            /// 1溢出
            getValue = getValue * 2 + A[i]; 
            answer.add(getValue % 5 == 0);
            /// 2成功
            getValue = (getValue * 2 + A[i]) % 5; 
            answer.add(getValue == 0);
        }
        return answer;
    }
}
```


