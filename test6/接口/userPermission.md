# 接口： userPermission [返回](../README.md)
### 用例: [指定用户权限](../用例/指定用户权限 .md)
* 权限: 学生或教师已登录

* 功能： 对用户权限进行设置，包括学生信息，教师信息，课程对外是否允许访问等

* API请求地址： 接口基本地址/my/api/userPermission/<sure_id>

* 请求方式 ： POST

* 请求实例 :

````
  {
      "sure_id": "1",
  }
````
* 请求参数说明: 

|参数名称|说明|
|:---:|:--:|
|sure_id|标识用户权限，0为空，1则赋予字符串|

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
