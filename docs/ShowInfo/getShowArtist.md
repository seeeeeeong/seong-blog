---
sidebar_position: 4
---

# 공연 아티스트


> ![](https://img.shields.io/static/v1?label=&message=GET&color=brightgreen) <br/>
> http://dev.officialhey.com/show/{id}/artist

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