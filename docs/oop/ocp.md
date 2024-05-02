---
sidebar_position: 7
---

# OCP(Open Closed Principle): 개방 폐쇄 원칙

소프트웨어의 모든 구성 요소는 확장에는 열려있고 변경에는 닫혀있아야 한다는 원칙

요구사항의 변경이나 추가가 발생해도, 기존 구성요소는 수정이 일어나서는 안되고
쉽게 확장이 가능하여 재사용할 수 있어야 한다.

OCP를 가능하게 하는 중요한 메커니즘은 추상화와 다형성으로
클래스를 설계할 때 변할 부분과 변하지 않을 부분을 명확히 구분하여,
변할 수 있는 부분을 추상화하여 상속하는 클래스가 의존할 수 있게 코드를 작성한다.


  ```
class 캐릭터 {
	public fun 베기() {
		print(“///“);
	}

	public fun 점프() {
		print(“jump”);
	}
}

//Game
fun playGame(어떤캐릭터 : 캐릭터) {
	어떤캐릭터.점프();
	어떤캐릭터.베기();
}
  ```

위의 코드에서 업데이트를 통해 베기 스킬을 없애고 회전베기로 바꾸는 수정이 일어났을 경우


  ```
class 캐릭터 {
	public fun 회전베기() {
		print(“xxx/“);
	}

	public fun 점프() {
		print(“jump”);
	}
}

//Game
fun playGame(어떤캐릭터 : 캐릭터) {
	어떤캐릭터.점프();
	어떤캐릭터.베기(); //에러!!
}

  ```
이렇듯 그대로 상속해버리면 문제가 발생한다.

스킬 두 개가 각각 Q, W버튼을 눌렀을 때 반응한다고 가정하고 이 부분을 Interface로 만들어준다.

```
interface 캐릭터 {
	fun QPressed()
	fun WPressed()
}

class 어떤 캐릭터 : 캐릭터 {
	override fun QPressed() {
		회전베기();
	}
	override fun WPressed() {
		점프();
	}
	private fun 회전베기() {
		print(“xxx”);
	}
	private fun 점프() {
		print(“jump”);
	}
}

  ```

interface를 상속하여 변하는 부분과 변하지 않을 부분을 나누어
변할 수 있는 부분은 private로 선언하여 접근할 수 없게 만들었다.
스킬에 변동 사항이 생기더라도 게임 진행에 문제가 없다.
이렇게 하면 확장에는 열려있되, 변경에는 닫히게 된다.

<br/>


