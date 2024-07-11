---
sidebar_position: 3
---

# 아티스트 공연


> ![](https://img.shields.io/static/v1?label=&message=GET&color=blue) <br/>
> http://dev.officialhey.com/artists/{id}/performances



### Parameters

|   name    |       type        |             description             |     required     |
|:---------:|:-----------------:|:-----------------------------------:|:----------------:|
|   size    |        Int        |                 사이즈                 | **Not Required** |
|   page    |        Int        |                 페이지                 |    **Not Required**     | 
| direction |     Direction     |                 정렬                  |    **Not Required**     | 


#### Path
| name |  type  | description | required |
|:----:|:------:|:-----------:| :---: |
|  id  | String |  아티스트 아이디   | **Required** |

### Headers
|      name     |           type            |  description  | required |
|:-------------:|:-------------------------:|:-------------:| :---: |
| Authorization | Bearer [TOKEN] 형식의 String | 사용자 인증 정보가 들어있는 토큰	 | **Required** |



### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.


|   Field    |       Type        | Description |   
|:----------:|:-----------------:|:----------:|
|     id     |      String       |   공연 아이디   | 
|   title    |      String       |     공연명    |   
| startDate  |   LocadDateTime   |   공연 시작일   |  
|  endDate   |   LocadDateTime   |   공연 종료일   |  
|  theater   |      String       |     공연장    |    
|   poster   |      String       | 공연 포스터 이미지 | 
|   status   | PerformanceStatus |    공연 상태   | 
| created_at |   LocadDateTime   |    생성일     | 

<br/>

  <details markdown="1">
  <summary>성공 예제</summary>

  ```
{
    "status": true,
    "data": {
        "content": [
            {
                "id": "PF244435",
                "title": "심수봉 전국투어콘서트: 꽃길 [의정부]",
                "startDate": "2024-10-12",
                "endDate": "2024-10-12",
                "theater": "http://www.kopis.or.kr/upload/pfmPoster/PF_PF244435_240705_133327.gif",
                "poster": "의정부예술의전당 (대극장)",
                "status": "UPCOMING",
                "createdAt": "2024-07-10 15:07:41"
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
<br/>

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
아티스트를 찾을 수 없을 때 반환하는 정보입니다.

<details markdown="1">
  <summary>에러 예제</summary>

  ```
{
    "status": false,
    "code": "AR001",
    "message": "아티스트를 찾을 수 없습니다."
}
  ```
 </details>