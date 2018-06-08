<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：delChooseCourses  [返回](../README.md)
用例： [删除选课信息](../用例/删除选课信息.md)

- 功能：
    用户删除自己所选择的课程。
    
- 权限：
    学生/老师：用户删除自己所选择的课程，必须先登录，不能删除其他用户所选择的课程。
    
- API请求地址： 
    接口基本地址/v1/api/delChooseCourses/<user_id>

- 请求方式 ：
    GET

- 请求参数说明:

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|
  |user_id|用户的ID，对于表USERS.USER_ID的值|

- 返回实例：

        {         
            "status": true,
            "info": null
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|


