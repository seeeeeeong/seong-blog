---
sidebar_position: 1
---

# OAuth2 로그인


> ![](https://img.shields.io/static/v1?label=&message=POST&color=brightgreen) <br/>
> http://dev.officialhey.com/oauth2/google/login

### Headers
|      name     |           type            |  description  | required |
|:-------------:|:-------------------------:|:-------------:| :---: |
| Authorization | Bearer [TOKEN] 형식의 String | 사용자 인증 정보가 들어있는 토큰	 | **Required** |



### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.


|    Field     |     Type      |      Description      |   
|:------------:|:-------------:|:---------------------:|
| accessToken  |    String     |      accessToken      | 
| refreshToken |    String     |   refreshToken        |   
 

<br/>

  <details markdown="1">
  <summary>성공 예제</summary>

  ```
  {
    "status": true,
    "data": {
        "accessToken": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzUxMiJ9.eyJ1c2VySWQiOiIxIiwiQXV0aGVudGljYXRpb25Sb2xlIjoiVVNFUiIsImlhdCI6MTcyMDYxMjI3NCwiZXhwIjoxNzIwNjE1ODc0fQ.p5xnT8i6qQYXnem1cEjGRaOOXNc_PMgNb4fBqNfCNX4k2ZmTkYaL5-WKBPz_aJ1fSGKMkk91hELg9r14g0AyWw",
        "refreshToken": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzUxMiJ9.eyJ1c2VySWQiOiIxIiwiQXV0aGVudGljYXRpb25Sb2xlIjoiVVNFUiIsImlhdCI6MTcyMDYxMjI3NCwiZXhwIjoxNzI1Nzk2Mjc0fQ.I6z_AMrT_Xm6_0jX2qrRv01eVi3b8NINKrHEwU5_Oy4nRsPf2d9V11g-DXX8vdSofO1Y9NSuDymm7I905APanw"
    }
}
  ```
  </details>
<br/>

### Error

외부로의 REST 통신에 실패하였을 때 발생하는 에러입니다.

<details markdown="1">
  <summary>에러 예제</summary>

  ```
{
    "status": false,
    "code": "R001",
    "message": "외부로의 REST 통신에 실패하였습니다."
}
  ```
  </details>

<br/>

authorization header가 비어있을 때 발생하는 에러입니다.

<details markdown="1">
  <summary>에러 예제</summary>

  ```
{
    "status": false,
    "code": "S007",
    "message": "authorization header가 비었습니다."
}
  ```
  </details>

<br/>