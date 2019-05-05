#空教室信息
获取空教室

##请求
``` url
GET http://教务系统URL/app.do?
```
##请求参数
```js
request.header{token:'运行身份验证authUser时获取到的token，有过期机制'},
request.data{
			'method':'getKxJscx',  //必填
			'time':'2019-04-28',  //格式"YYYY-MM-DD",非必填，默认返回当前日期空闲教室
			'idleTime':'allday',  //有allday,am,pm,night四种取值，非必填，默认值疑似allday
            'xqid':'1' , //校区ID，非必填
            'jxlid':'77',  //教学楼ID，非必填
            'classroomNumber':'30'  //可选项 30,30-40,40-50,60(分别意为30人以下，30-40人,···,60人以上)
			}
```

##返回
``` json
[
    {
	"jxl": "儋州校区-十号教学楼",   //教学楼名称
    "jsList": [
                {
                "jsid": "77",  //教室ID，暂不明与jsh关系
                "jzwid": "31",  //所在楼id
                "jsmc": "机具实验室(10201)",  //教室名称
                "zws": 40,  //座位数
                "xqmc": "儋州校区",  //校区名称
                "jsh": "103410201",  //教室号？意义未知
                "jzwmc": "十号教学楼",  //所在楼名称
                "yxzws": 40  //未知，值与zws保持一致
                }
            ]
    },{
	"jxl": "儋州校区-九号教学楼",
    "jsList": [
                {
                "jsid": "78",
                "jzwid": "34",
                "jsmc": "实验室(10202)",
                "zws": 40,
                "xqmc": "儋州校区",
                "jsh": "103410202",
                "jzwmc": "九号教学楼",
                "yxzws": 40
            }   
            ]
    }
]
```

##例程
``` url
GET http://教务系统URL/app.do?method=getKxJscx&time=2019-04-28&idleTime=allday
```