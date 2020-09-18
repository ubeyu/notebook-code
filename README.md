# leetcode-notebook
刷题笔记：


## <注意点>

数组：

```
以下tmp赋值方法完全不同：
1. 直接赋值，赋值完毕与nums无关：
        int[] tmp=new int[nums.length];
        for(int i=0;i<nums.length;i++){
            tmp[i]=nums[i];
        }
2. 引用，类似指针，tmp会随着nums变化而实时变化：
        int[] tmp=nums;
        
3.利用HashSet的元素不重复性，涉及到:set.contains(nums[i])、set.add(nums[i])方法。同时HashSet和HashMap相比Set是一维，Map是二维。
4.利用Arrays.sort(nums)排序方法，先排序，再判断相邻是否相等。
```

字符串：
```
1.long而非Long;
1.s.charAt(i)而非s.charAt[i];
3.s.indexOf('')可以找到字符在字符串的索引;
4.字符的大写字母比小写字母ASCII码小 32;
5.操作可变字符串使用StringBuilder或StringBuffer，在这些字符串尾部追加字符时用append;
```

