---
sidebar_position: 2
---

# 통합검색 - 아티스트


> ![](https://img.shields.io/static/v1?label=&message=GET&color=brightgreen) <br/>
> http://dev.officialhey.com/search/artist


### Parameters
|  name   |  type  |             description             |     required     |
|:-------:|:------:|:-----------------------------------:|:----------------:|
|  page   |  Int   |             page, size              | **Not Required** |
| keyword | String |               검색 키워드                |    **Not Required**     | 



#### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.


|    Field     |  Type  |   Description    |   
|:------------:|:------:|:----------------:|
|   artistId   |  Long  |     아티스트 아이디     | 
|  artistName  | String |      아티스트명       |   
| profileImage | String | 아티스트 프로필 이미지 url |  

<br/>

  <details markdown="1">
  <summary>성공 예제</summary>


  ```
  {
  "ok": true,
  "data": {
    "content": [
      {
        "artistId": 4,
        "artistName": "artist1",
        "profileImage": "image1"
      },
      {
        "artistId": 5,
        "artistName": "artist2",
        "profileImage": "image1"
      },
      {
        "artistId": 6,
        "artistName": "artist3",
        "profileImage": "image1"
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