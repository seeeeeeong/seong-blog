---
sidebar_position: 1
---

# 공연 리스트


> ![](https://img.shields.io/static/v1?label=&message=GET&color=blue) <br/>
> http://dev.officialhey.com/performances



### Parameters

|   name    |       type        |             description             |     required     |
|:---------:|:-----------------:|:-----------------------------------:|:----------------:|
|  status   | PerformanceStatus | 공연 상태(UPCOMING, ONGOING, COMPLETED) | **Not Required** |
|   size    |        Int        |                 사이즈                 | **Not Required** |
|   page    |        Int        |                 페이지                 |    **Not Required**     | 
| direction |     Direction     |                 정렬                  |    **Not Required**     | 



### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.


|   Field    |       Type        | Description |   
|:----------:|:-----------------:|:----------:|
|     id     |      String       |   공연 아이디   | 
|   title    |      String       |     공연명    |   
| startDate  |   LocadDateTime   |   공연 시작일   |  
|  endDate   |   LocadDateTime   |   공연 종료일   |  
|  theater   |      String       |     공연장    |    
|   poster   |      String       | 공연 포스터 이미지 | 
|   status   | PerformanceStatus |    공연 상태   | 
| created_at |   LocadDateTime   |    생성일     | 

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
            },
            {
                "id": "PF244705",
                "title": "1 to 10 레전드 콘서트: EP 04, 김종서 단독콘서트",
                "startDate": "2024-09-01",
                "endDate": "2024-09-01",
                "theater": "http://www.kopis.or.kr/upload/pfmPoster/PF_PF244705_240710_140612.png",
                "poster": "연세대학교 대강당 (연세대학교 대강당)",
                "status": "UPCOMING",
                "createdAt": "2024-07-11 19:15:21"
            },
            {
                "id": "PF244707",
                "title": "Theatre 이문세 [군산]",
                "startDate": "2024-10-25",
                "endDate": "2024-10-26",
                "theater": "http://www.kopis.or.kr/upload/pfmPoster/PF_PF244707_240710_142000.gif",
                "poster": "군산예술의전당 (대공연장)",
                "status": "UPCOMING",
                "createdAt": "2024-07-11 19:15:21"
            },
            {
                "id": "PF244706",
                "title": "청춘사운드콘서트 [대구]",
                "startDate": "2024-08-02",
                "endDate": "2024-08-02",
                "theater": "http://www.kopis.or.kr/upload/pfmPoster/PF_PF244706_240710_141946.jpg",
                "poster": "대덕문화전당 (대덕문화전당)",
                "status": "UPCOMING",
                "createdAt": "2024-07-11 19:15:21"
            },
            {
                "id": "PF244710",
                "title": "퀸유림 첫번째 단독 콘서트, The Coronation of Queen Yurim",
                "startDate": "2024-07-28",
                "endDate": "2024-07-28",
                "theater": "http://www.kopis.or.kr/upload/pfmPoster/PF_PF244710_240710_143422.jpg",
                "poster": "루끄 LOOK [홍대] (루끄 LOOK [홍대] )",
                "status": "UPCOMING",
                "createdAt": "2024-07-11 19:15:21"
            },
            {
                "id": "PF244712",
                "title": "크랙샷 앨범 발매 기념 공연, 충돌",
                "startDate": "2024-07-28",
                "endDate": "2024-07-28",
                "theater": "http://www.kopis.or.kr/upload/pfmPoster/PF_PF244712_240710_143834.jpg",
                "poster": "롤링홀 (롤링홀)",
                "status": "UPCOMING",
                "createdAt": "2024-07-11 19:15:21"
            },
            {
                "id": "PF244731",
                "title": "김경호 데뷔 30주년 전국투어 콘서트: THE ROCKER [목포]",
                "startDate": "2024-09-07",
                "endDate": "2024-09-07",
                "theater": "http://www.kopis.or.kr/upload/pfmPoster/PF_PF244731_240711_095708.jpg",
                "poster": "목포시민문화체육센터 (대공연장)",
                "status": "UPCOMING",
                "createdAt": "2024-07-11 19:15:21"
            },
            {
                "id": "PF244735",
                "title": "레이지본 콘서트, 요절복통 레이지본 vol.2",
                "startDate": "2024-07-19",
                "endDate": "2024-07-19",
                "theater": "http://www.kopis.or.kr/upload/pfmPoster/PF_PF244735_240711_101103.jpg",
                "poster": "컨벤트펍 (The convent Live Pub) (컨벤트펍 (The convent Live Pub))",
                "status": "UPCOMING",
                "createdAt": "2024-07-11 19:15:21"
            },
            {
                "id": "PF244738",
                "title": "리온 단독 콘서트: JUMP!",
                "startDate": "2024-08-10",
                "endDate": "2024-08-10",
                "theater": "http://www.kopis.or.kr/upload/pfmPoster/PF_PF244738_240711_101710.jfif",
                "poster": "롤링홀 (롤링홀)",
                "status": "UPCOMING",
                "createdAt": "2024-07-11 19:15:21"
            },
            {
                "id": "PF244740",
                "title": "먼데이프로젝트 시즌7, 벤치위레오 단독 콘서트: 푸른 늑대의 시간",
                "startDate": "2024-07-30",
                "endDate": "2024-07-30",
                "theater": "http://www.kopis.or.kr/upload/pfmPoster/PF_PF244740_240711_102652.jfif",
                "poster": "클럽온에어 (클럽온에어)",
                "status": "UPCOMING",
                "createdAt": "2024-07-11 19:15:21"
            },
            {
                "id": "PF244773",
                "title": "별은 팬 콘서트, lovelovelove!",
                "startDate": "2024-07-27",
                "endDate": "2024-07-27",
                "theater": "http://www.kopis.or.kr/upload/pfmPoster/PF_PF244773_240711_125957.gif",
                "poster": "클럽온에어 (클럽온에어)",
                "status": "UPCOMING",
                "createdAt": "2024-07-11 19:15:21"
            },
            {
                "id": "PF244774",
                "title": "PITTA 강형호 콘서트: New Normal Life [서울 (앵콜) ]",
                "startDate": "2024-08-24",
                "endDate": "2024-08-25",
                "theater": "http://www.kopis.or.kr/upload/pfmPoster/PF_PF244774_240711_130003.gif",
                "poster": "블루스퀘어 (Mastercard Hall(구.아이마켓홀))",
                "status": "UPCOMING",
                "createdAt": "2024-07-11 19:15:21"
            },
            {
                "id": "PF244744",
                "title": "MELTING LIVE: GENTLE",
                "startDate": "2024-07-21",
                "endDate": "2024-07-21",
                "theater": "http://www.kopis.or.kr/upload/pfmPoster/PF_PF244744_240711_104253.gif",
                "poster": "온맘씨어터 (온맘씨어터)",
                "status": "UPCOMING",
                "createdAt": "2024-07-11 19:15:21"
            },
            {
                "id": "PF244751",
                "title": "V.O.S & 제이세라 콘서트 [함안]",
                "startDate": "2024-08-23",
                "endDate": "2024-08-23",
                "theater": "http://www.kopis.or.kr/upload/pfmPoster/PF_PF244751_240711_110202.jpg",
                "poster": "함안문화예술회관 (대공연장)",
                "status": "UPCOMING",
                "createdAt": "2024-07-11 19:15:21"
            },
            {
                "id": "PF244806",
                "title": "유희열 Curated 23, PEPPERTONES CONCERT: Party Plenty [서울 (앵콜) ]",
                "startDate": "2024-07-27",
                "endDate": "2024-07-28",
                "theater": "http://www.kopis.or.kr/upload/pfmPoster/PF_PF244806_240711_144934.gif",
                "poster": "현대카드 언더스테이지 (스튜디오)",
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