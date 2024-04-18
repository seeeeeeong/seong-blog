---
sidebar_position: 1
---

# 통합검색 - 공연


> ![](https://img.shields.io/static/v1?label=&message=GET&color=brightgreen) <br/>
> http://dev.officialhey.com/search/show

<details markdown="1">
<summary>detail</summary>

#### Parameters
|  name   |  type  |             description             |     required     |
|:-------:|:------:|:-----------------------------------:|:----------------:|
|  page   |  Int   |             page, size              | **Not Required** |
| keyword | String |               검색 키워드                |    **Not Required**     | 
| exclude | String |            종료된 공연 제외(on)            |    **Not Required**     | 



#### Response

  <details markdown="1">
  <summary>200 Ok : 성공</summary>

  ```
  {
  "ok": true,
  "data": {
    "content": [
      {
        "showId": 3,
        "showName": "show5",
        "urlId": "dafafagagawg",
        "date": "2024-04-17T19:00:00",
        "poster": "https://example.com/image1.jpg",
        "place": "Hey Theater"
      },
      {
        "showId": 2,
        "showName": "show5",
        "urlId": "dafafagagawg",
        "date": "2024-04-17T19:00:00",
        "poster": "https://example.com/image1.jpg",
        "place": "Hey Theater"
      },
      {
        "showId": 1,
        "showName": "show5",
        "urlId": "dafafagagawg",
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