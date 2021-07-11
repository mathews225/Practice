# 20. Valid Parentheses

## Easy

Given a string s containing just the characters `'('`, `')'`, `'{'`, '`}'`, `'['` and `']'`, determine if the input string is valid.

An input string is valid if:

1. Open brackets must be closed by the same type of brackets.
2. Open brackets must be closed in the correct order.

### Example 1:

**Input** 
`s = "()"`

**Output:** `true`


### Example 2:

**Input** 
`s = "()[]{}"`

**Output:** `true`


### Example 3:

**Input** 
`s = "(]"`

**Output:** `flase`


### Example 4:

**Input** 
`s = "([)]"`

**Output:** `flase`


### Example 5:

**Input** 
`s = "{[]}"`

**Output:** `true`


### Constraints:

- 1 <= s.length <= 10<sup>4</sup>
- `s` consists of parentheses only `'()[]{}'`.

``` c#
public class Solution {
    public bool IsValid(string s) {
        List<string> openers = new List<string>();
        string[] opens = new string[3] { "{", "(", "[" };
        string[] closes = new string[3] { "}", ")", "]" };
        var valid = true;
        
        for (int idx = 0; idx < s.Length; idx++) {
            var item = s[idx].ToString();
            if ( Array.Exists(opens, element => element == item) ) {
                openers.Add(item);
            } else {
                if (openers.Count == 0) {
                    valid = false;
                    break;
                }
                var ct = openers.Count - 1;
                var cpsIdxC = Array.IndexOf(closes, item);
                var cpsIdxO = Array.IndexOf(opens, openers[ct]);
                if (cpsIdxC != cpsIdxO) {
                    valid = false;
                    break;
                } else {
                    openers.RemoveAt(ct);
                }
            }
        }
        valid = (openers.Count == 0)?valid:false;
        return valid;   
    }
}
```