# 实验5:图书管理系统数据库设计与界面设计

|    学号   |       班级       |      姓名     |
|:-------:|:------------- | ----------:|
|   201510414106  |     软工1班     |   费浩然   |

### 1.数据库表设计
#### 1.1书籍表：
|字段|类型|主键\外键|可以为空|约束|说明|
|:---:|:---:| :-----:|:-----:|:--:|:--: | 
|bookISBN|int(10)|主键|否|||
|bookName|varchar(100)|外键|否|||
|author|varchar(100)||否|||
|publisher|varchar(100)||否|||
|publishetime|datetime(100)||否|||
|price|int(100)||否|||
|number|int(100)||否|||
|describe|varchar(100)||否|||
|count|int(100)||是|||
|state|varchar(10)||否|||
|list|varchar(100)||是|||

#### 1.2借阅者表：
|字段|类型|主键\外键|可以为空|约束|说明|
|:---:|:---:| :-----:|:-----:|:--:|:--: | 
|userId|int(10)|主键|否|||
|userPwd|int(50)||否|||
|userName|varchar(100)||否|||
|userSex|varchar(100)||否|||
#### 1.3预定书籍表：
|字段|类型|主键\外键|可以为空|约束|说明|
|:---:|:---:| :-----:|:-----:|:--:|:--: | 
|bookISBN|int(10)|主键|否|||
|userId|int(50)||外键|||
|desdate|datatime(100)||否|||
|desgetdate|varchar(100)||否|||
|desbookway|varchar(100)||否|||
#### 1.4借阅书籍表：
|字段|类型|主键\外键|可以为空|约束|说明|
|:---:|:---:| :-----:|:-----:|:--:|:--: | 
|bookISBN|int(10)|主键|否|||
|userId|int(50)||外键|||
|lendnum|int(100)||是|||
|lendtime|datetime(100)||否|||
|returntime|datetime(100)||否|||

#### 1.5管理员表：
|字段|类型|主键\外键|可以为空|约束|说明|
|:---:|:---:| :-----:|:-----:|:--:|:--: | 
|adminId|int(10)|主键|否|||
|adminPwd|int(50)||否|||
#### 1.6超级管理员表：
|字段|类型|主键\外键|可以为空|约束|说明|
|:---:|:---:| :-----:|:-----:|:--:|:--: | 
|spadminId|int(10)|主键|否|||
|spadminPwd|int(50)||否|||
#### 1.7游客表
|字段|类型|主键\外键|可以为空|约束|说明|
|:---:|:---:| :-----:|:-----:|:--:|:--: | 
|readlist|varchar(100)|主键|否|||
|state|varchar(50)|外键|是|||
|bookId|int(50)|外键|否|||

### 2.界面设计
#### 2.1借书界面设计：
![](./mydesign.png '描述')

* 用例图参见：费浩然借出图
* 类图参见：借阅书籍类
* 顺序图参见：借阅图书顺序图
* API接口如下：

1. 获取全部分类
* 功能：用于所需借阅书籍
* 请求地址： http://127.0.0.1:32767/start.html#p=index&g=1
* 请求方法：POST
* 请求参数：

|参数|必填|说明|
|:---:|:---:|:---:|
|bookISBN|是|用于指定查询的书籍号|
|method|是|固定为“POST”|
* 返回实例：
````
{
    "code": 200,
    "data": {
            "bookISBN": "3",
            "userId": "费浩然",
            "lendnum": 1,
            "lendtime": "2018-05-07 07:59:59",
            "returntime": "2018-05-13"
     },
    "Info": "响应成功"
}
````
* 返回参数说明：

|参数名称|说明|
|:---:|:--:|
|Info|返回信息|
|data|用户的个人信息|
|code|返回码|
2. 借阅者
* 功能：用于获取全部分类
* 请求地址： http://127.0.0.1:32767/start.html#p=index&g=1
* 请求方法：POST
* 请求参数：

|参数|必填|说明|
|:---:|:---:|:--:|
|bookISBN|是|用于指定查询的书籍号|
|method|是|固定为“POST”|
* 返回实例：
````
{
    "code": 200,
    "data": {
            "bookISBN": "3",
            "userId": "费浩然",
            "lendnum": 1,
            "lendtime": "2018-05-07 07:59:59",
            "returntime": "2018-05-13"
     },
    "Info": "响应成功"
}
````
* 返回参数说明：

|参数名称|说明|
|:---:|:--:|
|Info|返回信息|
|data|用户的个人信息|
|code|返回码|
