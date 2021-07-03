# 58. Length of Last Word

## Easy

Given a string `s` consists of some words separated by spaces, return the length of the last word in the string. *If the last word does not exist, return* `0`.

A **word** is a maximal substring consisting of non-space characters only.



 

### Example 1:

**Input** 
`s = "Hello World"`

**Output:** `5`

### Example 2:


**Input:** `s = ' '`

**Output:** `0`

### Constraints:

- 1 <= s <= 3 * 10<sup>4</sup>
- `s` consists of only English letters and spaces `' '`.


``` c#
public class Solution {
    public int LengthOfLastWord(string s) {
        //var empty = (s.IsNullOrWhiteSpace)?0:
        var trimmed = s.TrimEnd();
        // Location of the space.
        int charPos = trimmed.LastIndexOf(" ");
        if (charPos == -1) {
            return trimmed.Length;
        } else {
            var x = trimmed.LastIndexOf(" ");
            // Get substring
            string sub = trimmed.Substring(x);
            return sub.Length-1;
        }
    }
}
```