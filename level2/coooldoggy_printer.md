https://programmers.co.kr/learn/courses/30/lessons/42587

```
import java.util.Collections;
import java.util.PriorityQueue;

class Solution {
    public int solution(int[] priorities, int location) {
        int answer = 0;

        PriorityQueue<Integer> priortyQ = new PriorityQueue<>(Collections.reverseOrder());

        for(int prority : priorities){
            priortyQ.offer(prority);
        }

        while(!priortyQ.isEmpty()){
            for(int i = 0; i < priorities.length; i ++){
                if(priortyQ.peek() == priorities[i]){
                    priortyQ.poll();
                    answer++;
                    if(location == i){
                        priortyQ.clear();
                        break;
                    }
                }
            }
        }

        return answer;
    }
}
```
