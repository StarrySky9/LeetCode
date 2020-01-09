### Problem:
https://leetcode.com/problems/two-sum/

```
## Description
Given an array of integers, return indices of the two numbers such that they add up to a specific target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

Example:

Given nums = [2, 7, 11, 15], target = 9,

Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].
```

## Code
```
##!python 3
class Solution(object):
    def twoSum(self, nums, target):
        """
        :type nums: List[int]
        :type target: int
        :rtype: List[int]
        """
        dict={}
        for i, n in enumerate(nums):
            m = target - n
            if m in dict:
                return [dict[m], i]
            else:
                dict[n] = i
 ```
 ## Think                
 1. 使用Python built-in function:enumerate()
 ```
     Python program to illustrate 
     enumerate function in loops 
    l1 = ["eat","sleep","repeat"] 
     printing the tuples in object directly 
    print(list(enumerate(l1)))
    
    # Output:
    [(0, 'eat'), (1, 'sleep'), (2, 'repeat')]
```    
2. 创建 空 字典保存"新" Key-value
    使得 index/key 与 value 对换，方便对比value与target


                
