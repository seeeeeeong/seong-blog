---
sidebar_position: 4
---

# 다형성

어떤 객체의 속성이나 기능이 상황에 따라 여러 가지 형태를 가질 수 있는 성질

중년 남성이 있다고 가정했을 때 그 남자의 역할이 아내에게는 남편, 자식에게는 아버지,
회사에서는 회사원 등 상황과 환경에 따라서 달라지는 것

ex) 메서드 오버라이딩, 메서드 오버로딩


### Vehicle 인터페이스

  ```
  public interface Vehicle {
	public abstract void start()
	void moveForward(); // public abstract 키워드 생략 가능
	void moveBackward();
} 
  ```

### Car 클래스

  ```
public class Car implements Vehicle {
	
	@Override
	public void moveForward() {
		System.out.println(“자동차가 앞으로 전진합니다);
	}

	@Override
	public void moveBackward() {
		System.out.println(“자동차가 뒤로 후진합니다);
	}

}
  ```

메서드 오버라이딩을 사용하여 같은 이름의 moveForward()와 moveBackward()를
각각의 클래스의 맥락에 맞게 재정의하여 사용할 수 있다.
즉, 같은 이름의 메서드가 상황에 따라 다른 역할을 수행한다.

### 객체 지향 맥락에서의 다형성 정의

한 타입의 참조변수를 통해 여러 타입의 객체를 참조할 수 있도록 만든 것
상위 클래스 타입의 참조변수로 하위 클래스의 객체를 참조할 수 있도록 하는 것


### Main 클래스

  ```
public class Main {
	public static void main(String[] args) {

	// 원래 사용했던 객체 생성 방식
	Car car = new Car();
	MotorBike motorBike = new MotorBike();

	// 다형성을 활용한 객체 생성 방식
	Vehicle car2 = new Car();

	}
}
  ```

다형성을 활용하면 여러 종류의 객체를 배열로 다룰 수 있다.

### Main 클래스

  ```
public class Main {
	public static void main(String[] args) {

	// 상위 클래스 타입의 객체 배열 생성
	Vehicle vehicles[] = new Vehicle[2];
	vehicle[0] = new Car();
	vehicle[1] = new MotorBike();

	for (Vehicle vehicle : vehicles) {
		System.out.println(vehicle.getClass()); // 각각의 클래스를 호출해주는 메서드
	}

	}
}

// 출력값
class Car
class MotorBike
  ```


상위 클래스 Vehicle 타입의 객체 배열을 생성해주면, 해당 타입의 참조 변수는
Vehicle 클래스와 상속 관계에 있는 모든 하위 클래스들을 그 안에 담을 수 있다.

다형성을 활용하여 하나의 타입만으로 여러 타입의 객체를 참조할 수 있어
보다 간편하고 유연하게 코드를 작성할 수 있다.



### Driver 클래스

  ```
public class Driver {

	void drive(Car car) {
		car.moveForward();
		car.moveBackword();
	}


	void drive(MotorBike motorBike) {
		motorBike.moveForward();
		motorBike.moveBackward();
	}
}

  ```




### Main 클래스

  ```
public class Main {
	public static void main(String[] args) {

		Car car = new Car();
		MotorBike motorBike = new MotorBike();
		Driver driver = new Driver();

		driver.drive(car);
		driver.drive(motorBike);
	}
}

// 출력값
전진합니다
후진합니다
오토바이가 앞으로 전진합니다
후진합니다
  ```

이동 수단이 수 십, 수 백 개라면 코드를 수 십, 수 백 번 작성해야 하는 문제가 있다.
객체 지향 프로그래밍은 지금까지 학습한 추상화, 상속, 다형성의 특성을 활용하여
프로그램을 설계할 때 역할과 구현을 구분, 객체들 간의 직접적인 결합을 피하고
느슨한 관계 설정을 통해 보다 유연하고 변경이 용이한 프로그램 설계를 가능하게 한다.



### Vehicle 인터페이스

  ```
public interface Vehicle { // 이동 수단의 역할 정의
	void moveForward();
	void moveBackward();
}

  ```

### Car 클래스

  ```
  
public class Car implements Vehicle {

	@Override
	public void moveForward() {
		System.out.printlin(“자동차가 앞으로 전진합니다”);
	}

	@Override
	public void moveBackward() {
		System.out.println(“자동차가 뒤로 후진합니다”);
	}

}

  ```

### MotorBike 클래스

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

### Driver 클래스

  ```
  
public class Driver {
	void drive(Vehicle vehicle) {
		vehicle.moveForward();
		vehicle.moveBackward();
	}
}


  ```

### Main 클래스

  ```
  
public class Main {
	public static void main(String[] args) {
		Car car = new Car();
		MotorBike motorBike = new MotorBike();
		Driver driver = new Driver();

		driver.drive(car);
		driver.drive(motorBike);
}
}

// 출력값
자동차가 앞으로 전진합니다.
자동차가 뒤로 후진합니다.
오토바이가 앞으로 전진합니다.
오토바이가 뒤로 후진합니다.


  ```

drive() 메서드로 전달되는 매개변수의 타입을 상위 클래스인 인터페이스 타입
Vehicle로 변경 하였다.

Driver 클래스는 더 이상 각각의 클래스 내부의 변경이나 다른 객체가 새롭게
교체되는 것을 신경 쓰지 않아도 인터페이스에만 의존하여 수정이 있을 때 마다
코드 변경을 하지 않아도 된다.



### Main 클래스

  ```
  
public class Main {
	public static void main(String[] args) {
		Car car = new Car();
		MotorBike motorBike = new MotorBike();
		Driver driver = new Driver();

		driver.drive(car);
		driver.drive(motorBike);
}
}

  ```

여전히 실행 클래스의 코드에서 객체를 생성 할 때, new Car()와 new MotorBike()
처럼 객체에 직접적으로 의존하고 있어, 해당 객체를 다른 객체로 변경할 시 코드의 변경이
불가피하다. - 의존관계 주입을 통해 해결

<br/>