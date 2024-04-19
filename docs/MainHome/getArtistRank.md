---
sidebar_position: 4
---

# 이달의 아티스트 TOP 5


> ![](https://img.shields.io/static/v1?label=&message=GET&color=blue) <br/>
> http://dev.officialhey.com/artist/rank



#### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.


| Field  |     Type      |           Description           |   
|:------:|:-------------:|:-------------------------------:|
|   id   |     Long      |             공연 아이디              | 
|  name  |    String     |              공연 명               |   
|  date  | LocadDateTime |              공연 날짜              |  
| poster |    String     |         공연 포스터 이미지 URL          |   


  <details markdown="1">
  <summary>성공 예제</summary>

  ```
  {
  "ok": true,
  "data": [
    {
      "id": 1,
      "name": "artist1",
      "profileImage": "image1"
    },
    {
      "id": 2,
      "name": "artist2",
      "profileImage": "image1"
    },
    {
      "id": 3,
      "name": "artist3",
      "profileImage": "image1"
    },
    {
      "id": 4,
      "name": "artist4",
      "profileImage": "image1"
    },
    {
      "id": 5,
      "name": "artist5",
      "profileImage": "image1"
    }
  ]
}
  ```
  </details>
<br/>