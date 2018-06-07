# 接口： setOneStudentResults [返回](../README.md)
### 用例: [评定成绩](../用例/评定成绩.md)
* 权限: 仅老师，可以查看所有学生的所有学期的所有课程实验成绩和评语。

* 功能： 用于设置一个学生单学期的部分实验成绩和评语

* API请求地址： 接口基本地址/my/api/setOneStudentResults

* 请求方式 ： POST

* 请求实例 : 
````
{
      "student_id": "201510414106",
      "system_id": "2",
      "data":[
          "course_id":"IT新技术",
          "data_course":[
                "test_id": 1,
                "result": 85,
                "memo": "表现优异，平时成绩良好，不缺席，不早退..."
          ]
      ]
}
````

* 请求参数说明: 

|参数名称|说明|
|:---:|:--:|
|student_id|学生的学号。对应表STUDENTS.STUDENT_ID的值|
|system_id|第几学期，不能为空|
|data|单个学生的所有课程的实验成绩和评语，不能为空|
|course_id|课程名称|
|data_course|单课程下所属实验内容，返回整个课程的完整所有实验项成绩|
|test_id|实验内容编号及名称，不能为空|
|result|实验编号对应的试验项成绩|
|memo|单个实验的评语，不能为空|
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
