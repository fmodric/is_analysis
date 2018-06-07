# 接口： setUserinfo [返回](../README.md)
### 用例: [修改用户信息](../用例/修改用户信息.md)
* 权限: 学生或教师已登录

* 功能： 修改用户的相关信息

* API请求地址： 接口基本地址/my/api/setUserinfo/<user_id>

* 请求方式 ： POST

* 请求实例 :

````
  {
      "user_id": "MRFEE",
      "password": 123456
      "newpassword": 111111
  }
````
* 请求参数说明: 

|参数名称|说明|
|:---:|:--:|
|user_id|用户ID，对应USERS表的USER_ID|
|password|用户密码，不能为空|
|newpassword|新密码，不能为空|

* 返回实例：
````
  {
      "status": true,
      "info": null
  }
````

* 返回参数说明:

|参数名称|说明|
|:---:|:--:|
|status|bool类型，true表示正确的返回，false表示有错误|
|info|返回结果说明信息|
