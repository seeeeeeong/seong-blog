---
sidebar_position: 1
---

# 아티스트 상세


> ![](https://img.shields.io/static/v1?label=&message=GET&color=blue) <br/>
> http://dev.officialhey.com/artist/{id}

### Parameters
#### Path
| name | type | description | required |
|:----:|:----:|:-----------:| :---: |
|  id  | Long |  아티스트 아이디   | **Required** |


### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.


|    Field     |     Type      |      Description      |   
|:------------:|:-------------:|:---------------------:|
|      id      |     Long      |       아티스트 아이디        | 
|     name     |    String     |         아티스트명         |   
| profileImage |    String     |   아티스트 프로필 이미지 url    |  
|    genre     |    String     | 판매처, url, 아이콘 이미지 url |  
|  debutDate   | LocalDateTime |         데뷔 날짜         |  

<br/>

  <details markdown="1">
  <summary>성공 예제</summary>

  ```
 {
    "ok": true,
    "data": {
        "id": 1,
        "name": "artist1",
        "profileImage": "image",
        "genre": "edm",
        "debutDate": "2024-03-28T22:44:00",
        "createdAt": "2024-04-18T18:09:30.787296",
        "updatedAt": "2024-04-18T18:09:30.787296"
    }
}
  ```
  </details>

<br/>

### Error

HTTP Status 가 404 ARTIST_NOT_FOUND일 때 반환하는 정보입니다.

<details markdown="1">
  <summary>에러 예제 </summary>

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