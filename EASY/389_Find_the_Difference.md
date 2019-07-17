# :books: [Find the Difference](https://leetcode.com/problems/find-the-difference/)

### :star: Question

- Given two strings s and t which consist of only lowercase letters.
- String t is generated by random shuffling string s and then add one more letter at a random position.
- Find the letter that was added in t.

--- 

### :car: Example

Input:
s = "abcd"
t = "abcde"
Output: e

---

### :hammer: Code

#### :coffee: Java Version - 1

```java
class Solution {
    public char findTheDifference(String s, String t) {
        int[] it = new int[26];
        
        for(char cs : s.toCharArray()) {
            it[cs - 'a']++;
        }
        
        for(char ct : t.toCharArray()) {
            it[ct - 'a']--;
            if(it[ct - 'a'] < 0) {
                return ct;
            }
        }
        
        return '0';
    }
}
```

- Runtime: 1 ms, faster than 99.08% of Java online submissions for Find the Difference.
- Memory Usage: 37.8 MB, less than 7.01% of Java online submissions for Find the Difference.

---

### :pencil: Explanation



---

### :computer: Complexity Analysis:

- Time complexity: 
- Space complexity: 

---

### :pen: Author

YIMING DAI - 2019.07.15