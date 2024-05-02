---
sidebar_position: 8
---

# ISP(Interface Segregation Principle): 인터페이스 분리 원칙

하나의 큰 인터페이스를 상속 받기 보다는 인터페이스를 구체적이고 작은 단위들로 분리시켜
꼭 필요한 인터페이스만 상속하자는 의미

  ```
interface Person {
	void cook(); 
	void plate(); 
	void order(); 
	void pickup(); 
	void eat(); 
}

  ```

Person 인터페이스를 요리사 인터페이스의 기능과, 손님 인터페이스로 구현할 수 있다.

  ```
interface Cook {
	void cook();
	void plate();
}

  ```
  ```
interface Customer {
	void order();
	void pickup();
	void eat();
}
  ```

Cook 인터페이스와 Customer 인터페이스로 구분해 만들어 준다면
Cook 인터페이스에서는 Customer 인터페이스의 기능을, 
Customer 인터페이스에서는 Cook 인터페이스의 기능을 구현하지 않아도 된다.

