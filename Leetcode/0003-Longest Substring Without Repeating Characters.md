# 3\. Longest Substring Without Repeating Characters

## Medium

https://leetcode.com/problems/longest-substring-without-repeating-characters/

Given a string s, find the length of the **longest substring** without repeating characters.

**Example 1:**

**Input:** s = "abcabcbb"

**Output:** 3

**Explanation:** The answer is "abc", with the length of 3.

**Example 2:**

**Input:** s = "bbbbb"

**Output:** 1

**Explanation:** The answer is "b", with the length of 1.

**Example 3:**

**Input:** s = "pwwkew"

**Output:** 3

**Explanation:** The answer is "wke", with the length of 3.

Notice that the answer must be a substring, "pwke" is a subsequence and not a substring.

**Example 4:**

**Input:** s = ""

**Output:** 0

**Constraints:**

-   0 <= s.length <= 5 * 10<sup>4</sup>
-   s consists of English letters, digits, symbols and spaces.

``` c#
public class Solution {
    public int LengthOfLongestSubstring(string s) {
        var longest = 0;
        var idx = 0;
        

        if (s.Length != 0) {
            for (idx = 0; idx+longest<s.Length; idx++) {
                var end = idx+1;
                var maxOfIdx = 1;
                List<int> sList = new List<int>();
                sList.Add(s[idx]);
                for (end = idx+1; end<s.Length; end++) {
                    if (sList.IndexOf(s[end])<0) {
                        sList.Add(s[end]);
                        maxOfIdx++;
                    } else {
                        break;
                    }
                                }
                if (maxOfIdx>longest) {
                    longest = maxOfIdx;
                }
            }
            return longest;
        } else {
            return 0;
        }
        
    }
}
```