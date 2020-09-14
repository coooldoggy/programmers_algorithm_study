https://programmers.co.kr/learn/courses/30/lessons/12903


```
class Solution {
    fun solution(s: String): String {
         var size = s.length
        return if (size %2 != 0){
            s.substring(size/2, (size/2)+1)
        }else{
            s.substring(size/2 - 1, (size/2)+1)
        }
    }
}
```
