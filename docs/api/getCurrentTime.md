#时间信息
获取所提交的日期的时间、周次、学年等信息

##请求
``` url
GET http://教务系统URL/app.do?
```
##请求参数
```js
request.header{token:'运行身份验证authUser时获取到的token，有过期机制'},
request.data{
			'method':'getCurrentTime',  //必填
			'currDate':  //格式为"YYYY-MM-DD"，必填，留空调用成功，但返回值均为null
			}
```

##返回
``` json
{
	"zc":20, //当前周次
	"e_time":"2019-01-20", //本周结束时间
	"s_time":"2019-01-14", //本周开始时间
	"xnxqh":"2018-2019-1" //学年学期名称
}
```

##例程
``` url
GET http://教务系统URL/app.do?method=getCurrentTime&currDate=2019-01-14
```