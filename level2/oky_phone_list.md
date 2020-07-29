# 전화 번호부

- phone_book을 정렬하면 인접한 값만 비교 가능

```
import java.util.Arrays;
class Solution {
    public boolean solution(String[] phone_book) {
        boolean answer = true;
        Arrays.sort(phone_book); // 정렬을 한다.
        for(var i=0; i<phone_book.length-1; i++){
            // 정렬을 했기 때문에 인접한 것만 비교 앞 원소가 뒤 원소의 접두사인지 
            if(phone_book[i+1].indexOf(phone_book[i]) == 0){ 
                return false; // 반복문 마치고 값반환
            }
        }
        return answer;
    }
}
```
