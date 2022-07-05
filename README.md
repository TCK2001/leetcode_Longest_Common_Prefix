# leetcode_Longest_Common_Prefix
+ 또 잴 긴 길이 구하는 문제
+ 又是求最長長度的string 並return

-----
+ Example1
```
Input: strs = ["flower","flow","flight"]
Output: "fl"
```
----
+ Example2
```
Input: strs = ["dog","racecar","car"]
Output: ""
Explanation: There is no common prefix among the input strings.
```
----
```python
class Solution:
    def longestCommonPrefix(self, strs: List[str]) -> str:
        prefix = strs[0] # 첫번째 값 저장하기
        strs.remove(prefix) # 그리고 list에서 그 첫번째 값을 지우고 밑에 판단식에 들어가기
        for words in strs: # 고로 두번째 것부터 판단
            res = ''
            for i in range(len(words)):
                if i >= len(prefix) or prefix[i] != words[i]: # 만약 i가 결과값인 prefix보다 클 경우 혹은 값이 다를경우
                    break # 종료 회문
                else:
                    res += words[i] # 같으면 더하기
            prefix = res # 결과값을 위해서 판단해서 나온 값으로 바꿈
# 모든 word를 대조해고 마지막 결과값 출력
        return(prefix)
```
---
```
결론 : 
for문이 두개라 매우 느림.....
```
---
```
結論:
非常慢......XD
```
---
### Result
Runtime: 51 ms, faster than 55.38% of Python3 online submissions for Longest Common Prefix.\
Memory Usage: 13.9 MB, less than 87.97% of Python3 online submissions for Longest Common Prefix.
