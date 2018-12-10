---
layout: post
title:  "Leetcode题3Sum解"					
modified: 2018-12-10			# Date
category: Academic
tags: []
comments: true
mathjax: true
---
{% include base.html %}

题目要求是给定数组nums，求无重复三元组，使三元组相加为0。
>Given array nums = [-1, 0, 1, 2, -1, -4],
>A solution set is:
>[
>  [-1, 0, 1],
>  [-1, -1, 2]
>]

以下算法复杂度O(n^2)且直接除去重复三元组

```python
class Solution:
    def threeSum(self, nums):
        """
        :type nums: List[int]
        :rtype: List[List[int]]
        """
        nums = sorted(nums) #首先进行排序
        res = []
        i = 0
        l = len(nums)
        while i < l:
            front = i+1 
            back = l - 1
            target = - nums[i] #固定第一个元素并设定头尾两个flag
            while front < back:
                tmp = nums[front] + nums[back]
                if tmp < target: #若过小则左flag右移
                    front += 1
                elif tmp > target: #若过大则右flag左移
                    back -= 1
                else: #正好则加入res
                    this = [nums[i], nums[front], nums[back]]
                    res += [this]
                    while front < back and nums[front] == this[1]: #左移移去重复
                        front += 1
                    while front < back and nums[back] == this[2]: #右移移去重复
                        back -= 1

            while i < l-1 and nums[i+1] == nums[i]: #若遇到重复则后移
                i+=1
            i+=1

        return res
```
将3Sum问题转化为2Sum问题

邻近的另一个问题3Sum Closest可以用类似方式进行解答
>Given array nums = [-1, 2, 1, -4], and target = 1.

>The sum that is closest to the target is 2. (-1 + 2 + 1 = 2). 

不重新上代码了，逻辑类似，sort后对i进行遍历，每次左右两个指针，故为N^2