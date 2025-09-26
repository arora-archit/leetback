# Indexes of Subarray Sum

## Problem Information
- **Platform:** Geeksforgeeks
- **Difficulty:** Medium
- **URL:** https://www.geeksforgeeks.org/problems/subarray-with-given-sum-1587115621/1
- **Date:** 2025-09-26

## Solution

```java
import java.util.ArrayList;
class Solution {
    static ArrayList<Integer> subarraySum(int[] arr, int target) {
        ArrayList<Integer> result = new ArrayList<Integer>();
        for (int i = 0; i < arr.length; i++) {
            int sum = 0;
            for (int j = i; j < arr.length; j++) {
                sum += arr[j];
                if (sum == target) {
                    result.add(i + 1); 
                    result.add(j + 1); 
                    return result;
                } else if (sum > target) {
                    break;
                }
            }
        }
        result.add(-1);
        return result;
    }
}
```

---
*Generated automatically by LeetFeedback Extension*
