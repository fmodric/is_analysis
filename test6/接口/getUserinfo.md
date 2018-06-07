# 接口： getUserinfo [返回](../README.md)
### 用例: [查看用户信息](../用例/查看用户信息.md) [修改用户信息](../用例/修改用户信息.md)
* 权限: 学生或教师已登录后即可查看

* 功能： 查看用户的相关信息。

* API请求地址： 接口基本地址/my/api/getUserinfo/<user_id>

* 请求方式 ： GET


* 请求参数说明: 

|参数名称|说明|
|:---:|:--:|
|user_id|用户ID，对应USERS表的USER_ID|

* 返回实例：
````
  {
      "status": true,
      "info": null,
      "PHOTO": ""
      "GITHUB_USERNAME": "Fee",
      "NAME": "费浩然",
      "CLASS": "软工一班",
      "DEPARTMENT": "",
      "TYPE": "学生"
  }
````

* 返回参数说明:

|参数名称|说明|
|:---:|:--:|
|status|bool类型，true表示正确的返回，false表示有错误|
|info|返回结果说明信息|
|GITHUB_USERNAME|用户的github用户名|
|NAME|学生姓名|
|PHOTO|图片/头像|
|CLASS|所属班级，教师为空|
|DEPARTMENT|所属部门，学生为空|
|TYPE|成员类型，教师或学生|
