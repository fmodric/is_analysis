# 接口： upPhoto [返回](../README.md)
### 用例: [上传图片](../用例/上传图片 .md)
* 权限: 学生或教师已登录

* 功能： 修改用户的头像图片

* API请求地址： 接口基本地址/my/api/upPhoto/<user_id>

* 请求方式 ： POST

* 请求实例 :

````
  {
      "user_id": "MRFEE",
      "password": 123456
      "PHOTO_USER": "010020"
  }
````
* 请求参数说明: 

|参数名称|说明|
|:---:|:--:|
|user_id|用户ID，对应USERS表的USER_ID|
|password|用户密码，不能为空|
|PHOTO_USER|用户图片占位编号，二进制|

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
