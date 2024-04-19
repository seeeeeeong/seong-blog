---
sidebar_position: 6
---

# 팔로우 취소 - 아티스트


> ![](https://img.shields.io/static/v1?label=&message=DELETE&color=red) <br/>
> http://dev.officialhey.com/user/follow/artist



### Headers
|      name     |           type            |  description  | required |
|:-------------:|:-------------------------:|:-------------:| :---: |
| Authorization | Bearer [TOKEN] 형식의 String | 사용자 인증 정보가 들어있는 토큰	 | **Required** |


### Body

```
[1, 2, 3]
```


### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.

<br/>

  <details markdown="1">
  <summary>성공 예제</summary>

  ```
{
    "ok": true,
    "data": null
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

