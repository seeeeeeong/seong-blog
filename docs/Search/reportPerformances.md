---
sidebar_position: 1
---

# 공연 오류 제보


> ![](https://img.shields.io/static/v1?label=&message=POST&color=brightgreen) <br/>
> http://dev.officialhey.com/performances/{id}/report


### Parameters
### Path
| name |  type  | description | required |
|:----:|:------:|:-----------:| :---: |
|  id  | String |   공연 아이디    | **Required** |

### Headers
|      name     |           type            |  description  | required |
|:-------------:|:-------------------------:|:-------------:| :---: |
| Authorization | Bearer [TOKEN] 형식의 String | 사용자 인증 정보가 들어있는 토큰	 | **Required** |

### Body

  ```
{
    "type" : [
        "공연명"
    ],
    "content" : "공연명 오류"
}
  ```


### Response

HTTP Result Code가 200일 때 반환하는 정보입니다.


<br/>
  <details markdown="1">
  <summary>성공 예제</summary>

```
{
    "status": true,
    "data": {
        "id": "PF244688",
        "userId": 1
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

공연을 찾을 수 없을 때 반환하는 정보입니다.

<details markdown="1">
  <summary>에러 예제</summary>

  ```
{
    "status": false,
    "code": "P001",
    "message": "공연을 찾을 수 없습니다."
}
  ```
  </details>