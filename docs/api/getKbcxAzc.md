#时间信息
获取当前时间、周次、学年等信息

##请求
``` url
GET http://教务系统URL/app.do?
```
##请求参数
```js
request.header{token:'运行身份验证authUser时获取到的token，有过期机制'},
request.data{
			'method':'getKbcxAzc',  //必填
			'xh':'2017168xxxxx',  //必填，使用与获取token时不同的学号，则可以获取到新输入的学号的课表
			'xnxqid':'2018-2019-1',  //格式为"YYYY-YYYY-X"，非必填，不包含时返回当前日期所在学期课表
			'zc':'1'  //必填
			}
```

##返回
``` json
[
	{
		"jsxm":"张三", //教师姓名
		"jsmc":"教学楼101", //教室名称
		"jssj":"10:00", //结束时间
		"kssj":"08:00", //开始时间
		"kkzc":"1", //开课周次，有三种已知格式1)a-b、2)a,b,c、3)a-b,c-d
		"kcsj":"10506", //课程时间，格式x0a0b，意为星期x的第a,b节上课
		"kcmc":"大学英语", //课程名称
		"sjbz":"0" //具体意义未知，据观察值为1时本课单周上，2时双周上
	},{
		"jsxm":"李四",
		"jsmc":"教学楼101",
		"jssj":"12:00",
		"kssj":"10:00",
		"kkzc":"1",
		"kcsj":"1000000",
		"kcmc":"微积分",
		"sjbz":"0"
	}
]
```

##例程
``` url
GET http://教务系统URL/app.do?method=getKbcxAzc&xh=101010000&xnxqid=2018-2019-1&zc=5
```