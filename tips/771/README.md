## Description

You're given strings `J` representing the types of stones that are jewels, and `S` representing the stones you have.  Each character in `S` is a type of stone you have.  You want to know how many of the stones you have are also jewels.

The letters in `J` are guaranteed distinct, and all characters in `J` and `S` are letters. Letters are case sensitive, so `"a"` is considered a different type of stone from `"A"`.

**Example 1**

```
Input: J = "aA", S = "aAAbbbb"
Output: 3
```

**Example 2**

```
Input: J = "z", S = "ZZ"
Output: 0
```

**Note**

`S` and `J` will consist of letters and have length at most 50.
The characters in `J` are distinct.

## 思路

从S字符串中寻找存在于J字符串中的字符，需要得出符合条件的字符的数量。二次循环即可。

###  Java

```java
public class Solution {
    public int numJewelsInStones(String J, String S) {
        int sum = 0;
        for (char c : S.toCharArray()) {
            if (J.indexOf(c) != -1) {
                sum++;
            }
        }
        return sum;
    }
}
```
