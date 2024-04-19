---
sidebar_position: 3
---

# 티켓 오픈 임박


> ![](https://img.shields.io/static/v1?label=&message=GET&color=blue) <br/>
> http://dev.officialhey.com/show/nearest




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
      "name": "show1",
      "date": "2024-04-03T19:00:00",
      "poster": "https://example.com/image1.jpg"
    },
    {
      "id": 2,
      "name": "show2",
      "date": "2024-04-03T19:00:00",
      "poster": "https://example.com/image1.jpg"
    },
    {
      "id": 3,
      "name": "show3",
      "date": "2024-04-03T19:00:00",
      "poster": "https://example.com/image1.jpg"
    },
    {
      "id": 4,
      "name": "show4",
      "date": "2024-04-03T19:00:00",
      "poster": "https://example.com/image1.jpg"
    },
    {
      "id": 5,
      "name": "show5",
      "date": "2024-04-03T19:00:00",
      "poster": "https://example.com/image1.jpg"
    }
  ]
}
  ```
  </details>
<br/>