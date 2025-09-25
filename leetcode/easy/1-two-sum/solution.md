# Two Sum

## Problem Information
- **Platform:** Leetcode
- **Difficulty:** Easy
- **URL:** https://leetcode.com/problems/two-sum/submissions/1782541659/
- **Date:** 2025-09-25

## Solution

```cpp
#include <vector>
using namespace std;
 
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        int n = nums.size();
        for (int i = 0; i < n; ++i) {
            for (int j = i + 1; j < n; ++j) {
                if (nums[i] + nums[j] == target) {
                    return {i, j};
                }
            }
        }
        return {}; // If no solution found
    }
};
```

---
*Generated automatically by LeetFeedback Extension*
