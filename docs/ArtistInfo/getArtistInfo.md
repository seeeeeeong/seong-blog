---
sidebar_position: 1
---

# 아티스트 상세


> ![](https://img.shields.io/static/v1?label=&message=GET&color=blue) <br/>
> http://dev.officialhey.com/artist/{id}

<details markdown="1">
<summary>detail</summary>

#### Parameters
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