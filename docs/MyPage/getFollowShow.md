---
sidebar_position: 3
---

# 팔로우 목록 - 공연


> ![](https://img.shields.io/static/v1?label=&message=GET&color=brightgreen) <br/>
> http://dev.officialhey.com/user/follow/show

<details markdown="1">
<summary>detail</summary>

### Parameters
|  name   |  type  |             description             |     required     |
|:-------:|:------:|:-----------------------------------:|:----------------:|
|  page   |  Int   |             page, size              | **Not Required** |

### Headers
|      name     |           type            |  description  | required |
|:-------------:|:-------------------------:|:-------------:| :---: |
| Authorization | Bearer [TOKEN] 형식의 String | 사용자 인증 정보가 들어있는 토큰	 | **Required** |


### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.


|     Field      |     Type      |  Description   |   
|:--------------:|:-------------:|:--------------:|
|       id       |     Long      |     공연 아이디     | 
|      name      |    String     |      공연명       |   
| ticketOpenTime | LocadDateTime |     티켓 오픈일     |  
|      date      | LocadDateTime |     공연 날짜      |  
|     poster     |    String     | 공연 포스터 이미지 url |    
|     place      |    String     |     공연 장소      | 

<br/>



  <details markdown="1">
  <summary>성공 예제</summary>

  ```
  {
  "ok": true,
  "data": {
    "content": [
      {
        "id": 1,
        "name": "show",
        "ticketOpenTime": "2024-04-03T17:44:00",
        "date": "2024-04-03T19:00:00",
        "poster": "https://example.com/image1.jpg",
        "place": "Hey Theater"
      }
    ],
    "pageable": {
      "pageNumber": 0,
      "pageSize": 20,
      "sort": {
        "empty": true,
        "unsorted": true,
        "sorted": false
      },
      "offset": 0,
      "paged": true,
      "unpaged": false
    },
    "last": true,
    "totalElements": 1,
    "totalPages": 1,
    "first": true,
    "size": 20,
    "number": 0,
    "sort": {
      "empty": true,
      "unsorted": true,
      "sorted": false
    },
    "numberOfElements": 1,
    "empty": false
  }
}
  ```
  </details>
<br/>

#### Error


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