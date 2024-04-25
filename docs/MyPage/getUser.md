---
sidebar_position: 1
---

# 프로필 조회


> ![](https://img.shields.io/static/v1?label=&message=GET&color=blue) <br/>
> http://dev.officialhey.com/user/{id}


### Parameters
### Path
| name | type | description | required |
|:----:|:----:|:-----------:| :---: |
|  id  | Long |   유저 아이디    | **Required** |

### Headers
|      name     |           type            |  description  | required |
|:-------------:|:-------------------------:|:-------------:| :---: |
| Authorization | Bearer [TOKEN] 형식의 String | 사용자 인증 정보가 들어있는 토큰	 | **Required** |



#### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.


|    Field    |  Type  | Description |   
|:-----------:|:------:|:-----------:|
|     id      |  Long  |   유저 아이디    | 
|    email    | String |     이메일     |   
|  userName   | String |     이름      |  
| phoneNumber | String |    전화번호     |   
|  nickName   | String |     닉네임     |  

<br/>

  <details markdown="1">
  <summary>성공 예제</summary>

  ```
{
    "ok": true,
    "data": {
        "id": 1,
        "email": "testt@test.com",
        "userName": "test",
        "phoneNumber": "01000100000",
        "nickName": "Test"
    }
}
  ```
  </details>

### Error

HTTP Status 가 401 SIGNIN_REQUIRED일 때 반환하는 정보입니다.

<details markdown="1">
  <summary>에러 예제 </summary>

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
<br/>

HTTP Status 가 401 JWT_TOKEN_MALFORMED일 때 반환하는 정보입니다.


<details markdown="1">
  <summary>에러 예제 </summary>

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
<br/>

HTTP Status 가 404 USER_NOT_FOUND일 때 반환하는 정보입니다.

<details markdown="1">
  <summary>에러 예제</summary>

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
<br/>