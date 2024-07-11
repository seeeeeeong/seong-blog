---
sidebar_position: 4
---

# 공연 순위


> ![](https://img.shields.io/static/v1?label=&message=GET&color=brightgreen) <br/>
> http://dev.officialhey.com/performances/rank


### Parameters


### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.


|   Field    |       Type        | Description |   
|:----------:|:-----------------:|:----------:|
|     id     |       Long        |   공연 아이디   | 
|   title    |      String       |     공연명    |   
| startDate  |   LocadDateTime   |   공연 시작일   |  
|  endDate   |   LocadDateTime   |   공연 종료일   |  
|  theater   |      String       |     공연장    |    
|   poster   |      String       | 공연 포스터 이미지 | 
|   status   | PerformanceStatus |    공연 상태   | 
| created_at | LocadDateTime |    생성일     | 

<br/>

  <details markdown="1">
  <summary>성공 예제</summary>

  ```
  {
    "status": true,
    "data": {
        "content": [
            {
                "id": "PF244688",
                "title": "D82 meet up live",
                "startDate": "2024-08-02",
                "endDate": "2024-08-02",
                "theater": "http://www.kopis.or.kr/upload/pfmPoster/PF_PF244688_240710_130911.png",
                "poster": "웨스트브릿지 라이브홀 (웨스트브릿지 라이브홀)",
                "status": "UPCOMING",
                "createdAt": "2024-07-11 19:15:21"
            },
            {
                "id": "PF244680",
                "title": "더베인 단독콘서트, MONSTER Ⅹ 0803",
                "startDate": "2024-08-03",
                "endDate": "2024-08-03",
                "theater": "http://www.kopis.or.kr/upload/pfmPoster/PF_PF244680_240710_124706.png",
                "poster": "KT&G 상상마당 라이브홀 [마포] (KT&G 상상마당 라이브홀 [마포] )",
                "status": "UPCOMING",
                "createdAt": "2024-07-11 19:15:21"
            },
            {
                "id": "PF244685",
                "title": "BoA LIVE TOUR, BoA: One' s Own",
                "startDate": "2024-10-12",
                "endDate": "2024-10-13",
                "theater": "http://www.kopis.or.kr/upload/pfmPoster/PF_PF244685_240710_130015.png",
                "poster": "올림픽공원 (SK핸드볼경기장(펜싱경기장))",
                "status": "UPCOMING",
                "createdAt": "2024-07-11 19:15:21"
            },
            {
                "id": "PF244690",
                "title": "TOMORROW X TOGETHER WORLD TOUR: ACT : PROMISE [일본]",
                "startDate": "2024-07-27",
                "endDate": "2024-09-15",
                "theater": "http://www.kopis.or.kr/upload/pfmPoster/PF_PF244690_240710_131249.gif",
                "poster": "교세라 돔 오사카 (KYOCERA DOME OSAKA) (KYOCERA DOME OSAKA)",
                "status": "UPCOMING",
                "createdAt": "2024-07-11 19:15:21"
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