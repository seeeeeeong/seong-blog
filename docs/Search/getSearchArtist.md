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
                "id": 1,
                "name": "artist1",
                "profileImage": "image"
            },
            {
                "id": 2,
                "name": "artist2",
                "profileImage": "image"
            },
            {
                "id": 3,
                "name": "artist3",
                "profileImage": "image"
            },
            {
                "id": 8,
                "name": "artist8",
                "profileImage": "image"
            },
            {
                "id": 9,
                "name": "artist9",
                "profileImage": "image"
            },
            {
                "id": 10,
                "name": "artist10",
                "profileImage": "image"
            },
            {
                "id": 4,
                "name": "artist4",
                "profileImage": "image"
            },
            {
                "id": 5,
                "name": "artist5",
                "profileImage": "image"
            },
            {
                "id": 6,
                "name": "artist6",
                "profileImage": "image"
            },
            {
                "id": 7,
                "name": "artist7",
                "profileImage": "image"
            }
        ],
        "currentPage": 0,
        "size": 20,
        "first": true,
        "last": true
    }
}
  ```
  </details>
<br/>