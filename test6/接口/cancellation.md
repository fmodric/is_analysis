# 接口： cancellation [返回](../README.md)
### 用例: [注销](../用例/注销.md)
* 权限: 学生/老师，必须先进行登录。

* 功能： 使登录的用户退出登录状态

* API请求地址： 接口基本地址/my/api/cancellation

* 请求方式 ： POST

* 请求实例 : 
````
{
      "user_id":233333
}
````

* 请求参数说明: 

|参数名称|说明|
|:---:|:--:|
|user_id|用户的ID号。对应表USERS.USER_ID的值|

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
