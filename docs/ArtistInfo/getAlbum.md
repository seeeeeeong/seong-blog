---
sidebar_position: 2
---

# 앨범 정보


> ![](https://img.shields.io/static/v1?label=&message=GET&color=brightgreen) <br/>
> http://dev.officialhey.com/artist/{id}/album


### Parameters
|  name   |  type  |             description             |     required     |
|:-------:|:------:|:-----------------------------------:|:----------------:|
|  page   |  Int   |             page, size              | **Not Required** |

#### Path
| name | type | description | required |
|:----:|:----:|:-----------:| :---: |
|  id  | Long |  아티스트 아이디   | **Required** |


### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.

|    Field    |     Type      | Description |   
|:-----------:|:-------------:|:-----------:|
|  coverImg   |    String     | 앨범 이미지 url  | 
|    title    |    String     |   앨범 타이틀    |   
| releaseDate | LocadDateTime |   앨범 발매일    |  

<br/>

  <details markdown="1">
  <summary>성공 예제</summary>

  ```
  {
  "ok": true,
  "data": {
    "content": [
      {
        "coverImg": "image1",
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

<br/>

### Error

HTTP Status 가 404 ARTIST_NOT_FOUND일 때 반환하는 정보입니다.

<details markdown="1">
  <summary>에러 예제</summary>

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


<br/>