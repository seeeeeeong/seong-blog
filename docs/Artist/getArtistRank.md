---
sidebar_position: 4
---

# 이달의 아티스트


> ![](https://img.shields.io/static/v1?label=&message=GET&color=brightgreen) <br/>
> http://dev.officialhey.com/artists/rank


### Parameters

#### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.

|    Field    |  Type  | Description |   
|:-----------:|:------:|:----------:|
|     id      | String |  아티스트 아이디  | 
| artistName  | String |    아티스트명   |  
| artistImage | String |  아티스트 이미지  |  


<br/>

  <details markdown="1">
  <summary>성공 예제</summary>

  ```
  {
    "status": true,
    "data": [
        {
            "id": "2eVlgLy3Aym09gM3dqx6cq",
            "artistName": "Lee Moon Sae",
            "artistImage": "https://i.scdn.co/image/ab67616d0000b273cc1386a402d65b68ff748bc0"
        },
        {
            "id": "2UjX6FLGyUQb4sbookjR3y",
            "artistName": "YdBB",
            "artistImage": "https://i.scdn.co/image/ab6761610000e5ebc827e4041ad2e45a1cb76777"
        },
        {
            "id": "1Z6Sy2Tn7jFqqPAPIAVMB1",
            "artistName": "Kim Jong Seo",
            "artistImage": "https://i.scdn.co/image/ab6761610000e5eb831b6fefe5e4ac07f34f40be"
        },
        {
            "id": "2p9c1SKG95v6V4eA3iu4IJ",
            "artistName": "이상우",
            "artistImage": "https://i.scdn.co/image/ab67616d0000b2734547eab0bebc821d2c095592"
        },
        {
            "id": "1OfdINxyzGwQlDulATMszM",
            "artistName": "박남정",
            "artistImage": "https://i.scdn.co/image/ab67616d0000b273be7d2584800229c194dae2d6"
        },
        {
            "id": "39Jf69SNjTiIQfCQyLh4Gb",
            "artistName": "Kim Hyun Chul",
            "artistImage": "https://i.scdn.co/image/ab67616d0000b27354c0c8cd657ce31632bdea8a"
        },
        {
            "id": "6oUBATBuMG0lnms8Nk6B5M",
            "artistName": "이은정",
            "artistImage": "https://i.scdn.co/image/ab67616d0000b273b20abbe371b35985763101d7"
        },
        {
            "id": "6ETqF15QgC4LfWc7gw69se",
            "artistName": "도희선",
            "artistImage": "https://i.scdn.co/image/ab67616d0000b2733b0077875f734a380e69c5d0"
        },
        {
            "id": "3y0G0pRY5v2iA6rR2fUS5q",
            "artistName": "김성민",
            "artistImage": "https://i.scdn.co/image/ab67616d0000b273a946e1cd5f56b0155217f0c9"
        },
        {
            "id": "31VffPWiL2AAwNIMODB9qZ",
            "artistName": "Kim Seungmin",
            "artistImage": "https://i.scdn.co/image/ab6761610000e5ebd0ac399ad60bc9ed40f22fec"
        },
        {
            "id": "6NuAIYZptWXWUCAInxX6PU",
            "artistName": "KIM DONG HYUN",
            "artistImage": "https://i.scdn.co/image/ab6761610000e5eb5771f0d3ebdf18daa9fda8f5"
        },
        {
            "id": "7BYHne6KtWNlbJnjZwLLRW",
            "artistName": "HAEUN",
            "artistImage": "https://i.scdn.co/image/ab67616d0000b273f466a57dff55ae263e1104e0"
        },
        {
            "id": "1p0J5PXJQMVqk5uVV4T1ja",
            "artistName": "Seong-Jin Cho",
            "artistImage": "https://i.scdn.co/image/ab6761610000e5eb5a08c3a0f98091a4ed11dd33"
        }
    ]
}
  ```

</details>