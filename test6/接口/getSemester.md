<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getSemester  [返回](../README.md)
用例： [查看学期信息](../用例/查看学期信息.md)

- 功能：
    查看用户以往的学期信息。
    
- 权限：
    学生/老师：查看以往的学期信息，必须先登录，不能查看其它用户学期信息。
    
- API请求地址： 
    接口基本地址/v1/api/getSemester/<user_id>

- 请求方式 ：
    GET

- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |user_id|用户的ID号。对应表USERS.USER_ID的值|
  
- 返回实例：

        {         
            "status": true,
            "info": null,
            "data1":[
            {
            "semesterID":"201601",
            "name":"2016-2017学年第一学期",
            "userID":"32144",
            "data2":[
                 {
                  "ChooseCoursesID":"1234561",
                  "CoursesID":"325061",
                  "CoursesName":"信息系统分析与设计",
                  "testID":"32506101",
                  "grade":"90"
                  },
                  {
                  ...所选择的其它课程信息
                  }
                  ]
            "begin":"2016-03-01",
            "end":"2016-07-15"
            },
            {
            ...其它学期
            }
            ]
        }

 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |data1|以往的所有学期信息|
  |semesterID|学期的编号|
  |name|学期的名称|
  |userID|用户的编号，对应表USERS.USER_ID的值|
  |data2|学期所包含的所选择的课程信息|
  |ChooseCoursesID|选课信息的标号，对应表ChooseCourses.ChooseCourses_ID的值|
  |CoursesID|课程编号，对应表COURSES.COURSES_ID的值|
  |CoursesName|课程的名称|
  |testID|课程实验的编号，对应表TESTS.TESTS_ID的值|
  |grade|实验成绩|
  |begin|学期开始时间|
  |end|学期结束时间|



