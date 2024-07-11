---
sidebar_position: 5
---

# 팔로우 아티스트 정보


> ![](https://img.shields.io/static/v1?label=&message=GET&color=brightgreen) <br/>
> http://dev.officialhey.com/users/follow/artists


### Parameters

### Headers
|      name     |           type            |  description  | required |
|:-------------:|:-------------------------:|:-------------:| :---: |
| Authorization | Bearer [TOKEN] 형식의 String | 사용자 인증 정보가 들어있는 토큰	 | **Required** |



### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.

|    Field    |       Type        | Description |   
|:-----------:|:-----------------:|:----------:|
|     id      |      String       |  아티스트 아이디  | 
| artistName  |      String       |    아티스트명   |
| artistImage |      String       |  아티스트 이미지  |



<br/>

  <details markdown="1">
  <summary>성공 예제</summary>

  ```
{
    "status": true,
    "data": [
        {
            "id": "2GmZFDBtCQ8EUGyzxEs2lj",
            "artistName": "조유찬",
            "artistImage": "https://i.scdn.co/image/ab67616d0000b273aaa310442647c95aa2662bad"
        },
        {
            "id": "1H0gcqLO1pSGOkLHMmqmyF",
            "artistName": "김정훈",
            "artistImage": "https://i.scdn.co/image/ab67616d0000b273ab45f2a9480e452c1ab9dd38"
        },
        {
            "id": "2j0NECZrf2rTkndYZQpTCz",
            "artistName": "김유민",
            "artistImage": null
        },
        {
            "id": "2zejz3SvONoXV9rqT7Xv3T",
            "artistName": "Park Jae Hui",
            "artistImage": null
        }
    ]
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
