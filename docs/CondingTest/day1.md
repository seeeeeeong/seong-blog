---
sidebar_position: 1
---

# 폰켓몬

#### 링크

https://school.programmers.co.kr/learn/courses/30/lessons/1845

#### 문제

N마리 폰켄몬의 종류가 담긴 배열 nums가 있고,
가져갈 수 있는 폰켄몬의 최대값은 N/2이다.
가져갈 수 있는 최대 폰켄몬 종류의 개수를 구해야한다. (중복일 경우 해당 폰켄몬의 개수는 1)


#### 예제

|     nums      | result |    
|:-------------:|:------:|
|   [3,1,2,3]   |   2    |   
| [3,3,3,2,2,4] |   3    |     
| [3,3,3,2,2,2] |   2    |    



#### 풀이 순서

1. 최대값을 구하기 위해 nums.length / 2 값을 max에 대입한다.
2. 중복을 제거한 값을 구하기 위해 Set을 이용한다.
3. 중복을 제거한 Set의 크기가 max보다 크면 max를, 작으면 Set을 리턴한다.


#### 코드

```
import java.util.*;

class Solution {
    public int solution(int[] nums) {
        int answer = 0;
        int max = nums.length / 2;
        
        HashSet<Integer> hashSet = new HashSet<>();
        
        for(int n : nums) {
            hashSet.add(n);
        }
        
        if(max >= hashSet.size()) {
            answer = hashSet.size();
        }
        else {
            answer = max;
        }
        return answer;
    }
}
```


