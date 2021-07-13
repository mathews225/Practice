# 1402. Reducing Dishes

## Hard

A chef has collected data on the `satisfaction` level of his `n` dishes. Chef can cook any dish in 1 unit of time.

Like-time coefficient of a dish is defined as the time taken to cook that dish including previous dishes multiplied by its satisfaction level  i.e.  `time[i] * satisfaction[i]`

Return the maximum sum of _Like-time coefficient_ that the chef can obtain after dishes preparation.

Dishes can be prepared in **any** order and the chef can discard some dishes to get this maximum value.

 

### Example 1:

**Input:** 
`satisfaction = [-1,-8,0,5,-9]`

**Output:** 
`14`

**Explanation:**
 After Removing the second and last dish, the maximum total Like-time coefficient will be equal to (-1 * 1 + 0 * 2 + 5 * 3 = 14). Each dish is prepared in one unit of time.


### Example 2:


**Input:** 
`satisfaction = [4,3,2]`

**Output:** 
`20`

**Explanation:** 
Dishes can be prepared in any order, (2 * 1 + 3 * 2 + 4 * 3 = 20)


### Example 3:


**Input:** 
`satisfaction = [-1,-4,-5]`

**Output:** 
`0`

**Explanation:** 
People don't like the dishes. No dish is prepared.


### Example 4:


**Input:** 
`satisfaction = [-2,5,-1,0,3,-3]`

**Output:** 
`35`
 

**Constraints:**

- n == satisfaction.length
- 1 <= n <= 500
- -10<sup>3</sup> <= satisfaction[i] <= 10<sup>3</sup>

``` c#
public class Solution {
    public int MaxSatisfaction(int[] satisfaction) {
        Array.Sort(satisfaction);
        int[] underZero = Array.FindAll(satisfaction, x => x < 0);
        int[] overZero = Array.FindAll(satisfaction, x => x >= 0);
        var posTot = overZero.Sum();
        var negsTot = 0;
        List<int> negsList = new List<int>();
        for (var idx = 1; idx<underZero.Length+1; idx++){
            var absNeg = Math.Abs(underZero[underZero.Length-idx]);
            if ( negsTot+absNeg < posTot){
                negsTot += absNeg;
                negsList.Add(underZero[underZero.Length-idx]);
            } else {
                break;
            }
        }
        var start = overZero.Length;
        Array.Resize(ref overZero, overZero.Length + negsList.Count);
        negsList.CopyTo(overZero, start);
        Array.Sort(overZero);
        return CalcTot(overZero);
    }

    private static int CalcTot(int[] nums) {
        var res = 0;
        for (var idx = 0; idx < nums.Length; idx++) {
            res += (nums[idx] * (idx+1));
        }
        return res;
    }
}
```