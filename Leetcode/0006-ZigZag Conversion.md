# 6. ZigZag Conversion

## Medium

The string `"PAYPALISHIRING"` is written in a zigzag pattern on a given number of rows like this: (you may want to display this pattern in a fixed font for better legibility)
```
P   A   H   N
A P L S I I G
Y   I   R
```
And then read line by line: `"PAHNAPLSIIGYIR"`

Write the code that will take a string and make this conversion given a number of rows:
```
string convert(string s, int numRows);
```

### Example 1:

**Input** 
`s = "PAYPALISHIRING", numRows = 3`

**Output:** `PAHNAPLSIIGYIR`


### Example 2:

**Input:** `s = "PAYPALISHIRING", numRows = 4`

**Output:** `PINALSIGYAHRPI`

**Explanation:**
```
P     I    N
A   L S  I G
Y A   H R
P     I
```

### Example 3:

**Input:** `s = "A", numRows = 1`

**Output:** `A`

### Constraints:

- 1 <= s.length <= 1000
- `s` consists of only English letters (lower-case and upper-case), `','` and `'.'`.
- 1 <= numRows <= 1000

``` c#
public class Solution {
    public string Convert(string s, int numRows) {
        var res = "";
        if (numRows == 1 || numRows >= s.Length) {
            res = s;
        } else {
            var rep = (numRows-1)*2;
            for (var row = 0; row<numRows; row++) {
                var idx = 0;
                if (row == 0 || row == numRows-1) {
                    idx = row;
                    while (idx < s.Length) {
                        res += s[idx];
                        idx += rep;
                    }
                } else {
                    res += s[idx+row];
                    idx += rep;
                    while (idx-row < s.Length) {
                        res += s[idx-row];
                        if (idx+row < s.Length) {
                            res += s[idx+row];
                        }
                        idx += rep;
                    }
                }
            }
        }
        return res;
    }
}
```