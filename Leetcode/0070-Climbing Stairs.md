# 283. Move Zeroes

## Easy

You are climbing a staircase. It takes `n` steps to reach the top.

Each time you can either climb `1` or `2` steps. In how many distinct ways can you climb to the top?


## Example 1:

**Input:** `n = 2`

**Output:** `2`

**Explanation:** `There are two ways to climb to the top.`

`1. 1 step + 1 step`

`2. 2 steps`


## Example 2:

**Input:** `n = 3`

**Output:** `3`

**Explanation:** `There are three ways to climb to the top.`

`1. 1 step + 1 step + 1 step`

`2. 1 step + 2 steps`

`3. 2 steps + 1 step`


## Constraints:

- `1 <= n <= 45`

``` c#
public class Solution {
    public int ClimbStairs(int n) {
        if (n==0 || n==1) {
            return n;
        } 
        var a = 1;
        var b = 1;
        var steps = 0;
        var idx = 1;
        while (idx < n) {
            steps = (a+b);
            a = b;
            b = steps;
            idx ++;
        }
        return steps;
    }
}
```