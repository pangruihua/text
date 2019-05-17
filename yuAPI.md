# 请求Url: /stuschedule
#### 功能：修改用户昵称
#### 接口描述：修改用户昵称那一栏
#### 请求类型：post
#### 输入：{"nickname":"xxx"}
#### 输出：json对象
####参数的请求与响应:
```
例子1:
请求(输入未存在的用户昵称):
{
	"nickname":"李四"
}
响应:
{
	"isSuccess":true,
	"message":"昵称修改成功"
}
*********************************
例子2:
请求(已经存在的用户名):
{
	"nickname":"王五"
}
响应：
{
	"isSuccess":false,
	"message":"昵称已经存在"
}

```
# 请求Url: /tUname
#### 功能：填写用户真实姓名
#### 接口描述：修改学员名字那一栏
#### 请求类型：post
#### 输入：{"tUsername":"xxx"}
#### 输出:json对象
#### 参数的请求与响应:
```
请求（输入真实姓名）:
{
	"tUsername":"王五"
}
响应:
{
	"isSuccess": true
	"message": "保存成功"
}
```
# 请求Url：/card
#### 功能：绑定身份证件号
#### 接口描述：绑定身份证证那一栏
#### 请求类型：post
#### 输入：{"IDcard":"xxx"}
#### 输出：json对象
#### 参数的请求与响应：
```
请求（输入真实身份证号）:
{
	"IDcard":"450521199610286928"
}
响应:
{
	"isSuccess": true
	"message": "绑定成功"
}
```
# 请求Url：/fcd
#### 功能：绑定子账号,便于老师跟踪学习
#### 接口描述:绑定子账号那一栏
#### 请求类型：post
#### 输入：Search Bar
#### 输出：json对象
#### 参数的请求与响应：
```
请求（输入自己的身份类型）:
{
	"fucard:"家长"
}
响应:
{
	"isSuccess": true
	"message": "绑定成功"
}
```
# 请求Url：/SearchBar/:coursename
#### 功能：搜索对应的课程
#### 接口描述:搜索那一栏
#### 请求类型：get
#### 输入：{"coursename","xxx"}
#### 输出：json对象
#### 参数的请求与响应:
```
/course/:userid
{
	"courses":
	[
		{
			"id":1,
			"kname":"微信小程序入门和实战",
			"kimgurl":"images/one.jpg","
			c_id":"1"
		},
		{
			"id":2,
			"kname":"玩转算法与数据结构",
			"kimgurl":"images/two.jpg","
			c_id":"15"
		}
	]
}
```
# 请求Url：/xcourses/:userid
#### 功能：反馈课程的通过情况和学习进度
#### 接口描述:发现那一栏
#### 请求类型：get
#### 输入：{"userid:","xxx"}
#### 输出：json对象
#### 参数的请求与响应:
```
/course/:userid
{
	"courses":
	[
		{
			"id":1,
			"kname":"微信小程序入门和实战",
			"kimgurl":"images/one.jpg","
			c_id":"1"
			"message1": "课程已经完成"
			"message2": "进度为100%"
		},
		{
			"id":2,
			"kname":"玩转算法与数据结构",
			"kimgurl":"images/two.jpg","
			c_id":"15"
			"message1": "课程未完成"
			"message2": "进度为60%"
		}
	]
}
```