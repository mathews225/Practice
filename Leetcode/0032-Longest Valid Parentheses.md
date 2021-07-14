# 32. Longest Valid Parentheses

## Hard

Given a string containing just the characters `'('` and `')'`, find the length of the longest valid (well-formed) parentheses substring.

**Assume the environment does not allow you to store 64-bit integers (signed or unsigned).**


## Example 1:

**Input:** `s = "(()"`

**Output:** `2`

**Explanation:** The longest valid parentheses substring is `"()"`.


## Example 2:

**Input:** `s = ")()())"`

**Output:** `4`

**Explanation:** The longest valid parentheses substring is `"()()"`.


## Example 3:

**Input:** `s = ""`

**Output:** `0`


## Constraints:

- 0 <= s.length <= 3 * 10<sup>4</sup>
- s`[i]` is `'('`, or `')'`.

``` c#
public class Solution {
    public int LongestValidParentheses(string s) {
        Stack<int> stack = new Stack<int>();
        stack.Push(-1);
        int max = 0;
        for (int idx = 0; idx < s.Length; idx++) {
            if (s[idx] == '(') {
                stack.Push(idx);
            }
            else {
                stack.Pop();
                if (stack.Count == 0) {
                    stack.Push(idx);
                }
                max = ( max< idx-stack.Peek() )?( idx-stack.Peek() ):max;
            }
        }
        return max;
    }
}
```