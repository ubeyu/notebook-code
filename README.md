# leetcode-notebook
刷题笔记：


## <注意点>

数组：

```
1.以下tmp赋值方法完全不同：
        int[] tmp=new int[nums.length];
        for(int i=0;i<nums.length;i++){
            tmp[i]=nums[i];
        } 
        直接赋值，赋值完毕与nums无关：
        
        int[] tmp=nums;
        引用，类似指针，tmp会随着nums变化而实时变化：
      
2.利用HashSet的元素不重复性，涉及到:set.contains(nums[i])、set.add(nums[i])方法。同时HashSet和HashMap相比Set是一维，Map是二维。
3.利用Arrays.sort(nums)排序方法，先排序，再判断相邻是否相等。
```

字符串：
```
1.long而非Long;
2.s.charAt(i)而非s.charAt[i];
3.s.indexOf('')可以找到字符在字符串的索引;
4.字符的大写字母比小写字母ASCII码小 32;
5.操作可变字符串使用StringBuilder或StringBuffer，在这些字符串尾部追加字符时用append;
6.equals可用于字符串的比较，不变字符串一般放到前面;
7.substring判断相等一般可以改写为循环每一位判断;
8.append时最好不要多个变量放到一起，可能会造成相加的现象;
               sb.append(String.valueOf(cur) + (sequence.charAt(sequence.length()-1)));
    最好写成：    sb.append(String.valueOf(cur));
                 sb.append((sequence.charAt(sequence.length()-1)));
```

