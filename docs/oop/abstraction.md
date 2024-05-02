---
sidebar_position: 2
---

# 추상화

객체의 공통적인 속성과 기능을 추출하여 정의하는 것

<br/>

#### Vehicle 인터페이스

자동차와 오토바이의 공통 기능을 추출하여 Vehicle 인터페이스에 정의

```
  
public interface Vehicle {
	public abstract void start()
	void moveForward(); // public abstract 키워드 생략 가능
	void moveBackward();
}

  ```

자동차와 오토바이는 모두 이동 수단이며, 전진과 후진을 할 수 있다는
공통점을 가지고 있다.

인터페이스에는 추상 메서드나 상수를 통해 어떤 객체가 수행해야 하는 핵심적인 역할만을 규정,
실제 구현은 해당 인터페이스를 구현하는 객체들에서 하도록 프로그램을 설계하는 것

#### Car 클래스

```
  
public class Car implements Vehicle {
	
@Override
public void moveForward() {
	System.out.println(“자동차가 앞으로 전진합니다”);
}

@Override
public void moveBackward() {
	System.out.println(“자동차가 뒤로 후진합니다”);
}
}
```

#### MotorBike 클래스


```
public class MotorBike implements Vehicle {
	
@Override
public void moveForward() {
	System.out.println(“오토바이가 앞으로 전진합니다”);
}

@Override
public void moveBackward() {
	System.out.println(“오토바이가 뒤로 후진합니다”);
}
}

  ```

Car와 MotorBike 클래스에서 인터페이스에서 정의한 역할을 맥락에 맞게 구현한다.
각 클래스 모두 전진, 후진의 공통된 기능을 가지지만 차는 차의 시동을 걸어야 하고, 오토바이는 오토바이의
시동을 걸어야 하기 때문에 그 구현은 각 클래스에 따라 달라야 한다.

이것을 객체 지향 프로그래밍에서 역할과 구현의 분리라고 하며, 이 부분이 다형성과 함께
유연하고 변경이 용이한 프로그램을 설계하는 데 가장 핵심적인 부분이다.

즉, 객체 지향 프로그래밍에서는 보다 유연하고 변경에 열려있는 프로그램을 설계하기 위해 역할과 구현을
분리 하는데, 여기서 역할에 해당하는 부분이 인터페이스를 통해 추상화 될 수 있다.

<br/>