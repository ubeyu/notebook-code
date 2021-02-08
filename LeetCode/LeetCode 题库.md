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
    - [628. 三个数的最大乘积](#628-三个数的最大乘积)
        - [笔记： Array.sort() 与 Collections.sort()](#笔记-arraysort-与-collectionssort)
        - [思路1：Array.sort()](#思路1arraysort)
        - [解法](#解法-8)
    - [665. 非递减数列](#665-非递减数列)
        - [思路1：数学判断](#思路1数学判断)
        - [解法](#解法-9)
    - [674. 最长连续递增序列](#674-最长连续递增序列)
        - [思路1：贪心算法](#思路1贪心算法)
        - [解法](#解法-10)
    - [724. 寻找数组的中心索引](#724-寻找数组的中心索引)
        - [思路1：类似双指针？](#思路1类似双指针)
        - [解法](#解法-11)
    - [778. 水位上升的泳池中游泳](#778-水位上升的泳池中游泳)
        - [思路1：二分查找 + BFS](#思路1二分查找--bfs)
        - [解法](#解法-12)
    - [978. 最长湍流子数组](#978-最长湍流子数组)
        - [思路1：快慢指针](#思路1快慢指针)
        - [解法](#解法-13)
    - [989. 数组形式的整数加法](#989-数组形式的整数加法)
        - [笔记： ArratList() 与 LinkedList()](#笔记-arratlist-与-linkedlist)
        - [思路1：ArrayList()](#思路1arraylist)
        - [解法](#解法-14)
        - [思路2：LinkedList()](#思路2linkedlist)
        - [解法](#解法-15)
    - [1018. 可被 5 整除的二进制前缀](#1018-可被-5-整除的二进制前缀)
        - [思路1：数学（注意 int 溢出）](#思路1数学注意-int-溢出)
        - [解法](#解法-16)
    - [1128. 等价多米诺骨牌对的数量](#1128-等价多米诺骨牌对的数量)
        - [注意：](#注意)
        - [思路1：哈希表](#思路1哈希表)
        - [解法](#解法-17)
        - [思路2：数组](#思路2数组)
        - [解法](#解法-18)
    - [1319. 连通网络的操作次数](#1319-连通网络的操作次数)
        - [思路1：并查集](#思路1并查集)
        - [解法](#解法-19)
    - [1423. 可获得的最大点数](#1423-可获得的最大点数)
        - [思路1：滑动窗口](#思路1滑动窗口)
        - [解法](#解法-20)
    - [1631. 最小体力消耗路径](#1631-最小体力消耗路径)
        - [注意](#注意)
        - [思路1：二分查找 + BFS思路？ 未写出来](#思路1二分查找--bfs思路-未写出来)
        - [解法](#解法-21)
        - [思路2：二分查找 + BFS](#思路2二分查找--bfs)
        - [解法](#解法-22)

<!-- /TOC -->


<!-- TOC -->
- **根据解题方法和思路分类**
    - 『数据类型』
        - 『数组』
            - [189. 旋转数组](#189-旋转数组)
            - [455. 分发饼干](#455-分发饼干)
            - [628. 三个数的最大乘积](#628-三个数的最大乘积)
            - [724. 寻找数组的中心索引](#724-寻找数组的中心索引)
            - [978. 最长湍流子数组](#978-最长湍流子数组)
            - [989. 数组形式的整数加法](#989-数组形式的整数加法)
            - [1128. 等价多米诺骨牌对的数量](#1128-等价多米诺骨牌对的数量)
        - 『矩阵/二维数组』
        - 『字符串』
            - [387.字符串中的第一个唯一字符](#387字符串中的第一个唯一字符)
        - 『字符流』
        - 『队列/堆栈』
            - [103.二叉树的锯齿形层序遍历](#103二叉树的锯齿形层序遍历)
        - 『链表』
            - [989. 数组形式的整数加法（ArrayList 和 LinkedList）](#989-数组形式的整数加法)
        - 『树』
            - [103.二叉树的锯齿形层序遍历](#103二叉树的锯齿形层序遍历)
        - 『哈希表』
            - [1128. 等价多米诺骨牌对的数量](#1128-等价多米诺骨牌对的数量)
        
    - 『算法』
        - 『位运算』
        - 『滑动窗口』
            - [1423. 可获得的最大点数](#1423-可获得的最大点数)
        - 『二分查找』
            - [778. 水位上升的泳池中游泳](#778-水位上升的泳池中游泳)
            - [1631. 最小体力消耗路径](#1631-最小体力消耗路径)
        - 『广度优先搜索 BFS 』
            - [778. 水位上升的泳池中游泳](#778-水位上升的泳池中游泳)
            - [1631. 最小体力消耗路径](#1631-最小体力消耗路径)
        - 『双/多指针』
            - [455. 分发饼干](#455-分发饼干)
            - [724. 寻找数组的中心索引](#724-寻找数组的中心索引)
            - [978. 最长湍流子数组](#978-最长湍流子数组)
            - [989. 数组形式的整数加法](#989-数组形式的整数加法)
        - 『双层循环』
            - [135.分发糖果](#135分发糖果)
        - 『排序算法』 
            - [628. 三个数的最大乘积](#628-三个数的最大乘积)
        - 『递归』
        - 『动态规划』
           - [123. 买卖股票的最佳时机 III](#123-买卖股票的最佳时机-iii)
           - [387.字符串中的第一个唯一字符](#387字符串中的第一个唯一字符)
        - 『数学』
            - [135.分发糖果](#135分发糖果)
            - [665. 非递减数列](#665-非递减数列)
        - 『二叉树遍历』
            - [103.二叉树的锯齿形层序遍历](#103二叉树的锯齿形层序遍历)
        - 『回溯法』  
        - 『贪心算法』    
           - [455. 分发饼干](#455-分发饼干)
        - 『并查集』    
            - [1319. 连通网络的操作次数](#1319-连通网络的操作次数) 

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

## 628. 三个数的最大乘积
**给定一个整型数组，在数组中找出由三个数组成的最大乘积，并输出这个乘积。**<br>

示例：
```
输入: [1,2,3]
输出: 6
```
```
输入: [1,2,3,4]
输出: 24
```
注意：
1. 给定的整型数组长度范围是[3,104]，数组中所有的元素范围是[-1000, 1000]。
2. 输入的数组中任意三个数的乘积不会超出32位有符号整数的范围。

### 笔记： Array.sort() 与 Collections.sort()
Java中常用的数组或集合排序的方法有两个：
* java.util.Arrays中的静态方法Arrays.sort()方法；
* java.util.Collections中的静态方法的Collections.sort()方法。
1. Arrays.sort()方法主要是针对各种数据类型（基本数据类型和引用对象类型）的数组元素排序。
2. Collection.sort()主要是针对集合框架中的动态数组，链表，树，哈希表等（ ArrayList、LinkedList、HashSet、LinkedHashSet、HashMap、LinkedHashMap ）进行排序。

### 思路1：Array.sort()
1. 边界条件；
2. 针对数组 Array.sort()；
3. 两种情况：
* 最后三个数相乘；
* 两个最小的负数相乘再乘以最大的正数；
4. 返回较大的那个即可。

### 解法
```java
import java.util.*;
class Solution {
    public int maximumProduct(int[] nums) {
        if(nums.length < 3) return 0;
        Arrays.sort(nums);
        return Math.max(nums[0]*nums[1]*nums[nums.length-1], nums[nums.length-3]*nums[nums.length-2]*nums[nums.length-1]);
    }
}
```
<br><br>

## 665. 非递减数列
**给你一个长度为 n 的整数数组，请你判断在 最多 改变 1 个元素的情况下，该数组能否变成一个非递减数列。我们是这样定义一个非递减数列的： 对于数组中所有的 i (0 <= i <= n-2)，总满足 nums[i] <= nums[i + 1]。**
<br>

示例：
```
输入: nums = [4,2,3]
输出: true
解释: 你可以通过把第一个4变成1来使得它成为一个非递减数列。
```

### 思路1：数学判断
1. 边界条件；
2. 通过分析可以发现，当我们发现后面的数字小于前面的数字产生冲突后：
    * [1]有时候需要修改前面较大的数字(比如前两个例子需要修改4)
    * [2]有时候却要修改后面较小的那个数字(比如前第三个例子需要修改2)
3. 返回即可。

### 解法
```java
class Solution {
    public boolean checkPossibility(int[] nums) {
        if(nums == null || nums.length <= 0)    return true;
        int flag = 0;
        for(int i=0;i<nums.length-1;i++){
            if(nums[i] > nums[i+1]){
                flag++;
                //如果首位不满足，则修改首位
                if(i == 0)  nums[i] = nums[i+1];
                //如果中间不满足，则继续判断 i+1 位置与 i-1 位置元素的大小关系，若i-1位置大，则必须修改 i+1 位置元素，才能保证修改后前面符合要求。
                else if(nums[i-1] > nums[i+1])  nums[i+1] = nums[i];
                //若 i-1 位置小，则也可修改 i 位置元素
                else nums[i] = nums[i-1];
            }
        }
        return flag <= 1 ? true:false;
    }
}
```
<br><br>

## 674. 最长连续递增序列
**给定一个未经排序的整数数组，找到最长且 连续递增的子序列，并返回该序列的长度。连续递增的子序列可以由两个下标 l 和 r（l < r）确定，如果对于每个 l <= i < r，都有 nums[i] < nums[i + 1] ，那么子序列 [nums[l], nums[l + 1], ..., nums[r - 1], nums[r]] 就是连续递增子序列。**

例如：
```
输入：nums = [1,3,5,4,7]
输出：3
解释：最长连续递增序列是 [1,3,5], 长度为3。
尽管 [1,3,5,7] 也是升序的子序列, 但它不是连续的，因为 5 和 7 在原数组里被 4 隔开。 
```

### 思路1：贪心算法
1. 边界处理。
2. 进循环：
* nums[i] < nums[i+1]时： len++，ans 取最大的len；
* nums[i] < nums[i+1]时： len = 1；
3. 返回ans。

### 解法
```java
class Solution {
    public int findLengthOfLCIS(int[] nums) {
        if(nums.length == 0)    return 0;
        int len = 1, ans = 1;
        for(int i=0;i<nums.length-1;i++){
            if(nums[i] < nums[i+1]){
                len ++;
                ans = Math.max(ans,len);
            }else{
                len = 1;
            }
        }
        return ans;
    }
}
```
<br><br>

## 724. 寻找数组的中心索引
**给定一个整数类型的数组 nums，请编写一个能够返回数组 “中心索引” 的方法。我们是这样定义数组 中心索引 的：数组中心索引的左侧所有元素相加的和等于右侧所有元素相加的和。如果数组不存在中心索引，那么我们应该返回 -1。如果数组有多个中心索引，那么我们应该返回最靠近左边的那一个。**

例如：
```
输入：
nums = [1, 7, 3, 6, 5, 6]
输出：3
解释：
索引 3 (nums[3] = 6) 的左侧数之和 (1 + 7 + 3 = 11)，与右侧数之和 (5 + 6 = 11) 相等。
同时, 3 也是第一个符合要求的中心索引。
```

### 思路1：类似双指针？
1. 边界处理；
2. 设置类似双指针：
    * 左边部分 l： 0 ；
    * 右边部分 r： 先对索引 i = 1 及后面所有元素求和 ；
3. 循环数组：
    * 如果左右部分相等，记录 i 值，退出循环；
    * 如果 i < nums.length-1 则对 l 加上当前元素，r 减去当前后面一个元素；
    * 如果 i == nums.length-1，且未达到相等退出条件，直接退出循环；
4. 返回索引即可。

### 解法
```java
class Solution {
    public int pivotIndex(int[] nums) {
        int index = -1;
        if(nums.length < 3) return index;
        int l = 0, r = 0;
        for(int i=1;i<nums.length;i++){
            r = r + nums[i];
        }
        for(int i=0;i<nums.length;i++){
            if(l == r){
                index = i;
                break;
            }else if(i < nums.length-1){
                l = l + nums[i];
                r = r - nums[i+1];
            }
        }
        return index;
    }
}
```
<br><br>

## 778. 水位上升的泳池中游泳
**在一个 N x N 的坐标方格 grid 中，每一个方格的值 grid[i][j] 表示在位置 (i,j) 的平台高度。现在开始下雨了。当时间为 t 时，此时雨水导致水池中任意位置的水位为 t 。你可以从一个平台游向四周相邻的任意一个平台，但是前提是此时水位必须同时淹没这两个平台。假定你可以瞬间移动无限距离，也就是默认在方格内部游动是不耗时的。当然，在你游泳的时候你必须待在坐标方格里面。你从坐标方格的左上平台 (0，0) 出发。最少耗时多久你才能到达坐标方格的右下平台 (N-1, N-1)？**

例如：
```
输入: [[0,2],[1,3]]
输出: 3
解释:
时间为0时，你位于坐标方格的位置为 (0, 0)。
此时你不能游向任意方向，因为四个相邻方向平台的高度都大于当前时间为 0 时的水位。

等时间到达 3 时，你才可以游向平台 (1, 1). 因为此时的水位是 3，坐标方格中的平台没有比水位 3 更高的，所以你可以游向坐标方格中的任意位置
```

### 思路1：二分查找 + BFS
1. 建立全局变量，记录方向数组：
```
private int[][] dir = {{-1,0},{1,0},{0,-1},{0,1}};
```
2. 边界条件；
3. 设置二分查找 l 和 r，进入 while 循环，注意：
    * 条件带 =
    * 左界限 l 设置为 左上角的值，因为最低要经过左上角值的时间
    * 右界限 r 设置为 最大值的 2 倍
4. 二分查找内，先获取 mid，然后初始化 Queue 队列，将左上角坐标加入，同时建立状态矩阵 flag，将第一个赋值为 true，表示已走过。
5. 进入队列非空时的循环，每次取出一个坐标，对其上下左右循环判断，若符合要求：
    * 0 <= 横坐标 < rows, 0 <= 纵坐标 < cols 
    * flag[横坐标][纵坐标] 状态为 false ，表示未走过
    * 精髓： grid[nx][ny] <= mid ，表示当前坐标的值小于等于这个 mid，求这个最小的 mid 即为答案
6. 符合要求后，对当前位置 flag 赋值 true，同时加入当前坐标到 queue；
7. 队列非空循环结束，若右下角为 true，表示经过，则再往左找最小，若不为 true，则将 mid 放大，找到可能的点；
8. 返回 l 即可。

### 解法
```java
class Solution {
    private int[][] dir = {{-1,0},{1,0},{0,-1},{0,1}};
    public int swimInWater(int[][] grid) {
        if(grid.length == 0 || grid[0].length == 0) return 0;
        int rows = grid.length, cols = grid[0].length;
        int l = grid[0][0], r = rows * rows * 2;
        while(l <= r){
            int mid = l + (r-l)/2;
            boolean[][] flag = new boolean[rows][cols];
            Queue<int[]> queue = new LinkedList<>();
            queue.offer(new int[]{0,0});
            flag[0][0] = true;
            while(!queue.isEmpty()){
                int[] index = queue.poll();
                int x = index[0], y = index[1];
                for(int i=0;i<4;i++){
                    int nx = x + dir[i][0];
                    int ny = y + dir[i][1];
                    if(nx>=0 && ny>=0 && nx<rows && ny<cols && !flag[nx][ny] && grid[nx][ny]<=mid){
                        flag[nx][ny] = true;
                        queue.offer(new int[]{nx,ny});
                    }
                }
            }          
            if(flag[rows-1][cols-1] == true){
                r = mid - 1;
            }else{
                l = mid + 1;
            }
        }
        return l;
    }
}
```
<br><br>

## 978. 最长湍流子数组
**当 A 的子数组 A[i], A[i+1], ..., A[j] 满足下列条件时，我们称其为湍流子数组：若 i <= k < j，当 k 为奇数时， A[k] > A[k+1]，且当 k 为偶数时，A[k] < A[k+1]；或 若 i <= k < j，当 k 为偶数时，A[k] > A[k+1] ，且当 k 为奇数时， A[k] < A[k+1]。也就是说，如果比较符号在子数组中的每个相邻元素对之间翻转，则该子数组是湍流子数组。返回 A 的最大湍流子数组的长度。**

例如：
```
输入：[9,4,2,10,7,8,8,1,9]
输出：5
解释：(A[1] > A[2] < A[3] > A[4] < A[5])
```

### 思路1：快慢指针
1. 建立快慢指针，同时初始化结果变量 ans；
```
int slow = 0, fast = 0, ans = 1;
```
2. 进入 while 循环，当快指针 **fast < 数组长度-1** 时：
* 若此时 **fast == slow**，则说明从此处开始，此时 **快指针 fast+1** 用于进一步判断；同时判断 **fast 与 fast+1** 索引下元素值是否相等，若相等则 **慢指针 slow+1**；
* 若此时 **fast != slow**，则说明从此时开始进入三数判断，法则为：
    1. arr[fast-1] > arr[fast] && arr[fast] < arr[fast+1]
    2. arr[fast-1] < arr[fast] && arr[fast] > arr[fast+1]
    
    若满足一次这种情况，说明最大湍流子数组长度增加 1。否则，将慢指针 slow 赋值为 fast。

3. 每次记录 ans = Math.max(ans, fast-slow+1);
4. 返回结果即可。

### 解法
```java
class Solution {
    public int maxTurbulenceSize(int[] arr) {
        int slow = 0, fast = 0, ans = 1;
        while(fast < arr.length-1){
            if(fast == slow){
                if(arr[fast] == arr[fast+1]){
                    slow++;
                }
                fast++;
            }else{
                if(arr[fast-1] > arr[fast] && arr[fast] < arr[fast+1]){
                    fast++;
                }else if(arr[fast-1] < arr[fast] && arr[fast] > arr[fast+1]){
                    fast++;
                }else{
                    slow = fast;
                }
            }
            ans = Math.max(ans, fast-slow+1);
        }
        return ans; 
    }
}
```
<br><br>

## 989. 数组形式的整数加法
**对于非负整数 X 而言，X 的数组形式是每位数字按从左到右的顺序形成的数组。例如，如果 X = 1231，那么其数组形式为 [1,2,3,1]。给定非负整数 X 的数组形式 A，返回整数 X+K 的数组形式。**<br>

示例：
```
输入：A = [1,2,0,0], K = 34
输出：[1,2,3,4]
解释：1200 + 34 = 1234
```
```
输入：A = [2,1,5], K = 806
输出：[1,0,2,1]
解释：215 + 806 = 1021
```
注意：
1. 给定的整型数组长度范围是[3,104]，数组中所有的元素范围是[-1000, 1000]。
2. 输入的数组中任意三个数的乘积不会超出32位有符号整数的范围。

### 笔记： ArratList() 与 LinkedList()
ArrayList是基于**数组**实现的，LinkedList是基于**双链表**实现的：
1. LinkedList类不仅是List接口的实现类，可以根据索引来随机访问集合中的元素，除此之外，LinkedList还实现了Deque接口，Deque接口是Queue接口的子接口，它代表一个双向队列，因此LinkedList可以作为双向队列 ，栈（可以参见Deque提供的接口方法）和List集合使用，功能强大。
2. 因为Array是基于索引(index)的数据结构，它使用索引在数组中搜索和读取数据是很快的，可以直接返回数组中index位置的元素，因此在随机访问集合元素上有较好的性能。Array获取数据的时间复杂度是O(1),但是要插入、删除数据却是开销很大的，因为这需要移动数组中插入位置之后的的所有元素。
3. 相对于ArrayList，LinkedList的随机访问集合元素时性能较差，因为需要在双向列表中找到要index的位置，再返回；但在插入，删除操作是更快的。因为LinkedList不像ArrayList一样，不需要改变数组的大小，也不需要在数组装满的时候要将所有的数据重新装入一个新的数组，这是ArrayList最坏的一种情况，时间复杂度是O(n)，而LinkedList中插入或删除的时间复杂度仅为O(1)。ArrayList在插入数据时还需要更新索引（除了插入数组的尾部）。
4. 对于本题 LinkedList() 方法而言，用到：
    * void addFirst(Object o) 在列表首部添加元素
    * void addLast(Object o) 在列表末尾添加元素
    * Object getFirst() 返回列表第一个元素
    * Object geLast() 返回列表最后一个元素
    * Object removeFirst() 删除列表中第一个元素
    * Object removeLast() 删除列表中最后一个元素

### 思路1：ArrayList()
1. 边界条件；
2. 第一个 for 循环对 A[] 数组处理，将 A 数组各个位赋值为与 K 对应位相加后的结果：
    * flag 表示是否有进位；
    * k_cop 表示 K 去掉后面 A.length 位后剩下的数； 
    * A[i] 表示处理后的结果后 A.length 位。
3. 第一个 while 循环用于获得此时 k_cop 剩下的位数：
    * ksub 表示剩下位数 + 1；
4. ksub 先除以 10，获得剩下位数，然后进第二个 while 循环，用于将 k_cop 按从最大位到最小位的顺序添加到 list 中；
5. 最后按照同样顺序添加 A[i] 到 list 中。
6. 返回结果即可。

### 解法
```java
class Solution {
    public List<Integer> addToArrayForm(int[] A, int K) {
        List<Integer> list = new ArrayList<>();
        if(A.length == 0)   return list;
        int flag = 0, k_cop = K;
        for(int i=A.length-1;i>=0;i--){
            int bit = A[i] + k_cop % 10 + flag;
            A[i] = bit % 10;
            flag = bit / 10;
            k_cop = k_cop / 10;
        }
        k_cop = k_cop + flag;
        int ksub = 1;
        while(k_cop / ksub != 0){
            ksub = ksub * 10;
        }
        ksub = ksub / 10;
        while(ksub != 0){
            list.add(k_cop / ksub);
            k_cop = k_cop % ksub;
            ksub = ksub / 10;
        }
        for(int a:A){
            list.add(a);
        }
        return list;
    }
}
```

### 思路2：LinkedList()
1. 边界条件；
2. 建立变量：
    * i 表示当前 A[] 的索引位；
    * flag 表示是否有进位；
    * k_cop 去掉后面 i 位后剩下的数；
3. 进 while 循环，条件为 i >= 0 或 k_cop > 0 或 flag > 0：
    * 建立 bit 记录当前 i 位置 K + flag 的值；
    * 若 A[] 在 i 位置还有数，则 bit 加这个数；
    * list 添加 bit % 10 到首位;
    * flag 为 bit / 10；
    * k_cop 为 k_cop / 10；
    * i --；
    * ksub 表示剩下位数 + 1；
4. 循环退出时，返回结果即可。

### 解法
```java
import java.util.*;
class Solution {
    public List<Integer> addToArrayForm(int[] A, int K) {
        // List<Integer> list = new LinkedList<>();
        // 注意报错:cannot find symbol。
        // 原因：addFirst 是子类的方法，必须显示声明
        LinkedList<Integer> list = new LinkedList<>();
        if(A.length == 0)   return list;
        int i = A.length-1, flag = 0, k_cop = K;
        while(i >= 0 || k_cop > 0 || flag > 0){
            int bit = k_cop % 10 + flag;
            if(i >= 0){
                bit = bit + A[i];
            }
            list.addFirst(bit % 10);
            flag = bit / 10;
            k_cop = k_cop / 10;
            i--;
        }
        return list;
    }
}
```

<br><br>

## 1018. 可被 5 整除的二进制前缀
**给定由若干 0 和 1 组成的数组 A。我们定义 N_i：从 A[0] 到 A[i] 的第 i 个子数组被解释为一个二进制数（从最高有效位到最低有效位）。返回布尔值列表 answer，只有当 N_i 可以被 5 整除时，答案 answer[i] 为 true，否则为 false。**<br>

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
<br><br>


## 1128. 等价多米诺骨牌对的数量
**给你一个由一些多米诺骨牌组成的列表 dominoes。如果其中某一张多米诺骨牌可以通过旋转 0 度或 180 度得到另一张多米诺骨牌，我们就认为这两张牌是等价的。形式上，dominoes[i] = [a, b] 和 dominoes[j] = [c, d] 等价的前提是 a==c 且 b==d，或是 a==d 且 b==c。在 0 <= i < j < dominoes.length 的前提下，找出满足 dominoes[i] 和 dominoes[j] 等价的骨牌对 (i, j) 的数量。**

示例1：
```
输入：dominoes = [[1,2],[2,1],[3,4],[5,6]]
输出：1
```

### 注意：
1. for(Integer i:map.values()) 可以用来循环 HashMap 的 value。
### 思路1：哈希表
1. 边界条件；
2. 建立哈希表，键 Integer 值 Integer ，循环：
    * key： [a,b]，a>b 则为 a×10+b，否则为 b×10+a（记录了翻转后相等的情况，一共 0-99/2 种）；
    * 若 map 包含 key，则 value 加一，否则 value 赋值为 1；
3. 结束后 map.values() 包含每种情况的元素数目，循环 map.values() 对每个数进行 **组合数C(N)(2)** 计算，结果相加；
4. 输出结果即可。
### 解法
```java
class Solution {
    public int numEquivDominoPairs(int[][] dominoes) {
        if(dominoes.length == 0 || dominoes.length == 1)    return 0;
        HashMap<Integer,Integer> map = new HashMap<>();
        for(int i=0;i<dominoes.length;i++){
            int key = dominoes[i][0] > dominoes[i][1] ? dominoes[i][0] * 10 + dominoes[i][1] : dominoes[i][1] * 10 + dominoes[i][0]; 
            if(map.containsKey(key)){
                map.put(key,map.get(key)+1);
            }else{
                map.put(key,1);
            }
        }
        int ans = 0;
        for(Integer i:map.values()){
            ans = ans + cul(i);
        }
        return ans;
    }
    private int cul(int n){
        return n*(n-1)/2;
    }
}
```

### 思路2：数组
1. 边界条件；
2. 建立数组 new int[100]，记录 0-99 种情况 ，循环：
    * 索引： [a,b]，a>b 则为 a×10+b，否则为 b×10+a（记录了翻转后相等的情况，一共 0-99/2 种）；
    * 每个对应索引的数组元素累加 1；
3. 结束后数组包含每种情况的数目，循环对每个元素进行 **组合数C(N)(2)** 计算，结果相加；
4. 输出结果即可。
### 解法
```java
class Solution {
    public int numEquivDominoPairs(int[][] dominoes) {
        if(dominoes.length == 0 || dominoes.length == 1)    return 0;
        int[] rec = new int[100];
        for(int i=0;i<dominoes.length;i++){
            int key = dominoes[i][0] > dominoes[i][1] ? dominoes[i][0] * 10 + dominoes[i][1] : dominoes[i][1] * 10 + dominoes[i][0]; 
            rec[key]++;
        }
        int ans = 0;
        for(Integer i:rec){
            ans = ans + cul(i);
        }
        return ans;
    }
    private int cul(int n){
        return n*(n-1)/2;
    }
}
```

<br><br>

## 1319. 连通网络的操作次数
**用以太网线缆将 n 台计算机连接成一个网络，计算机的编号从 0 到 n-1。线缆用 connections 表示，其中 connections[i] = [a, b] 连接了计算机 a 和 b。网络中的任何一台计算机都可以通过网络直接或者间接访问同一个网络中其他任意一台计算机。给你这个计算机网络的初始布线 connections，你可以拔开任意两台直连计算机之间的线缆，并用它连接一对未直连的计算机。请你计算并返回使所有计算机都连通所需的最少操作次数。如果不可能，则返回 -1。**<br>

示例1：
```
输入：n = 4, connections = [[0,1],[0,2],[1,2]]
输出：1
解释：拔下计算机 1 和 2 之间的线缆，并将它插到计算机 1 和 3 上。
```


### 思路1：并查集
1. 建立全局变量，记录父节点的数组：
```
private int[] parent;
```
2. 边界条件；
3. 赋值 parent[i] = i；
4. **union()** 方法根据 connections[][] 更新 parent 的值，找到每个节点的父节点：
    * 找到 root1 的根父节点
    * 找到 root2 的根父节点
    * 若相等，则属于同一联通分量，直接返回；若不相等，则将 root1 的父节点赋值为 root2
5. **find()** 方法用于找到当前节点的父节点：
    * parent[node] == node 返回 node；
    * parent[node] != node 赋值并返回 parent[node] = find(parent[node])；
6. 再次遍历 parent 对每个节点判断，记录联通分量的个数；
7. 输出结果为 **联通分量的个数 - 1** 即可。
### 解法
```java
class Solution {
    //建立记录父节点的数组
    private int[] parent;

    public int makeConnected(int n, int[][] connections) {
        if(connections.length < n-1)    return -1;
        //将每个节点的父节点赋值为自己
        parent = new int[n];
        for(int i=0;i<n;i++){
            parent[i] = i;
        }
        //遍历 connections，更新联通分量的信息
        for(int[] connection:connections){
            union(connection[0], connection[1]);
        }
        //count 用于记录联通分量的个数
        int count = 0;
        //对每个节点判断，记录联通分量的个数
        for(int i=0;i<n;i++){
            //4,[[0,1],[0,2],[1,2]] 
            //共4个节点：p[0]指向1，p[1]指向2，p[2]指向2，p[3]指向3
            //说明p[0],p[1],p[2]属于1个联通分量，p[3]属于1个联通分量
            //count = 2，所以电缆需要 2-1 = 1 根。
            if(parent[i] == i){
                count++;
            }
        }
        //返回联通分量的个数 - 1，即为需要移动的电缆数目
        return count-1;
    }
    private void union(int n1, int n2){
        //找到 root1 的根父节点
        int root1 = find(n1);
        //找到 root2 的根父节点
        int root2 = find(n2);
        //若相等，则属于同一联通分量，直接返回
        if(root1 == root2){
            return;
        }
        //若不相等，则将 root1 的父节点赋值为 root2
        parent[root1] = root2;
    }
    private int find(int node){
        //若当前节点的父节点指向自己，则返回自己；若不指向自己，则找到它的根父节点
        return parent[node] == node ? node : (parent[node] = find(parent[node]));
    }
}
```

<br><br>

## 1423. 可获得的最大点数
**几张卡牌 排成一行，每张卡牌都有一个对应的点数。点数由整数数组 cardPoints 给出。每次行动，你可以从行的开头或者末尾拿一张卡牌，最终你必须正好拿 k 张卡牌。你的点数就是你拿到手中的所有卡牌的点数之和。给你一个整数数组 cardPoints 和整数 k，请你返回可以获得的最大点数。**<br>

示例1：
```
输入：cardPoints = [1,2,3,4,5,6,1], k = 3
输出：12
解释：第一次行动，不管拿哪张牌，你的点数总是 1 。但是，先拿最右边的卡牌将会最大化你的可获得点数。最优策略是拿右边的三张牌，最终点数为 1 + 6 + 5 = 12 。
```


### 思路1：滑动窗口
**维护一个 len-k 的窗口，保证窗口里面和最小，然后剩余的 k 个数的和就是最大。**
1. 边界条件；
2. 建立窗口 win， 记录值 rec， 和 sum；
3. 遍历数组，每次累加一个元素，但：
* 若 i == win-1 时，记录 rec 为 rec，sum 中较小的值；
* 若 i > win-1 时，将 sum 减去时首部元素值，记录 rec 为 rec，sum 中较小的值；
4. 此时 rec 即为滑动窗口中最小的值，此时将总和减去此值即可。
5. 返回即可。
### 解法
```java
class Solution {
    public int maxScore(int[] cardPoints, int k) {
        if(cardPoints.length == 0) return 0; 
        int win = cardPoints.length - k;
        int rec = Integer.MAX_VALUE, sum = 0;
        for(int i=0;i<cardPoints.length;i++){
            sum = sum + cardPoints[i];
            if(i == win-1){
                rec = Math.min(rec, sum);
            }else if(i > win - 1){
                sum = sum - cardPoints[i-win];
                rec = Math.min(rec, sum);
            }
        }
        int all = 0;
        for(int cardPoint:cardPoints){
            all = all+cardPoint;
        }
        return all-rec;
    }
}
```

<br><br>

## 1631. 最小体力消耗路径
**你准备参加一场远足活动。给你一个二维 rows x columns 的地图 heights ，其中 heights[row][col] 表示格子 (row, col) 的高度。一开始你在最左上角的格子 (0, 0) ，且你希望去最右下角的格子 (rows-1, columns-1) （注意下标从 0 开始编号）。你每次可以往 上，下，左，右 四个方向之一移动，你想要找到耗费 体力 最小的一条路径。一条路径耗费的 体力值 是路径上相邻格子之间 高度差绝对值 的 最大值 决定的。请你返回从左上角走到右下角的最小 体力消耗值 。**<br>

示例1：
```
输入：heights = [[1,2,2],[3,8,2],[5,3,5]]
输出：2
解释：路径 [1,3,5,3,5] 连续格子的差值绝对值最大为 2 。
这条路径比路径 [1,2,2,2,5] 更优，因为另一条路径差值最大值为 3 。
```


### 注意
1. queue.offer(new int[]{0,0});

### 思路1：二分查找 + BFS思路？ 未写出来
1. 建立全局变量，记录父节点的数组：
```
private int[] parent;
```
2. 边界条件；
3. 赋值 parent[i] = i；
4. **union()** 方法根据 connections[][] 更新 parent 的值，找到每个节点的父节点：
    * 找到 root1 的根父节点
    * 找到 root2 的根父节点
    * 若相等，则属于同一联通分量，直接返回；若不相等，则将 root1 的父节点赋值为 root2
5. **find()** 方法用于找到当前节点的父节点：
    * parent[node] == node 返回 node；
    * parent[node] != node 赋值并返回 parent[node] = find(parent[node])；
6. 再次遍历 parent 对每个节点判断，记录联通分量的个数；
7. 输出结果为 **联通分量的个数 - 1** 即可。
### 解法
```java
class Solution {
    public int minimumEffortPath(int[][] heights) {
        int rows = heights.length, cols = rows == 0 ? 0 : heights[0].length;
        if(rows == 0 || cols == 0 )  return 0;
        int min = Integer.MAX_VALUE, max = 0;
        for(int i=0;i<rows;i++){
            for(int j=0;j<cols;j++){
                min = Math.min(min,heights[i][j]);
                max = Math.max(max,heights[i][j]);
            }
        }
        int l = 0 ,r = max - min;
        while(l < r){
            int mid = l + (r - l)/2;
            if(backTrackFlag(heights,heights[0][0],0,0,rows,cols,mid)){
                r = mid - 1;
            }else{
                l = mid + 1;
            }
        }
        return l; 
    }
    private boolean backTrackFlag(int[][] heights, int pre, int i, int j, int rows, int cols, int k){
        boolean[][] flag = new boolean[rows][cols];
        return backTrack(heights,heights[0][0],i,j,rows,cols,k,flag);
    }
    private boolean backTrack(int[][] heights, int pre, int i, int j, int rows, int cols, int k, boolean[][] flag){
        if(i<0 || j<0 || i>=rows || j>=cols || flag[i][j] == true ||  Math.abs(heights[i][j] - pre) > k){
            if(i>0 && j>0 && i<rows && j<cols && flag[i][j] == true){
                flag[i][j] = false;
            }
            return false;
        }
        flag[i][j] = true;
        if(i == rows - 1 && j == cols - 1) return true;
        return backTrack(heights, heights[i][j], i-1, j, rows, cols, k, flag) || 
            backTrack(heights, heights[i][j], i+1, j, rows, cols, k, flag) || 
            backTrack(heights, heights[i][j], i, j-1, rows, cols, k, flag) || 
            backTrack(heights, heights[i][j], i, j+1, rows, cols, k, flag);

    }
}
```

### 思路2：二分查找 + BFS
1. 建立全局变量，记录方向数组：
```
private int[][] dir = {{-1,0},{1,0},{0,-1},{0,1}};
```
2. 边界条件；
3. 设置二分查找 l 和 r，进入 while 循环，注意条件：
    * 条件带 =
    * 左界限 l 设置为 0
    * 右界限 r 设置为 最大值 - 0
4. 二分查找内，先获取 mid，然后初始化 Queue 队列，将左上角坐标加入，同时建立状态矩阵 flag，将第一个赋值为 true，表示已走过。
5. 进入队列非空时的循环，每次取出一个坐标，对其上下左右循环判断，若符合要求：
    * 0 <= 横坐标 < rows, 0 <= 纵坐标 < cols 
    * flag[横坐标][纵坐标] 状态为 false ，表示未走过
    * 精髓： Math.abs(heights[x][y] - heights[nx][ny]) <= mid ，表示走到的坐标与先前坐标的差的绝对值小于这个 mid，求这个最小的 mid 即为答案
6. 符合要求后，对当前位置 flag 赋值 true，同时加入当前坐标到 queue；
7. 队列非空循环结束，若右下角为 true，表示经过，则再往左找最小，若不为 true，则将 mid 放大，找到可能的点；
8. 返回 l 即可。
### 解法
```java
class Solution {
    private int[][] dir = {{-1,0},{1,0},{0,-1},{0,1}};

    public int minimumEffortPath(int[][] heights) {
        int rows = heights.length, cols = rows == 0 ? 0 : heights[0].length;
        if(rows == 0 || cols == 0 )  return 0;
        int l = 0 ,r = 999999;
        while(l <= r){
            int mid = l + (r - l)/2;
            Queue<int[]> queue = new LinkedList<>();
            queue.offer(new int[]{0,0});
            boolean[][] flag = new boolean[rows][cols];
            flag[0][0] = true;
            while(!queue.isEmpty()){
                int[] index = queue.poll();
                int x = index[0], y = index[1];
                for(int i=0;i<4;i++){
                    int nx = x + dir[i][0];
                    int ny = y + dir[i][1];
                    if(nx>=0 && ny>=0 && nx<rows && ny<cols && !flag[nx][ny] && Math.abs(heights[x][y] - heights[nx][ny]) <= mid){
                        flag[nx][ny] = true;
                        queue.offer(new int[]{nx,ny});
                    }
                }
            }    
            if(flag[rows-1][cols-1]){
                r = mid - 1;
            }else{
                l = mid + 1;
            }
        }
        return l; 
    }
}
```
