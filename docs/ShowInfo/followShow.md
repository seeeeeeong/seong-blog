---
sidebar_position: 3
---

# 공연 팔로우


> ![](https://img.shields.io/static/v1?label=&message=POST&color=brightgreen) <br/>
> http://dev.officialhey.com/user/follow/show/{id}
>
### Parameters
#### Path
| name | type |  description  | required |
|:----:|:----:|:-------------:| :---: |
|  id  | Long | 팔로우 할 공연의 아이디 | **Required** |

### Headers
|      name     |           type            |  description  | required |
|:-------------:|:-------------------------:|:-------------:| :---: |
| Authorization | Bearer [TOKEN] 형식의 String | 사용자 인증 정보가 들어있는 토큰	 | **Required** |



### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.

|  Field  |  Type  |    Description     |   
|:-------:|:------:|:------------------:|
|   id    |  Long  |       공연 아이디       | 
| message | String | 팔로우, 팔로우 취소 메시지 응답 |  


<br/>

  <details markdown="1">
  <summary>성공 예제 - 팔로우</summary>

  ```
  {
  "ok": true,
  "data": {
    "id": 1,
    "message": "follow"
  }
}
  ```
  </details>
<br/>
<details markdown="1">
  <summary>성공 예제 - 팔로우 취소 </summary>

  ```
  {
  "ok": true,
  "data": {
    "id": 1,
    "message": "unfollow"
  }
}
  ```


  </details>
<br/>

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

HTTP Status 가 404 SHOW_NOT_FOUND일 때 반환하는 정보입니다.

<details markdown="1">
  <summary>에러 예제</summary>

  ```
{
    "ok": false,
    "timestamp": "2024-04-18T16:24:34.500251",
    "status": 404,
    "error": "NOT_FOUND",
    "code": "SHOW_NOT_FOUND",
    "message": "공연을 찾을 수 없습니다."
}
  ```
  </details>
<br/>