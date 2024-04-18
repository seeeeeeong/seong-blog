---
sidebar_position: 3
---

# 공연 상세


> ![](https://img.shields.io/static/v1?label=&message=GET&color=blue) <br/>
> http://dev.officialhey.com/show/{id}

<details markdown="1">
<summary>api specification</summary>

#### Parameters
#### Path
| name | type | description  | required |
|:----:|:----:|:------------:| :---: |
|  id  | Long |    공연 아이디    | **Required** |


#### Response

  <details markdown="1">
  <summary>200 OK : 성공</summary>

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
    "urlId": "dafafagagawg",
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

#### Error
<details markdown="1">
  <summary>4O4 NOT_FOUND : 공연을 찾을 수 없을 경우 </summary>

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
</details>
<br/>