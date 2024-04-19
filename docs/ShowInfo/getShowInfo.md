---
sidebar_position: 2
---

# 공연 상세


> ![](https://img.shields.io/static/v1?label=&message=GET&color=blue) <br/>
> http://dev.officialhey.com/show/{id}

### Parameters
#### Path
| name | type | description  | required |
|:----:|:----:|:------------:| :---: |
|  id  | Long |    공연 아이디    | **Required** |


### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.


|     Field      |     Type      |                Description                 |   
|:--------------:|:-------------:|:------------------------------------------:|
|       id       |     Long      |                   공연 아이디                   | 
|      name      |    String     |                    공연명                     |   
|   PriceInfo    |   PriceInfo   |                 좌석 정보, 가격                  |  
|  TicketSeller  | TicketSeller  |           판매처, url, 아이콘 이미지 url            |  
| ticketOpenTime | LocalDateTime |                   티켓 오픈일                   | 
|      date      | LocalDateTime |                   공연 날짜                    | 
|  strictedAge   |    Integer    |                   제한 연령                    |   
|  runningTime   |   LocalTime   |                   러닝 타임                    |    
|     place      |    String     |                   공연 장소                    |  
|      type      |    String     |          공연 타입(국내공연, 페스티벌, 내한공연)           |  
|     genre      |    String     | 공연 장르(발라드, 힙합/R&B, EDM, 인디/록, 재즈, 아이돌, 기타) |    
|     poster      |    String     |               공연 포스터 이미지 url               | 
|      type      |     Long      |                   공연 타입                    | 
|     genre      |    String     |                     장르                     |   
|  detailImages  |`List<String>` |               공연 상세 이미지 url                |  
|  isConfirmed  |    Boolean    |                공연 확정(백오피스)                 |  

<br/>

  <details markdown="1">
  <summary>성공 예제</summary>

  ```
  {
  "ok": true,
  "data": {
    "id": 1,
    "name": "show",
    "priceInfos": [
      {
        "type": "Regular",
        "price": 30000
      },
      {
        "type": "VIP",
        "price": 50000
      }
    ],
    "ticketSellers": [
      {
        "name": "yes24",
        "baseUrl": "https://www.yes24.com",
        "icon": "yes24.png"
      },
      {
        "name": "interpark",
        "baseUrl": "https://www.interpark.com",
        "icon": "interpark.png"
      }
    ],
    "ticketOpenTime": "2024-04-03T17:44:00",
    "date": "2024-04-03T19:00:00",
    "strictedAge": 18,
    "runningTime": "19:00:00",
    "place": "Hey Theater",
    "type": "local",
    "genre": "edm",
    "poster": "https://example.com/image1.jpg",
    "detailImages": [
      "https://example.com/image2.jpg",
      "https://example.com/image3.jpg",
      "https://example.com/image4.jpg"
    ],
    "isConfirmed": true,
    "createdAt": "2024-04-05T21:07:24.439169",
    "updatedAt": "2024-04-05T21:08:15.975783"
  }
}
  ```
  </details>

<br/>

### Error

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