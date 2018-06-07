# 接口： getOneStudentSystems [返回](../README.md)
### 用例: [评定成绩](../用例/评定成绩.md)
* 权限: 老师可以查看所有学生的所有学期和课程，学生只能看个人的。

* 功能： 用于显示一个学生的所有学期及课程

* API请求地址： 接口基本地址/my/api/getOneStudentSystems

* 请求方式 ： GET


* 请求参数说明: 

|参数名称|说明|
|:---:|:--:|
|student_id|学生学号|

* 返回实例：
````
  {
      "status": true,
      "info": null,
      "GITHUB_USERNAME": "Fee",
      "STUDENT_ID": "201510414106",
      "CLASS": "软件(本)15-1",
      "NAME": "费浩然",
      "system_all": [
          "system_id":"1"
      ]
      "course_list":[
            {
            "COURSE_ID": "移动开发技术",
            "TEST_ID": "实验一：前台展示",
            "UPDATE_DATE": "2018-06-03 15:45:57"},
      ]
  }
````

* 返回参数说明:

|参数名称|说明|
|:---:|:--:|
|status|bool类型，true表示正确的返回，false表示有错误|
|info|返回结果说明信息|
|github_username|用户的github用户名|
|student_id|学生的学号。对应表STUDENTS.STUDENT_ID的值|
|class|用户所属班级|
|name|用户姓名|
|system_all|学期列表，包含所有学期|
|system_id|第几学期，不能为空|
|course_list|单学期的课程列表，包含一个学期的所有课程|
|course_id|课程名称|
|update_date|本实验教师的批改日期|
|test_id|实验内容编号及名称，不能为空|
