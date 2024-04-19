---
sidebar_position: 4
---

# 공연 아티스트


> ![](https://img.shields.io/static/v1?label=&message=GET&color=brightgreen) <br/>
> http://dev.officialhey.com/show/{id}/artist


### Parameters
#### Path
| name | type | description  | required |
|:----:|:----:|:------------:| :---: |
|  id  | Long |    공연 아이디    | **Required** |

### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.

|    Field     |  Type  |   Description    |   
|:------------:|:------:|:----------------:|
|      id      |  Long  |     아티스트 아이디     | 
|     name     | String |      아티스트 명      |   
| profileImage | String | 아티스트 프로필 이미지 url |  

<br/>

  <details markdown="1">
  <summary>성공 예제</summary>

  ```
  {
  "ok": true,
  "data": [
    {
      "id": 1,
      "name": "artist",
      "profileImage": "image1"
    }
  ]
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