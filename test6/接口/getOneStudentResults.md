# 接口： getOneStudentResults [返回](../README.md)
### 用例: [评定成绩](../用例/评定成绩.md) [查看总成绩](../用例/查看总成绩.md)
* 权限: 教师可以查看所有学生该学期的所有课程成绩。学生只能查看自己的课程成绩，不能查看别人的成绩。

* 功能： 返回一个学生的单学期所有实验课程的成绩与评分。

* API请求地址： 接口基本地址/my/api/getOneStudentResults

* 请求方式 ： GET

* 请求参数说明: 

|参数名称|说明|
|:---:|:--:|
|system_id|学期号，第几学期。对应表SYSTEMS.SYSTEM_ID的值|
|student_id|学生号|
* 返回实例：
````
  {
      "status": true,
      "info": null,
      "GITHUB_USERNAME": "Fee",
      "STUDENT_ID": "201510414106",
      "CLASS": "软件(本)15-1",
      "NAME": "费浩然",
      "SYSTEM_ID": "第二学期",
      "AVERAGE":61
      "TOTAL":5
      "data":[
            {
            "RESULT_SUM": "66.99,85,98,N",
            "COURSE_ALL": "IT新技术，移动开发技术，软件系统分析与设计技术，linux程序设计，c语言程序与设计",
            "UPDATE_DATE": "2018-06-03 15:45:57"},
            "memo":"'及格...' '优秀..'  '良好...' '优秀...' '无该实验课程' ",
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
|github_username|用户的github用户名|
|student_id|学生的学号|
|class|学生所属班级|
|name|学生姓名|
|system_id|当前所属学期|
|average|学生当前学期所有课程的平均分，取小数点后一位|
|total|当前学期的课程总数，一般在0——10之间|
|data|返回单个学期的所有课程分数及评语|
|result_sum|各科总分，可以为空，成绩应在0——100分数之间，未批改的则补计入成绩，并以N显示|
|course_all|课程名称，不能为空|
|update_date|本实验教师的批改日期|
|memo|课程下的教师评价，是个集合|
