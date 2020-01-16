## Linked
https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/

## Problem
```
Given an array of integers that is already sorted in ascending order, find two numbers such that they add up to a specific target number.

The function twoSum should return indices of the two numbers such that they add up to the target, where index1 must be less than index2.

Note:

Your returned answers (both index1 and index2) are not zero-based.
You may assume that each input would have exactly one solution and you may not use the same element twice.
Example:

Input: numbers = [2,7,11,15], target = 9
Output: [1,2]
Explanation: The sum of 2 and 7 is 9. Therefore index1 = 1, index2 = 2.
```

## 思路
A. 与0001思路一样，区别在于返回index按照语言逻辑序列
B. 假如题目空间复杂度有要求，由于数组是有序的，只需要双指针即可。一个left指针，一个right指针， 如果left + right 值 大于target 则 right左移动， 否则left右移，代码见下方python code。

## 答案
```
Runtime: 48 ms
class Solution:
    def twoSum(self, numbers: List[int], target: int) -> List[int]:
        dictionary = {}
        for index, number in enumerate(numbers):
            if target-number in dictionary:
                return [dictionary[target - number], index + 1]
            else:
                dictionary[number] = index + 1
```
```
Two Pointers - Runtime: 48 ms
class Solution:
    def twoSum(self, numbers: List[int], target: int) -> List[int]:
        left, right = 0, len(numbers) - 1
        while left < right:
            if numbers[left] + numbers[right] < target:
                left += 1
            if numbers[left] + numbers[right] > target:
                right -= 1
            if numbers[left] + numbers[right] == target:
                return [left+1, right+1]
```                
