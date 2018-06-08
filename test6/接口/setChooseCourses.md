<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：setChooseCourses  [返回](../README.md)
用例： [选课](../用例/选课.md)

- 功能：
    用户选择自己所需要的课程。
    
- 权限：
    学生/老师：用户选择自己做需要的课程，必须先登录，不能使用其他用户选择课程。
    
- API请求地址： 
    接口基本地址/v1/api/setChooseCourses

- 请求方式 ：
    POST

- 请求实例：

        {
            "id":"32144",
        }
        
- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |user_id|用户的ID号。对应表USERS.USER_ID的值|
  
- 返回实例：

        {         
            "status": true,
            "info": null,
            "data":
            {
            "ChooseCoursesID":"1234561",
            "userID":"32144",
            "CoursesID":"325061",
            "name":"信息系统分析与设计",
            "number":"60",
            "rest":"36",
            "duration":"共13周"
            }
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |data|选课信息|
  |ChooseCoursesID|选课信息的标号，对应表ChooseCourses.ChooseCourses_ID的值|
  |userID|用户的编号，对应表USERS.USER_ID的值|
  |CoursesID|课程编号，对应表COURSES.COURSES_ID的值|
  |name|课程名称|
  |number|课程数量|
  |rest|课程剩余量|
  |duration|课程时长|


