# 接口： getStudents [返回](../README.md)
### 用例: [学生列表](../用例/学生列表.md)
* 权限: 学生可看个人用户，所属班级，所选修课程（包括COURSE_ID），但不可查看RESULT_SUM.  教师可查看所有信息。UPDATE_DATE学生和教师皆无权限隐藏。

* 功能： 返回所有学生的列表。

* API请求地址： 接口基本地址/my/api/getStudents

* 请求方式 ： GET

* 请求参数说明: 无

* 返回实例：
````
  {
      "status": true,
      "info": null,
      "total": 121,
      "data": [
          {
            "RESULT_SUM": "92.67,88,57,N",
            "PHOTO_USER": "010020"
            "GITHUB_USERNAME": "Fee",
            "STUDENT_ID": "201510414106",
            "CLASS": "软件(本)15-1",
            "SYSTEM": "第六学期",
            "NAME": "费浩然",
            "COURSE_ID": "IT新技术，移动开发技术，软件系统分析与设计技术，linux程序设计，c语言程序与设计",
            "average": 84,
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
|total|返回学生总人数|
|data|所有学生的数组|
|RESULT_SUM|返回各课程的成绩（各课程的总分分别显示）|
|PHOTO_USER|上传头像图转换成二进制数|
|GITHUB_USERNAME|github的用户名|
|SYSTEM|当前学期|
|STUDENT_ID|学生学号|
|CLASS|班级|
|NAME|姓名|
|COURSE_ID|已选择所有课程名称|
|average|平均分|
|UPDATE_DATE|github用户名修改日期|
