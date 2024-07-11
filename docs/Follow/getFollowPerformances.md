---
sidebar_position: 2
---

# 팔로우 공연 정보


> ![](https://img.shields.io/static/v1?label=&message=GET&color=brightgreen) <br/>
> http://dev.officialhey.com/users/follow/performances


### Parameters

### Headers
|      name     |           type            |  description  | required |
|:-------------:|:-------------------------:|:-------------:| :---: |
| Authorization | Bearer [TOKEN] 형식의 String | 사용자 인증 정보가 들어있는 토큰	 | **Required** |



### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.


|   Field    |       Type        | Description |   
|:----------:|:-----------------:|:----------:|
|     id     |       Long        |   공연 아이디   | 
|   title    |      String       |     공연명    |   
| startDate  |   LocadDateTime   |   공연 시작일   |  
|  endDate   |   LocadDateTime   |   공연 종료일   |  
|  theater   |      String       |     공연장    |    
|   poster   |      String       | 공연 포스터 이미지 | 
|   status   | PerformanceStatus |    공연 상태   | 
| created_at | LocadDateTime |    생성일     | 

<br/>

  <details markdown="1">
  <summary>200 Ok : 성공</summary>

  ```
  {
    "status": true,
    "data": {
        "content": [
            {
                "id": "PF244635",
                "title": "Hathaw9y 해서웨이 X PATZ 파츠, Leap",
                "startDate": "2024-07-27",
                "endDate": "2024-07-27",
                "theater": "http://www.kopis.or.kr/upload/pfmPoster/PF_PF244635_240710_101002.png",
                "poster": "KT&G 상상마당 라이브홀 [마포] (KT&G 상상마당 라이브홀 [마포] )",
                "status": "UPCOMING",
                "createdAt": "2024-07-10 20:51:25"
            }
        ],
        "currentPage": 0,
        "size": 20,
        "first": true,
        "last": true
    }
}
  ```
  </details>

### Error

유저 정보를 찾을 수 없을 때 반환하는 정보입니다.

<details markdown="1">
  <summary>에러 예제 </summary>

  ```
{
    "status": false,
    "code": "U001",
    "message": "회원을 찾을 수 없습니다."
}
  
  ```

  </details>
<br/>

토큰이 만료 되었을 때 반환하는 정보입니다.

<details markdown="1">
  <summary>에러 예제 </summary>

  ```
{"status":false,"code":"S005","message":"jwt access token이 만료되었습니다."}
  ```

  </details>
<br/>

유효하지 않은 토큰일 때 반환하는 정보입니다.

<details markdown="1">
  <summary>에러 예제 </summary>

  ```
  {"status":false,"code":"S002","message":"유효하지 않은 토큰입니다."}
  ```


  </details>
<br/>

jwt token이 없을 때 반환하는 정보입니다.

<details markdown="1">
  <summary>에러 예제</summary>

  ```
{"status":false,"code":"S008","message":"jwt token이 없습니다."}
  ```
  </details>
<br/>
