---
sidebar_position: 3
---

# 아티스트 공연


> ![](https://img.shields.io/static/v1?label=&message=GET&color=blue) <br/>
> http://dev.officialhey.com/artist/show



### Parameters

|  name   |  type  |             description             |     required     |
|:-------:|:------:|:-----------------------------------:|:----------------:|
|  page   |  Int   |              페이지, 사이즈               | **Not Required** |
| exclude | String |            종료된 공연 제외(on)            |    **Not Required**     | 


#### Path
| name | type | description | required |
|:----:|:----:|:-----------:| :---: |
|  id  | Long |  아티스트 아이디   | **Required** |


### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.


|     Field      |     Type      |  Description   |   
|:--------------:|:-------------:|:--------------:|
|       id       |     Long      |     공연 아이디     | 
|      name      |    String     |      공연명       |   
| ticketOpenTime | LocadDateTime |     티켓 오픈일     |  
|      date      | LocadDateTime |     공연 날짜      |  
|     poster     |    String     | 공연 포스터 이미지 url |    
|     place      |    String     |     공연 장소      | 

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
                "name": "show1",
                "ticketOpenTime": "2024-04-21T19:00:00",
                "date": "2024-04-22T19:00:00",
                "poster": "https://example.com/image1.jpg",
                "place": "Hey Theater"
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