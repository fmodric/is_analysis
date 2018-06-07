# 接口： systemChoose [返回](../README.md)
### 用例: [登录](../用例/登录.md)
* 权限: 学生/老师

* 功能： 使用户登录到平台

* API请求地址： 接口基本地址/my/api/login

* 请求方式 ： POST

* 请求实例 : 
````
{
      "type": "",
      "user_id": "MRS.woman",
      "password": "123man"
}
````

* 请求参数说明: 

|参数名称|说明|
|:---:|:--:|
|user_id|用户的ID号。对应表USERS.USER_ID的值|
|password|用户密码|
|type|用户类型，学生或教师|
* 返回实例：
````
  {
      "status": true,
      "info": null,
  }
````

* 返回参数说明:

|参数名称|说明|
|:---:|:--:|
|status|bool类型，true表示正确的返回，false表示有错误|
|info|返回结果说明信息|
