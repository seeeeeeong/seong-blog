---
sidebar_position: 1
---

# 중앙값 구하기

#### 세 값의 대소 관계 13종류의 모든 조합에 대해 중앙값을 구하여 출력하는 프로그램을 작성하세요.

  ```
public class Med3 {

    static int med3(int a, int b, int c) {
        if(a >= b) {
            if(b >= c)
                return b;
            else if (a <= c) {
                return a;
            }
            else
                return c;
        }
        else if(a > c)
            return a;
        else if (b > c)
            return c;
        else
            return b;
    }

    public static void main(String[] args) {
        System.out.println("med3(3,2,1) = " + med3(3, 2, 1)); // a＞b＞c
        System.out.println("med3(3,2,2) = " + med3(3, 2, 2)); // a＞b＝c
        System.out.println("med3(3,1,2) = " + med3(3, 1, 2)); // a＞c＞b
        System.out.println("med3(3,2,3) = " + med3(3, 2, 3)); // a＝c＞b
        System.out.println("med3(2,1,3) = " + med3(2, 1, 3)); // c＞a＞b
        System.out.println("med3(3,3,2) = " + med3(3, 3, 2)); // a＝b＞c
        System.out.println("med3(3,3,3) = " + med3(3, 3, 3)); // a＝b＝c
        System.out.println("med3(2,2,3) = " + med3(2, 2, 3)); // c＞a＝b
        System.out.println("med3(2,3,1) = " + med3(2, 3, 1)); // b＞a＞c
        System.out.println("med3(2,3,2) = " + med3(2, 3, 2)); // b＞a＝c
        System.out.println("med3(1,3,2) = " + med3(1, 3, 2)); // b＞c＞a
        System.out.println("med3(2,3,3) = " + med3(2, 3, 3)); // b＝c＞a
        System.out.println("med3(1,2,3) = " + med3(1, 2, 3)); // c＞b＞a
    }
}
  ```

#### 중앙값을 구하는 메서드는 다음과 같이 작성할 수도 있습니다. 그러나 실습 1C-1의 med3 메서드에 비해 효율이 떨어지는데, 그 이유를 설명하세요.

  ```
static int med3(int a, int b, int c){
    if((b >= a && c <= a) || (b <= a && c >= a))
        return a;
    else if((a > b && c < b) || (a < b && c > b))
        return b;
    return c;
}
  ```

(b >= a && c <= a)가 true일 경우 (or) 이기 때문에 바로 return으로 넘어가 괜찮지만
false의 경우에 뒤에 나오는 조건도 확인해야 해서 가장 적은 경우의 수가 두 번, 
그렇지 않으면 네 번으로 두 번 또는 네 번을 검사한다.

하지만 1C-1의 med3의 경우 최소 두 번에서 최대 네 번까지로 이 메서드에서 세 번 검사하는 경우는
예시에서 제시하는 메서드는 네 번 검사해야 하기 때문에 효율성이 떨어진다.

