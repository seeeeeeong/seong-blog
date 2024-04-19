---
sidebar_position: 1
---

# 통합검색 - 공연


> ![](https://img.shields.io/static/v1?label=&message=GET&color=brightgreen) <br/>
> http://dev.officialhey.com/search/show


### Parameters
|  name   |  type  |             description             |     required     |
|:-------:|:------:|:-----------------------------------:|:----------------:|
|  page   |  Int   |             page, size              | **Not Required** |
| keyword | String |               검색 키워드                |    **Not Required**     | 
| exclude | String |            종료된 공연 제외(on)            |    **Not Required**     | 



### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.


|     Field      |     Type      |  Description   |   
|:--------------:|:-------------:|:--------------:|
|     showId     |     Long      |     공연 아이디     | 
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
        "showId": 3,
        "showName": "show5",
        "ticketOpenTime": 2024-04-17T19:00:00,
        "date": "2024-04-17T19:00:00",
        "poster": "https://example.com/image1.jpg",
        "place": "Hey Theater"
      },
      {
        "showId": 2,
        "showName": "show5",
        "date": "2024-04-17T19:00:00",
        "ticketOpenTime": 2024-04-17T19:00:00,
        "poster": "https://example.com/image1.jpg",
        "place": "Hey Theater"
      },
      {
        "showId": 1,
        "showName": "show5",
        "date": "2024-04-17T19:00:00",
        "ticketOpenTime": 2024-04-17T19:00:00,
        "poster": "https://example.com/image1.jpg",
        "place": "Hey Theater"
      }
    ],
    "pageable": {
      "pageNumber": 0,
      "pageSize": 20,
      "sort": {
        "empty": true,
        "sorted": false,
        "unsorted": true
      },
      "offset": 0,
      "paged": true,
      "unpaged": false
    },
    "last": true,
    "totalElements": 3,
    "totalPages": 1,
    "first": true,
    "size": 20,
    "number": 0,
    "sort": {
      "empty": true,
      "sorted": false,
      "unsorted": true
    },
    "numberOfElements": 3,
    "empty": false
  }
}
  ```
  </details>

<br/>