<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getChooseCourses  [返回](../README.md)
用例： [查看选课信息](../用例/查看选课信息.md)

- 功能：
    查看用户所选课程信息。
    
- 权限：
    学生/老师：查看用户所选课程信息，必须先登录，不能查看其它用户所选课程信息。
    
- API请求地址： 
    接口基本地址/v1/api/getChooseCourses/<user_id>

- 请求方式 ：
    GET

- 请求参数说明:

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|
  |user_id|用户的ID，对于表USERS.USER_ID的值|

- 返回实例：

        {         
            "status": true,
            "info": null,
            "data":[
            {
            "ChooseCoursesID":"1234561",
            "userID":"32144",
            "CoursesID":"325061",
            "name":"信息系统分析与设计",
            "date":"2018-03-05",
            "status":"已开课/未开课"
            }
            {
            ...其他选课信息
            }
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |data|所有选课信息|
  |ChooseCoursesID|选课信息的标号，对应表ChooseCourses.ChooseCourses_ID的值|
  |userID|用户的ID，对于表USERS.USER_ID的值|
  |CoursesID|课程编号，对应表COURSES.COURSES_ID的值|
  |name|课程的名称|
  |date|选课时间|
  |status|课程状态：已开课/未开课|


