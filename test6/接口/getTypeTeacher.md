# 接口： getTypeTeacher [返回](../README.md)
### 用例: [课程选择](../用例/课程选择.md)
* 权限: 学生/老师，必须先进行登录。不能查看别人的信息，在老师选择课程之前学生不可查看课程列表。

* 功能： 返回教师是否选择了课程。

* API请求地址： 接口基本地址/my/api/getTypeTeacher

* 请求方式 ： GET

* 请求参数说明: 

|参数名称|说明|
|:---:|:--:|
|user_id|用户的ID号。对应表USERS.USER_ID的值|

* 返回实例：
````
  {
      "status": true,
      "info": null,
      "data": [
          {
            "GITHUB_USERNAME": "Fee",
            "USER_ID": "MR.MAN",
            "COURSE_ID": "IT新技术，移动开发技术，软件系统分析与设计技术，linux程序设计，c语言程序与设计",
            "UPDATE_DATE": "2018-06-02 17:32:57"},
          {
          ...other students
          }
      ]
  }
````

* 返回参数说明:

|参数名称|说明|
|:---:|:--:|
|status|bool类型，true表示正确的返回，false表示有错误|
|info|返回结果说明信息|
|data|用户数组|
|USER_ID|返回用户的ID号|
|COURSE_ID|已选择课程名称|
|type|状态码，标志教师是否选择了课程，0未选，1为已选择|
|UPDATE_DATE|github用户名修改日期|
