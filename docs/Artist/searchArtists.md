---
sidebar_position: 5
---

# 아티스트 검색


> ![](https://img.shields.io/static/v1?label=&message=POST&color=brightgreen) <br/>
> http://dev.officialhey.com/artists/search


### Parameters


|   name    |   type    | description |     required     |
|:---------:|:---------:|:-----------:|:----------------:|
|  keyword  |  String   |     키워드     | **Not Required** |
|   size    |    Int    |     사이즈     | **Not Required** |
|   page    |    Int    |     페이지     |    **Not Required**     | 
| direction | Direction |     정렬      |    **Not Required**     | 


### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.

|    Field    |       Type        | Description |   
|:-----------:|:-----------------:|:----------:|
|     id      |      String       |  아티스트 아이디  | 
| artistName  |      String       |    아티스트명   |
| artistImage |      String       |  아티스트 이미지  |

  <details markdown="1">
  <summary>성공 예제</summary>

  ```
{
    "status": true,
    "data": {
        "content": [
            {
                "id": "1Z6Sy2Tn7jFqqPAPIAVMB1",
                "artistName": "Kim Jong Seo",
                "artistImage": "https://i.scdn.co/image/ab6761610000e5eb831b6fefe5e4ac07f34f40be"
            },
            {
                "id": "2eVlgLy3Aym09gM3dqx6cq",
                "artistName": "Lee Moon Sae",
                "artistImage": "https://i.scdn.co/image/ab67616d0000b273cc1386a402d65b68ff748bc0"
            },
            {
                "id": "52IPniXhQmDTYa5xQnoA2K",
                "artistName": "Jo Sung Mo",
                "artistImage": "https://i.scdn.co/image/ab67616d0000b2737302eceb236b80170c943ab9"
            },
            {
                "id": "0JIW1Ofq2ixNxfuivNHjlb",
                "artistName": "Kim Kyung Rok",
                "artistImage": "https://i.scdn.co/image/ab67616d0000b27398f6e4316468071b0f934220"
            },
            {
                "id": "15Tra1ytu0naoNByIhZArl",
                "artistName": "Kim Kyung Ho",
                "artistImage": "https://i.scdn.co/image/ab6761610000e5ebddcd5b81107c6894cfed36fa"
            },
            {
                "id": "6KsmQPHXE3qhzNNBPSZ0eB",
                "artistName": "Yoon Do Hyun",
                "artistImage": "https://i.scdn.co/image/ab67616d0000b2738c6e57176117299a272d5bf3"
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


