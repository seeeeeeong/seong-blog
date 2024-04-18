---
sidebar_position: 3
---

# 앨범 정보


> ![](https://img.shields.io/static/v1?label=&message=GET&color=brightgreen) <br/>
> http://dev.officialhey.com/artist/{id}/album

<details markdown="1">
<summary>detail</summary>

#### Parameters
|  name   |  type  |             description             |     required     |
|:-------:|:------:|:-----------------------------------:|:----------------:|
|  page   |  Int   |             page, size              | **Not Required** |

#### Path
| name | type | description | required |
|:----:|:----:|:-----------:| :---: |
|  id  | Long |  아티스트 아이디   | **Required** |


#### Response

  <details markdown="1">
  <summary>200 OK : 성공</summary>

  ```
  {
  "ok": true,
  "data": {
    "content": [
      {
        "coverImg": "image1",
        "url": "https://www.url.com",
        "title": "album",
        "releaseDate": "2024-03-28T22:44:00"
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

#### Error

<details markdown="1">
  <summary>4O4 NOT_FOUND : 아티스트를 찾을 수 없을 경우 </summary>

  ```
{
    "ok": false,
    "timestamp": "2024-04-18T16:24:34.500251",
    "status": 404,
    "error": "NOT_FOUND",
    "code": "ARTIST_NOT_FOUND",
    "message": "아티스트를 찾을 수 없습니다."
}
  ```


  </details>

</details>
<br/>