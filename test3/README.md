# 实验3:图书管理系统领域对象建模

|    学号   |       班级       |      姓名     |
|:-------:|:------------- | ----------:|
|   201510414106  |     软工1班     |   费浩然   |

### 1.图书管理系统类图
#### 1.1PlantUML源码如下：

````
@startuml
class 预订书籍{
    +String  ISBN
    +String  预订人ID
    +Data  预订日期
    +Data  预定归还日期
    +Data  预定书籍
    +新增预订信息()
    +删除预订信息()
    +更新预订信息()
    +查询预订信息()
}
class 借阅书籍{
    +String  ISBN
    +String  借阅者ID
    +Number  借阅数量
    +Data  借书时间
    +Data  还书时间
    +String  书籍活跃度
    +新增书籍()
    +删除书籍()
    +更新书籍()
    +查询书籍()
}

class 借阅者{
    +String  ID
    +String  密码
    +String  姓名
    +String  性别
    +查询书籍()
    +借阅书籍()
    +预订书籍()
    +归还书籍()
    +续借书籍()
}
class 游客{
    +查阅分类()
    +查阅状态()
    +查询书籍()
}
class 书籍信息{
    +String  ISBN
    +String 书名
    +Number 数量
    +String 作者
    +String 出版社
    +Date 出版日期
    +String 描述
    +int 库存
    +int 价格
    +List<String> 分类
    +String 书籍状态
    +新增书籍信息()
    +删除书籍信息()
    +更新书籍信息()
    +查询书籍信息()
}
class 管理员{
    String adminID
    String password
    +增、删、查、改()
}
class 超级管理员{
    String adminID
    String password
    +增、删、查、改()
}

游客"1" -- "N"书籍信息:查询书籍
借阅者"1" -- "N"书籍信息:查询书籍
借阅者"1" -- "N"预订书籍:预订、取消预订
借阅者"1" -- "N"借阅书籍:借阅、归还书籍
书籍信息 <.. 管理员:增、删、查、改
预订书籍 <.. 管理员:增、删、查、改
借阅书籍  <.. 管理员:增、删、查、改
管理员  <.. 超级管理员:增、删、查、改
@enduml

````
#### 1.2类图如下：
![](./fee1图.png '描述')

### 2.图书管理系统对象图
#### 2.1 预定书籍类
##### 2.1.1PlantUML源码如下：
````
class 预订书籍{
    +String  ISBN
    +String  预订人ID
    +Data  预订日期
    +Data  预定归还日期
    +Data  预定书籍
    +新增预订信息()
    +删除预订信息()
    +更新预订信息()
    +查询预订信息()
}
````
##### 2.1.2类图如下：
![](./fee2图.png '描述')
#### 2.2 借阅书籍类
##### 2.2.1PlantUML源码如下：
````
class 借阅书籍{
    +String  ISBN
    +String  借阅者ID
    +Number  借阅数量
    +Data  借书时间
    +Data  还书时间
    +String  书籍活跃度
    +新增书籍()
    +删除书籍()
    +更新书籍()
    +查询书籍()
}
````
##### 2.2.2类图如下：
![](./fee3图.png '描述')
#### 2.3 详细书籍类
##### 2.3.1PlantUML源码如下：
````
class 书籍信息{
    +String  ISBN
    +String 书名
    +Number 数量
    +String 作者
    +String 出版社
    +Date 出版日期
    +String 描述
    +int 库存
    +int 价格
    +List<String> 分类
    +String 书籍状态
    +新增书籍信息()
    +删除书籍信息()
    +更新书籍信息()
    +查询书籍信息()
}
````
##### 2.3.2类图如下：
![](./fee4图.png '描述')
#### 2.4 借阅者类
##### 2.4.1PlantUML源码如下：
````
class 借阅者{
    +String  ID
    +String  密码
    +String  姓名
    +String  性别
    +查询书籍()
    +借阅书籍()
    +预订书籍()
    +归还书籍()
    +续借书籍()
}
````
##### 2.4.2类图如下：
![](./fee5图.png '描述')
#### 2.5 用户类
##### 2.5.1PlantUML源码如下：
````
class 游客{
    +查阅分类()
    +查阅状态()
    +查询书籍()
}
````
##### 2.5.2类图如下：
![](./fee6图.png '描述')
#### 2.6 管理员类
##### 2.6.1PlantUML源码如下：
````
class 管理员{
    String adminID
    String password
    +增、删、查、改()
}
````
##### 2.6.2类图如下：
![](./fee7图.png '描述')

#### 2.7 超级管理员类
##### 2.7.1PlantUML源码如下：
````
class 超级管理员{
    String adminID
    String password
    +增、删、查、改()
}
````
##### 2.7.2类图如下：
![](./fee8图.png '描述')

