# 请求Url: /stuschedule
#### 功能：修改用户昵称
#### 接口描述：修改用户昵称那一栏
#### 请求类型：post
#### 输入：{"userid":"x","nickname":"xxx"}
#### 输出：json对象
#### 参数的请求与响应:
```
例子1:
请求:(输入新的用户昵称):

{
	"userid":"1",
	"nickname":"李四"
}
响应：
{
	"isSuccess":true,
	"message":"昵称修改成功"
}

******************

例子2:
请求:(输入已经存在的用户名):
{
	"userid":"2",
	"nickname":"王五"
}
响应：
{
	"isSuccess":false,
	"message":"昵称已经存在,请输入新的昵称"
}

```
# 请求Url: /tUname
#### 功能：填写用户真实姓名
#### 接口描述：修改学员名字那一栏
#### 请求类型：post
#### 输入：{"userid":"x"，"tUsername":"xxx"}
#### 输出:json对象
#### 参数的请求与响应:
```
请求:（输入真实姓名）:
{
	"userid":"2",
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
#### 输入：{"userid":"x","tUsername":"xxx","IDcard":"xxx"}
#### 输出：json对象
#### 参数的请求与响应：
```
例子1
请求:（输入真实姓名和身份证号）:
{
	"userid":"5",
	"tUsername":"陈皮",
	"IDcard":"450521199610286928"
}
响应:
{
	"isSuccess": true
	"message": "绑定成功"
}
*******
例子2
请求:（输入真实姓名和身份证号）:
{
	"userid":"5",
	"tUsername":"陈皮",
	"IDcard":"450521199610286938"
}
响应:
{
	"isSuccess": false
	"message": "信息错误，重新输入"
}
```
# 请求Url：/fcd
#### 功能：绑定子账号,便于老师跟踪学习
#### 接口描述:绑定子账号那一栏
#### 请求类型：post
#### 输入：{"userid":"x","fucard":"家长"}
#### 输出：json对象
#### 参数的请求与响应：
```
请求:（输入自己的身份类型）:
{
	"userid":"1",
	"fucard":"家长"
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
#### 输入：{"coursename":"xxx"}
#### 输出：json对象
#### 参数的请求与响应:
```
/SearchBar/:couresename
{
	"courses":
	[
		{
			"c_id":"1",
			"coursename":"微信小程序入门和实战",
			"kimgurl":"images/one.jpg"
		},
		{
			"c_id":"15",
			"coursename":"玩转算法与数据结构",
			"kimgurl":"images/two.jpg"
		}
	]
}
```
# 请求Url：/xcourses/:userid
#### 功能：反馈课程的通过情况和学习进度
#### 接口描述:发现那一栏
#### 请求类型：get
#### 输入：{"userid":"xxx"}
#### 输出：json对象
#### 参数的请求与响应:
```
/xcourses/:userid
{
	"courses":
	[
		{
			"userid":"1",
			"c_id":"1",
			"kname":"微信小程序入门和实战",
			"kimgurl":"images/one.jpg","
			"message1": "课程已经完成",
			"message2": "进度为100%"
		},
		{
			"userid":"1",
			"c_id":"15",
			"kname":"玩转算法与数据结构",
			"kimgurl":"images/two.jpg","
			"message1": "课程未完成",
			"message2": "进度为60%"
		}
	]
}
```
# 请求Url: /Eanswer
#### 功能：进入练习
#### 接口描述：练习小节那一栏
#### 请求类型：post
#### 输入：{"exersiseid":"xxx"}
#### 输出：json对象
#### 参数的请求与响应:
```
请求:（点击练习章节）:
{
	"exersiseid":"1"
}
响应:
{
	        "exersiseid":"1"
			"message": "编写一段程序，输出：Hello world"
}