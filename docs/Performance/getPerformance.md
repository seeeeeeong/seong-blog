---
sidebar_position: 5
---

# 공연 상세


> ![](https://img.shields.io/static/v1?label=&message=GET&color=blue) <br/>
> http://dev.officialhey.com/performances/{id}


### Parameters
#### Path
| name |  type  | description | required |
|:----:|:------:|:-----------:| :---: |
|  id  | String |   공연 아이디    | **Required** |

### Headers
|      name     |           type            |  description  | required |
|:-------------:|:-------------------------:|:-------------:| :---: |
| Authorization | Bearer [TOKEN] 형식의 String | 사용자 인증 정보가 들어있는 토큰	 | **Required** |



### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.

|   Field   |       Type        | Description |   
|:---------:|:-----------------:|:-----------:|
|    id     |      String       |   공연 아이디    | 
|  placeId  |      String       |  공연 장소 아이디  |
|   title   |      String       |     공연명     |
| startDate |   LocadDateTime   |   공연 시작일    |  
|  endDate  |   LocadDateTime   |   공연 종료일    |
|   cast    |      String       |     출연진     |
|  runtime  |      String       |    러닝타임     |    
|    age    |      String       |    관람 연령    | 
|   price   |      String       |     가격      | 
|  poster   |      String       | 공연 포스터 이미지  | 
|   visit   |      Boolean      |    내한 여부    |
|  status   | PerformanceStatus |    공연 상태    | 
| storyUrls |      String       |  공연 상세 이미지  |      
| schedule  |      String       |    공연 시간    | 
| latitude  |      Double       |     위도      | 
| longitude |   Double   |     경도      | 
|  address  |      String       |     주소      | 


<br/>

  <details markdown="1">
  <summary>성공 예제</summary>

  ```
{
    "status": true,
    "data": {
        "id": "PF244688",
        "placeId": "FC001608",
        "title": "D82 meet up live",
        "startDate": "2024-08-02",
        "endDate": "2024-08-02",
        "theater": "웨스트브릿지 라이브홀 (웨스트브릿지 라이브홀)",
        "cast": null,
        "runtime": "1시간 30분",
        "age": "전체 관람가",
        "price": "전석 82,000원",
        "poster": "http://www.kopis.or.kr/upload/pfmPoster/PF_PF244688_240710_130911.png",
        "visit": false,
        "status": "UPCOMING",
        "storyUrls": [
            "http://www.kopis.or.kr/upload/pfmIntroImage/PF_PF244688_240710_0109110.jpg"
        ],
        "schedule": "금요일(20:02)",
        "latitude": 37.553639,
        "longitude": 126.92614449999996,
        "address": "서울특별시 마포구 와우산로25길 6 (서교동)"
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

공연을 찾을 수 없을 때 반환하는 정보입니다.

<details markdown="1">
  <summary>에러 예제</summary>

  ```
{
    "status": false,
    "code": "P001",
    "message": "공연을 찾을 수 없습니다."
}
  ```
  </details>