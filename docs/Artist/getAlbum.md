---
sidebar_position: 2
---

# 앨범 정보


> ![](https://img.shields.io/static/v1?label=&message=GET&color=brightgreen) <br/>
> http://dev.officialhey.com/artists/{id}/albums


### Parameters

|   name    |       type        |             description             |     required     |
|:---------:|:-----------------:|:-----------------------------------:|:----------------:|
|   size    |        Int        |                 사이즈                 | **Not Required** |
|   page    |        Int        |                 페이지                 |    **Not Required**     | 
| direction |     Direction     |                 정렬                  |    **Not Required**     | 


#### Path
| name |  type  | description | required |
|:----:|:------:|:-----------:| :---: |
|  id  | String |  아티스트 아이디   | **Required** |

### Headers
|      name     |           type            |  description  | required |
|:-------------:|:-------------------------:|:-------------:| :---: |
| Authorization | Bearer [TOKEN] 형식의 String | 사용자 인증 정보가 들어있는 토큰	 | **Required** |



### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.

|    Field    |     Type      | Description |   
|:-----------:|:-------------:|:-----------:|
|     id      |    String     |   앨범 아이디    | 
|    title    |    String     |   앨범 타이틀    |   
| albumImage  |    String     |   앨범 이미지    |  
| releaseDate | LocadDateTime |   앨범 발매일    |  


<br/>

  <details markdown="1">
  <summary>성공 예제</summary>

  ```
{
    "status": true,
    "data": {
        "content": [
            {
                "id": "6UEdTpBXKltxiiXATnUIkp",
                "title": "7",
                "albumImage": "https://i.scdn.co/image/ab67616d0000b273fa1322f68598b245c634415a",
                "releaseDate": "2023-03-27"
            },
            {
                "id": "7a3hsgaPiy2cW7qOIY8rph",
                "title": "Vooyou/Salty",
                "albumImage": "https://i.scdn.co/image/ab67616d0000b2739e8851120d1db2072543d22e",
                "releaseDate": "2022-11-14"
            },
            {
                "id": "2VoFDh96t4ob4qLMBH9lu3",
                "title": "Here we are",
                "albumImage": "https://i.scdn.co/image/ab67616d0000b27331fa50065491559e7a0dcbc5",
                "releaseDate": "2022-11-28"
            },
            {
                "id": "3mWczskll4zPDbRjPIfgjt",
                "title": "Missing Crown Prince (Original Television Soundtrack)",
                "albumImage": "https://i.scdn.co/image/ab67616d0000b2732bf1639abaa0036d9a004b51",
                "releaseDate": "2024-07-03"
            },
            {
                "id": "47FlhqtVgyxD2uFOjz98TG",
                "title": "SBS Drama OST Compilation Album",
                "albumImage": "https://i.scdn.co/image/ab67616d0000b273247840779ed7c41cf6555d06",
                "releaseDate": "2020-10-29"
            },
            {
                "id": "1GsIHj2gZzXfOGzDqZLR8K",
                "title": "FOODCOURT",
                "albumImage": "https://i.scdn.co/image/ab67616d0000b27341eb542ae477ba0381cd5e83",
                "releaseDate": "2022-03-18"
            },
            {
                "id": "5eGq0dKU0NKxc5tUSIis7R",
                "title": "The Crowned Clown (Original Television Soundtrack)",
                "albumImage": "https://i.scdn.co/image/ab67616d0000b2734515369fa35d29553e388f17",
                "releaseDate": "2019-03-04"
            },
            {
                "id": "7asUMK1cqZ1B5GSyzZqxMl",
                "title": "Love..ing (Reply)",
                "albumImage": "https://i.scdn.co/image/ab67616d0000b2735408269eff1de43adfcc2107",
                "releaseDate": "2018-09-14"
            },
            {
                "id": "6EEVcQaFxNckdv5JVSHm3a",
                "title": "SHIN YONG JAE",
                "albumImage": "https://i.scdn.co/image/ab67616d0000b273d4b04feb4b9b5b06922bdfa5",
                "releaseDate": "2018-11-06"
            },
            {
                "id": "70uDNnMOWleLn8Cx40cpkg",
                "title": "The Crowned Clown Pt. 4 (Original Television Soundtrack)",
                "albumImage": "https://i.scdn.co/image/ab67616d0000b2732085a0fa27a28cecf516a832",
                "releaseDate": "2019-02-04"
            },
            {
                "id": "7qH3C41mcnfeHoyq84dAuT",
                "title": "Girlfriend",
                "albumImage": "https://i.scdn.co/image/ab67616d0000b2733f07eacce8cc8a5a3250663f",
                "releaseDate": "2019-03-07"
            },
            {
                "id": "1NJZlFJpIpG4VNHKA4HHTc",
                "title": "RAINY DAY",
                "albumImage": "https://i.scdn.co/image/ab67616d0000b273834aaffd05642b343278d5c9",
                "releaseDate": "2019-07-11"
            },
            {
                "id": "2zCQGlNPkwNMt8KjvMicUi",
                "title": "Honkono",
                "albumImage": "https://i.scdn.co/image/ab67616d0000b273294ca0035a157aa5b2972e0b",
                "releaseDate": "2019-10-17"
            },
            {
                "id": "4VJaYxFuaZTeo7gAH4tmvW",
                "title": "99.9",
                "albumImage": "https://i.scdn.co/image/ab67616d0000b27376b27d46a358392dec9ad4ef",
                "releaseDate": "2020-09-07"
            },
            {
                "id": "7d1Emvo8w1NSqn2Rban4md",
                "title": "I Love You",
                "albumImage": "https://i.scdn.co/image/ab67616d0000b27353450ac6db1f050b09de64d0",
                "releaseDate": "2021-09-07"
            },
            {
                "id": "1YAQIPbjTAhXGBmvI8hNO8",
                "title": "No words",
                "albumImage": "https://i.scdn.co/image/ab67616d0000b2731e8aad0f28e5a31aa5b91fff",
                "releaseDate": "2021-11-12"
            },
            {
                "id": "6HkTrFBT35KKrjHZwog4Uy",
                "title": "On my lips",
                "albumImage": "https://i.scdn.co/image/ab67616d0000b2736f8a75470d9da1e72a0ba695",
                "releaseDate": "2022-07-20"
            },
            {
                "id": "53tsjWGD78dDPuxM9eYKKG",
                "title": "I'm Okay",
                "albumImage": "https://i.scdn.co/image/ab67616d0000b27336161758167c5f7dcd3a70a5",
                "releaseDate": "2024-04-23"
            },
            {
                "id": "2DGXz0USHVje4KFPUMfogv",
                "title": "Missing Crown Prince (Original Television Soundtrack) Pt. 4 - Love Is Like The Wind",
                "albumImage": "https://i.scdn.co/image/ab67616d0000b273f466a57dff55ae263e1104e0",
                "releaseDate": "2024-05-25"
            },
            {
                "id": "2xfz5encUu0CF2eIGqvCGl",
                "title": "Nokdu Flower OST Part.6",
                "albumImage": "https://i.scdn.co/image/ab67616d0000b27313a118cf4b0b97fd54aae1f1",
                "releaseDate": "2019-06-21"
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

### Error

유저 정보를 찾을 수 없을 때 반환하는 정보입니다.

<details markdown="1">
  <summary>에러 예제 </summary>

  ```
{
    "status": false,
    "code": "U001",
    "message": "회원을 찾을 수 없습니다."
}
  
  ```

  </details>
<br/>

토큰이 만료 되었을 때 반환하는 정보입니다.

<details markdown="1">
  <summary>에러 예제 </summary>

  ```
{"status":false,"code":"S005","message":"jwt access token이 만료되었습니다."}
  ```

  </details>
<br/>

유효하지 않은 토큰일 때 반환하는 정보입니다.

<details markdown="1">
  <summary>에러 예제 </summary>

  ```
  {"status":false,"code":"S002","message":"유효하지 않은 토큰입니다."}
  ```


  </details>
<br/>

jwt token이 없을 때 반환하는 정보입니다.

<details markdown="1">
  <summary>에러 예제</summary>

  ```
{"status":false,"code":"S008","message":"jwt token이 없습니다."}
  ```
  </details>
<br/>

아티스트를 찾을 수 없을 때 반환하는 정보입니다.

<details markdown="1">
  <summary>에러 예제</summary>

  ```
{
    "status": false,
    "code": "AR001",
    "message": "아티스트를 찾을 수 없습니다."
}
  ```
 </details>