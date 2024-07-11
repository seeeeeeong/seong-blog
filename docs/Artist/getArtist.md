---
sidebar_position: 1
---

# 아티스트 상세


> ![](https://img.shields.io/static/v1?label=&message=GET&color=blue) <br/>
> http://dev.officialhey.com/artists/{id}

### Parameters
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


|    Field    |   Type   |   Description    |   
|:-----------:|:--------:|:----------------:|
|     id      |  String  |     아티스트 아이디     | 
| artistName  |  String  |      아티스트명       |   
| artistImage |  String  | 아티스트 이미지  |  
|    genre    | String[] |        장르        |  


<br/>

  <details markdown="1">
  <summary>성공 예제</summary>

  ```
 {
    "status": true,
    "data": {
        "id": "7BYHne6KtWNlbJnjZwLLRW",
        "artistName": "HAEUN",
        "artistImage": "https://i.scdn.co/image/ab67616d0000b273f466a57dff55ae263e1104e0",
        "genre": [
            "k-pop ballad",
            "korean pop"
        ]
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