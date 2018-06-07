# 接口： getOneStudentViewResult [返回](../README.md)
### 用例: [评定成绩](../用例/评定成绩.md) [查看具体评分项](../用例/查看具体评分项.md)
* 权限: 教师和学生皆可查看，教师可查看所有学生的单个课程，学生只能看自己用户的单个课程。

* 功能： 用于显示一个学生的单个课程的所有实验项评分

* API请求地址： 接口基本地址/my/api/getOneStudentViewResult

* 请求方式 ： GET

* 请求实例 : 
````
{
      "student_id": "201510414106"
      "system_id": "3"
      "course_id": "web前端基础设计"
}
````

* 请求参数说明: 

|参数名称|说明|
|:---:|:--:|
|student_id|学生学号.表STUDENTS中USER_ID的值|
|system_id|学期编号，表SYSTEMS中SYSTEM_ID的值|
|course_id|课程编号，表COURSES中COURSE_ID的值|
* 返回实例：
````
  {
      "status": true,
      "info": null,
      "course_id": "web前端基础设计",
      "test_all":[
        "test_id": "实验一",
        "result_simple": 97,
        "memo": "该实验表现突出，成绩优异...",
        "update_date": "2018-06-03 15:45:57"
      ]
  }
````

* 返回参数说明:

|参数名称|说明|
|:---:|:--:|
|status|bool类型，true表示正确的返回，false表示有错误|
|info|返回结果说明信息|
|course_id|课程名称|
|test_all|该课程下的所有实验数组|
|test_id|单个实验编号，不能为空|
|result_simple|单个实验成绩,值为0-100之间，不得为空|
|memo|教师评语|
|update_date|本实验教师的批改日期|
