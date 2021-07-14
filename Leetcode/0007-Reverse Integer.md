# 7. Reverse Integer

## Easy

Given a signed 32-bit integer `x`, return `x` with its digits reversed. If reversing `x` causes the value to go outside the signed 32-bit integer range `[-231, 231 - 1]`, then return `0`.

**Assume the environment does not allow you to store 64-bit integers (signed or unsigned).**

 



## Example 1:

**Input:** `x = 123`

**Output:** `321`


## Example 2:

**Input:** `x = -123`

**Output:** `-321`


## Example 3:

**Input:** `x = 120`

**Output:** `21`


## Example 4:

**Input:** `x = 0`

**Output:** `0`
 

## Constraints:

- -2<sup>31</sup> <= x <= 2<sup>31</sup> - 1

``` c#
public class Solution {
    public int Reverse(int x) {
        var stop = (x < 0)?1:0;
        var arr = x.ToString().ToCharArray();
        Array.Reverse(arr);
        var str = "";
        for (var idx = 0; idx < arr.Length-stop; idx++){
            str += arr[idx].ToString();
        }
        str = (stop == 1)?("-"+str):str;
        try {
            return Int32.Parse(str);
        } catch (OverflowException) {
            return 0;
        }
    }
}
```