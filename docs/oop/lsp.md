---
sidebar_position: 8
---

# LSP(Listov Substitution Principle): 리스코프 치환 원칙

하위 타입이 상위 타입이 지정한 제약 조건들을 지키고,
상위 타입에서 하위 타입으로의 변동이 일어나도 상위타입의 역할을 문제없이 제공하는 것

  ```
class Car {
	int speed;
	void drive() {
		this.speed += 10;
	}
}

class Bus extends Car {
	int speed;
	int km;

	@Override
	void drive() {
		// 부모 기능 그대로 수행
		this.speed += 10;
		this.km += 1;
	}
}
  ```

위와 같이 Bus 클래스는 Car 클래스가 제공하는 drive 메소드의 speed += 10 기능을
그대로 수행하고, 하위 타입에서 추가적으로 구현한 km += 1을 수행한다.

이는 상위 타입인 Car 클래스가 제공하던 speed += 10 기능을 하위타입에서
제대로 수행할 수 있기 때문에 해당 원칙을 잘 지킨 것이다.

리스코프 치환 원칙을 지키기는 것은 무분별한 메서드 오버라이딩을 줄이는 것이다.
메서드 오버라이딩을 하더라도 상위 타입이 구현한 기능을 변경 없이 구현 후 
추가적인 기능을 구현하는 것이 바람직하다.