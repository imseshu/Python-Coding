# 1. Two Sum
## Problem Statement:
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

 

**Example 1:**

Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].

**Example 2:**

Input: nums = [3,2,4], target = 6
Output: [1,2]

**Example 3:**

Input: nums = [3,3], target = 6
Output: [0,1]
 

**Constraints:**

2 <= nums.length <= 104
-109 <= nums[i] <= 109
-109 <= target <= 109
Only one valid answer exists.
 

Follow-up: Can you come up with an algorithm that is less than O(n2) time complexity?

## My Code:
```
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        for i in range(0,len(nums)):
            for j in range(i+1, len(nums)):
                if nums[i]+nums[j] == target:
                    return [i,j]
```
> ### Complexity Analysis:
>    1. Time Complexity : O(n^2)
>    2. Space Complexity : O(1)                  
## Using Hash-map:
![image](https://drive.google.com/uc?export=view&id=14irjgDmkFfbWonYJ8gzu2U_4NvBPOtW-)
## Hash-map Code:
```
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        hashidx={}
        for index, value in enumerate(nums):
            remaining=target-value
            if remaining in hashidx:
                return [index,hashidx[remaining]]
            else:
                hashidx[value]=index
```
> ### Complexity Analysis:
>    1. Time Complexity : O(n)
>    2. Space Complexity : O(n) 
## HAPPY CODING!!!