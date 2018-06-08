<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getCourses  [返回](../README.md)
用例： [查看课程信息](../用例/查看课程信息.md)

- 功能：
    查看所有课程的详细信息。
    
- 权限：
    学生/老师：查看所有课程的详细信息，必须先登录。
    
- API请求地址： 
    接口基本地址/v1/api/getCourses

- 请求方式 ：
    GET
  
- 返回实例：

        {         
            "status": true,
            "info": null,
            "data":[
            {
            "CoursesID":"325061",
            "name":"信息系统分析与设计",
            "number":"60",
            "rest":"36",
            "begin":"2018-03-07",
            "end":"2018-06-15",
            "duration":"共13周"
            }
            {
            ...其他课程信息
            }
            ]
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |data|所有课程信息|
  |CoursesID|课程编号，对应表COURSES.COURSES_ID的值|
  |name|课程名称|
  |number|课程数量|
  |rest|课程剩余量|
  |begin|课程开始时间|
  |end|课程结束时间|
  |duration|课程时长|


