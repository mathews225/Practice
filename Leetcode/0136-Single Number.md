# 136. Single Number

## Easy

Given a **non-empty** array of integers `nums`, every element appears twice except for one. Find that single one.

You must implement a solution with a linear runtime complexity and use only constant extra space.


## Example 1:

**`Input:`** `nums = [2,2,1]`

**`Output:`** `1`


## Example 2:

**`Input:`** `nums = [4,1,2,1,2]`

**`Output:`** `4`


## Example 3:

**`Input:`** `nums = [1]`

**`Output:`** `1`


 

## Constraints:

- `1 <= nums.length <= 3 * 10`<sup>`4`</sup>
- `-3 * 10`<sup>`4`</sup>` <= nums[i] <= 3 * 10`<sup>`4`</sup>
- Each element in the array appears twice except for one element which appears only once.


``` c#
public class Solution {
    public int SingleNumber(int[] nums) {
        var res = 0;
        for (var idx = 0; idx<nums.Length; idx++) {
            var first = Array.IndexOf(nums, nums[idx]);
            var second = Array.IndexOf(nums, nums[idx], first+1);
            if (second == -1) {
                res = nums[idx];
            }
        }
        return res;
    }
}
```