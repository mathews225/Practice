# 14. Longest Common Prefix

## Easy

Write a function to find the longest common prefix string amongst an array of strings.

If there is no common prefix, return an empty string `""`.
 

### Example 1:

**Input** `strs = ["flower","flow","flight"]`

**Output:** `"fl"`

### Example 2:

**Input:** `strs = ["dog","racecar","car"]`

**Output:** `""`

**Explanation:** `There is no common prefix among the input strings.`

### Constraints:

- `1 <= strs.length <= 200`
- `0 <= strs[i].length <= 200`
- `strs[i]` consists of only lower-case English letters.



``` c#
public class Solution {
    public string LongestCommonPrefix(string[] strs) {
        var prefix = "";
        var len = 0;
        var idx = 0;
        for (len=0; len<strs[0].Length; len++){
            var pass = true;
            var search = strs[0].Substring(0,len+1);
            for (idx=1; idx<strs.Length; idx++){
                if (strs[idx].StartsWith(search) && pass == true) {
                    pass = true;
                } else {
                    pass = false;
                }   
            }
            prefix = (pass)?search:prefix;
            
        }
        return prefix;
    }
}
```