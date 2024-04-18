---
sidebar_position: 1
---

# 공연 리스트 


> ![](https://img.shields.io/static/v1?label=&message=GET&color=blue) <br/>
> http://dev.officialhey.com/show

<details markdown="1">
<summary>api specification</summary>

#### Parameters
#### Path
|  name   |  type  |             description             |     required     |
|:-------:|:------:|:-----------------------------------:|:----------------:|
|  page   |  Int   |             page, size              | **Not Required** |
| exclude | String |            종료된 공연 제외(on)            |    **Not Required**     | 
|  type   | String |          국내공연, 페스티벌, 내한공연           |    **Not Required**     | 
|  genre  | String | 발라드, 힙합/R&B, EDM, 인디/록, 재즈, 아이돌, 기타 |    **Not Required**     | 
| status  | String |   공연 예정(up), 공연 중(on), 공연 종료(end)   |    **Not Required**     |
| ticket  | String |   판매 예정(up), 판매 중(on), 판매 종료(end)   |    **Not Required**     |


#### Response

  <details markdown="1">
  <summary>200 Ok : 성공</summary>

  ```
  {
  "ok": true,
  "data": {
    "content": [
      {
        "id": 3,
        "name": "show3",
        "urlId": "url",
        "ticketOpenTime": 2024-04-17T19:00:00,
        "date": "2024-04-17T19:00:00",
        "poster": "https://example.com/image1.jpg",
        "place": "Hey Theater"
      },
      {
        "id": 2,
        "name": "show2",
        "urlId": "url",
        "ticketOpenTime": 2024-04-17T19:00:00,
        "date": "2024-04-17T19:00:00",
        "poster": "https://example.com/image1.jpg",
        "place": "Hey Theater"
      },
      {
        "id": 1,
        "name": "show1",
        "urlId": "url",
        "ticketOpenTime": 2024-04-17T19:00:00,
        "date": "2024-04-17T19:00:00",
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
</details>
<br/>