# 《剑指Offer》 ——题解

<!-- TOC -->

- [《剑指Offer》 ——题解](#剑指offer-题解)
    - [题目1：二维数组中的查找](#题目1二维数组中的查找)
        - [思路：类似二分查找思想](#思路类似二分查找思想)
        - [解法](#解法)
    - [题目2：替换空格](#题目2替换空格)
        - [思路：while循环处理](#思路while循环处理)
        - [解法](#解法-1)
    - [题目3：从尾到头打印链表](#题目3从尾到头打印链表)
        - [思路 1：递归](#思路-1递归)
        - [解法](#解法-2)
    - [题目4：重建二叉树](#题目4重建二叉树)
        - [思路 1：递归](#思路-1递归-1)
        - [解法](#解法-3)
    - [题目5：用两个栈实现队列](#题目5用两个栈实现队列)
        - [思路 1：栈先进后出，队列先进先出](#思路-1栈先进后出队列先进先出)
        - [解法](#解法-4)
    - [题目6：旋转数组的最小数字](#题目6旋转数组的最小数字)
        - [思路 1：二分查找](#思路-1二分查找)
        - [解法](#解法-5)
    - [题目7：斐波那契数列](#题目7斐波那契数列)
        - [理解：](#理解)
        - [思路 1：递归](#思路-1递归-2)
        - [解法：](#解法)
        - [思路 2：动态规划](#思路-2动态规划)
        - [解法：](#解法-1)
    - [题目8：跳台阶](#题目8跳台阶)
        - [思路 1：动态规划](#思路-1动态规划)
        - [解法：](#解法-2)
    - [题目9：变态跳台阶](#题目9变态跳台阶)
        - [思路 1：动态规划](#思路-1动态规划-1)
        - [解法：](#解法-3)
        - [思路 2：数学](#思路-2数学)
        - [解法：](#解法-4)
    - [题目10：矩形覆盖](#题目10矩形覆盖)
        - [理解：](#理解-1)
        - [思路 1：递归](#思路-1递归-3)
        - [解法：](#解法-5)
        - [思路 2：动态规划](#思路-2动态规划-1)
        - [解法：](#解法-6)
    - [★ 题目11：二进制中1的个数](#★-题目11二进制中1的个数)
        - [理解：](#理解-2)
        - [思路 1：位运算](#思路-1位运算)
        - [解法：](#解法-7)
    - [★ 题目12：数值的整数次方](#★-题目12数值的整数次方)
        - [理解：](#理解-3)
        - [思路 1：分类讨论](#思路-1分类讨论)
        - [官方解法：](#官方解法)
        - [模仿解法：](#模仿解法)
    - [题目13：调整数组顺序使奇数位于偶数前面](#题目13调整数组顺序使奇数位于偶数前面)
        - [理解：](#理解-4)
        - [思路 1：队列+遍历](#思路-1队列遍历)
    - [题目14：链表中倒数第k个结点](#题目14链表中倒数第k个结点)
        - [理解：](#理解-5)
        - [思路 1：快慢指针](#思路-1快慢指针)
        - [思路 2：先得到链表长度，再循环处理到倒数第k个](#思路-2先得到链表长度再循环处理到倒数第k个)
    - [题目15：反转链表](#题目15反转链表)
        - [理解：](#理解-6)
        - [思路 1：加 pre、node 和 临时节点tmp](#思路-1加-prenode-和-临时节点tmp)
    - [★ 题目16：合并两个排序的链表](#★-题目16合并两个排序的链表)
        - [理解：](#理解-7)
        - [思路 1：递归](#思路-1递归-4)
        - [思路 2：非递归](#思路-2非递归)
    - [题目17：树的子结构](#题目17树的子结构)
        - [理解：](#理解-8)
        - [思路 1：递归](#思路-1递归-5)
    - [题目18：二叉树的镜像](#题目18二叉树的镜像)
        - [理解：](#理解-9)
        - [思路 1：递归](#思路-1递归-6)
    - [题目19：顺时针打印矩阵](#题目19顺时针打印矩阵)
        - [思路 1：定义变量，依次循环](#思路-1定义变量依次循环)
    - [题目20：包含min函数的栈](#题目20包含min函数的栈)
        - [注意：](#注意)
        - [思路 1：利用数据栈、最小值栈两个栈解决，时间复杂度为O（1）](#思路-1利用数据栈最小值栈两个栈解决时间复杂度为o1)
    - [题目21：栈的压入、弹出序列](#题目21栈的压入弹出序列)
        - [思路 1：利用辅助栈解决](#思路-1利用辅助栈解决)
    - [题目22：从上往下打印二叉树 (二叉树的层序遍历)](#题目22从上往下打印二叉树-二叉树的层序遍历)
            - [关于 Queue 注意：](#关于-queue-注意)
        - [思路 1：非递归写法-利用队列 Queue](#思路-1非递归写法-利用队列-queue)
    - [题目23：二叉搜索树的后序遍历序列](#题目23二叉搜索树的后序遍历序列)
        - [思路 1：递归写法](#思路-1递归写法)
    - [题目24：二叉树中和为某一值的路径](#题目24二叉树中和为某一值的路径)
            - [注意：](#注意-1)
        - [思路 1：递归写法](#思路-1递归写法-1)
    - [题目25：复杂链表的复制](#题目25复杂链表的复制)
        - [思路 1：三步法：先复制，再处理随机节点，最后拆分](#思路-1三步法先复制再处理随机节点最后拆分)
    - [题目26：二叉搜索树与双向链表](#题目26二叉搜索树与双向链表)
        - [注意](#注意)
        - [思路 1：二叉树的中序遍历（递归）](#思路-1二叉树的中序遍历递归)
    - [题目27：字符串的排列](#题目27字符串的排列)
        - [思路：](#思路)
        - [知识点：](#知识点)
        - [解法1： 回溯法](#解法1-回溯法)
    - [题目28：数组中出现次数超过一半的数字](#题目28数组中出现次数超过一半的数字)
        - [解法1：哈希表](#解法1哈希表)
            - [思路：](#思路-1)
        - [解法2：候选法](#解法2候选法)
            - [思路：](#思路-2)
    - [题目29：最小的K个数](#题目29最小的k个数)
        - [解法1： Arrays.sort() 排序](#解法1-arrayssort-排序)
            - [思路：](#思路-3)
    - [题目30：连续子数组的最大和](#题目30连续子数组的最大和)
        - [解法1： 动态规划](#解法1-动态规划)
            - [思路：](#思路-4)
    - [题目31：整数中1出现的次数（从1到n整数中1出现的次数）](#题目31整数中1出现的次数从1到n整数中1出现的次数)
        - [解法1： 数学/按位计算](#解法1-数学按位计算)
            - [思路：](#思路-5)
    - [题目32：把数组排成最小的数](#题目32把数组排成最小的数)
        - [解法1： 回溯法（耗时太长）](#解法1-回溯法耗时太长)
            - [注意：](#注意-2)
            - [思路：](#思路-6)
        - [解法2： 冒泡排序](#解法2-冒泡排序)
            - [注意：](#注意-3)
            - [思路：](#思路-7)
    - [题目33：丑数](#题目33丑数)
        - [解法1： 多指针](#解法1-多指针)
            - [思路：](#思路-8)
    - [题目34：第一个只出现一次的字符](#题目34第一个只出现一次的字符)
        - [解法1： 哈希表（耗时太长）](#解法1-哈希表耗时太长)
            - [注意：](#注意-4)
            - [思路：](#思路-9)
        - [解法2： 双指针循环](#解法2-双指针循环)
            - [思路：](#思路-10)
    - [★ 题目35：数组中的逆序对](#★-题目35数组中的逆序对)
        - [解法：归并排序](#解法归并排序)
            - [思路：](#思路-11)
    - [题目36：两个链表的第一个公共结点](#题目36两个链表的第一个公共结点)
        - [解法1：遍历链表(O(n^2))](#解法1遍历链表on^2)
            - [思路：](#思路-12)
        - [解法2：双指针(O(2n))](#解法2双指针o2n)
            - [思路：](#思路-13)
    - [题目37：数字在排序数组中出现的次数](#题目37数字在排序数组中出现的次数)
        - [思路：](#思路-14)
        - [解法1： 二分查找](#解法1-二分查找)
            - [注意：](#注意-5)
            - [思路：](#思路-15)
    - [题目38：二叉树的深度](#题目38二叉树的深度)
        - [解法1： 递归](#解法1-递归)
            - [思路：](#思路-16)
        - [解法2： 层序遍历](#解法2-层序遍历)
            - [思路：](#思路-17)
    - [题目39：平衡二叉树](#题目39平衡二叉树)
        - [解法1： 两层递归](#解法1-两层递归)
            - [思路：](#思路-18)
        - [解法2： 一层递归](#解法2-一层递归)
            - [思路：先序遍历](#思路先序遍历)
    - [题目40：数组中只出现一次的数字](#题目40数组中只出现一次的数字)
        - [解法1： 哈希表](#解法1-哈希表)
            - [注意：](#注意-6)
            - [思路：](#思路-19)
    - [题目41：和为S的连续正数序列](#题目41和为s的连续正数序列)
        - [解法1： 双层循环](#解法1-双层循环)
            - [注意：](#注意-7)
            - [思路：](#思路-20)
        - [解法2： 双指针](#解法2-双指针)
            - [思路：](#思路-21)
    - [题目42：和为S的两个数字](#题目42和为s的两个数字)
            - [注意：](#注意-8)
        - [解法1： 双指针加入乘积判断：11ms](#解法1-双指针加入乘积判断11ms)
            - [思路：](#思路-22)
        - [解法2： 双指针：不用判断，利用 “因为 a 和 b 和一定， a 和 b 相差越多，乘积越小”](#解法2-双指针不用判断利用-因为-a-和-b-和一定-a-和-b-相差越多乘积越小)
            - [思路：](#思路-23)
    - [题目43：左旋转字符串](#题目43左旋转字符串)
            - [注意：](#注意-9)
        - [解法1： 循环每一位调整位置。](#解法1-循环每一位调整位置)
            - [思路：](#思路-24)
    - [题目44：翻转单词顺序列](#题目44翻转单词顺序列)
            - [注意：](#注意-10)
        - [解法1： 双指针，由最右侧开始循环存放每个单词到 list。](#解法1-双指针由最右侧开始循环存放每个单词到-list)
            - [思路：](#思路-25)
    - [题目45：扑克牌顺子](#题目45扑克牌顺子)
            - [注意：](#注意-11)
        - [解法1： 双指针，由最右侧开始循环存放每个单词到 list。](#解法1-双指针由最右侧开始循环存放每个单词到-list-1)
            - [思路：](#思路-26)
    - [题目46：孩子们的游戏(圆圈中最后剩下的数)](#题目46孩子们的游戏圆圈中最后剩下的数)
        - [解法1： list（耗时过长）或链表](#解法1-list耗时过长或链表)
            - [思路：](#思路-27)
    - [题目47：求1+2+3+...+n](#题目47求123n)
        - [解法1：递归](#解法1递归)
            - [思路：](#思路-28)
    - [题目48：不用加减乘除做加法](#题目48不用加减乘除做加法)
        - [解法1：!!! 位运算做加法 !!!](#解法1-位运算做加法-)
            - [思路：](#思路-29)
    - [题目49：把字符串转换成整数](#题目49把字符串转换成整数)
        - [解法1：字符串/循环判断](#解法1字符串循环判断)
            - [思路：](#思路-30)
    - [题目50：数组中重复的数字](#题目50数组中重复的数字)
        - [解法1：哈希表](#解法1哈希表-1)
            - [思路：](#思路-31)
    - [题目51：构建乘积数组](#题目51构建乘积数组)
        - [解法1：二层循环](#解法1二层循环)
            - [思路：](#思路-32)
        - [解法2：左右循环](#解法2左右循环)
            - [思路：](#思路-33)
    - [题目54：字符流中第一个不重复的字符](#题目54字符流中第一个不重复的字符)
        - [解法1：字符流处理](#解法1字符流处理)
            - [思路：](#思路-34)
    - [题目55：链表中环的入口结点](#题目55链表中环的入口结点)
        - [解法1：哈希表](#解法1哈希表-2)
            - [思路：](#思路-35)
    - [题目56：删除链表中重复的结点](#题目56删除链表中重复的结点)
        - [解法1：链表处理，定义 head,pre,last 三个节点进行操作。](#解法1链表处理定义-headprelast-三个节点进行操作)
            - [思路：](#思路-36)
    - [题目57：二叉树的下一个结点](#题目57二叉树的下一个结点)
        - [解法1：递归中序遍历](#解法1递归中序遍历)
            - [思路：](#思路-37)
    - [题目58：对称的二叉树](#题目58对称的二叉树)
        - [解法1：层序遍历](#解法1层序遍历)
            - [思路：](#思路-38)
        - [解法2：递归](#解法2递归)
            - [思路：](#思路-39)
    - [题目59：按之字形顺序打印二叉树](#题目59按之字形顺序打印二叉树)
        - [解法1：层序遍历 + 双堆栈](#解法1层序遍历--双堆栈)
            - [思路：](#思路-40)
    - [题目60：把二叉树打印成多行](#题目60把二叉树打印成多行)
        - [解法1：层序遍历](#解法1层序遍历-1)
            - [思路：](#思路-41)
    - [题目61：序列化二叉树](#题目61序列化二叉树)
        - [注意](#注意-1)
        - [解法1：前序遍历](#解法1前序遍历)
            - [思路：](#思路-42)
    - [题目62：二叉搜索树的第k个结点](#题目62二叉搜索树的第k个结点)
        - [解法1：中序遍历（全部遍历）](#解法1中序遍历全部遍历)
            - [思路：](#思路-43)
        - [解法2：中序遍历（部分遍历）](#解法2中序遍历部分遍历)
            - [思路：](#思路-44)
    - [题目63：数据流中的中位数](#题目63数据流中的中位数)
        - [注意：优先队列/大/小顶堆](#注意优先队列大小顶堆)
        - [解法1：优先队列/大/小顶堆](#解法1优先队列大小顶堆)
            - [思路：](#思路-45)
    - [题目64：滑动窗口的最大值](#题目64滑动窗口的最大值)
        - [解法1：双循环](#解法1双循环)
            - [思路：](#思路-46)
    - [题目65：矩阵中的路径](#题目65矩阵中的路径)
        - [解法1：回溯法](#解法1回溯法)
            - [思路：](#思路-47)
    - [题目66：机器人的运动范围](#题目66机器人的运动范围)
        - [解法1：回溯法](#解法1回溯法-1)
            - [思路：](#思路-48)
    - [题目67：剪绳子](#题目67剪绳子)
        - [解法1：数学](#解法1数学)
            - [思路：](#思路-49)

<!-- /TOC -->


<!-- TOC -->
- **根据解题方法和思路分类**
    - 『数据类型』
        - 『数组』
            - [题目23：二叉搜索树的后序遍历序列](#题目23二叉搜索树的后序遍历序列)
            - [题目28：数组中出现次数超过一半的数字](#题目28数组中出现次数超过一半的数字)
            - [题目29：最小的K个数](#题目29最小的k个数)
            - [题目30： 连续子数组的最大和](#题目30-连续子数组的最大和)
            - [题目33：丑数](#题目33丑数)
        - 『矩阵/二维数组』
            - [题目19：顺时针打印矩阵](#题目19顺时针打印矩阵)
            - [题目64：滑动窗口的最大值](#题目64滑动窗口的最大值)
        - 『字符串』
            - [题目2：替换空格](#题目2替换空格)
            - [题目34：第一个只出现一次的字符](#题目34第一个只出现一次的字符)
            - [题目43：左旋转字符串](#题目43左旋转字符串)
            - [题目44：翻转单词顺序列](#题目44翻转单词顺序列)
        - 『字符流』
            - [题目54：字符流中第一个不重复的字符](#题目54字符流中第一个不重复的字符)
        - 『队列/堆栈』
            - [题目5：用两个栈实现队列](#题目5用两个栈实现队列)
            - [题目13：调整数组顺序使奇数位于偶数前面](#题目13调整数组顺序使奇数位于偶数前面)
            - [题目20：包含min函数的栈](#题目20包含min函数的栈)
            - [题目21：栈的压入、弹出序列](#题目21栈的压入弹出序列)
            - [题目22：从上往下打印二叉树 (二叉树的层序遍历)](#题目22从上往下打印二叉树-二叉树的层序遍历)
            - [题目38：二叉树的深度](#题目38二叉树的深度)
            - [题目59：按之字形顺序打印二叉树](#题目59按之字形顺序打印二叉树)
        - 『PriorityQueue优先队列/堆』
            - [题目63：数据流中的中位数](#题目63数据流中的中位数)
        - 『链表』
            - [题目3：从尾到头打印链表](#题目3从尾到头打印链表)
            - [题目14：链表中倒数第k个结点](#题目14链表中倒数第k个结点)
            - [题目15：反转链表](#题目15反转链表)
            - [题目25：复杂链表的复制](#题目25复杂链表的复制)
            - [题目26：二叉搜索树与双向链表](#题目26二叉搜索树与双向链表)
            - [题目36：两个链表的第一个公共结点](#题目36两个链表的第一个公共结点)
            - [题目46：孩子们的游戏(圆圈中最后剩下的数)](#题目46孩子们的游戏圆圈中最后剩下的数)
            - [题目55：链表中环的入口结点](#题目55链表中环的入口结点)
            - [题目56：删除链表中重复的结点](#题目56删除链表中重复的结点)
        - 『树』
            - [题目4：重建二叉树](#题目4重建二叉树)
            - [题目17：树的子结构](#题目17树的子结构)
            - [题目18：二叉树的镜像](#题目18二叉树的镜像)
            - [题目26：二叉搜索树与双向链表](#题目26二叉搜索树与双向链表)
            - [题目38：二叉树的深度](#题目38二叉树的深度)
            - [题目57：二叉树的下一个结点](#题目57二叉树的下一个结点)
            - [题目62：二叉搜索树的第k个结点](#题目62二叉搜索树的第k个结点)
        - 『哈希表』
            - [题目34：第一个只出现一次的字符](#题目34第一个只出现一次的字符)
            - [题目40：数组中只出现一次的数字](#题目40数组中只出现一次的数字)
    - 『算法』
        - 『位运算』
            - [题目48：不用加减乘除做加法](#题目48不用加减乘除做加法)
        - 『二分查找』
            - [题目1：二维数组中的查找](#题目1二维数组中的查找)
            - [题目6：旋转数组的最小数字](#题目6旋转数组的最小数字)
            - [题目37：数字在排序数组中出现的次数](#题目37数字在排序数组中出现的次数)
        - 『双/多指针』
            - [题目33：丑数](#题目33丑数)
            - [题目34：第一个只出现一次的字符](#题目34第一个只出现一次的字符)
            - [题目36：两个链表的第一个公共结点](#题目36两个链表的第一个公共结点)
            - [题目41：和为S的连续正数序列](#题目41和为s的连续正数序列)
            - [题目42：和为S的两个数字](#题目42和为s的两个数字)
            - [题目44：翻转单词顺序列](#题目44翻转单词顺序列)
            - [题目45：扑克牌顺子](#题目45扑克牌顺子)
            - [题目51：构建乘积数组](#题目51构建乘积数组)
        - 『双层循环』
            - [题目36：两个链表的第一个公共结点](#题目36两个链表的第一个公共结点)
            - [题目41：和为S的连续正数序列](#题目41和为s的连续正数序列)
            - [题目51：构建乘积数组](#题目51构建乘积数组)
            - [题目64：滑动窗口的最大值](#题目64滑动窗口的最大值)
            - [题目65：矩阵中的路径](#题目65矩阵中的路径)
        - 『排序算法』 
            - [题目32：把数组排成最小的数](#题目32把数组排成最小的数)
        - 『归并排序』 
            - [★ 题目35：数组中的逆序对](#★-题目35数组中的逆序对)
        - 『递归』
            - [题目3：从尾到头打印链表](#题目3从尾到头打印链表)
            - [题目4：重建二叉树](#题目4重建二叉树)
            - [题目17：树的子结构](#题目17树的子结构)
            - [题目18：二叉树的镜像](#题目18二叉树的镜像)
            - [题目23：二叉搜索树的后序遍历序列](#题目23二叉搜索树的后序遍历序列)
            - [题目38：二叉树的深度](#题目38二叉树的深度)
            - [题目47：求1+2+3+...+n](#题目47求123n)
            - [题目57：二叉树的下一个结点](#题目57二叉树的下一个结点)
            - [题目58：对称的二叉树](#题目58对称的二叉树)
            - [题目60：把二叉树打印成多行](#题目60把二叉树打印成多行)
            - [题目61：序列化二叉树](#题目61序列化二叉树)
            - [题目62：二叉搜索树的第k个结点](#题目62二叉搜索树的第k个结点)
        - 『动态规划』
            - [题目7：斐波那契数列](#题目7斐波那契数列)
            - [题目9：变态跳台阶](#题目9变态跳台阶)
            - [题目30： 连续子数组的最大和](#题目30-连续子数组的最大和)
        - 『数学』
            - [题目9：变态跳台阶](#题目9变态跳台阶)
            - [★ 题目11：二进制中1的个数](#★-题目11二进制中1的个数)
            - [★ 题目12：数值的整数次方](#★-题目12数值的整数次方)
            - [题目31：整数中1出现的次数（从1到n整数中1出现的次数）](#题目31整数中1出现的次数从1到n整数中1出现的次数)
            - [题目41：和为S的连续正数序列](#题目41和为s的连续正数序列)
            - [题目67：剪绳子](#题目67剪绳子)
        - 『二叉树遍历』
            - [题目22：从上往下打印二叉树 (二叉树的层序遍历)](#题目22从上往下打印二叉树-二叉树的层序遍历)
            - [题目23：二叉搜索树的后序遍历序列](#题目23二叉搜索树的后序遍历序列)
            - [题目26：二叉搜索树与双向链表](#题目26二叉搜索树与双向链表)
            - [题目38：二叉树的深度](#题目38二叉树的深度)
            - [题目58：对称的二叉树](#题目58对称的二叉树)
            - [题目59：按之字形顺序打印二叉树](#题目59按之字形顺序打印二叉树)
            - [题目60：把二叉树打印成多行](#题目60把二叉树打印成多行)
            - [题目61：序列化二叉树](#题目61序列化二叉树)
            - [题目62：二叉搜索树的第k个结点](#题目62二叉搜索树的第k个结点)
        - 『回溯法』   
            - [题目27：字符串的排列](#题目27字符串的排列)
            - [题目32： 把数组排成最小的数](#题目32-把数组排成最小的数)
            - [题目65：矩阵中的路径](#题目65矩阵中的路径)
            - [题目66：机器人的运动范围](#题目66机器人的运动范围)
            

<!-- /TOC -->


<br><br><br><br><br><br>

## 题目1：二维数组中的查找
**在一个二维数组中（每个一维数组的长度相同），每一行都按照从左到右递增的顺序排序，每一列都按照从上到下递增的顺序排序。请完成一个函数，输入这样的一个二维数组和一个整数，判断数组中是否含有该整数。**

### 思路：类似二分查找思想

[小]-->>[增]-->>[B]<br>
[A]-->>[增]-->>[大]

选择从 A 或者 B 开始，类似二分查找的思想，循环查找是否有与 target 相等的：
1. 若当前值与 t 正好相等，则返回 true；
2. 若当前值小于 t，则 col++； 
3. 若当前值大于 t，则 row--； 
### 解法
```java
public class Solution {
    public boolean Find(int target, int [][] array){
        if(array.length == 0 || array[0].length == 0){
            return false;
        }
        int row = array.length - 1 ,col = 0;
        while(row >= 0 && col < array[0].length){
            if(array[row][col] == target) return true; 
            else if(array[row][col] > target) row--;
            else col++;
        }
        return false;
    }
}
```
<br><br>

## 题目2：替换空格
**请实现一个函数，将一个字符串中的每个空格替换成“%20”。例如，当字符串为We Are Happy.则经过替换之后的字符串为We%20Are%20Happy。**
###  思路：while循环处理
注意：<br>
1. StringBuffer 方法 sb.replace(i,i+1,string str) 将 sb 的索引 i~i+1 部分替换为 str；
2. str.toString().replace(" ", "%20");//直接将所有空格替换
### 解法
```java
public class Solution {
    public String replaceSpace(StringBuffer str){
        String rep = "%20";
        int i = 0;
        while(i < str.length()){
            if( str.charAt(i) == ' '){
                str.replace(i,i+1,rep);
                i = i+2;
            }else{
                i++;
            }
        }
        return str.toString();
    }
}
```
<br><br>

## 题目3：从尾到头打印链表
**输入一个链表，按链表从尾到头的顺序返回一个ArrayList。**
###  思路 1：递归
注意：<br>
1. 递归每次处理的是当前节点，而非下一个！ 
2. 在**类内**的**方法**外面声明字段！
###  解法
```java
/**
*    public class ListNode {
*        int val;
*        ListNode next = null;
*
*        ListNode(int val) {
*            this.val = val;
*        }
*    }
*
*/
import java.util.ArrayList;
public class Solution {
    private ArrayList<Integer> ans = new ArrayList<>();
    public ArrayList<Integer> printListFromTailToHead(ListNode listNode){
        if(listNode != null){
            printListFromTailToHead(listNode.next);
            ans.add(listNode.val);
        }
        return ans;
    }
}
```
<br><br>

## 题目4：重建二叉树
**输入某二叉树的前序遍历和中序遍历的结果，请重建出该二叉树。假设输入的前序遍历和中序遍历的结果中都不含重复的数字。例如输入前序遍历序列{1,2,4,7,3,5,6,8}和中序遍历序列{4,7,2,1,5,3,8,6}，则重建二叉树并返回。**

###  思路 1：递归
1. java Arrays.copyOfRange使用方法：
* original：第一个参数为要拷贝的数组对象
* from：第二个参数为拷贝的开始位置（包含）
* to：第三个参数为拷贝的结束位置（不包含） <br>
使用（左闭右开）：
```java
public class Test {
    public static void main(String[] args) {
        int[] array = {0, 1, 2, 3, 4, 5, 6};
        int[] array2 = Arrays.copyOfRange(array, 2, 4); //注意4位置是不包含的
        System.out.println(Arrays.toString(array2)); //[2, 3]
    }
}
```
2. pre 的第一位为根，将 pre 和 in 按照这个跟分左子树和右子树，做相应处理。
###  解法
```java
/**
 * Definition for binary tree
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
import java.util.*;
public class Solution {
    public TreeNode reConstructBinaryTree(int [] pre,int [] in) {
        if(pre.length == 0 || in.length == 0) return null;
        TreeNode node = new TreeNode(pre[0]);
        for(int i = 0;i < in.length; i++){
            if(pre[0] == in[i]){
                node.left = reConstructBinaryTree(Arrays.copyOfRange(pre, 1,i+1),Arrays.copyOfRange(in, 0,i));
                node.right = reConstructBinaryTree(Arrays.copyOfRange(pre, i+1,pre.length),Arrays.copyOfRange(in, i+1,in.length));
                break;
            }
        }
        return node;
    }
}
```
<br><br>

## 题目5：用两个栈实现队列
用两个栈来实现一个队列，完成队列的Push和Pop操作。 队列中的元素为int类型。
###  思路 1：栈先进后出，队列先进先出
注意：<br>
1. 利用 stack1 push() 存放；
2. 利用 stack2 pop() 取出，此时分两种情况：
    * 若 stack2 为空，则需要填充，利用 while 循环将 stack1 中元素全部填入 stack2，此时正好由先进后出变为先进先出；
    * 若 stack2 不为空，则上次填充完的还没全部出来，可以直接让 stack2 元素出栈，即代表队列取首元素。
###  解法
```java
import java.util.Stack;

public class Solution {
    Stack<Integer> stack1 = new Stack<Integer>();
    Stack<Integer> stack2 = new Stack<Integer>();
    
    public void push(int node) {
        stack1.push(node);
    }
    
    public int pop() {
        if(stack2.isEmpty()){
            while(!stack1.isEmpty()){
                stack2.push(stack1.pop());
            }
        }
        return stack2.pop();
    }
}
```
<br><br>

## 题目6：旋转数组的最小数字
**把一个数组最开始的若干个元素搬到数组的末尾，我们称之为数组的旋转。输入一个非递减排序的数组的一个旋转，输出旋转数组的最小元素。NOTE：给出的所有元素都大于0，若数组大小为0，请返回0。**
###  思路 1：二分查找
注意：<br>
1. 新建 l、r、mid 三个 int 型变量，mid 在 while 循环内赋值；
2. 考虑输出值的索引使用 l、r 还是 mid？
###  解法
```java
import java.util.ArrayList;
public class Solution {
    public int minNumberInRotateArray(int [] array){
        if(array.length == 0) return 0;
        int l = 0 , r = array.length-1;
        while(l < r){
            int mid = l + (r-l) /2;
            if(array[mid] > array[r]) l = mid + 1;
            else r = mid;
        }
        return array[r];
    }
}
```

<br><br>

## 题目7：斐波那契数列
**大家都知道斐波那契数列，现在要求输入一个整数n，请你输出斐波那契数列的第n项（从0开始，第0项为0，第1项是1）。**
n<=39。**
### 理解：
斐波那契数列： 0 1 1 2 3 5 8 ...

前两项为0 1，后面项为前面两项的和。
### 思路 1：递归
注意：<br>
1. 处理前两项，如果 n = 0或1，则直接返回对应结果；
2. 处理后面项，如果 n ≠ 0或1，则递归返回 F(n-1)+F(n-2)。
3. 优点，代码简单好写，缺点：慢，会超时。
###  解法：
```java
public class Solution {
    public int Fibonacci(int n) {
        if(n == 0 || n == 1) return n == 0 ? 0 : 1;
        return Fibonacci(n-1) + Fibonacci(n-2);
    }
}
```
### 思路 2：动态规划
注意：<br>
1. 处理前两项，如果 n = 0或1，则直接返回对应结果；
2. 处理后面项，如果 n > 1，则循环赋值 dp；
3. 返回 dp[n]；
4. 如果想让时间/空间继续优化，那就用动态规划，优化掉递归栈空间。方法二是从上往下递归的然后再从下往上回溯的，最后回溯的时候来合并子树从而求得答案。
###  解法：
```java
public class Solution {
    public int Fibonacci(int n) {
        if(n == 0 || n == 1) return n;
        int dp[] = new int[n+1];
        dp[0] = 0;
        dp[1] = 1;  //一定要处理前两项再赋值，不然不存在dp[1]。
        for(int i = 2;i <= n;i++){
            dp[i] = dp[i-1] + dp[i-2];
        }
        return dp[n];
    }
}
```

<br><br>

## 题目8：跳台阶
**一只青蛙一次可以跳上1级台阶，也可以跳上2级。求该青蛙跳上一个n级的台阶总共有多少种跳法（先后次序不同算不同的结果）。**

### 思路 1：动态规划
注意：<br>
1. 处理前两项，如果 n = 0或1，则直接返回对应结果：一层一种，二层两种；
2. 处理后面项，如果 n ≠ 0或1，则到该位置的方式有两种：
* 前面一个进一步
* 前面二个进两步（前面二个进1+1，属于前面一个的那种情况）<br>
> 即可以表示为：F(n-1) + F(n-2)

###  解法：
```java
public class Solution {
    public int JumpFloor(int target) {
        if(target == 1 || target == 2) return target;
        int dp[] = new int[target+1];
        dp[1] = 1;
        dp[2] = 2;
        for(int i = 3 ; i <= target; i++){
            dp[i] = dp[i-1] + dp[i-2];
        }
        return dp[target];
    }
}
```

<br><br>

## 题目9：变态跳台阶
**一只青蛙一次可以跳上1级台阶，也可以跳上2级……它也可以跳上n级。求该青蛙跳上一个n级的台阶总共有多少种跳法。**

### 思路 1：动态规划
注意：<br>
1. dp[i] 代表跳到第 i 层所有的跳法总数；
2. dp[i] 就等于 i 前面所有的dp值相加 ＋ 1：

###  解法：
```java
public class Solution {
    public int JumpFloorII(int target) {
        int dp[] = new int[target+1];
        for(int i = 1;i <= target; i++){
            int ans = 0;
            for(int j = 0 ; j < target; j++){
                ans = ans + dp[j];
            }
            dp[i] = ans + 1;
        }
        return dp[target];
    }
}
```

### 思路 2：数学
注意：<br>
1. 找规律：到每层的方法数为 2 ^ (target - 1) 种。

###  解法：
```java
public class Solution {
    public int JumpFloorII(int target) {
        return 1 << (target - 1);
    }
}
```
或：
```java
public class Solution {
    public int JumpFloorII(int target) {
        return (int) Math.pow(2, target - 1);
    }
}
```
<br><br>

## 题目10：矩形覆盖
**我们可以用2×1的小矩形横着或者竖着去覆盖更大的矩形。请问用n个2*1的小矩形无重叠地覆盖一个2*n的大矩形，总共有多少种方法？**<br>
### 理解：
类似斐波那契数列，在 n 大于 2 时，当前方法数 = n-1时种数＋ n-2时种数。
### 思路 1：递归
###  解法：
```java
public class Solution {
    public int RectCover(int target) {
        if(target <= 0) return 0;
        else if(target == 1 || target == 2 ) return target == 1 ? 1:2;
        else return RectCover(target-1) + RectCover(target -2);
    }
}
```
### 思路 2：动态规划
###  解法：
```java
public class Solution {
    public int RectCover(int target) {
        if(target <= 0) return 0;
        else if(target == 1 || target ==2) return target;
        int dp[] = new int[target+1];
        dp[0] = 0;
        dp[1] = 1;
        dp[2] = 2;
        for(int i = 3; i<=target; i++){
            dp[i] = dp[i-1] +dp[i-2];
        }
        return dp[target];
    }
}
```
<br><br>

## ★ 题目11：二进制中1的个数
**输入一个整数，输出该数32位二进制表示中1的个数。其中负数用补码表示。**<br>
### 理解：
如果一个整数不为0，那么这个整数至少有一位是1。如果我们把这个整数减1，那么原来处在整数最右边的1就会变为0，原来在1后面的所有的0都会变成1(如果最右边的1后面还有0的话)。其余所有位将不会受到影响。

举个例子：一个二进制数1100，从右边数起第三位是处于最右边的一个1。减去1后，第三位变成0，它后面的两位0变成了1，而前面的1保持不变，因此得到的结果是1011.我们发现减1的结果是把最右边的一个1开始的所有位都取反了。这个时候如果我们再把原来的整数和减去1之后的结果做与运算，从原来整数最右边一个1那一位开始所有位都会变成0。如1100&1011=1000.也就是说，把一个整数减去1，再和原整数做与运算，会把该整数最右边一个1变成0.那么一个整数的二进制有多少个1，就可以进行多少次这样的操作。

### 思路 1：位运算
###  解法：
```java
public class Solution {
    public int NumberOf1(int n) {
        int ans = 0;
        while(n != 0){
            ans++;
            n = n & (n-1);
        }
        return ans;
    }
}
```
<br><br>

## ★ 题目12：数值的整数次方
**给定一个double类型的浮点数base和int类型的整数exponent，求base的exponent次方。保证base和exponent不同时为0。**
### 理解：
 * 1.全面考察指数的正负、底数是否为零等情况。
 * 2.写出指数的二进制表达，例如13表达为二进制1101。
 * 3.举例:10^1101 = 10^0001×10^0100×10^1000。
 * 4.通过&1和>>1来逐位读取1101，为1时将该位代表的乘数累乘到最终结果。


### 思路 1：分类讨论
###  官方解法：
```java
public class Solution {
    public double Power(double base, int exponent) {
        double res = 1,curr = base;
        int n = exponent;
        if(n==0){
            return 1;// 0的0次方
        }else if(n<0){
            if(base==0)
                throw new RuntimeException("分母不能为0"); 
            exponent = -n;
        }
        while(exponent!=0){
            if((exponent&1)==1)
                res = res * curr;
            curr= curr * curr;// 翻倍
            exponent= exponent >> 1;// 右移一位
        }
        return n>=0?res:(1/res); 
  }
}
```
###  模仿解法：
```java
public class Solution {
    public double Power(double base, int exponent) {
        double ans = 1, cur = base;
        int n = exponent;
        if(exponent == 0){
            return 1;
        }else if(exponent < 0){
            if(base == 0) 
                throw new RuntimeException("分母为零");
            n = - exponent;
        }
        while(n != 0){
            if((n&1)== 1)
                ans = ans * cur;
            cur = cur * cur;
            n = n >> 1;
        }
        return exponent < 0 ? 1/ans:ans;
  }
}
```
<br><br>

## 题目13：调整数组顺序使奇数位于偶数前面
**输入一个整数数组，实现一个函数来调整该数组中数字的顺序，使得所有的奇数位于数组的前半部分，所有的偶数位于数组的后半部分，并保证奇数和奇数，偶数和偶数之间的相对位置不变。**
### 理解：
1. 使用队列，先进先出记录偶数值；
2. 使用flag，记录前面全部为奇数的位置索引；
3. 先对数组进行一次循环，分别处理三种情况：
* 当前值为偶数，存入队列；
* 当前值为奇数，且队列为空，flag加一；
* 当前值为奇数，且队列不为空，将当前flag位置赋值为该奇数，flag加一。
4. while 队列不为空，依次将数组后半部分按照进队列的顺序赋值偶数值。

### 思路 1：队列+遍历
```java
import java.util.*;
public class Solution {
    public void reOrderArray(int [] array) {
        Queue<Integer> queue = new LinkedList<Integer>();
        int flag = 0;
        for(int i=0; i<array.length;i++){
            if(array[i] % 2 == 0){
                queue.offer(array[i]);
            }else if(array[i] % 2 != 0 && !queue.isEmpty()){
                array[flag] = array[i];
                flag++;
            }else if(array[i] % 2 != 0 && queue.isEmpty()){
                flag++;
            }
        }
        while(!queue.isEmpty()){
            array[flag] = queue.poll();
            flag++;
        }        
    }
}
```
<br><br>

## 题目14：链表中倒数第k个结点
**输入一个链表，输出该链表中倒数第k个结点。**
### 理解：
1. 示例

输入
> 1,{1,2,3,4,5}

返回值
> {5}
2. 注意
* 一定处理 k > 链表长度 的情况，输出 null。

### 思路 1：快慢指针
```java
/*
public class ListNode {
    int val;
    ListNode next = null;

    ListNode(int val) {
        this.val = val;
    }
}*/
public class Solution {
    public ListNode FindKthToTail(ListNode head,int k){
        ListNode fast = head,slow = head; //快指针遍历链表，同时k--；
        while(fast != null){
            if(k<=0) slow = slow.next;    //当k<=0时，慢指针开始前进；
            fast = fast.next;
            k--;
        }
        return k<=0? slow:null;  //遍历结束，慢指针到的位置即是倒数第k个节点位置。
    }
}
```
### 思路 2：先得到链表长度，再循环处理到倒数第k个
```java
/*
public class ListNode {
    int val;
    ListNode next = null;

    ListNode(int val) {
        this.val = val;
    }
}*/
public class Solution {
    public ListNode FindKthToTail(ListNode head,int k) {
        ListNode test = head;
        int length = 0;
        while(test != null){
            length++;              //先遍历得到链表长度；
            test = test.next;
        }
        if(k>length) return null;  //若k大于链表长度，直接返回null；
        ListNode ans = head;
        for(int i=0;i<length-k;i++){  
            ans = ans.next;       //若k不大于链表长度，则找到倒数第k个节点。
        }
        return ans;
    }
}
```
<br><br>

## 题目15：反转链表
**输入一个链表，反转链表后，输出新链表的表头。**
### 理解：
1. 示例

输入
> {1,2,3}

返回值
> {3,2,1}

### 思路 1：加 pre、node 和 临时节点tmp
```java
/*
public class ListNode {
    int val;
    ListNode next = null;

    ListNode(int val) {
        this.val = val;
    }
}*/
public class Solution {
    public ListNode ReverseList(ListNode head) {
        ListNode pre = null , node = head;
        ListNode tmp;
        while(node != null){
            tmp = node.next;
            node.next = pre;
            pre = node;
            node = tmp;
        }
        return pre;
    }
}
```
<br><br>

## ★ 题目16：合并两个排序的链表
**输入一个链表，反转链表后，输出新链表的表头。**
### 理解：
1. 示例

输入
> {1,3,5},{2,4,6}

返回值
> {1,2,3,4,5,6}

### 思路 1：递归
递归处理两个链表：
1. 若当前有节点为空，则返回不为空的节点即可，递归结束；
2. 若当前节点不为空，则判断值的大小，将值较小的节点指向*较大节点*和*较小节点的下一个节点*为参数的递归处理结果。
```java
/*
public class ListNode {
    int val;
    ListNode next = null;

    ListNode(int val) {
        this.val = val;
    }
}*/
public class Solution {
    public ListNode Merge(ListNode list1,ListNode list2){
        if(list1 == null || list2 == null) return list1 == null ? list2:list1;
        if(list1.val > list2.val) {
            list2.next = Merge(list1,list2.next);
            return list2;
        }
        else{
            list1.next = Merge(list1.next,list2);
            return list1;
        }

    }
}
```
### 思路 2：非递归
非递归处理两个链表：
1. 建立 node1、node2 从而不使用 list，建立 ans、node 用于输出结果；
2. 若当前节点全部不为，则判断值的大小，将 node 的下一个节点指向值较小的节点，同时该节点前进一位；
3. 当有一个节点为空，判断是哪一个，然后将 node 的下一个节点指向不为空的那个；
4. 输出 ans.next；
```java
/*
public class ListNode {
    int val;
    ListNode next = null;

    ListNode(int val) {
        this.val = val;
    }
}*/
public class Solution {
    public ListNode Merge(ListNode list1,ListNode list2){
        ListNode node1 = list1;
        ListNode node2 = list2;
        ListNode ans = new ListNode(-1);
        ListNode node = ans;
        while(node1 != null && node2 != null){
            if(node1.val > node2.val) {
                node.next = node2;
                node2 = node2.next;
            }else{
                node.next = node1;
                node1 = node1.next;
            }
            node = node.next;
        }
        if(node1 == null){
            node.next = node2;
        }else if(node2 ==null){
            node.next = node1;
        }
        return ans.next;
    }
}
```

<br><br>

## 题目17：树的子结构
**输入两棵二叉树A，B，判断B是不是A的子结构。（ps：我们约定空树不是任意一个树的子结构）。**
### 理解：
1. 示例

输入
> {8,8,#,9,#,2,#,5},{8,9,#,2}

返回值
> true

### 思路 1：递归
递归处理两个二叉树：
* **HashSubtree() 方法**，用于找到与子树根节点值相同的节点，然后进入 judgeSub() 方法进一步判断：
    1. 首先设置递归退出条件：判断 root1 和 root2 是否为空，为空说明**子树为空**或**父树的左或右支不存在相等节点**，则直接返回 false；
    2. 如果当前父树的**根节点**或**左或右支节点**与子树根节点相等，则以**父树中的相等节点**和**子树根节点**为参数，进入判断方法，判断以此节点为根节点是否与子树相等。
* **judgeSub() 方法**，用于判断以当前节点为根节点和子树根节点形成的树是否相等：
    1. 递归退出条件：若 root2 为空，则不影响相等，返回 true；
    2. 递归退出条件：若 root2 不为空，而此时 root1 为空，则说明不等，不是子树，返回 false；
    3. 都不为空，判断两节点值是否相等：若相等，则递归判断各自的左右节点是否相等；
    4. 若不相等，则此条路线不通，返回 false。
```java
/**
public class TreeNode {
    int val = 0;
    TreeNode left = null;
    TreeNode right = null;

    public TreeNode(int val) {
        this.val = val;
    }
}
*/
public class Solution {
    public boolean HasSubtree(TreeNode root1,TreeNode root2) {
        if(root1 == null || root2 == null)  return false;
        if(root1.val == root2.val){
            return judgeSub(root1,root2);  
        }
        return HasSubtree(root1.left,root2) || HasSubtree(root1.right,root2);
    }
    private boolean judgeSub(TreeNode root1,TreeNode root2){
        if(root2 == null){
            return true;
        }
        if(root1 == null){
            return false;
        }
        if(root1.val == root2.val){
            return judgeSub(root1.left,root2.left) && judgeSub(root1.right,root2.right);
        }
        return false;
    }
}
```


<br><br>

## 题目18：二叉树的镜像
**操作给定的二叉树，将其变换为源二叉树的镜像。**
输入描述:
```
 二叉树的镜像定义：  源二叉树: 
                               8
                             /  \
                            6   10
                           / \  / \
                          5  7  9 11
                   镜像二叉树:
                               8
                             /  \
                            10   6
                           / \  / \
                          11  9 7  5
```
### 理解：
1. 示例

输入
> {1,3,5},{2,4,6}

返回值
> {1,2,3,4,5,6}

### 思路 1：递归
1. 首先设置递归退出条件，若当前节点为空，则不处理直接返回；
2. 然后从根节点开始，调换其左右节点，然后对其左右节点再分别调用 Mirror 方法，直到下属节点都为空。
```java
/**
public class TreeNode {
    int val = 0;
    TreeNode left = null;
    TreeNode right = null;

    public TreeNode(int val) {
        this.val = val;

    }
}
*/
public class Solution {
    public void Mirror(TreeNode root) {
        if(root == null) return ;
        TreeNode tmp = root.left;
        root.left = root.right;
        root.right = tmp;
        Mirror(root.left);
        Mirror(root.right);
    }
}
```

<br><br>

## 题目19：顺时针打印矩阵
**输入一个矩阵，按照从外向里以顺时针的顺序依次打印出每一个数字，例如，如果输入如下4 X 4矩阵： 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 则依次打印出数字1,2,3,4,8,12,16,15,14,13,9,5,6,7,11,10。**
### 思路 1：定义变量，依次循环
1. 定义 a、b、c、d 分别代表参与循环的矩阵左、右、上、下索引；
2. 依 "上→右→下→左" 的顺序循环打印数组，每次循环结束判断是否越界，越界跳出循环；
3. 输出。
```java
import java.util.ArrayList;
public class Solution {
    public ArrayList<Integer> printMatrix(int [][] matrix) {
        ArrayList<Integer> list = new ArrayList<>();
        int a = 0 ,b = matrix.length-1;
        int c = 0 ,d = matrix[0].length-1;
        while(true){
            for(int i=c;i<=d;i++){
                list.add(matrix[a][i]);
            }
            a = a+1;
            if(a>b) break;
            for(int i=a;i<=b;i++){
                list.add(matrix[i][d]);
            }
            d = d-1;
            if(d<c) break;
            for(int i=d;i>=c;i--){
                list.add(matrix[b][i]);
            }
            b = b-1;
            if(b<a) break;
            for(int i=b;i>=a;i--){
                list.add(matrix[i][c]);
            }
            c = c+1;
            if(c>d) break;
        }
        return list;
    }
}
```

<br><br>  
  
## 题目20：包含min函数的栈
**定义栈的数据结构，请在该类型中实现一个能够得到栈中所含最小元素的min函数（时间复杂度应为O（1））。**
### 注意：
1. stack.peek() 与 stack.pop() 的区别：
* 相同点：大家都返回栈顶的值；
* 不同点：peek() 不改变栈的值（不删除栈顶的值），pop() 会把栈顶的值删除。

### 思路 1：利用数据栈、最小值栈两个栈解决，时间复杂度为O（1）
1. 定义 data、min 分别代表数据栈、最小值栈；
2. push 时：data 直接存入；min 判断是否为空，空直接存入，非空则节点值小于等于时才存入；
3. pop 时：同时输出；
4. top 时：data.peek() 输出栈顶值；
5. min 时： min.peek() 输出最小值。
```java
import java.util.Stack;

public class Solution {

    Stack<Integer> data = new Stack<>();
    Stack<Integer> min = new Stack<>();

    public void push(int node) {
        data.push(node);
        if(min.isEmpty()){
            min.push(node);
        }else{
            min.push(node > min.peek() ? min.peek():node);
        }
    }
    
    public void pop() {
        data.pop();  
        min.pop();
    }
    
    public int top() {
        return data.peek();
    }
    
    public int min() {
        return min.peek();
    }
}
```

<br><br>  
  
## 题目21：栈的压入、弹出序列
**输入两个整数序列，第一个序列表示栈的压入顺序，请判断第二个序列是否可能为该栈的弹出顺序。假设压入栈的所有数字均不相等。例如序列1,2,3,4,5是某栈的压入顺序，序列4,5,3,2,1是该压栈序列对应的一个弹出序列，但4,3,5,1,2就不可能是该压栈序列的弹出序列。（注意：这两个序列的长度是相等的）。**

### 思路 1：利用辅助栈解决
1. 定义 stack 分别代表辅助栈；
2. 对压栈数组 pushA 循环，每次将对应索引元素压栈；
3. 同时循环判断 若栈不为空且栈顶元素与出栈数组 popA 当前 p 索引元素相等，则该元素出栈，索引值 p 加一；
4. 循环结束，若辅助栈为空，则出栈数组合理，返回 true，若不为空，则 false。
```java
import java.util.Stack;
public class Solution {
    public boolean IsPopOrder(int [] pushA,int [] popA) {
        Stack<Integer> stack = new Stack<>();
        int p = 0;
        for(int i=0;i<pushA.length;i++){
            stack.push(pushA[i]);
            while(!stack.isEmpty() && stack.peek() == popA[p]){
                stack.pop();
                p++;
            }
        }
        return stack.isEmpty();
    }
}
```
<br><br>  
  
## 题目22：从上往下打印二叉树 (二叉树的层序遍历)
**从上往下打印出二叉树的每个节点，同层节点从左至右打印。**

#### 关于 Queue 注意：
1. 队列 Queue 是一种特殊的线性表，LinkedList类实现了Queue接口。  
2. 队列操作时：
    * add： 增加一个元索。如果队列已满，则抛出一个IIIegaISlabEepeplian异常。
    * remove： 移除并返回队列头部的元素。如果队列为空，则抛出一个NoSuchElementException异常。
    * element： 返回队列头部的元素。如果队列为空，则抛出一个NoSuchElementException异常。
    * offer： 添加一个元素并返回true。如果队列已满，则返回false。
    * poll： 移除并返问队列头部的元素。如果队列为空，则返回null。
    * peek： 返回队列头部的元素。如果队列为空，则返回null。
    * put： 添加一个元素。如果队列满，则阻塞。
    * take： 移除并返回队列头部的元素。如果队列为空，则阻塞。
    
### 思路 1：非递归写法-利用队列 Queue
1. 定义 ArrayList 用于结果返回，root 为空时直接返回；
2. 建立 Queue 用于层序遍历，依次存放每层的元素；
3. 第一个 While 循环即代表当队列不为空时，一直遍历，同时每次进入这个循环时，用 size 记录该层的元素数量；
4. 当 size 大于 0 时，每次取一个元素，将其值添加到结果 list 中，同时判断左右节点是否需要添加进队列 queue，记得size--；
5. 循环结束，输出 list 即可。
```java
import java.util.*;
/**
public class TreeNode {
    int val = 0;
    TreeNode left = null;
    TreeNode right = null;
    
    public TreeNode(int val) {
        this.val = val;
    }
}
二叉树的层序遍历
*/
public class Solution {
    public ArrayList<Integer> PrintFromTopToBottom(TreeNode root) {
        ArrayList<Integer> list = new ArrayList<>();
        if(root == null) return list;
        Queue<TreeNode> queue = new LinkedList<>();
        queue.offer(root);
        while(!queue.isEmpty()){
            int size = queue.size();
            while(size > 0){
                TreeNode node = queue.poll();
                list.add(node.val);
                if(node.left != null) queue.offer(node.left);
                if(node.right != null) queue.offer(node.right);
                size--;
            }
        }
        return list;
    }

}
```
<br><br> 

## 题目23：二叉搜索树的后序遍历序列
**输入一个整数数组，判断该数组是不是某二叉搜索树的后序遍历的结果。如果是则返回true,否则返回false。假设输入的数组的任意两个数字都互不相同。**

### 思路 1：递归写法
BST后序序列的合法序列是：
对于一个序列S，最后一个元素是x（也就是根），如果去掉最后一个元素的序列为T，那么T满足完美的递归定义：
* T可以分成两段，前一段（左子树）小于x，后一段（右子树）大于x；
* 且这两段（子树）都是合法的后序序列。
1. 先判断 sequence 长度，为 0 则直接返回 false；
2. 进入递归，参数为 序列sequence、左索引l 、右索引r；
3. 递归内：
    * 首先设置退出条件，如果 左 >= 右，则说明遍历完毕，都符合二叉搜索树条件。
    * 若未退出，则从0索引开始，记录**sequence最后一位（根）**，先循环至**sequence大于等于根的节点（左子树）**，记录此位置，然后再判断**到根之前的（右子树）**是否存在小于根的，若存在则返回false；
    * 若以上循环都完成，说明以当前 r 为根的序列符合二叉搜索树的合法定义，此时再去判断其左子树和右子树，注意用 && 相连。
4. 递归完全结束，若未在某一步输出 false，则符合二叉搜索树。
```java
public class Solution {
    public boolean VerifySquenceOfBST(int [] sequence) {
        if(sequence.length == 0) return false;
        return VerifySTree(sequence,0,sequence.length-1);
    }
    private boolean VerifySTree(int [] sequence,int l,int r){
        if(l >= r) return true;
        int root = sequence[r];
        int i = 0;
        while(sequence[i] < root){
            i++;
        }
        int iRec = i;
        for(; i<r; i++){
            if(sequence[i] < root){
                return false;
            }
        }
        return VerifySTree(sequence,0,iRec-1) && VerifySTree(sequence,iRec,r-1);
    }
}
```
<br><br> 

## 题目24：二叉树中和为某一值的路径
**输入一颗二叉树的根节点和一个整数，按字典序打印出二叉树中结点值的和为输入整数的所有路径。路径定义为从树的根结点开始往下一直到叶结点所经过的结点形成一条路径。**
输入
> {10,5,12,4,7},22

返回值
> [[10,5,7],[10,12]]

#### 注意：
1. 虽然使用了全局变量，但每次放入 lists 要新建一个：
```
lists.add(new ArrayList(list));
```
2. list的remove()方法，该方法有两个：
* 一个是remove(Object obj)，会删除list中的第一个该元素；
* 一个是remove(int index)，会删除该下标的元素。
* 调用一次remove方法，会使list中的所有该删除元素后面的元素前移。

### 思路 1：递归写法
1. 新建lists、list两个ArrayList，首先边界条件判断；
2. 递归内：
    * 首先设置退出条件，设置退出条件为边界条件判断的条件；
    * 若未退出，则首先添加当前根的值进list，同时target减去此值，判断target是否为0 && 左右节点是否为空，若全部满足，则添加此list进lists；
    * 若不为0，将其root.left/root.right放入递归；
    * 同时，在每个list结束remove最后一个元素。
3. 返回 lists。
```java
import java.util.ArrayList;
/**
public class TreeNode {
    int val = 0;
    TreeNode left = null;
    TreeNode right = null;

    public TreeNode(int val) {
        this.val = val;
    }
}
*/
public class Solution {
    private ArrayList<ArrayList<Integer>> lists = new ArrayList<>();
    private ArrayList<Integer> list = new ArrayList<>();
    public ArrayList<ArrayList<Integer>> FindPath(TreeNode root,int target) {
        if(root == null) return lists;
        list.add(root.val);
        target = target - root.val;
        if(target == 0 && root.left == null && root.right == null){
            lists.add(new ArrayList(list)); //每次放入要新建一个
        }
        FindPath(root.left,target);
        FindPath(root.right,target);
        list.remove(list.size()-1);
        return lists;
    }
}
```
<br><br> 

## 题目25：复杂链表的复制
**输入一个复杂链表（每个节点中有节点值，以及两个指针，一个指向下一个节点，另一个特殊指针random指向一个随机节点），请对此链表进行深拷贝，并返回拷贝后的头结点。（注意，输出结果中请不要返回参数中的节点引用，否则判题程序会直接返回空）。**

### 思路 1：三步法：先复制，再处理随机节点，最后拆分
1. 定义 copy 节点用于将每个节点按顺序进行复制；
2. 循环判断每个节点是否有随机节点，有的话将其**下个节点的随机节点**赋值为**随机节点的下个节点**；
3. 循环拆分偶数节点和奇数节点，奇数节点为复制结果；
4. 注意在拆分前保存 RandomListNode ans = pHead.next，因为拆分后无法从 pHead 找到了。
```java
/*
public class RandomListNode {
    int label;
    RandomListNode next = null;
    RandomListNode random = null;

    RandomListNode(int label) {
        this.label = label;
    }
}
*/
public class Solution {
    public RandomListNode Clone(RandomListNode pHead){
        if(pHead == null) return null;
        RandomListNode node = pHead;
        while(node != null){
            RandomListNode copy = new RandomListNode(node.label);
            copy.next = node.next;
            node.next = copy;
            node = copy.next;            
        }
        node = pHead;
        while(node!=null){
            if(node.random != null){
                 node.next.random =  node.random.next;
            }
            node = node.next.next;
        }
        node = pHead;
        RandomListNode ans = pHead.next;
        while(node!=null){
            RandomListNode tmp = node.next;
            node.next = tmp.next;
            tmp.next = tmp.next==null? null:tmp.next.next;
            node = node.next;
        }
        return ans;
    }
}
```
<br><br> 

## 题目26：二叉搜索树与双向链表
**输入一棵二叉搜索树，将该二叉搜索树转换成一个排序的双向链表。要求不能创建任何新的结点，只能调整树中结点指针的指向。**

### 注意
1. 二叉树的递归中序遍历；
2. 中序遍历后的逐次赋值，从 i=0 到 i=size()-1:
* **当前元素节点**的右指针指向**下个元素节点**；
* **下个元素节点**的左节点指向**当前元素节点**；

### 思路 1：二叉树的中序遍历（递归）
1. 边界条件判断；
2. 先遍历将元素添加到 list；
3. 根据list将每个元素转化：左指针代表上个元素，右指针代表下个元素。
4. 返回list.get(0);
```java
/**
public class TreeNode {
    int val = 0;
    TreeNode left = null;
    TreeNode right = null;

    public TreeNode(int val) {
        this.val = val;
    }
}
*/
import java.util.*;
public class Solution {
    public TreeNode Convert(TreeNode pRootOfTree) {
        if(pRootOfTree == null) return pRootOfTree;
        ArrayList<TreeNode> list = new ArrayList<>();
        Inorder(pRootOfTree,list);
        ConvertList(list);
        return list.get(0);
    }
    //中序遍历
    private void Inorder(TreeNode node,ArrayList<TreeNode> list){
        if(node == null){
            return;
        }
        Inorder(node.left,list);
        list.add(node);
        Inorder(node.right,list);
    }
    //按照list重新排序
    private void ConvertList(ArrayList<TreeNode> list) {
        for(int i=0;i<list.size()-1;i++){
            list.get(i).right = list.get(i+1);
            list.get(i+1).left = list.get(i);
        }
    }
}
```
<br><br>

## 题目27：字符串的排列

**输入一个字符串,按字典序打印出该字符串中字符的所有排列。例如输入字符串abc,则按字典序打印出由字符a,b,c所能排列出来的所有字符串abc,acb,bac,bca,cab和cba。**

> 输入一个字符串,长度不超过9(可能有字符重复),字符只包括大小写字母。

### 思路：

1. 建立 ArrayList<> 集合用于输出答案，判断字符串是否为空，若为空直接返回 lists，若不为空则调用 Process() 处理；

2. Process() 参数分别为：由字符串转为的字符数组、存放结果的 lists、当前索引 i；

3. Process() 采用**回溯法**，首先判断是否满足退出条件，若索引 i 到达字符数组最后一位，则判断当前字符串是否在结果 lists 中，若不在则添加，若在则退出；若不满足退出条件，则开始循环处理：定义 j=i，当 j<字符数组长度时，利用 swap() 方法交换 i 与 j 位置的字符，同时回溯调用 Process()，此时的参数为：交换字符位置后的字符数组、存放结果的 lists、当前索引 i +1；处理完毕后，再次调用 swap() 将字符换回；

4. swap() 方法参数为：字符数组、索引 i、索引 j。作用就是交换 i、j 位置的字符；

5. 利用这种方法得到的顺序为：                // 括号内为 (i,j) ，P(,,i+1)

   ```makefile
   1.交换 (0,0)，调用 P(,,1)； 		 //此时为"abc"
   
   ​	交换 (1,1)，调用 P(,,2)；      //此时为"abc"
   
   ​		满足退出条件，添加 "abc"；
   
   ​	换回 (1,1)；
   
   ​	交换 (1,2)，调用 P(,,2)；       //此时为"acb"
   
   ​		满足退出条件，添加 "acb"；
   
   ​	换回 (1,2)，循环结束；          //此时为"abc"
   
   换回 (0,0)， j=0 循环结束；
   
   
   
   2.交换 (0,1)，调用 P(,,1)；           //此时为"bac"
   
   ​	交换 (1,1)，调用 P(,,2)；       //此时为"bac"
   
   ​		满足退出条件，添加 "bac"；
   
   ​	换回 (1,1)；
   
   ​	交换 (1,2)，调用 P(,,2)；        //此时为"bca"
   
   ​		满足退出条件，添加 "bca"；
   
   ​	换回 (1,2)；							 //此时为"bac"
   
   换回 (0,1)， j=1 循环结束；           //此时为"abc"
   
   
   
   3.交换 (0,2)，调用 P(,,1)；               //此时为"cba"
   
   ​	交换 (1,1)，调用 P(,,2)；          //此时为"cba"
   
   ​		满足退出条件，添加 "cba"；
   
   ​	换回 (1,1)；
   
   ​	交换 (1,2)，调用 P(,,2)；      	  //此时为"cab"
   
   ​		满足退出条件，添加 "cab"；
   
   ​	换回 (1,2)；					   //此时为"cba"
   
   换回 (0,2)， j=2 循环结束；				//此时为"abc"
   ```

### 知识点：

1. Collections.sort() 和 Arrays.sort() 的使用：

* Collections.sort() 针对集合 List，排序类型为 List 对应的类型，实质上调用了Arrays.sort()，其底层是归并排序。
* Arrays.sort() 针对任意对象，排序类型为传入的对象类，对于 *基本类型数组* 其底层是快速排序，对于 *对象数组* 其底层是归并排序。

2. 返回值类型为 ArrayList<> 时，需要定义为 ArrayList<> 类型；

### 解法1： 回溯法

```java
import java.util.*;
public class Solution {
    public ArrayList<String> Permutation(String str) {
        ArrayList<String> lists = new ArrayList<>();
        if(str.length()==0) return lists;
        PermutationProcess(str.toCharArray(),lists,0);
        Collections.sort(lists);
        return lists;
    }
    
    private void PermutationProcess(char[] ch , List<String> lists,int i){
        if(i == ch.length-1){
            if(!lists.contains(new String(ch))){
                lists.add(new String(ch));
            }
        }else{
            for(int j=i;j<ch.length;j++){
                swap(ch,i,j);
                //注意是 i + 1;
                PermutationProcess(ch,lists,i+1);
                swap(ch,j,i);
            }
        }
    }
    private void swap(char[] ch,int i ,int j){
        if(i != j){
            char tmp = ch[i];
            ch[i] = ch[j];
            ch[j] = tmp;
        }
    }
}
```
<br><br>

## 题目28：数组中出现次数超过一半的数字

**数组中有一个数字出现的次数超过数组长度的一半，请找出这个数字。例如输入一个长度为9的数组{1,2,3,2,2,2,5,4,2}。由于数字2在数组中出现了5次，超过数组长度的一半，因此输出2。如果不存在则输出0。**

输入
> [1,2,3,2,2,2,5,4,2]

返回值
> 2


### 解法1：哈希表
#### 思路：
1. 建立哈希表，Key 存元素，Value 存出现次数；
2. 循环 array 数组，若不存在对应元素的键，则添加键为对应元素，值为 1；若存在对应元素的键，则添加键为对应元素，值为 原始值＋1；
3. 遍历 map 的键集合，若有值，即出现次数大于 2，则返回 m；
4. 若遍历结束没有返回，说明这样的元素不存在，则返回 0；
```java
import java.util.*;
public class Solution {
    public int MoreThanHalfNum_Solution(int [] array) {
        Map<Integer,Integer> map = new HashMap<>();
        for(int i = 0;i<array.length; i++){
            if(!map.containsKey(array[i])){
                map.put(array[i],1);
            }else{
                map.put(array[i], map.get(array[i])+1);
            }
        }
        for(Integer m:map.keySet()){
            if(map.get(m)>array.length/2) return m;
        }
        return 0;
    }
}
```


### 解法2：候选法
#### 思路：
如果两个数不相等，就消去这两个数，最坏情况下，每次消去一个众数和一个非众数，那么如果存在众数，最后留下的数肯定是众数。
1. rec 用于记录当前有可能的众数元素，flag 用于记录是否需要消去；
2. 遍历数组：
* 如果当前 flag 为 0，则将当前元素赋予 rec，flag 加一；
* 如果当前 flag 不为 0，判断 rec 与当前元素值是否相等，最终得到的 rec 就是众数值。
   * 若相等则 flag 加一；
   * 若不等则 flag 减一。 
3. flag 赋为 0，遍历数组记录众数出现次数；
4. 判断若次数大于一半则输出 rec，若不大于则返回 0；
```java
import java.util.*;
public class Solution {
    public int MoreThanHalfNum_Solution(int [] array) {
        int rec = -1 ,flag = 0;
        for(int i = 0;i<array.length;i++){
            if(flag == 0){
                rec = array[i];
                flag++;
            }else{
                if(rec == array[i]) flag++;
                else flag--;
            }
        }
        flag = 0;
        for(int a:array){
            if(a == rec) flag++;
        }
        if(flag > array.length/2) return rec;
        return 0;
    }
}
```
<br><br>

## 题目29：最小的K个数

**输入n个整数，找出其中最小的K个数。例如输入4,5,1,6,2,7,3,8这8个数字，则最小的4个数字是1,2,3,4。**

### 解法1： Arrays.sort() 排序
#### 思路：
1. 判断 k 值与 input 数组长度的关系，当 k 大于 input.length 或 小于0，直接返回集合；
2. Arrays.sort() 排序；
3. 取前 k 个元素添加进 ans 集合，即为结果。
```java
import java.util.*;
public class Solution {
    public ArrayList<Integer> GetLeastNumbers_Solution(int [] input, int k) {
        ArrayList<Integer> ans = new ArrayList<>();
        if(k > input.length || k < 0) return ans;
        Arrays.sort(input);
        for(int i=0;i<k;i++){
            ans.add(input[i]);
        }
        return ans;
    }
}
```
<br><br>

## 题目30：连续子数组的最大和

**{6,-3,-2,7,-15,1,2,2},连续子向量的最大和为8(从第0个开始,到第3个为止)。给一个数组，返回它的最大连续子序列的和 (子向量的长度至少是1)。**

### 解法1： 动态规划
#### 思路：
1. 判断 array.length 为 0，直接返回 0；
2. 定义 dp[] ，元素代表以 dp[i] 为结尾的连续子数组的最大和；
3. 选择这其中最大的一个，即为结果。
```java
public class Solution {
    public int FindGreatestSumOfSubArray(int[] array) {
        if(array.length == 0) return 0;
        int dp[] = new int[array.length];
        dp[0] = array[0];
        int max = array[0];
        for(int i = 1;i<array.length;i++){
            dp[i] = dp[i-1] > 0? dp[i-1]+array[i] :array[i];
            max = Math.max(max,dp[i]) ;
        }
        return max;
    }
}
```
<br><br>

## 题目31：整数中1出现的次数（从1到n整数中1出现的次数）

**求出1~13的整数中1出现的次数,并算出100~1300的整数中1出现的次数？为此他特别数了一下1~13中包含1的数字有1、10、11、12、13因此共出现6次,但是对于后面问题他就没辙了。ACMer希望你们帮帮他,并把问题更加普遍化,可以很快的求出任意非负整数区间中1出现的次数（从1 到 n 中1出现的次数）。**

### 解法1： 数学/按位计算
#### 思路：
1. 思路是分别计算个位、十位、百位........上出现 1 的个数。
2. 以  n = 216 为例：
* 个位上： 1 ，11，21，31，.....211。个位上共出现（216/10）+ 1个 1 。因为除法取整，210~216间个位上的1取不到，所以我们加8进位。你可能说为什么不加9，n=211怎么办，这里把最后取到的个位数为1的单独考虑，先往下看。
* 十位上：10到19，110到119，210到216.   十位上可看成 求（216/10）=21 个位上的1的个数然后乘10。这里再次把最后取到的十位数为1的单独拿出来，即210到16要单独考虑 ，个数为（216%10）+1 。这里加8就避免了判断的过程。
3. count 为 **前一位出现 1 的次数** + **当前位出现 1 的次数**。
* 当前位出现 1 的次数计算方法为：
当前位前面的数 n/i 加 8 除以 10，若未进位则说明当前数最小位小于或等于 1，然后这个结果加上进位算数。
* 进位算数为：
若当前数最小位等于 1，则看看后面数有多少（b=n%i），则加上多少（b+1）。
```
如 31：判断个位时为 1，则 (31+8)/10*i + 31%1+1 = 3，即个位出现了 4 次 1。
```
```
如 113：判断十位时为 1，则 (11+8)/10*i + 113%10+1 = 10+4 = 14，即十位出现了 14 次 1。
```

```java
public class Solution {
    public int NumberOf1Between1AndN_Solution(int n) {
        int count = 0;
        for(int i=1;i<=n;i=i*10){
            int a=n/i,b=n%i;
            count = count + (a+8)/10*i + (a % 10 == 1? b+1:0); 
        }
        return count;
    }
}
```
<br><br>

## 题目32：把数组排成最小的数

**输入一个正整数数组，把数组里所有数字拼接起来排成一个数，打印能拼接出的所有数字中最小的一个。例如输入数组{3，32，321}，则打印出这三个数字能排成的最小数字为321323。**

### 解法1： 回溯法（耗时太长）
精髓：用一个数组，一个list，一个索引！
#### 注意：
1. 如果字符串不满足要求，返回的是 ""，而非 null，所以在判断中也通常加入这两个条件；
2. 注意回溯法不能用 *基本变量* 代替 *list*，否则丢失数据；
#### 思路：
1. 判断 numbers.length 为 0，直接返回 ""；
2. 建立 ArrayList，进入回溯方法处理；
3. 回溯设置判断，符合索引条件添加入 lists 并退出，否则循环进入回溯；
4. 需要定义一个 swap 交换方法；
5. 需要定义一个 numbersToNumber 方法用来将多个元素逐次合并为一个长整型数值并返回；
6. 回溯结束，lists 存放了所有可能的拼接情况，只需要循环一次判断最小的输出为字符串型即可。
```java
import java.util.*;
public class Solution {
    public String PrintMinNumber(int [] numbers) {
        if(numbers.length == 0) return "";
        List<Long> lists = new ArrayList<Long>();
        PrintMinNumberProcess(numbers,lists,0);
        Long ans = Long.MAX_VALUE;
        for(Long list:lists){
            ans = Math.min(list,ans);
        }
        return String.valueOf(ans);
    }
    private void PrintMinNumberProcess(int [] numbers,List<Long> lists,int i){
        if(i == numbers.length-1 && !lists.contains(numbersToNumber(numbers))){
                lists.add(numbersToNumber(numbers));
        }else{
            for(int j=i;j<numbers.length;j++){
                swap(numbers,i,j);
                PrintMinNumberProcess(numbers,lists,i+1);
                swap(numbers,i,j);
            }
        }
    }
    private void swap(int [] numbers,int i, int j){
        int tmp = numbers[i];
        numbers[i] = numbers[j];
        numbers[j] = tmp;
    }
    private Long numbersToNumber(int [] numbers){
        StringBuilder sb = new StringBuilder();
        for(int number:numbers){
            sb.append(number);
        }
        return Long.valueOf(sb.toString());
    }
}
```
### 解法2： 冒泡排序
精髓：用一个数组，一个list，一个索引！
#### 注意：
1. 如果字符串不满足要求，返回的是 ""，而非 null，所以在判断中也通常加入这两个条件；
2. 冒泡排序采用双循环，第二个循环的限定条件为 j<numbers.length-i-1 ；
#### 思路：
1. 判断 numbers.length 为 0，直接返回 ""；
2. 循环内判断第 j 位和第 j+1 位字符正反相加后的大小，保留小的在前。结束后 numbers 排序完毕；
3. 循环添加进字符串，返回即可；
```java
import java.util.*;
public class Solution {
    public String PrintMinNumber(int [] numbers) {
        if(numbers.length == 0) return "";
        for(int i=0; i<numbers.length;i++){
            for(int j=0;j<numbers.length-i-1;j++){
                //new String(int) + new String(int) 不行
                String a = String.valueOf(numbers[j]) +  String.valueOf(numbers[j+1]);
                String b = String.valueOf(numbers[j+1]) +  String.valueOf(numbers[j]);
                if(a.compareTo(b) > 0){
                    int tmp = numbers[j];
                    numbers[j] = numbers[j+1];
                    numbers[j+1] = tmp;
                }
            }
        }
        //方法一：
        StringBuilder ans = new StringBuilder();
        for(int number:numbers){
            ans.append(number);
        }
        return ans.toString();
        ///方法二：
        String ans = String.valueOf(numbers[0]);
        for(int i = 1; i < numbers.length; i++)
            ans += String.valueOf(numbers[i]);
        return ans;
    }
}
```
<br><br>

## 题目33：丑数

**把只包含质因子2、3和5的数称作丑数（Ugly Number）。例如6、8都是丑数，但14不是，因为它包含质因子7。 习惯上我们把1当做是第一个丑数。求按从小到大的顺序的第N个丑数。**

### 解法1： 多指针
精髓：用三个指针 p2、p3、p5 分别代表丑数的质因数。
#### 思路：
1. 判断 index 为 0，直接返回 0；
2. 建立 numbers，同时赋值 numbers[0] = 1；
3. 赋值三个指针，进入循环。
4. 每次取三个指针索引的对应值乘积最小的一个作为数组当前 i 索引的值，同时判断是取了哪个索引，将其加一；
5. 最后一个元素即为结果。
```java
import java.util.*;
public class Solution {
    public int GetUglyNumber_Solution(int index) {
        if(index == 0) return 0;
        int numbers[] = new int[index];
        numbers[0] = 1;
        int p2 = 0 , p3 = 0, p5 = 0;
        for(int i=1;i<index;i++){
            numbers[i] = Math.min(numbers[p2]*2,Math.min(numbers[p3]*3,numbers[p5]*5));
            if(numbers[i]==numbers[p2]*2) p2++;
            if(numbers[i]==numbers[p3]*3) p3++;
            if(numbers[i]==numbers[p5]*5) p5++;
        }
        return numbers[index-1];
    }
}
```
<br><br>

## 题目34：第一个只出现一次的字符

**在一个字符串(0<=字符串长度<=10000，全部由字母组成)中找到第一个只出现一次的字符,并返回它的位置, 如果没有则返回 -1（需要区分大小写）.（从0开始计数）。**

### 解法1： 哈希表（耗时太长）
精髓：HashSet 存放出现一次的字符。
#### 注意：
1. 常见ASCII码的大小规则：0~9<A~Z<a~z。 
* 数字比字母要小。如 “7”<“F”；
* 数字0比数字9要小，并按0到9顺序递增。如 “3”<“8” ；
* 字母A比字母Z要小，并按A到Z顺序递增。如“A”<“Z” ；
* 同个字母的大写字母比小写字母要小32。如“A”<“a” 。
#### 思路：
1. 判断 str 为空或 str.length() 为 0，直接返回 -1；
2. 建立 dp[] 用于存放字符的出现次数；建立 HashSet，用于存放出现一次的字符的数值。a~z,A~Z对应 0~52；
3. 当 Set 不为空，从头开始判断当前字符是否在 Set 内，若在则为第一个出现一次的字符；
4. Set 为空，则直接范返回 -1。
```java
import java.util.*;
public class Solution {
    public int FirstNotRepeatingChar(String str) {
        if(str == null || str.length() == 0) return -1;  //通用的字符串边界条件判断方法。
        int dp[] = new int[52];
        HashSet<Integer> set = new HashSet<>();
        for(int i=0;i<str.length();i++){
            int index = str.charAt(i) >='a' ? str.charAt(i)-'a':str.charAt(i)-'A'+26;
            dp[index] ++;
            if(dp[index] == 1) set.add(index);
            else set.remove(index);
        }
        if(!set.isEmpty()){
            for(int i=0;i<str.length();i++){
                int index = str.charAt(i) >='a' ? str.charAt(i)-'a':str.charAt(i)-'A'+26;
                if(set.contains(index)) return i;
            }
        }
        return -1;
    }
} 
```

### 解法2： 双指针循环
精髓：利用嵌套双循环。
#### 思路：
1. 判断 str 为空或 str.length() 为 0，直接返回 -1；
2. 建立： ans 用来保存结果，flag 用于保存是否是出现两次及以上而退出的标志；
3. 直接双循环：内循环内判断两个指针索引的字符值是否相等，若相等且索引不等，说明当前 i 位置的字符出现不只一次，此时 flag 赋为 1，若循环结束，flag 还为 0 ，说明当前 i 位置的字符出现一次；外循环内赋值 flag = 0，内循环结束后外循环判断 flag 值，若为 0，则将结果赋为 i，退出外循环；
3. 输出结果即可。
```java
import java.util.*;
public class Solution {
    public int FirstNotRepeatingChar(String str) {
        if(str == null ||  str.length() == 0) return -1;
        int ans = -1,flag = 0;
        for(int i=0;i<str.length();i++){
            flag = 0;
            for(int j=0;j<str.length();j++){
                if(str.charAt(i) == str.charAt(j) && i!=j){
                    flag = 1;
                    break;
                }
            }
            if(flag == 0){
                ans = i;
                break;
            }
        }
        return ans;
    }
} 
```
<br><br>

## ★ 题目35：数组中的逆序对
**在数组中的两个数字，如果前面一个数字大于后面的数字，则这两个数字组成一个逆序对。输入一个数组,求出这个数组中的逆序对的总数P。并将P对1000000007取模的结果输出。 即输出P%1000000007。**

### 解法：归并排序
归并排序使用分治策略，序列一分为二(O(1))后，将子序列递归排序(2 * T(n / 2))，最后合并有序子序列(O(n)),T(n) = 2 * T(n / 2) + O(n) = O(n * logn)。

#### 思路：
1. 二路归并即merge，是将两个有序的序列合并为一个有序的序列，在两个子序列left、right合并过程中，当left中当前元素A小于right中当前元素B时，因为right序列已经有序，所以不用比较，A一定是left、right两个子序列当前剩余元素中最小的元素，这省去了A与B后其他元素比较的操作。
2. 对于本题，在两个子序列left、right合并过程中，当left中当前元素A大于right中当前元素B时，因为right序列已经有序，所以不用比较，A一定大于right序列当前所有剩余元素，其全部可以与A组成逆序对，即通过一次比较可到一批逆序对，加速统计过程。
```java
public class Solution {
    public int InversePairs(int [] array) {
        if(array.length == 0) return 0;
        if(array == null) return 0;
        int[] tmp = new int[array.length];
        return mergeSort(array, tmp, 0, array.length-1);
    }
     //归并排序，递归
    private static int mergeSort(int[] array, int[] tmp, int low, int high) {
        if(low >= high) return 0;
        int res = 0, mid = low + (high - low) / 2;
        res += mergeSort(array, tmp, low, mid);
        res %= 1000000007;
        res += mergeSort(array, tmp, mid + 1, high);
        res %= 1000000007;
        res += merge(array, tmp, low, mid, high);
        res %= 1000000007;
        return res;
    }
    //归并排序，合并
    private static int merge(int[] array, int[] tmp, int low, int mid, int high) {
        int i1 = low, i2 = mid + 1,k = low;
        int res = 0;
        while(i1 <= mid && i2 <= high) {
            if(array[i1] > array[i2]) {
                res += mid - i1 + 1;
                res %= 1000000007;
                tmp[k++] = array[i2++];
            } else
                tmp[k++] = array[i1++];
        }
        while(i1 <= mid)
            tmp[k++] = array[i1++];
        while(i2 <= high)
            tmp[k++] = array[i2++];
        for (int i = low; i <= high; i++)
            array[i] = tmp[i];
        return res;
    }
    
}
```
<br><br>

## 题目36：两个链表的第一个公共结点
**输入两个链表，找出它们的第一个公共结点。（注意因为传入数据是链表，所以错误测试数据的提示是用其他方式显示的，保证传入数据是正确的）。**
### 解法1：遍历链表(O(n^2))
分别遍历两链表，找到相等的节点输出。
#### 思路：
1. 边界条件；
2. 两个 while 循环遍历，当节点 1 和节点 2 相等时，输出即可；
3. 若遍历完毕无输出，则返回 null。
```java
/*
public class ListNode {
    int val;
    ListNode next = null;

    ListNode(int val) {
        this.val = val;
    }
}*/
public class Solution {
    public ListNode FindFirstCommonNode(ListNode pHead1, ListNode pHead2) {
        if(pHead1 == null || pHead2 == null)   return null;
        while(pHead1 != null){
            ListNode head2 = pHead2;
            while(head2 != null){
                if(pHead1 == head2)   return pHead1;
                head2 = head2.next;
            }
            pHead1 = pHead1.next;
        }
        return null;   
    }
}
```
### 解法2：双指针(O(2n))
分别遍历两链表，找到相等的节点输出。
#### 思路：
1. 边界条件；
2. 判断谁先走到了头，先走到头的回来继续走；
3. 相当于减去长链表比短链表长的部分，然后 2 个相同长度的链表从头开始遍历；
4. 若无相等，最后循环至两节点都为空，此时退出循环；
5. 时间复杂度为 O(2n) 比遍历的 O(n^2) 复杂度的代码好很多；
6. 遍历完毕，返回 p1。
```java
/*
public class ListNode {
    int val;
    ListNode next = null;

    ListNode(int val) {
        this.val = val;
    }
}*/
public class Solution {
    public ListNode FindFirstCommonNode(ListNode pHead1, ListNode pHead2) {
        if(pHead1 == null || pHead2 == null)   return null;
        ListNode p1 = pHead1;
        ListNode p2 = pHead2;
        while(p1 != p2){
            p1 = p1.next; 
            p2 = p2.next;
            if(p1 != p2){
                if(p1 == null)   p1 = pHead1;
                if(p2 == null)   p2 = pHead2;
            }
        }
        return p1;
    }
}
```
<br><br>

## 题目37：数字在排序数组中出现的次数
**统计一个数字在升序数组中出现的次数。**
### 思路：
**二分查找**关键特征：升序/降序/有序数组。

### 解法1： 二分查找
#### 注意：
1. 如果运行超时，检查循环赋值和判断条件是否有错； 
2. 注意 while 循环内用 l <= r ，而非 "小于"。
3. 在循环内赋值 mid；
4. 先判断当前索引对应值与目标值是否相等，相等则直接做出相应结果，不等则进入大小判断； 
5. 若索引对应值大，则将右端值 r 赋值为 mid；否则将左端值 l 赋值为 mid；
#### 思路：
1. 按照二分查找找到目标值的位置；
2. 若与目标值相等，则进入统计次数逻辑，以当前索引为出发点，定义 sub和 plu，分别朝前后遍历，若相等则ans加一，直到与目标值不等，ans 即为结果；
3. 若没进入统计次数逻辑，则说明不存在目标值，直接返回 0。
```java
public class Solution {
    public int GetNumberOfK(int [] array , int k) {
        int l=0,r=array.length-1;
        while(l<=r){
            int mid = l + (r-l)/2;
            if(array[mid] == k) {
                int ans = 0,sub = mid-1,plu = mid;
                while(plu < array.length && array[plu] == k){
                    ans++;
                    plu++;
                 }
                while(sub >=0 && array[sub] == k){
                    ans++;
                    sub--;
                }
                return ans;
            }
            else if(array[mid] < k){
                l = mid + 1;
            }else{
                r = mid - 1; 
            }
        }
        return 0;
    }
}
```
<br><br>

## 题目38：二叉树的深度
**输入一棵二叉树，求该树的深度。从根结点到叶结点依次经过的结点（含根、叶结点）形成树的一条路径，最长路径的长度为树的深度。**

### 解法1： 递归
#### 思路：
1. 设置递归退出条件；
2. 将问题分解，求当前节点左子树的深度、右子树的深度，然后返回其最大值；
3. 如果在递归左右子树为空时，则返回 0，同时当前节点加一，即当前长度为 1；
4. 逐次向上返回时，即累加了长度，并且淘汰了左右子树中较小的深度，最终得到深度。
```java
/**
public class TreeNode {
    int val = 0;
    TreeNode left = null;
    TreeNode right = null;

    public TreeNode(int val) {
        this.val = val;
    }

}
*/
public class Solution {
    public int TreeDepth(TreeNode root) {
        if(root == null) return 0;
        int ldep = TreeDepth(root.left) + 1;
        int rdep = TreeDepth(root.right) + 1;
        return Math.max(ldep,rdep);
    }
}
```
### 解法2： 层序遍历
#### 思路：
1. 边界条件；
2. 层序遍历，在外面的 while 循环中添加计数器；
3. 返回计数结果即可。
```java
/**
public class TreeNode {
    int val = 0;
    TreeNode left = null;
    TreeNode right = null;

    public TreeNode(int val) {
        this.val = val;
    }

}
*/
import java.util.*;
public class Solution {
    public int TreeDepth(TreeNode root) {
        if(root == null) return 0;
        Queue<TreeNode> queue = new LinkedList<>();
        queue.offer(root);
        int ans = 0;
        while(!queue.isEmpty()){
            int size = queue.size();
            while(size > 0){
                TreeNode node = queue.poll();
                if(node.left != null)    queue.offer(node.left);
                if(node.right != null)    queue.offer(node.right);
                size--;
            }
            ans++;
        }
        return ans;
    }
}
```

<br><br>

## 题目39：平衡二叉树
**输入一棵二叉树，判断该二叉树是否是平衡二叉树。在这里，我们只需要考虑其平衡性，不需要考虑其是不是排序二叉树平衡二叉树（Balanced Binary Tree），具有以下性质：它是一棵空树或它的左右两个子树的高度差的绝对值不超过1，并且左右两个子树都是一棵平衡二叉树。**

### 解法1： 两层递归
#### 思路：
1. culDepth() 递归方法用于计算当前节点的高度；
2. IsBalanced_Solution() 递归方法用于判断当前节点左右子节点的高度是否相差大于 1，若大于 1 则返回 false；否则判断其 **左、右节点** 是否满足这种规则，若判断完毕，则返回 true。
```java
public class Solution {
    public boolean IsBalanced_Solution(TreeNode root) {
        if(root == null)    return true;
        if(Math.abs(culDepth(root.left) - culDepth(root.right)) > 1) return false;
        return IsBalanced_Solution(root.left) && IsBalanced_Solution(root.right);
    }
    private int culDepth(TreeNode node){
        if(node == null)    return 0;
        int left = culDepth(node.left) + 1;
        int right = culDepth(node.right) + 1;
        return Math.max(left, right);
    }
}
```
### 解法2： 一层递归
#### 思路：先序遍历
1. IsBalanced_Solution() 方法直接返回 getDepth() 方法；
2. getDepth() 递归方法：
* 设置递归退出条件；
* 先序遍历的思想。
```java
public class Solution {
    public boolean IsBalanced_Solution(TreeNode root) {
        return getDepth(root) != -1;
    }
    private int getDepth(TreeNode root) {
        if (root == null) return 0;
        int left = getDepth(root.left);
        if (left == -1) return -1;
        int right = getDepth(root.right);
        if (right == -1) return -1;
        return Math.abs(left - right) > 1 ? -1 : 1 + Math.max(left, right);
    }
}
```


<br><br>

## 题目40：数组中只出现一次的数字
**一个整型数组里除了两个数字之外，其他的数字都出现了两次。请写程序找出这两个只出现一次的数字。**

### 解法1： 哈希表
#### 注意：
1. HashSet 是不重复的集合；
#### 思路：
1. 首先遍历 array ，若存在当前元素，则移除；若不存在，则添加；
2. 遍历 Set，将第一个元素给 num1，第二个元素给 num2。
```java
//num1,num2分别为长度为1的数组。传出参数
//将num1[0],num2[0]设置为返回结果
import java.util.*;
public class Solution {
    public void FindNumsAppearOnce(int [] array,int num1[] , int num2[]) {
        HashSet<Integer> set = new HashSet<>();
        for(int i=0;i<array.length;i++){
            if(set.contains(array[i])) set.remove(array[i]);
            else set.add(array[i]);
        }
        int index = 0;
        for(Integer num:set){
            if(index == 0) {
                num1[0] = num;
                index++;
            }else{
                num2[0] = num;
            }
        }
    }
}
```
<br><br>


## 题目41：和为S的连续正数序列
**小明很喜欢数学,有一天他在做数学作业时,要求计算出9~16的和,他马上就写出了正确答案是100。但是他并不满足于此,他在想究竟有多少种连续的正数序列的和为100(至少包括两个数)。没多久,他就得到另一组连续正数和为100的序列:18,19,20,21,22。现在把问题交给你,你能不能也很快的找出所有和为S的连续正数序列? Good Luck!**

### 解法1： 双层循环
#### 注意：
1. 因为至少包含两个数，所以循环的边界条件只需要到 sum/2 即可；
2. 通过计算双层循环中，两个指针对应的前n项和，将其相减得到结果，判断是否与 sum 相等。
#### 思路：
1. 首先建立 ArrayList<ArrayList<Integer>> lists 用来存放结果；
2. 判断边界条件，若 sum 小于等于 2，则不存在相应结果，直接返回 lists；
3. 进入双层循环，第一层 i 从 0 到 sum/2，第二层从 i+1 到 sum/2+1，内层进行判断，如果当前计算的前 n 项和相减结果为 sum，则建立循环从i+1到j，将其添加到结果 ans 中，同时退出循环，减少后面的遍历，因为不再需要。
4. 循环结束，返回 lists 即可；
5. frontSum() 方法用于计算输入参数 i 的前 i 项和。
```java
import java.util.ArrayList;
public class Solution {
    public ArrayList<ArrayList<Integer>> FindContinuousSequence(int sum) {
        ArrayList<ArrayList<Integer>> lists = new ArrayList<>();
        if(sum<=2) return lists;
        for(int i=0;i<=sum/2;i++){
             for(int j=i+1;j<=sum/2+1;j++){
                 if(frontSum(j)-frontSum(i) == sum){
                     ArrayList<Integer> list = new ArrayList<>();
                     for(int m=i+1;m<=j;m++){
                         list.add(m);
                     }
                     lists.add(list);
                     break;
                 } 
             }
        }
        return lists;
    }
    private int frontSum(int i){
        return (i+1)*i/2;
    }
}
```

### 解法2： 双指针
#### 思路：
1. 首先建立 ArrayList<ArrayList<Integer>> lists 用来存放结果；
2. 判断边界条件，若 sum 小于等于 2，则不存在相应结果，直接返回 lists；
3. 建立 frontSum() 方法用于计算输入参数 l 到 r 个数相加的到的结果；
3. 建立指针 l=1，r=2。进入双指针循环，判断条件：
* 若 sumCul(l,r) == sum，则将 l 到 r 个数添加进结果，同时 l 加一，判断下一组数；
* 若 sumCul(l,r) < sum，则说明数不够，则 r 再加一；
* 若 sumCul(l,r) > sum，则说明当前数和已经超过，则 l 再加一，减少数和；
4. l < r 为判断条件，因为若等于则会造成当前值的重复使用（123，出现2+2的判断）。循环结束，返回 lists 即可；
```java
import java.util.ArrayList;
public class Solution {
    public ArrayList<ArrayList<Integer>> FindContinuousSequence(int sum) {
        ArrayList<ArrayList<Integer>> lists = new ArrayList<>();
        if(sum<=2) return lists;
        int l=1,r=2;
        while(l<r){
            if(sumCul(l,r) == sum){
                ArrayList<Integer> list = new ArrayList<>();
                for(int i=l;i<=r;i++){
                    list.add(i);
                }
                lists.add(list);
                l++;
            }else if(sumCul(l,r) < sum){
                r++;
            }else{
                l++;
            }
        }
        return lists;
    }
    private int sumCul(int l,int r){
        return (l+r)*(r+1-l)/2;
    }
}
```
<br><br>

## 题目42：和为S的两个数字
**输入一个递增排序的数组和一个数字S，在数组中查找两个数，使得他们的和正好是S，如果有多对数字的和等于S，输出两个数的乘积最小的。**

#### 注意：
1. 如果按照双指针从相隔最远进入循环，不需要再判断乘积是否最小。因为 a 和 b 和一定， a 和 b 相差越多，乘积越小；
### 解法1： 双指针加入乘积判断：11ms
#### 思路：
1. 首先建立 ArrayList<Integer> list 用来存放结果；
2. 判断边界条件，若 sum 小于 2，则不存在相应结果，直接返回 list；
3. 建立变量 l、r 用于双指针。同时建立记录乘积最小的相关变量；
4. 进入循环：
    * 若相等且乘积小于当前记录的乘积，则令 flag 为 1，min 和 max 赋为当前索引，prod 赋为当前乘积，l--，r++；
    * 若小于，l++；
    * 若大于，r--；
4. 循环结束，若 flag 为 1，则说明存在相等的且进行了记录，则在 list 中存入 min 和 max 值即可；
5. 返回 list。
```java
import java.util.ArrayList;
public class Solution {
    public ArrayList<Integer> FindNumbersWithSum(int [] array,int sum) {
        ArrayList<Integer> list = new ArrayList<>();
        if(array.length < 2) return list;
        int l=0,r=array.length-1;
        int prod = Integer.MAX_VALUE;   //用来判断乘积最小
        int min=array[l],max=array[r];  //用来记录乘积最小的索引坐标
        int flag=0;                     //用来记录是否存在相等
        while(l<r){
            if(array[l] + array[r] == sum && array[l] * array[r] < prod){
                flag = 1;
                min = array[l];
                max = array[r];
                prod = array[l] * array[r];
                l++;r--;
            }else if(array[l] + array[r] < sum){
                l++;
            }else{
                r--;
            }
        }
        if(flag==1){
            list.add(min);
            list.add(max);
        }
        return list;
    }
}
```
### 解法2： 双指针：不用判断，利用 “因为 a 和 b 和一定， a 和 b 相差越多，乘积越小”
#### 思路：
1. 首先建立 ArrayList<Integer> list 用来存放结果；
2. 判断边界条件，若 sum 小于 2，则不存在相应结果，直接返回 list；
3. 建立变量 l、r 用于双指针；
4. 进入循环：
    * 若相等则存入list直接返回即可；
    * 若小于，l++；
    * 若大于，r--；
4. 循环结束，若在循环内未返回结果，说明不存在相等，则返回 空list。
```java
import java.util.ArrayList;
public class Solution {
    public ArrayList<Integer> FindNumbersWithSum(int [] array,int sum) {
        ArrayList<Integer> list = new ArrayList<>();
        if(array.length < 2) return list;
        int l=0,r=array.length-1;
        while(l<r){
            if(array[l] + array[r] == sum){
                list.add(array[l]);
                list.add(array[r]);
                return list;
            }else if(array[l] + array[r] < sum){
                l++;
            }else{
                r--;
            }
        }
        return list;
    }
}
```
<br><br>

## 题目43：左旋转字符串
**汇编语言中有一种移位指令叫做循环左移（ROL），现在有个简单的任务，就是用字符串模拟这个指令的运算结果。对于一个给定的字符序列S，请你把其循环左移K位后的序列输出。例如，字符序列S=”abcXYZdef”,要求输出循环左移3位后的结果，即“XYZdefabc”。是不是很简单？OK，搞定它！**

#### 注意：
1. 边界条件；
2. StringBuilder() 和 .append() 方法。
### 解法1： 循环每一位调整位置。
#### 思路：
1. 首先判断边界，然后建立 StringBuilder 用来存放结果；
2. n > str.length() 时，取余；
3. 循环判断对应位的存放方法，左移 n 位：
* 新字符的前 str.length()-n 个 为旧字符的后 str.length()-n 个
* 新字符的后 n 个 为旧字符的前 n 个
4. 返回结果 .toString()。
```java
public class Solution {
    public String LeftRotateString(String str,int n) {
        if(str == null || str.length() == 0) return str; 
        StringBuilder sb = new StringBuilder();
        n = n % str.length();
        for(int i=0;i<str.length();i++){
            if(i < str.length()-n) sb.append(str.charAt(i+n));
            else sb.append(str.charAt(i-str.length()+n));
        }
        return sb.toString();       
    }
}
```
<br><br>

## 题目44：翻转单词顺序列
**牛客最近来了一个新员工Fish，每天早晨总是会拿着一本英文杂志，写些句子在本子上。同事Cat对Fish写的内容颇感兴趣，有一天他向Fish借来翻看，但却读不懂它的意思。例如，“student. a am I”。后来才意识到，这家伙原来把句子单词的顺序翻转了，正确的句子应该是“I am a student.”。Cat对一一的翻转这些单词顺序可不在行，你能帮助他么？**

#### 注意：
1. substring(i,j) 都是小写：i 表示 i 从 0 开始，包括 i ；j 表示到 j 结束，不包括 j；
2. ArrayList 判断是否是最后一个元素： **list.indexOf(li) == list.size()-1**。
3. String 和 char[] 相互转换：
    * char[] = string.toCharArray()
    * string = new String(char[])

### 解法1： 双指针，由最右侧开始循环存放每个单词到 list。
#### 思路：
1. 判断边界条件，若 str == null || str.length() == 0 ，直接返回 str ；
2. 首先建立 List<String> list 用来存放 *每个单词* 和 *最后一个单词加 .* ；
3. 建立变量 l、r 用于双指针，循环判断：
    * 若当前 l 索引位置字符为' '，则说明 l 与 r 间存在一个单词，将 (l+1,r) 存放到 list（注意边界）。同时 r 赋值为 l， l--；
    * 若当前 l 为 0 ，则说明到字符串的首部，则将 (l,r) 的存放，同时 l--，到达退出循环条件；
    * 若为其他情况，则 l-- 即可。
4. 循环 list：
    * 若当前字符串在list中的坐标为list.size() - 1，即为最后一个，则不需要加 ' '；
    * 否则循环在 sb 中加入 当前 s + ' '。 
4. 循环结束，返回 sb.toString()。
```java
import java.util.*;
public class Solution {
    public String ReverseSentence(String str) {
        if(str == null || str.length() == 0) return str;
        List<String> list = new ArrayList<>();
        int l=str.length()-1,r=str.length();
        while(l>=0){
            if(str.charAt(l) == ' '){
                list.add(str.substring(l+1,r));
                r=l;
                l--;
            }else if(l==0){
                list.add(str.substring(l,r));
                l--;
            }else{
                l--;
            }
        }
        StringBuilder sb = new StringBuilder();
        for(String s:list){
            if(list.size() - 1 == list.indexOf(s)){
                sb.append(s);
            }else{
                sb.append(s+' ');
            }
        }
        return sb.toString();
    }
}
```
<br><br>

## 题目45：扑克牌顺子
**LL今天心情特别好,因为他去买了一副扑克牌,发现里面居然有2个大王,2个小王(一副牌原本是54张^_^)...他随机从中抽出了5张牌,想测测自己的手气,看看能不能抽到顺子,如果抽到的话,他决定去买体育彩票,嘿嘿！！“红心A,黑桃3,小王,大王,方片5”,“Oh My God!”不是顺子.....LL不高兴了,他想了想,决定大\小 王可以看成任何数字,并且A看作1,J为11,Q为12,K为13。上面的5张牌就可以变成“1,2,3,4,5”(大小王分别看作2和4),“So Lucky!”。LL决定去买体育彩票啦。 现在,要求你使用这幅牌模拟上面的过程,然后告诉我们LL的运气如何， 如果牌能组成顺子就输出true，否则就输出false。为了方便起见,你可以认为大小王是0。**

#### 注意：
1. 边界条件判断；
2. Arrays.sort() 排序。

### 解法1： 双指针，由最右侧开始循环存放每个单词到 list。
#### 思路：
1. 判断边界条件，若 str == null || str.length() == 0 ，直接返回 str ；
2. 首先建立 List<String> list 用来存放 *每个单词* 和 *最后一个单词加 .* ；
3. 建立变量 l、r 用于双指针，循环判断：
    * 若当前 l 索引位置字符为' '，则说明 l 与 r 间存在一个单词，将 (l+1,r) 存放到 list（注意边界）。同时 r 赋值为 l， l--；
    * 若当前 l 为 0 ，则说明到字符串的首部，则将 (l,r) 的存放，同时 l--，到达退出循环条件；
    * 若为其他情况，则 l-- 即可。
4. 循环 list：
    * 若当前字符串在list中的坐标为list.size() - 1，即为最后一个，则不需要加 ' '；
    * 否则循环在 sb 中加入 当前 s + ' '。 
4. 循环结束，返回 sb.toString()。
```java
import java.util.*;
public class Solution {
    public boolean isContinuous(int [] numbers) {
        if(numbers.length == 0) return false;
        Arrays.sort(numbers);
        int cha = 0, i = 0;
        while(numbers[i] == 0){
            cha++;
            i++;
        }
        for(i=i+1;i<numbers.length;i++){
            int sub = numbers[i]-numbers[i-1];
            cha = cha - sub + 1;
            if(sub == 0 || cha < 0) return false;
        }
        return true;
    }
}
```
<br><br>

## 题目46：孩子们的游戏(圆圈中最后剩下的数)
**每年六一儿童节,牛客都会准备一些小礼物去看望孤儿院的小朋友,今年亦是如此。HF作为牛客的资深元老,自然也准备了一些小游戏。其中,有个游戏是这样的:首先,让小朋友们围成一个大圈。然后,他随机指定一个数m,让编号为0的小朋友开始报数。每次喊到m-1的那个小朋友要出列唱首歌,然后可以在礼品箱中任意的挑选礼物,并且不再回到圈中,从他的下一个小朋友开始,继续0...m-1报数....这样下去....直到剩下最后一个小朋友,可以不用表演,并且拿到牛客名贵的“名侦探柯南”典藏版(名额有限哦!!^_^)。请你试着想下,哪个小朋友会得到这份礼品呢？(注：小朋友的编号是从0到n-1)。如果没有小朋友，请返回-1。**

### 解法1： list（耗时过长）或链表
#### 思路：
1. 边界条件判断；
2. 建立 list，填充 0 至 n-1；
3. 建立 cur 用于记录当前删除元素索引，在 list 大于 1 时循环删除对应节点；
4. 输出结果即可。
```java
import java.util.*;
public class Solution {
    public int LastRemaining_Solution(int n, int m) {
        if(n == 0 || m == 0)    return -1;
        List<Integer> list = new ArrayList<>();
        for(int i=0;i<n;i++){
            list.add(i);
        }
        int cur = 0;
        while(list.size() > 1) {
            cur = (cur+m-1) % list.size();
            list.remove(list.get(cur));
        }        
        return list.get(0);
    }
}
```
<br><br>

## 题目47：求1+2+3+...+n
**求1+2+3+...+n，要求不能使用乘除法、for、while、if、else、switch、case等关键字及条件判断语句（A?B:C）。**

### 解法1：递归
#### 思路：
1. 设置递归退出条件，当 n <= 1 时，直接返回 1；
2. 其他条件下，n = n + Sum_Solution(n-1)。
```java
public class Solution {
    public int Sum_Solution(int n) {
        if(n <= 1) return 1;
        n = n + Sum_Solution(n-1);
        return n;
    }
}
```
<br><br>

## 题目48：不用加减乘除做加法
**写一个函数，求两个整数之和，要求在函数体内不得使用+、-、*、/四则运算符号。**

### 解法1：!!! 位运算做加法 !!!
#### 思路：
1. 计算 a 与 b 相加的结果，使用位运算；
2. 当数 a 不为 0 时：
* 赋值 tmp 为 a 与 b 相或;
* 赋值 a 为 a 与 b 相与，并且左移一位；
* 赋值 b 为 tmp；
3. 循环直到 a 为 0，此时输出 b 即可。
```java
public class Solution {
    public int Add(int num1,int num2) {
        while(num1 != 0){
             int tmp = num1 ^ num2;
             num1 = (num1 & num2) << 1;
             num2 = tmp;
         }
        return num2;
    }
}
```
<br><br>

## 题目49：把字符串转换成整数
**将一个字符串转换成一个整数，要求不能使用字符串转换整数的库函数。 数值为0或者字符串不是一个合法的数值则返回0。**

### 解法1：字符串/循环判断
#### 思路：
1. 建立 flag 和 ans 用于结果输出；
2. 先判断首位，是+/-/数字/其他字符，分别对应处理；
3. 循环处理字符串，利用 ans = 当前 + ans * 10 赋值；
4. 返回结果，包含正负。
```java
public class Solution {
    public int StrToInt(String str) {
        if(str == null || str.length() == 0) return 0;
        int flag = 1,ans = 0; // flag 表示正负，ans 表示结果。
        int i = 0;            // i 表示索引。
        //判断首位是+/-/数字/其他字符，分别对应处理。
        if(str.charAt(i) == '+' || str.charAt(i) == '-'){
            flag = str.charAt(i) == '+' ? 1:-1;
        }else if(str.charAt(i) >= '0' && str.charAt(i) <= '9'){
            flag = 1;
            ans = str.charAt(i)-'0' + ans * 10;
        }else{
            return 0;
        }
        //从下一位开始循环，利用 ans = 当前 + ans * 10 赋值。
        for(i=i+1;i<str.length();i++){
            if(str.charAt(i) >= '0' && str.charAt(i) <= '9'){
                ans = str.charAt(i)-'0' + ans * 10;
            }else{
                return 0;
            }
        }
        //返回结果，包含正负。
        return ans * flag;
    }
}
```
<br><br>

## 题目50：数组中重复的数字
**在一个长度为n的数组里的所有数字都在0到n-1的范围内。 数组中某些数字是重复的，但不知道有几个数字是重复的。也不知道每个数字重复几次。请找出数组中第一个重复的数字。 例如，如果输入长度为7的数组{2,3,1,0,2,5,3}，那么对应的输出是第一个重复的数字2。

返回描述：
如果数组中有重复的数字，函数返回true，否则返回false。
如果数组中有重复的数字，把重复的数字放到参数duplication[0]中。（ps:duplication已经初始化，可以直接赋值使用。）。**

### 解法1：哈希表
#### 思路：
1. 建立 flag 和 ans 用于结果输出；
2. 当数 a 不为 0 时，：
* 赋值 tmp 为 a 与 b 相或;
* 赋值 a 为 a 与 b 相与，并且左移一位；
* 赋值 b 为 tmp；
3. 循环直到 a 为 0，此时输出 b 即可。
```java
public class Solution {
    public int StrToInt(String str) {
        if(str == null || str.length() == 0) return 0;
        int flag = 1,ans = 0; // flag 表示正负，ans 表示结果。
        int i = 0;            // i 表示索引。
        //判断首位是+/-/数字/其他字符，分别对应处理。
        if(str.charAt(i) == '+' || str.charAt(i) == '-'){
            flag = str.charAt(i) == '+' ? 1:-1;
        }else if(str.charAt(i) >= '0' && str.charAt(i) <= '9'){
            flag = 1;
            ans = str.charAt(i)-'0' + ans * 10;
        }else{
            return 0;
        }
        //从下一位开始循环，利用 ans = 当前 + ans * 10 赋值。
        for(i=i+1;i<str.length();i++){
            if(str.charAt(i) >= '0' && str.charAt(i) <= '9'){
                ans = str.charAt(i)-'0' + ans * 10;
            }else{
                return 0;
            }
        }
        //返回结果，包含正负。
        return ans * flag;
    }
}
```
<br><br>

## 题目51：构建乘积数组
**给定一个数组A[0,1,...,n-1],请构建一个数组B[0,1,...,n-1],其中B中的元素B[i]=A[0]×A[1]×...×A[i-1]×A[i+1]×...×A[n-1]。不能使用除法。（注意：规定B[0] = A[1] × A[2] × ... × A[n-1]，B[n-1] = A[0] × A[1] × ... × A[n-2];）对于A长度为1的情况，B无意义，故而无法构建，因此该情况不会存在。**

### 解法1：二层循环
#### 思路：
1. 建立 B[]用于结果输出；
2. 当 A 长度小于等于 1 时，直接返回 B；
3. 进入 for 循环：
    * 一层循环内先赋值 B[i] = 1，用于计算乘积；
    * 二层循环内初始化 tmp ：若当前 i == j，则为1，否则为 A[j]，然后累乘；
4. 返回 B。
```java
import java.util.ArrayList;
public class Solution {
    public int[] multiply(int[] A) {
        int B[] = new int[A.length];
        if(A.length <= 1) return B;
        for(int i=0;i<A.length;i++){
            B[i] = 1;
            for(int j=0;j<A.length;j++){
                int tmp = i==j? 1:A[j];
                B[i] = B[i] * tmp;
            }
        }
        return B;
    }
}
```
### 解法2：左右循环
#### 思路：
1. 建立 B[]用于结果输出；
2. 当 A 长度小于等于 1 时，直接返回 B；
3. 新建 tmp 为 1，用于计算乘积，进入 for 左循环，每次让 B[i] 为 tmp， tmp 为累乘，即 B 结束后为对应位前面所有项的乘积；
4. 赋值 tmp 为 1，进入 for 右循环，每次让 B[i] 为 B[i]*tmp，tmp 为后面位的累乘，即 B 结束后为对应位乘 后面所有项的乘积。
5. 返回即可。
```java
import java.util.ArrayList;
public class Solution {
    public int[] multiply(int[] A) {
        int B[] = new int[A.length];
        if(A.length <= 1) return B;
        int tmp = 1;
        for(int i=0;i<A.length;i++){
            B[i] = tmp;
            tmp = tmp * A[i];
        }
        tmp = 1;
        for(int i=A.length-1;i>=0;i--){
            B[i]=B[i]*tmp;
            tmp = tmp * A[i];
        }
        return B;
    }
}
```
<br><br>

## 题目54：字符流中第一个不重复的字符
**请实现一个函数用来找出字符流中第一个只出现一次的字符。例如，当从字符流中只读出前两个字符"go"时，第一个只出现一次的字符是"g"。当从该字符流中读出前六个字符“google"时，第一个只出现一次的字符是"l"。如果当前字符流没有存在出现一次的字符，返回#字符。**

### 解法1：字符流处理
#### 思路：
1. 首先建立类内字段 rec[] 用来记录插入字符出现的次数，index 用来记录插入字符的先后顺序，index 越小，插入时间越早；
2. Insert 方法用于在插入字符时，对当前字符对应的状态进行改变：
* 若当前字符对应次数为 0，说明第一次出现，则将其赋值为 index，然后index ++;
* 若当前字符对应次数不为 0，说明不只出现一次，则将其赋值为 -1，用于标记。
3. FirstAppearingOnce 方法用于从 rec[] 中得到出现一次的最先记录，赋值ans为 '#'：
* 若循环中判断未进入，则说明不存在出现一次的字符，直接返回 '#'；
* 若循环中判断进入，则逐次将较小的 rec[i] 赋值为 cul，ans 则赋值为 当前 i 表示的字符。 
4. 返回 ans 即可。
```java
public class Solution {
    private int[] rec = new int[256];
    private int index = 1;
    //Insert one char from stringstream
    public void Insert(char ch)
    {
        if(rec[ch] == 0){
            rec[ch] = index;
            index ++;
        }else{
            rec[ch] = -1;
        }
    }
  //return the first appearence once char in current stringstream
    public char FirstAppearingOnce()
    {
        char ans = '#';
        int cul = Integer.MAX_VALUE;
        for(int i=0;i<rec.length;i++){
            if(rec[i] != -1 && rec[i] != 0 && rec[i] < cul){
                cul = rec[i];
                ans = (char) i;
            }
        }
        return ans;
    }
}
```
<br><br>

## 题目55：链表中环的入口结点
**给一个链表，若其中包含环，请找出该链表的环的入口结点，否则，输出null。**

### 解法1：哈希表
#### 思路：
1. 边界条件；
2. 建立 HashSet<ListNode>；
2. 循环链表：
* 若当前节点在 set 内，则说明此时的节点为环入口，返回即可；
* 若当前节点不在 set 内，则添加此节点到 set。
3. 循环完毕没有返回，说明无环，则返回 null。
```java
/*
 public class ListNodeListNode {
    int val;
    ListNode next = null;

    ListNode(int val) {
        this.val = val;
    }
}
*/
import java.util.*;
public class Solution {
    public ListNode EntryNodeOfLoop(ListNode pHead){
        if(pHead == null)    return null;
        ListNode pH = pHead;
        Set<ListNode> set = new HashSet<>();
        while(pH != null){
            if(set.contains(pH)){
                return pH;
            }else{
                set.add(pH);
                pH = pH.next;
            }
        }
        return null; 
    }
}
```
<br><br>

## 题目56：删除链表中重复的结点
**在一个排序的链表中，存在重复的结点，请删除该链表中重复的结点，重复的结点不保留，返回链表头指针。 例如，链表1->2->3->3->4->4->5 处理后为 1->2->5。**

### 解法1：链表处理，定义 head,pre,last 三个节点进行操作。
#### 思路：
1. 首先检查**头结点**及**头结点下一个节点**是否为空，若为空直接返回即可；
2. 定义一个新节点 head，其下一个节点指向 pHead，定义 pre为 head，last 为 head.next；
3. 进入 while 循环，当 last 不为空时：
    * 判断 **last.next 节点是否为空** 及 **last 与 last.next 节点的值是否相等**，若都成立，说明没到末尾且存在相等值，则进入 while 循环，让last = last.next，直到**不等**或**为空**，while 循环结束，此时**last.next 为空** 或 **last 与 last.next 节点的值不等**，即 当前last的值还在重复中，则将 pre.next 指向 last.next，last变为 last.next；
    * 其他情况下，pre 赋值 pre.next，last 赋值 last.next；
4. 返回 head.next 即可。
```java
/*
 public class ListNode {
    int val;
    ListNode next = null;

    ListNode(int val) {
        this.val = val;
    }
}
*/
import java.util.*;
public class Solution {
    public ListNode deleteDuplication(ListNode pHead){
        if(pHead == null || pHead.next == null) return pHead;
        ListNode head = new ListNode(0);
        head.next = pHead;
        ListNode pre = head;
        ListNode last = head.next;
        while(last != null){
            if(last.next != null && last.val == last.next.val){
                while(last.next != null && last.val == last.next.val){
                    last = last.next;
                }
                pre.next = last.next;
                last = last.next;
            }else{
                pre = pre.next;
                last = last.next;
            }
        }
        return head.next;
    }
}
```
<br><br>

## 题目57：二叉树的下一个结点
**给定一个二叉树和其中的一个结点，请找出中序遍历顺序的下一个结点并且返回。注意，树中的结点不仅包含左右子结点，同时包含指向父结点的指针。**

### 解法1：递归中序遍历
#### 思路：
1. 边界条件；
2. 循环到根节点，中序遍历得到 list；
3. 循环找到 list 中节点的位置，返回结果即可，注意：
    * 若 i = list.size()-1 说明到达最后一个，则输出 null；
    * 若不等，则输出 list.get(i+1) 即可；
```java
/*
public class TreeLinkNode {
    int val;
    TreeLinkNode left = null;
    TreeLinkNode right = null;
    TreeLinkNode next = null;

    TreeLinkNode(int val) {
        this.val = val;
    }
}
*/
import java.util.*;
public class Solution {
    public TreeLinkNode GetNext(TreeLinkNode pNode){
        if(pNode == null)    return null;
        List<TreeLinkNode> list = new ArrayList<>();
        TreeLinkNode pHead = pNode;
        while(pHead.next != null){
            pHead = pHead.next;
        }
        inorder(list, pHead);
        int i=0;
        for(;i<list.size();i++){
            if(list.get(i) == pNode) break;
        }
        return i == list.size()-1 ? null : list.get(i+1);        
    }
    private void inorder(List<TreeLinkNode> list, TreeLinkNode pNode){
        if(pNode == null)    return;
        inorder(list, pNode.left);
        list.add(pNode);
        inorder(list, pNode.right);
    }
}
```
<br><br>

## 题目58：对称的二叉树
**请实现一个函数，用来判断一棵二叉树是不是对称的。注意，如果一个二叉树同此二叉树的镜像是同样的，定义其为对称的。**

### 解法1：层序遍历
#### 思路：
1. 边界条件；
2. 把每一层进行对称判断；
3. 存在问题，若是以下结构，无法判断：
```
        5
    5       5
  5   5   5   5
5  # 5 # # # #  #
```
```java
/*
public class TreeNode {
    int val = 0;
    TreeNode left = null;
    TreeNode right = null;

    public TreeNode(int val) {
        this.val = val;

    }

}
*/
import java.util.*;
public class Solution {
    boolean isSymmetrical(TreeNode pRoot){
        if(pRoot == null)    return true;
        Queue<TreeNode> queue = new LinkedList<>();
        //直接将根节点的左右子节点添加
        if(pRoot.left != null)    queue.offer(pRoot.left);
        if(pRoot.right != null)    queue.offer(pRoot.right);
        //若无，直接退出，返回true
        while(!queue.isEmpty()){
            int size = queue.size();
            //若某一层的节点数不为偶数，则一定不对称，返回false
            if(size % 2 != 0)    return false;
            //循环内分一半判断前半段和后半段是否相等
            int length = size/2;
            int[] tmp = new int[length];
            while(size > 0){
                TreeNode node = queue.poll();
                if(size > length){
                    tmp[length*2 - size] = node.val;
                }else{
                    if(node.val != tmp[size-1]) return false;
                }
                if(node.left != null)    queue.offer(node.left);
                if(node.right != null)    queue.offer(node.right);
                size --;
            }
        }
        return true;
    }
}
```

### 解法2：递归
**递归方法一定是传入两个参数，因为涉及到两个分支的比较。**
#### 思路：
1. 边界条件；
2. 返回递归方法，方法传入根节点的左、右子节点；
3. 递归方法：
    1. 退出条件设置：
    * 如果两个参数都为空，则直接返回 true；
    * 如果两个参数有一个为空，则不对称，返回 false。
    2. 退出条件之外，判断三项：
    * 两节点值相等；
    * 递归判断 1 节点的左子节点和 2 节点的右子节点是否符合规则；
    * 递归判断 1 节点的右子节点和 2 节点的左子节点是否符合规则；
4. 输出结果即可。
```
        5
    5       5
  5   5   5   5
5  # 5 # # # #  #
```
```java
/*
public class TreeNode {
    int val = 0;
    TreeNode left = null;
    TreeNode right = null;

    public TreeNode(int val) {
        this.val = val;

    }

}
*/
import java.util.*;
public class Solution {
    boolean isSymmetrical(TreeNode pRoot){
        if(pRoot == null)    return true;
        return leftAndRightIsSym(pRoot.left, pRoot.right);
    }
    private boolean leftAndRightIsSym(TreeNode le, TreeNode ri){
        if(le == null && ri == null)    return true;
        if(le == null || ri == null)    return false;
        return le.val == ri.val && leftAndRightIsSym(le.right,ri.left) && leftAndRightIsSym(le.left,ri.right);
    }
}
```
<br><br>

## 题目59：按之字形顺序打印二叉树
**请实现一个函数按照之字形打印二叉树，即第一行按照从左到右的顺序打印，第二层按照从右至左的顺序打印，第三行按照从左到右的顺序打印，其他行以此类推。**

### 解法1：层序遍历 + 双堆栈
#### 思路：
1. 边界条件；
2. 建立两个堆栈，分别用于奇数层和偶数层的遍历；
3. 将每一层的结果存入 list，然后再存放到 lists；
4. 返回 lists 即可。

```java
import java.util.ArrayList;

/*
public class TreeNode {
    int val = 0;
    TreeNode left = null;
    TreeNode right = null;

    public TreeNode(int val) {
        this.val = val;

    }
}
*/
import java.util.*;
public class Solution {
    public ArrayList<ArrayList<Integer> > Print(TreeNode pRoot) {
        ArrayList<ArrayList<Integer>> lists = new ArrayList<>();
        if(pRoot == null)    return lists;
        Stack<TreeNode> stack1 = new Stack<>();
        Stack<TreeNode> stack2 = new Stack<>();
        stack1.push(pRoot);
        while(!stack1.isEmpty() || !stack2.isEmpty()){
            ArrayList<Integer> list = new ArrayList<>();
            if(!stack1.isEmpty()){
                while(!stack1.isEmpty()){
                    TreeNode node = stack1.pop();
                    if(node.left != null)    stack2.push(node.left);
                    if(node.right != null)    stack2.push(node.right);
                    list.add(node.val);
                }
            }else{
                while(!stack2.isEmpty()){
                    TreeNode node = stack2.pop();
                    if(node.right != null)    stack1.push(node.right);
                    if(node.left != null)    stack1.push(node.left); 
                    list.add(node.val);
                }
            }
            lists.add(list);
        }
        return lists;
    }

}
```
<br><br>


## 题目60：把二叉树打印成多行
**从上到下按层打印二叉树，同一层结点从左至右输出。每一层输出一行。**

### 解法1：层序遍历
#### 思路：
1. 边界条件；
2. 层序遍历；
4. 返回 lists 即可。

```java
/*
public class TreeNode {
    int val = 0;
    TreeNode left = null;
    TreeNode right = null;

    public TreeNode(int val) {
        this.val = val;

    }

}
*/
import java.util.*;
public class Solution {
    ArrayList<ArrayList<Integer> > Print(TreeNode pRoot) {
        ArrayList<ArrayList<Integer>> lists = new ArrayList<>();
        if(pRoot == null)    return lists;
            Queue<TreeNode> queue = new LinkedList<>();
        queue.offer(pRoot);
        while(!queue.isEmpty()){
            int size = queue.size();
            ArrayList<Integer> list = new ArrayList<>();
            while(size>0){
                TreeNode node = queue.poll();
                if(node.left != null)    queue.offer(node.left);
                if(node.right != null)    queue.offer(node.right);
                list.add(node.val);
                size--;
            }
            lists.add(list);
        }
        return lists;
    }
}
```
<br><br>

## 题目61：序列化二叉树
**请实现两个函数，分别用来序列化和反序列化二叉树：**</br>
**二叉树的序列化是指：把一棵二叉树按照某种遍历方式的结果以某种格式保存为字符串，从而使得内存中建立起来的二叉树可以持久保存。序列化可以基于先序、中序、后序、层序的二叉树遍历方式来进行修改，序列化的结果是一个字符串，序列化时通过 某种符号表示空节点（#），以 ！ 表示一个结点值的结束（value!）。二叉树的反序列化是指：根据某种遍历顺序得到的序列化字符串结果str，重构二叉树。例如，我们可以把一个只有根节点为1的二叉树序列化为"1,"，然后通过自己的函数来解析回这个二叉树。**


### 注意
1. str.split("!") 根据 某段字符串""，将 str 分为几段 String[]。
2. 由于 strs[] 为 String[] 类型，则赋值采用：
```
node.val = Integer.parseInt(strs[index]);
```
3. StringBuilder sb = new StringBuilder()l; 中 sb.append() 内加字符串而非字符：
```
sb.append("#!").toString();
```

### 解法1：前序遍历
#### 思路：
1. 边界条件；
2. preorder 用于递归前序遍历；
3. revpreorder 用于递归根据字符串赋值二叉树；

```java
/*
public class TreeNode {
    int val = 0;
    TreeNode left = null;
    TreeNode right = null;

    public TreeNode(int val) {
        this.val = val;

    }

}
*/
import java.util.*;
public class Solution {
    
    //序列化
    String Serialize(TreeNode root) {
        StringBuilder sb = new StringBuilder();
        if(root == null)    return sb.append("#!").toString();
        preorder(root, sb);
        return sb.toString();
    }
    private void preorder(TreeNode node, StringBuilder sb){
        if(node == null){
            sb.append("#!");
            return;
        }
        sb.append(node.val  + "!");
        preorder(node.left, sb);
        preorder(node.right, sb);
    }
    
    //反序列化
    TreeNode Deserialize(String str) {
        if(str == null || str.length() == 0)    return null;
        return revpreorder(str.split("!"));
    }
    private int index = -1;
    
    private TreeNode revpreorder(String[] strs){
        index ++;
        if(strs[index].equals("#")){ //用equals，不用==
            return null;
        }
        TreeNode node = new TreeNode(0);
        node.val = Integer.parseInt(strs[index]);
        node.left = revpreorder(strs);
        node.right = revpreorder(strs);
        return node;
    }
}
```
<br><br>


## 题目62：二叉搜索树的第k个结点
**给定一棵二叉搜索树，请找出其中的第k小的结点。**

### 解法1：中序遍历（全部遍历）
#### 思路：
1. 边界条件；
2. inorder 用于递归中序遍历；
3. 判断 k 是否大于 size，若大于则返回 null，否则返回结果；

```java
/*
public class TreeNode {
    int val = 0;
    TreeNode left = null;
    TreeNode right = null;

    public TreeNode(int val) {
        this.val = val;

    }
}
*/
import java.util.*;
public class Solution {
    TreeNode KthNode(TreeNode pRoot, int k){
        if(pRoot == null || k == 0)    return null;
        List<TreeNode> list = new ArrayList<>();
        inorder(pRoot, list);
        return k > list.size() ? null:list.get(k-1);
    }
    private void inorder(TreeNode node, List<TreeNode> list){
        if(node == null)    return;
        inorder(node.left, list);
        list.add(node);
        inorder(node.right, list);
    }
}
```

### 解法2：中序遍历（部分遍历）
#### 思路：
1. 边界条件；
2. inorder 用于递归中序遍历；
3. 判断 k 是否大于全局变量 index，若大于则返回 null，否则返回 index 结果；

```java
/*
public class TreeNode {
    int val = 0;
    TreeNode left = null;
    TreeNode right = null;

    public TreeNode(int val) {
        this.val = val;

    }

}
*/
import java.util.*;
public class Solution {
    TreeNode KthNode(TreeNode pRoot, int k){
        if(pRoot == null || k == 0)    return null;
        inorder(pRoot,k);
        return index < k ? null : ans;
    }
    private int index = 0;
    private TreeNode ans = new TreeNode(0);
    private void inorder(TreeNode node,int k){
        if(node == null)    return;
        inorder(node.left,k);
        index++;
        if(index == k){
            ans = node;
            return;
        }
        inorder(node.right,k);
    }
}
```
<br><br>


## 题目63：数据流中的中位数
**如何得到一个数据流中的中位数？如果从数据流中读出奇数个数值，那么中位数就是所有数值排序之后位于中间的数值。如果从数据流中读出偶数个数值，那么中位数就是所有数值排序之后中间两个数的平均值。我们使用Insert()方法读取数据流，使用GetMedian()方法获取当前读取数据的中位数。**

### 注意：优先队列/大/小顶堆
1. 堆结构在逻辑上是完全二叉树，物理存储上是数组。
2. 默认维护小顶堆，即入列后自动排序，出列输出最小的那个数，可以自己覆写比较器实现规则；
3. 方法：
    * add()和offer()
    add(E e)和offer(E e)的语义相同，都是向优先队列中插入元素，只是Queue接口规定二者对插入失败时的处理不同，前者在插入失败时抛出异常，后则则会返回false。对于PriorityQueue这两个方法其实没什么差别。
    * element()和peek()
    element()和peek()的语义完全相同，都是获取但不删除队首元素，也就是队列中权值最小的那个元素，二者唯一的区别是当方法失败时前者抛出异常，后者返回null。根据小顶堆的性质，堆顶那个元素就是全局最小的那个；由于堆用数组表示，根据下标关系，0下标处的那个元素既是堆顶元素，所以直接返回数组0下标处的那个元素即可。
    * remove()和poll()
    remove()和poll()方法的语义也完全相同，都是获取并删除队首元素，区别是当方法失败时前者抛出异常，后者返回null。由于删除操作会改变队列的结构，为维护小顶堆的性质，需要进行必要的调整。
    * remove(Object o)
    remove(Object o)方法用于删除队列中跟o相等的某一个元素（如果有多个相等，只删除一个），该方法不是Queue接口内的方法，而是Collection接口的方法。由于删除操作会改变队列结构，所以要进行调整；又由于删除元素的位置可能是任意的，所以调整过程比其它函数稍加繁琐。具体来说，remove(Object o)可以分为2种情况：
        1. 删除的是最后一个元素。直接删除即可，不需要调整。
        2. 删除的不是最后一个元素，从删除点开始以最后一个元素为参照调用一次siftDown()即可。

### 解法1：优先队列/大/小顶堆
#### 思路：
1. 全局：
    * cnt：用于判断此时数据流数量的奇偶性；
    * low：用于存放大数，默认维护小顶堆；
    * high：用于存放小数，维护大顶堆（**需要自己实现 Comparator 方法**）；
2. **Insert()** 存入数据流：
    * 每次进入此方法 cnt + 1；
    * 数据流数量为偶数时，此时**大顶堆个数 = 小顶堆个数 + 1**，需要添加数到 **小顶堆**：
        1. 比较 num 与大顶堆出列数的大小：若 num 小，则将其存入大顶堆，然后将 num 赋值为大顶堆出列数；
        2. 将此时的 num 存入 小顶堆。
    * 数据流数量为奇数时，此时**大顶堆个数 = 小顶堆个数**，需要添加数到 **大顶堆**：
        1. 比较 num 与小顶堆出列数的大小：若 num 大，则将其存入小顶堆，然后将 num 赋值为小顶堆出列数；
        2. 将此时的 num 存入 大顶堆。
3. **GetMedian()** 读取数据流：
    * 数据流数量为偶数时，此时输出 (大顶堆出列数字 + 小顶堆个数出列数字)/2 ；
    * 数据流数量为奇数时，此时输出 大顶堆出列数字；

```java
import java.util.*;
public class Solution {
    //用于判断此时数据流数量的奇偶性
    private int cnt = 0;
    //用于存放大数，默认维护小顶堆
    private PriorityQueue<Integer> low = new PriorityQueue<>();
    //用于存放小数，维护大顶堆
    private PriorityQueue<Integer> high = new PriorityQueue<>(new Comparator<Integer>(){
        @Override
        public int compare(Integer i1,Integer i2){
            return i2.compareTo(i1);
        }
    });

    public void Insert(Integer num) {
        cnt++;
        //数据流数量为偶数时，存入
        if(cnt % 2 == 0){
            if(!high.isEmpty() && num < high.peek()){
                high.offer(num);
                num = high.poll();
            }
            low.offer(num); 
        }else{//数据流数量为奇数时，存入
            if(!low.isEmpty() && num > low.peek()){
                low.offer(num);
                num = low.poll();
            }
            high.offer(num); 
        }
    }

    public Double GetMedian() {
        double ans;
        //数据流数量为偶数时，取出
        if(cnt % 2 == 0){
            ans = (high.peek() + low.peek()) / 2.0;
        }else{//数据流数量为奇数时。取出
            ans = high.peek();
        }
        return ans;
    }
}
```
<br><br>


## 题目64：滑动窗口的最大值
**给定一个数组和滑动窗口的大小，找出所有滑动窗口里数值的最大值。例如，如果输入数组{2,3,4,2,6,2,5,1}及滑动窗口的大小3，那么一共存在6个滑动窗口，他们的最大值分别为{4,4,6,6,6,5}； 针对数组{2,3,4,2,6,2,5,1}的滑动窗口有以下6个： {[2,3,4],2,6,2,5,1}， {2,[3,4,2],6,2,5,1}， {2,3,[4,2,6],2,5,1}， {2,3,4,[2,6,2],5,1}， {2,3,4,2,[6,2,5],1}， {2,3,4,2,6,[2,5,1]}。窗口大于数组长度的时候，返回空。**

### 解法1：双循环
#### 思路：
1. 边界条件，以下三种情况时，直接输出空 list：
    * num 长度为零；
    * size 为零；
    * size 大于 num 长度；
2. 第一个 for 循环，遍历每个窗口的第一个元素；
3. 循环内初始化一个最大值 eveNum，然后进第二个 for 循环，遍历窗口内每个元素求最大值，在循环结束将最大值 eveNum 添加进 list；
4. 返回 list 即可。
```java
import java.util.*;
public class Solution {
    public ArrayList<Integer> maxInWindows(int [] num, int size){
        ArrayList<Integer> list = new ArrayList<>();
        if(num.length == 0 || size == 0 || size > num.length)    return list;
        for(int i=0;i<=num.length-size;i++){
            int eveNum = Integer.MIN_VALUE;
            for(int j=i;j<i+size;j++){
                eveNum = Math.max(eveNum, num[j]);
            }
            list.add(eveNum);
        }
        return list;
    }
}
```
<br><br>

## 题目65：矩阵中的路径
**请设计一个函数，用来判断在一个矩阵中是否存在一条包含某字符串所有字符的路径。路径可以从矩阵中的任意一个格子开始，每一步可以在矩阵中向左，向右，向上，向下移动一个格子。如果一条路径经过了矩阵中的某一个格子，则该路径不能再进入该格子。如矩阵中包含一条字符串"bcced"的路径，但是矩阵中不包含"abcb"路径，因为字符串的第一个字符b占据了矩阵中的第一行第二个格子之后，路径不能再次进入该格子。**
```
输入
"ABCESFCSADEE",3,4,"ABCCED"
返回值
true
```
### 解法1：回溯法
#### 思路：
1. 边界条件，以下情况时，直接输出 false：
    * matrix 长度为零；
    * matrix 长度小于 str 长度；
2. 建立 flag[matrix.length] 标志位，初始化为false；
3. 回溯法：循环遍历二维数组，找到起点等于 str 第一个元素的值，再递归判断四周是否符合条件；
4. backTrack() 方法：
* backTrack(初始矩阵，索引行坐标 i，索引纵坐标 j，矩阵行数，矩阵列数，待判断的字符串，字符串索引初始为 0 即先判断字符串的第一位)；
* 先根据 i 和 j 计算匹配的第一个元素转为一维数组的位置；
* 设置递归终止条件；
* 若 k 已经到达 str 末尾了，说明之前的都已经匹配成功了，直接返回 true 即可；
* 若未达到末尾，则设置当前位置 flag 为已经选择过，然后递归对当前位置 上下左右 进行判断，若成立返回 true；
* 若不成立，设置当前位置 flag 为未选择，然后返回 false。
5. 当主循环结束，未返回 true，说明不存在路径，返回 false 即可。
。
```java
import java.util.*;
public class Solution {
    public boolean hasPath(char[] matrix, int rows, int cols, char[] str){
        if(matrix.length == 0 || matrix.length < str.length)    return false;
        boolean[] flag = new boolean[matrix.length];
        for(int i=0;i<rows;i++){
            for(int j=0;j<cols;j++){
                if(backTrack(matrix,i,j,rows,cols,flag,str,0)){
                    return true;
                }                
            }
        }
        return false;
    }
    private boolean backTrack(char[] matrix, int i, int j, int rows, int cols, boolean[] flag, char[] str, int k){
        //注意 flag 索引 index 的计算方法
        int index = i*cols + j;
        if(i<0 || j<0 || i>=rows || j>=cols || flag[index] == true || k>=str.length || matrix[index] != str[k]){
            return false;
        }
        if(k == str.length-1){
            return true;
        }
        flag[index] = true;
        if(backTrack(matrix,i-1,j,rows,cols,flag,str,k+1) || backTrack(matrix,i+1,j,rows,cols,flag,str,k+1) 
          || backTrack(matrix,i,j-1,rows,cols,flag,str,k+1) || backTrack(matrix,i,j+1,rows,cols,flag,str,k+1)){
            return true;
        }
        flag[index] = false;
        return false;
    }
}
```
<br><br>

## 题目66：机器人的运动范围
**地上有一个m行和n列的方格。一个机器人从坐标0,0的格子开始移动，每一次只能向左，右，上，下四个方向移动一格，但是不能进入行坐标和列坐标的数位之和大于k的格子。 例如，当k为18时，机器人能够进入方格（35,37），因为3+5+3+7 = 18。但是，它不能进入方格（35,38），因为3+5+3+8 = 19。请问该机器人能够达到多少个格子。**
```
输入
5,10,10
返回值
21
```
### 解法1：回溯法
#### 思路：
1. 不进行边界条件判断；
2. 建立 flag[][] 标志位，初始化为false；
3. 回溯法 backTrack() 方法：
    * backTrack(数位之和，行坐标 i，纵坐标 j，矩阵行数，矩阵列数，标志位矩阵)；
    * 设置递归终止条件；
    * 若未退出递归，则标记此位置走过了，赋值 true 即可；
    * 返回 上下左右 + 1。
5. cul() 用于计算一个数按位相加后的结果，用于递归退出条件判断。
```java
public class Solution {
    public int movingCount(int threshold, int rows, int cols){
        boolean[][] flag = new boolean[rows][cols];
        return backTrack(threshold, 0 ,0 ,rows, cols, flag);
    }
    private int backTrack(int threshold, int i, int j, int rows, int cols, boolean[][] flag){
        if(i<0 || j<0 || i>=rows || j>=cols || flag[i][j] == true || cul(i)+cul(j) > threshold){
            return 0;
        }
        flag[i][j] = true;
        return backTrack(threshold, i-1, j, rows, cols, flag) + 
            backTrack(threshold, i+1, j, rows, cols, flag) +
            backTrack(threshold, i, j-1, rows, cols, flag) +
            backTrack(threshold, i, j+1, rows, cols, flag) + 1 ;   
    }
    private int cul(int num){
        int sum = 0;
        int numc = num;
        while(numc != 0){
            sum = sum + numc % 10;
            numc = numc / 10;
        }
        return sum;
    }
}
```


<br><br>

## 题目67：剪绳子
**给你一根长度为n的绳子，请把绳子剪成整数长的m段（m、n都是整数，n>1并且m>1，m<=n），每段绳子的长度记为k[1],...,k[m]。请问k[1]x...xk[m]可能的最大乘积是多少？例如，当绳子的长度是8时，我们把它剪成长度分别为2、3、3的三段，此时得到的最大乘积是18。**
```
输入描述:
    输入一个数n，意义见题面。（2 <= n <= 60）
返回值描述:
    输出答案。
```
### 解法1：数学
#### 思路：
1. 边界条件判断；
2. 三种情况：
    * target % 3 == 1 时，返回 4 * (int) Math.pow(3, target/3 - 1)；
    * target % 3 == 2 时，返回 2 * (int) Math.pow(3, target/3)；
    * target % 3 == 0 时，返回 (int) Math.pow(3, target/3)；
5. 返回结果。
```java
public class Solution {
    public int cutRope(int target) {
        if(target == 2){
            return 1;
        }else if(target == 3){
            return 2;
        }else if(target % 3 == 1){
            return 4 * (int) Math.pow(3, target/3 - 1);
        }else if(target % 3 == 2){
            return 2 * (int) Math.pow(3, target/3);
        }else{
            return (int) Math.pow(3, target/3);
        }
    }
}
```
