---
sidebar_position: 6
---

# SRP(Single Responsibility Principle): 단일 책임 원칙

모든 클래스는 각각 하나의 기능만 가진다는 의미, 클래스가 제공하는 모든 서비스는
단 하나에 책임을 수행하는데 집중되어야 한다.

#### Person 클래스

  ```
class Person {
	void cook(); // 요리하기 - 요리사
	void plate(); // 플레이팅 - 요리사
	void order(); // 주문하기 - 손님
	void pickup(); // 픽업하기 - 손님
	void eat(); // 먹기 - 손님
}
  ```

Person 클래스는 요리사의 역할과 손님의 역할을 모두 가진 클래스로,
하나의 책임만을 가지고 있지 않다.
따라서 Person 클래스는 요리사의 역할과 관련된 기능이 추가될 때 마다
코드의 변경이 불가피하다.

#### Cook 클래스

  ```
class Cook {
	void cook();
	void plate();
}

  ```

#### Customer 클래스

  ```
class Customer {
	void order();
	void pickup();
	void eat();
}

  ```

Person 클래스를 단 하나의 책임만 갖도록 Cook 클래스와 Customer 클래스로 구분하였다.

이렇게 단일 책임 원칙에 맞게 클래스를 수정한다면, 요리사의 역할과 관련한 기능이 추가 될 때
Customer 클래스가 변경되지 않아도 된다.

즉, 클래스 변경으로 인한 다른 클래스에게 주는 영향을 줄일 수 있기 때문에
응집도가 높아지고 결합도가 낮아지는 장점이 있다.

<br/>


