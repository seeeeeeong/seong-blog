---
sidebar_position: 2
---

# 회원정보 수정


> ![](https://img.shields.io/static/v1?label=&message=PUT&color=orange) <br/>
> http://dev.officialhey.com/user/1

<details markdown="1">
<summary>detail</summary>

#### Parameters
#### Headers
|      name     |           type            |  description  | required |
|:-------------:|:-------------------------:|:-------------:| :---: |
| Authorization | Bearer [TOKEN] 형식의 String | 사용자 인증 정보가 들어있는 토큰	 | **Required** |

#### Path
| name | type | description | required |
|:----:|:----:|:-----------:| :---: |
|  id  | Long |   유저 아이디    | **Required** |

##### Body
  ```
{
    "nickName": "nickName",
    "password": "password",
    "email": "email@email.com:,
    "privider": "kakao",
    "userName": "name",
    "phoneNumber": "01012345678"
}
  ```
#### Response

  <details markdown="1">
  <summary>200 Ok : 성공</summary>

  ```
  {
  "ok": true,
  "data": {
    "id": 1,
    "nickName": "nickName",
    "phoneNumber": "01012345678"
  }
}
  ```
  </details>

#### Error


<details markdown="1">
  <summary>401 UNAUTHORIZED : 로그인을 하지 않았을 경우 </summary>

  ```
  {
    "ok": false,
    "timestamp": "2024-04-18T16:20:43.101276",
    "status": 401,
    "error": "UNAUTHORIZED",
    "code": "SIGNIN_REQUIRED",
    "message": "로그인을 하지 않았습니다."
}
  ```


  </details>

<details markdown="1">
  <summary>401 UNAUTHORIZED : JWT 토큰 형식이 맞지 않을 경우 </summary>

  ```
  {
    "ok": false,
    "timestamp": "2024-04-18T16:33:08.654105",
    "status": 401,
    "error": "UNAUTHORIZED",
    "code": "JWT_TOKEN_MALFORMED",
    "message": "JWT 토큰 형식이 맞지 않습니다."
}
  ```


  </details>

<details markdown="1">
  <summary>4O4 NOT_FOUND : 유저를 찾을 수 없을 경우 </summary>

  ```
{
    "ok": false,
    "timestamp": "2024-04-18T16:24:34.500251",
    "status": 404,
    "error": "NOT_FOUND",
    "code": "USER_NOT_FOUND",
    "message": "유저를 찾을 수 없습니다."
}
  ```


  </details>
</details>
<br/>