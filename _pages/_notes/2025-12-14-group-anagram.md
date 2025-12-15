---
title: "Group Anagram"
date: 2025-12-14
collection: notes
---
```python
class Solution:
    def groupAnagrams(self, strs: List[str]) -> List[List[str]]:
        #Find anagrams
        #each list has anagrams
        dic = {}
        s = []
        ans = []
        for i in range(len(strs)):
            si = ''.join(sorted(strs[i]))
            s.append(si)

        for i in range(len(s)):
            dic.setdefault(s[i], []).append(i)

        for val in dic.values():
            anas = []

            for i in range(len(val)):
                anas.append(strs[val[i]])

            ans.append(anas)
        return ans

```
First Idea: 1. Sort each word 2. Find anagrams and put index of anagram in dictionary. 3. Make list with anagrams. 
