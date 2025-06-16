# 🧮 Two Sum

🔗 [LeetCode Problem Link](https://leetcode.com/problems/two-sum/)

## 💬 Problem Statement:
Given an array of integers `nums` and an integer `target`, return the **indices of the two numbers** such that they add up to target.

### ✨ Example:
Input: `nums = [2, 7, 11, 15]`, `target = 9`  
Output: `[0, 1]`  
(2 + 7 = 9)

---

## 🧠 Approach:
- Loop through array.
- Use a hashmap to store previously seen numbers.
- Check if target - current number exists in hashmap.

---

## ✅ Python Code:

```python
def twoSum(nums, target):
    seen = {}
    for i, num in enumerate(nums):
        diff = target - num
        if diff in seen:
            return [seen[diff], i]
        seen[num] = i

