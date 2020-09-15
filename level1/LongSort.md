https://programmers.co.kr/learn/courses/30/lessons/12933

<h1>문제 설명</h1>
함수 solution은 정수 n을 매개변수로 입력받습니다. n의 각 자릿수를 큰것부터 작은 순으로 정렬한 새로운 정수를 리턴해주세요. 예를들어 n이 118372면 873211을 리턴하면 됩니다.

<h1>제한 조건</h1>
n은 1이상 8000000000 이하인 자연수입니다.
입출력 예
n	return
118372



```
class Solution {
    fun solution(n: Long): Long {
       var resultArr = n.toString().toCharArray().apply {
            sortDescending()
        }.joinToString("")

         return resultArr.toLong()
    }
}
```
