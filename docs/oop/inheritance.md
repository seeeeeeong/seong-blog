---
sidebar_position: 3
---

# 상속

기존의 클래스를 재활용 하여 새로운 클래스를 작성하는 자바의 문법 요소
추상화의 연장선에서, 상속은 클래스 간 공유될 수 있는 속성과 기능들을
상위 클래스로 추상화 시켜 해당 상위 클래스로부터 확장된 여러 개의 하위 클래스들이
모두 상위 클래스의 속성과 기능들을 간편하게 사용할 수 있도록 한다.

즉, 클래스들 간 공유하는 속성과 기능들을 반복적으로 정의할 필요 없이
딱 한 번만 정의 해두고 간편하게 재사용 할 수 있어 반복적인 코드를 최소화 하고
공유하는 속성과 기능에 간편하게 접근하여 사용할 수 있도록 한다.



#### Car 클래스

  ```
  public class Car {

	String model;
	String color;
	int wheels;

	// Car 클래스 고유의 속성
	boolean isConvertible;

	void moveForward() {
		System.out.println(“앞으로 전진합니다”);
	}

	void moveBackward() {
		System.out.println(“뒤로 후진합니다”);
	}

	// Car 클래스 고유의 기능
	void openWindow() {
		System.out.println(“모든 창문을 엽니다”);
	}
}
  ```

#### MotorBike 클래스

  ```
  public class MotorBike {

	String model;
	String color;
	int wheels;

	// MotorBike 클래스 고유의 속성
	boolean isRaceable;

	void moveForward() {
		System.out.println(“앞으로 전진합니다”);
	}

	void moveBackward() {
		System.out.println(“뒤로 후진합니다”);
	}

	// MotorBike 클래스 고유의 기능
	public void stunt() {
		System.out.println(“오토바이로 묘기를 부립니다”);
	}
}
  ```

각각의 클래스마다 속성으로 model, color, wheel
기능으로 moveForward(), moveBackward()가 반복된다.
하나의 코드에서 변경 사항이 일어나면, 해당 코드의 변경 사항을 다른 클래스에서도 일일이 
수정해주어야 하는 어려움이 있다.

<br/>

### 추상화와 상속을 활용하여 재정의

#### Vehicle 클래스

  ```
public class Vehicle {

	String model;
	String color;
	int wheels;


	void moveForward() {
		System.out.println(“앞으로 전진합니다”);
	}

	void moveBackward() {
		System.out.println(“뒤로 후진합니다”);
	}

}
  ```

#### Car 클래스

  ```
public class Car extends Vehicle {

	boolean isConvertible;

	void openWindow() {
		System.out.println(“모든 창문을 엽니다”);
	}
}
  ```

#### MotorBike 클래스

  ```
public class MotorBike extends Vehicle {

	boolean isRaceble;

	// 메서드 오버라이딩 -> 기능 재정의
	@Override
	void moveForward() {
		System.out.println(“오토바이가 앞으로 전진합니다”);
	}


	public void stunt() {
		System.out.println(“오토바이로 묘기를 부립니다”);
	}
}

  ```

#### Main 클래스

  ```
public class Main {
	public static void main(String[] args) {

	// 객체 생성
	Car car = new Car();
	MotorBike motorBike = new MotorBike();

	// car 객체의 속성 정의
	car.model = “테슬라”;
	car.color = “빨강색”;

	// 객체들의 기능 실행
	car.moveForward();
	motorBike.moveForward();
	motorBike.moveBackword();
	}
}

  ```

Car와 MotorBike 클래스의 공통적인 속성과 기능들을 추출하여 Vehicle 클래스에 정의
extends 키워드를 통해 각각의 하위 클래스로 확장, 해당 기능과 속성들을 반복적으로 정의해야 하는
번거로움을 제거했다.

공통적인 코드의 변경이 있는 경우 상위 클래스에서 한 번의 수정으로 모든 클래스에 
변경 사항이 반영될 수 있도록 하였다.
