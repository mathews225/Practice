# 12. Integer to Roman

## Medium

Roman numerals are represented by seven different symbols: I, V, X, L, C, D and M.
```
Symbol       Value
I             1
V             5
X             10
L             50
C             100
D             500
M             1000
```
For example, 2 is written as II in Roman numeral, just two one's added together. 12 is written as XII, which is simply X + II. The number 27 is written as XXVII, which is XX + V + II.

Roman numerals are usually written largest to smallest from left to right. However, the numeral for four is not IIII. Instead, the number four is written as IV. Because the one is before the five we subtract it making four. The same principle applies to the number nine, which is written as IX. There are six instances where subtraction is used:

- I can be placed before V (5) and X (10) to make 4 and 9. 
- X can be placed before L (50) and C (100) to make 40 and 90. 
- C can be placed before D (500) and M (1000) to make 400 and 900.
Given an integer, convert it to a roman numeral.
 

### Example 1:

**Input** `num = 3`

**Output:** `"III"`

### Example 2:

**Input:** `num = 4`

**Output:** `"IV"`

### Example 3:

**Input:** `num = 9`

**Output:** `"IX"`

### Example 4:

**Input:** `num = 58`

**Output:** `"LVIII"`

**Explanation:** `L = 50, V = 5, III = 3.`

### Example 5:

**Input:** `num = 1994`

**Output:** `"MCMXCIV"`

**Explanation:** `M = 1000, CM = 900, XC = 90 and IV = 4.`

### Constraints:

- `1 <= num <= 3999`



``` c#
public class Solution {
    public string IntToRoman(int num) {
        var sum = 0;
        
        var res = "";
        while (sum+1000 <= num) {
            sum+=1000;
            res = res+"M";
        }
        while (sum+500 <= num) {
            sum+=500;
            res = res+"D";
        }
        while (sum+100 <= num) {
            sum+=100;
            res = res+"C";
        }
        while (sum+50 <= num) {
            sum+=50;
            res = res+"L";
        }
        while (sum+10 <= num) {
            sum+=10;
            res = res+"X";
        }
        while (sum+5 <= num) {
            sum+=5;
            res = res+"V";
        }
        while (sum+1 <= num) {
            sum+=1;
            res = res+"I";
        }
        res = res.Replace("DCCCC","CM").Replace("CCCC","CD").Replace("LXXXX","XC").Replace("XXXX","XL").Replace("VIIII","IX").Replace("IIII","IV");
    
        return res;
        
        
    }
}
```