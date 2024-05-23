---
sidebar_position: 1
---

# 공연 리스트


> ![](https://img.shields.io/static/v1?label=&message=GET&color=blue) <br/>
> http://dev.officialhey.com/show



### Parameters

|  name   |  type  |             description             |     required     |
|:-------:|:------:|:-----------------------------------:|:----------------:|
|  page   |  Int   |              페이지, 사이즈               | **Not Required** |
| exclude | String |            종료된 공연 제외(on)            |    **Not Required**     | 
|  type   | String |          국내공연, 페스티벌, 내한공연           |    **Not Required**     | 
|  genre  | String | 발라드, 힙합/R&B, EDM, 인디/록, 재즈, 아이돌, 기타 |    **Not Required**     | 
| status  | String |   공연 예정(up), 공연 중(on), 공연 종료(end)   |    **Not Required**     |
| ticket  | String |   판매 예정(up), 판매 중(on), 판매 종료(end)   |    **Not Required**     |


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
                "id": 5,
                "name": "show5",
                "ticketOpenTime": "2024-04-21T19:00:00",
                "date": "2024-04-22T19:00:00",
                "poster": "https://example.com/image1.jpg",
                "place": "Hey Theater"
            },
            {
                "id": 4,
                "name": "show4",
                "ticketOpenTime": "2024-04-21T19:00:00",
                "date": "2024-04-22T19:00:00",
                "poster": "https://example.com/image1.jpg",
                "place": "Hey Theater"
            },
            {
                "id": 3,
                "name": "show3",
                "ticketOpenTime": "2024-04-21T19:00:00",
                "date": "2024-04-22T19:00:00",
                "poster": "https://example.com/image1.jpg",
                "place": "Hey Theater"
            },
            {
                "id": 2,
                "name": "show2",
                "ticketOpenTime": "2024-04-21T19:00:00",
                "date": "2024-04-22T19:00:00",
                "poster": "https://example.com/image1.jpg",
                "place": "Hey Theater"
            },
            {
                "id": 1,
                "name": "show1",
                "ticketOpenTime": "2024-04-21T19:00:00",
                "date": "2024-04-22T19:00:00",
                "poster": "https://example.com/image1.jpg",
                "place": "Hey Theater"
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