# 35. Search Insert Position

## Hard

Given n non-negative integers representing an elevation map where the width of each bar is 1, compute how much water it can trap after raining.



 

### Example 1:
![alt text](https://assets.leetcode.com/uploads/2018/10/22/rainwatertrap.png "elevation map")

**Input** 
`height = [0,1,0,2,1,0,1,3,2,1,2,1]`

**Output:** `6`

**Explanation:**
`The above elevation map (black section) is represented by array [0,1,0,2,1,0,1,3,2,1,2,1]. In this case, 6 units of rain water (blue section) are being trapped.`

### Example 2:


**Input:** `height = [4,2,0,3,2,5]`

**Output:** `9`

### Constraints:

- n == height.length
- 0 <= n <= 3 * 10<sup>4</sup>
- 0 <= height[i] <= 10<sup>5</sup>


``` c#
public class Solution {
    public int Trap(int[] height) {
        if (height.Length!=0) {
            var m = height.Max();
            var l = Array.LastIndexOf(height,m);
            var ra=0; // total rain left of max
            var rb=0; // total rain right of max
            var x=0; // current max
            var v=0; // current volume
            for (var i = 0; i < Array.LastIndexOf(height,m); i++) {
                var n=height[i];
                if (n<x) {
                    v = x-n;
                    ra +=v;
                }
                else {
                    x=n;
                }
            }
            x = 0; // reset max;
            for (var i = 1; i < height.Length-l; i++) {
                var q=height.Length-i;
                var n=height[q];
                if (n<x) {
                    v = x-n;
                    rb +=v;
                }
                else {
                    x=n;
                }
            }
            return ra+rb;
        }
        else {
            return 0;
        }
    }
}
```