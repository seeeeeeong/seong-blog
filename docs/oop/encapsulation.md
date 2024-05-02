---
sidebar_position: 5
---

# 캡슐화

클래스 안에 서로 연관 있는 속성과 기능들을 하나의 캡슐로 만들어
데이터를 외부로부터 보호하는 것

즉, 외부로부터 클래스에 정의된 속성과 기능들을 보호하고, 
필요한 부분만 외부로 노출될 수 있도록 하여 각 객체 고유의 독립성과
책임 영역을 안전하게 지키고자 하는 목적


#### 접근 제어자


|  접근 제어자   |     클래스 내     | 패키지 내 | 다른 패키지의 하위 클래스 | 패키지 외  |               설명                | 
|:---------:|:-------------:|:-----:|:--------------:|:------:|:-------------------------------:|
|  private  |       O       |   X   |     X     | X |        동일 클래스 내에서만 접근 가능        | 
|  default  |    O     |   O   |     X     | X |        동일 패키지 내에서만 접근 가능        | 
| protected | O |   O   |    O     | X | 동일 패키지 + 다른 패키지의 하위 클래스에서 접근 가능 | 
|  public   |    O     |   O   |    O     | O |            접근 제한 없음             | 

#### getter / setter

모든 속성값들이 private 접근 제어자로 선언되어 있고, getter/setter 메서드의 접근 제어자만이 public으로 열려있다.
선택적으로 외부에 접근을 허용할 속성과 그렇지 않을 속성을 getter/setter 메서드를 통해 설정할 수 있다.


  
#### Car 클래스

  ```
public class Car {
	private String model;
	private String color;

	public Car(String model, String color) {
		this.model = model;
		this.color = color;
	}

	private void startEngine() {
		System.out.println(“시동을 겁니다.”);
	}

	private void moveForward() {
		System.out.println(“자동차가 앞으로 전진합니다”);
	}

	private void openWindow() {
		System.out.println(“모든 창문을 엽니다”);
	}

	public void operate() { // 앞서 Driver 클래스에 정의된 메서드들 이용하여 메서드 추출
		startEngine();
		moveForward();
		openWindow();
	}
}
  ```

#### Driver 클래스

  ```
public class Driver {
	private String name;
	private Car car;

	public Driver(String name, Car car) {
		this.name = name;
		this.car = car;
	}

	public String getName() {
		return name;
	}

	public void drive() {
		car.operate(); // Car 클래스에 있는 메서드를 단순하게 호출
	}
}

  ```

#### Main 클래스

  ```
public class Main {
	public static void main(String[] args) {
		Car car = new Car(“테슬라”, “레드”);
		Driver driver = new Driver(“김코딩”, car);

		driver.drive();
	}
	
}

// 출력값
시동을 겁니다.
자동차가 앞으로 전진합니다.
모든 창문을 엽니다.

  ```

operate() 메서드 내부의 메서드들은 외부에서 호출되어 사용할 일이 없으므로
접근 제어자를 모두 private로 변경, Car 클래스와 관련된 기능들은 온전히 Car에서만 관리, 불필요한 내부 동작의 노출을 최소화한다.

Driver 클래스의 입장에서는 더 이상 Car 클래스의 내부 로직을 알지 못하고 알 필요도 없어졌다.
이렇게 캡슐화를 활용하여, 객체 내부 동작의 외부로의 노출을 최소하하고 각 객체의 자율성을 높이며,
이를 통해 객체 간 결합도를 낮추어 객체 지향의 핵심적인 이점을 잘 살리는 방법으로 프로그램을 설계할 수 있다.

<br/>


