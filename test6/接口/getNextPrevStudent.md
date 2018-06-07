# 接口： getNextPrevStudent [返回](../README.md)
### 用例: [评定成绩](../用例/评定成绩.md)
* 权限: 仅老师能够使用

* 功能： 返回上一个学生的学号或下一个学生的学号

* API请求地址： 接口基本地址/my/api/getNextPrevStudent/<is_sequence>/<student_id>

* 请求方式 ： GET


* 请求参数说明: 

|参数名称|说明|
|:---:|:--:|
|is_sequence|选择下一个或者上一个|
|student_id|学生的学号|

* 返回实例：
````
  {
      "status": true,
      "info": null,
      "student_id": "201510414106"
      "result_code": 200
  }
````

* 返回参数说明:

|参数名称|说明|
|:---:|:--:|
|status|bool类型，true表示正确的返回，false表示有错误|
|info|返回结果说明信息|
|student_id|返回学生的学号|
|result_code|返回跳转的状态码，200显示跳转成功，404显示跳转失败|
